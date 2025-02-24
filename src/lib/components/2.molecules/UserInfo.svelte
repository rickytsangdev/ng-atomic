<script>
import Avatar from "../1.atoms/Avatar.svelte";
import Text from "../1.atoms/Text.svelte";
import Chip from "../1.atoms/Chip.svelte";

export let name; 
export let imageUrl;
</script>

<div class="flex flex-col items-center">
    <Avatar src={imageUrl} alt={name} />
    <Text content="Hello " className="text-gray-500 text-sm"/>
    <Text content={name} className="text-lg font-bold"/>
    <!-- <Chip text={name} options="rewards"/>
    <Chip text={name} options="personnal information"/> -->

</div>
