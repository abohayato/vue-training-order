<template>
  <div class="memberComponent">
    {{member.id}}{{member.name}}{{member.position}}
    <Height :changeHeight="changeHeight" :height="member.height" :id="member.id"/>
  </div>
</template>

<script>
import Height from "./Height";
export default {
  props: {
    member: Object,
    changeHeight: Function
  },
  components: {
    Height
  }
};
</script>

<style scoped>
.memberComponent {
  border: 1px solid blue;
}
</style>

