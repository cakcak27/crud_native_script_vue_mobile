<template>
    <Page actionBarHidden="true">
        <StackLayout  backgroundColor="#FFFFFF">
            <GridLayout height="55" columns="50, *" rows="50, *" class="header-shadow">
                <!-- <NavigationButton
                    android.systemIcon="ic_menu_back"
                    text="Go back" @tap="goBack" /> -->
                <Button
                    class="fas"
                    text.decode="&#xf0d9;"
                    width="50"
                    height="50"
                    @tap="goBack" />
                <Label
                    row="0"
                    col="1"
                    style="margin: 0 15px;"
                    text="NativeScript" fontSize="24"/>
            </GridLayout>
            <FlexboxLayout style="padding: 15px;" flexDirection="column">
                <!-- <Label
                    class="header-shadow"
                    width="100%"
                    /> -->
                <Label backgroundColor="#1c6b48" text="in flex box" />
            </FlexboxLayout>
        </StackLayout>
    </Page>
</template>
<script>
    export default {
        data(){
            return {
                title: "Details"
            }
        },
        methods: {
            goBack(){
                this.$navigateBack()
            }
        }

    }

</script>
