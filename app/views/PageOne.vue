<template>
    <Page>
      <ActionBar title="My App" class="action-bar" />
      <StackLayout>
        <Label text="When clicking on go two the component will be rendered but it won't navigate." />
        <Button text="Go two" @tap="goTwo" />

      </StackLayout>
    </Page>
</template>

<script lang="ts">
import Vue from 'vue';
import PageTwoVue from './PageTwo.vue';

export default Vue.extend({
    methods: {
        goTwo() {
            this.$navigateTo(PageTwoVue);
        }
    }
})
</script>
