<script>
    import UserInfo from "../2.molecules/UserInfo.svelte";
    import Chip from "../1.atoms/Chip.svelte"
</script>

<style>
    .container {
        display: flex;
        flex-direction: column;
        align-items: center;    
        width: 100%;
        max-width: 600px;
        margin: 0 auto;
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
    <UserInfo name="John Doe" imageUrl="   " />
    <div class="chip-container" >
        <Chip text="Rewards" />
        <Chip text="Personnal information" />
        <Chip text="Favorites and Searches" />
    </div>
</div>