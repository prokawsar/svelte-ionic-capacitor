<script>
    // native API Toast
    import { Toast } from '@capacitor/toast';
    var name = "svelte with ionic with capacitor"
    var image = "svelte_ionic_cap.png"
    
    const showHelloToast = async () => {
        await Toast.show({
            text: 'Test Toast!',
        });
    };

</script>

<div class="main">
    <img src={image} alt=""/>
    <h1>Welcome to {name}!</h1>

    
    <ion-grid>
        <ion-row>
            <ion-col>
                <ion-button color="warning" on:click={showHelloToast}>Show Toast</ion-button>    
            </ion-col>
        </ion-row>
    </ion-grid>

</div>

<style>
    .main {
        text-align: center;
        margin: 50px auto;
    }

    img {
        max-width: 100%;
    }
</style>