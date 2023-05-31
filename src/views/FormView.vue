<script setup lang="ts">
import { reactive, ref } from 'vue';
import { useRouter } from 'vue-router';

const router = useRouter()

const labelPosition = ref('right');

const formLabelAlign = reactive({
  name: 'James',
  lastName: 'Hernández',
  number: '1234567890'
});

const navNext = () => {
  router.push({
    name: 'thankyou'
  })
}
</script>

<template>
  <div class="d-flex align-items-center justify-content-center flex-column h-100">
    <div>
      <h1 class="mb-5">Formulario template</h1>
    </div>
    <div>
      <el-form :label-position="labelPosition" label-width="auto" :model="formLabelAlign" :disabled="true">
        <el-form-item label="Nombre">
          <el-input v-model="formLabelAlign.name" />
        </el-form-item>
        <el-form-item label="Apellido">
          <el-input v-model="formLabelAlign.lastName" />
        </el-form-item>
        <el-form-item label="Telefono">
          <el-input v-model="formLabelAlign.number" />
        </el-form-item>
      </el-form>
      <div class="d-flex justify-content-center">
        <el-button type="success" @click="navNext">Siguiente</el-button>
      </div>
    </div>
  </div>
</template>

<style scoped>
::v-deep(.el-form-item__label){
  font-weight: 900;
  color: black;
}

::v-deep(.el-input__wrapper){
  border: 1px solid black;
  background-color: bisque;
}
</style>
