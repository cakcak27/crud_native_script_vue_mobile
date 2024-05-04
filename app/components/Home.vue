<template>
    <Page>
        <ActionBar>
            <Label :text="title"/>
        </ActionBar>

        <StackLayout>
            <!-- <Label class="info">
                <FormattedString>
                    <Span class="fas" text.decode="&#xf135; "/>
                    <Span :text="message"/>
                </FormattedString>
            </Label> -->
            <Button text="To Details2" @tap="navigateToDetail" ></Button>
            <Button text="Grid Layout" @tap="navigateToDetail"></Button>
        </StackLayout>
    </Page>
</template>

<script>
    import Details from '@/components/Details.vue'
  export default {
    data(){
        return {
            title: 'Stack Layout'
        }
    },
    computed: {
      message() {
        return "Blank {N}-Vue app";
      }
    },
    methods: {
        navigateToDetail(){
            this.$navigateTo(Details)
        }
    }
  };
</script>

<style scoped lang="scss">
    @import '@nativescript/theme/scss/variables/blue';

    // Custom styles
    .fas {
        @include colorize($color: accent);
    }

    .info {
        font-size: 20;
        horizontal-align: center;
        vertical-align: center;
    }
</style>
