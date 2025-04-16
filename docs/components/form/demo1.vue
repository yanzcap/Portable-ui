<template>
  <div>
    <p-form :model="ruleForm" label-width="120px" ref="ruleFormRef">
      <p-form-item label="Activity name" prop="name">
        <p-input v-model="ruleForm.name" placeholder="请输入" />
      </p-form-item>
      <p-form-item label="Activity zone" prop="region">
        <p-select
          :option="options"
          placeholder="请选择"
          v-model="ruleForm.region"
        ></p-select>
      </p-form-item>
      <p-form-item label="Address" prop="address">
        <p-input
          v-model="ruleForm.inputValue"
          placeholder="please input address"
        />
      </p-form-item>
      <p-form-item>
        <p-button @click.prevent="submitForm(ruleFormRef)">Submit</p-button>
      </p-form-item>
    </p-form>
  </div>
</template>

<script setup>
import { ref } from "vue";

const options = [
  {
    label: "option1",
    value: "1",
  },
  {
    label: "option2",
    value: "2",
  },
  {
    label: "option3",
    value: "3",
  },
  {
    label: "option4",
    value: "4",
  },
];

const ruleForm = ref({
  name: "",
  region: "",
  inputValue: "",
});
const ruleFormRef = ref();

const submitForm = () => {
  console.log("submit!");
};
</script>
