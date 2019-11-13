<script>
  export let variant;
</script>

<style>
  .box {
    border-radius: 3px;
    padding: 24px;
    margin-bottom: 24px;
  }

  .blue {
    background: #F7FAFD;
    border: 1px solid #CED9EA;
  }

  .orange {
    background: #EC4F27;
    color: white;
  }
</style>

<div class="box" class:blue={variant=="blue"} class:orange={variant=="orange"}>
  <slot></slot>
</div>