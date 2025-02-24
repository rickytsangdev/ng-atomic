<script lang="ts">
  export let classList = "";
  export let selected = false;
  export let light = false;
</script>

<div
  class:selected
  class="{light ? 'circle-light ' : 'circle'} {classList}"
></div>

<style lang="postcss">
  .circle {
    width: 27px;
    height: 27px;
    position: relative;
    transition: all;
    
  }

  .circle::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: 50%;
    background: linear-gradient(180deg, #50156b 0%, #3e127f 100%);
    /* border: 1px solid; */

    -webkit-mask: radial-gradient(
      farthest-side,
      transparent calc(100% - 1px),
      #fff 0
    );
  }

  .selected.circle::after {
    content: "";
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    border-radius: 50%;
    background: linear-gradient(180deg, #50156b 0%, #3e127f 100%);
    width: calc(100% - 8px);
    height: calc(100% - 8px);
    /* border: 1px solid; */
  }

  .circle-light {
    width: 27px;
    height: 27px;
    position: relative;
    transition: all;
  }

  .circle-light::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: 50%;
    background: #c09ff9;
    /* border: 1px solid; */

    -webkit-mask: radial-gradient(
      farthest-side,
      transparent calc(100% - 1px),
      #fff 0
    );
  }

  .selected.circle-light::after {
    content: "";
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    border-radius: 50%;
    background: #c09ff9;
    width: calc(100% - 8px);
    height: calc(100% - 8px);
    /* border: 1px solid; */
  }

  .wide.selected.circle-light::after {
    content: "";
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    border-radius: 50%;
    background: #c09ff9;
    width: calc(100% - 20px);
    height: calc(100% - 20px);
    /* border: 1px solid; */
  }
</style>