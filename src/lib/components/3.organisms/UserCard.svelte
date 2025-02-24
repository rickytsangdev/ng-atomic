<script>
    import UserInfo from "../2.molecules/UserInfo.svelte";
    import Chip from "../1.atoms/Chip.svelte"
</script>

<style>
    .container {
        position: relative;
        width: 100%;
        max-width: 600px;
        margin: 0 auto;
        display: flex;
        flex-direction: column;
        align-items: center;


    }

     /* Fond gris qui commence à la moitié de l’image */
     .background {
        position: absolute;
        top: 10%;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: #dedede;
        border-radius: 12px;
        z-index: -1; /* Place l'arrière-plan derrière les éléments */
    }


    .content {
        width: 100%;
        padding: 20px;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 10px;
    }


    .chip-container {
        display: flex;
        flex-direction: column;
        gap: 14px;
        width: 100%;
    }

    @media (min-width: 768px) {
        .chip-container {
            flex-direction: column;
            justify-content: space-between;
        }
    }
</style>

<div class="container">
    <!-- arriere plan gris -->
    <div class="background"></div>

    <!-- composant userInfo -->
    
    <!-- composant principale -->
    <div class="content">
        <div class="chip-container">
            <UserInfo name="John Doe" imageUrl="   " />
            <Chip text="Rewards" />
            <Chip text="Informations personnelles" />
            <Chip text="Favoris et recherches" />
            <Chip text="Réservations" />
            <Chip text="Travel lab" />
            <Chip text="EVR Selection" />
        </div>
    </div>
</div>