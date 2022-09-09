<template>
  <Frame>
    <Page>
      <ActionBar title="My App" class="action-bar" />
      <StackLayout>
        <Label text="After clicking the button below no navigation will be possible" />
        <Button text="Go to page one" @tap="goOne" />
      </StackLayout>
    </Page>
  </Frame>
</template>

<script lang="ts">
import Vue from 'vue';
import PageOneVue from './views/PageOne.vue';

export default Vue.extend({
    methods: {
        goOne() {
            this.$navigateTo(PageOneVue, {
                clearHistory: true
            });
        }
    }
})
</script>
