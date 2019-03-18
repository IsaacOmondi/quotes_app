<template>
  <div class="col-sm-6 col-md-4 col-lg-3">
    <div class="card">
      <div class="card-body quote">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.card-body {
  font-family: "ZCOOL XiaoWei", cursive;
  font-size: 24px;
  font-weight: 600;
  color: #6e6e6e;
}

.quote {
  cursor: pointer;
}
.quote:hover {
  background-color: #ffe2e2;
}
</style>
