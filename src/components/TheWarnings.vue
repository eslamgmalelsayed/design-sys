<template>
    <div>
        <h2 class="fw-bold py-3">التنبيهات</h2>
        <div class="alert alert-white shadow-sm px-0" role="alert">
            <div class="row">
                <div class="col-lg-1 col-md-2 col-4">
                    <div class="circle ms-auto">
                        x
                    </div>
                </div>
                <div class="col-lg col">
                    <p class="mb-0 fw-bold">رسالة نجاح</p>
                    <span>رسالة وصف الخدمة </span>
                </div>
            </div>
        </div>
    </div>
    </div>
</template>

<script>
    export default {
        name:'TheWarnings',
    }
</script>

<style scoped>
.alert{
    max-width: 1106px;
    min-height: 85px;
    height: fit-content;
    overflow-wrap: anywhere;
    border-right: 5px solid var(--lightGreen);
}
.circle{
    width: 45px;
    height: 45px;
    border-radius: 50%;
    border: 2px solid var(--lightGreen);
    text-align: center;
    line-height: 2.5rem;
    color: var(--lightGreen);
}
p{
    color: var(--lightGreen);
}
span{
    color: #02363D;
}
</style>