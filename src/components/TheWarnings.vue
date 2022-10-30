<template>
  <div>
    <h2 class="fw-bold py-3">التنبيهات</h2>
    <div class="alert alert-white shadow-sm px-0" role="alert">
      <div class="row">
        <div class="col-lg-1 col-md-2 col-4">
          <div class="circle ms-auto">{{icon}}</div>
        </div>
        <div class="col-lg col">
          <p class="mb-0 fw-bold">رسالة نجاح</p>
          <span>رسالة وصف الخدمة </span>
        </div>
      </div>
    </div>
    <hr>
    <!-- classes -->
    <h2> * ال 'classes' المتاحة</h2>
    <p class="text-success fw-bold">- SuccessWarningrClass</p>
    <p class="text-danger fw-bold">- DangerWarningClass</p>
    <p class="text-info fw-bold">- InfoWarningClass</p>
    <hr>
    <!-- props -->
    <h2> * ال 'props' المتاحة</h2>
    <p class="fw-bold">- icon class</p>
  </div>
</template>

<script>
export default {
  name: "TheWarnings",
  props:['icon']
};
</script>

<style scoped lang="scss">
@import "../assets/styles/colors";
@import "../assets/styles/TheWarningsClasses.scss";
.alert {
  @extend .SuccessWarningrClass;
}
</style>
