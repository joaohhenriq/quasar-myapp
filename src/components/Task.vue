<template>
  <ul>
    <li>
      <slot></slot>
      <!--semelhante ao children do react-->
      , {{prop.dueDate}}, {{prop.dueTime}}
    </li>
  </ul>
</template>

<script>
export default {
  props: ["prop"]
};
</script>

<style>
</style>