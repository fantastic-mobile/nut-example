<script setup lang="ts">
const input = ref('')
const radio = ref(1)
const rate = ref(3)
const toggle = ref(true)
</script>

<template>
  <FmPageLayout :navbar="false" tabbar>
    <FmPageMain title="Button">
      <nut-button type="primary">
        主要按钮
      </nut-button>
      <nut-button type="success">
        成功按钮
      </nut-button>
      <nut-button type="default">
        默认按钮
      </nut-button>
      <nut-button type="danger">
        危险按钮
      </nut-button>
      <nut-button type="warning">
        警告按钮
      </nut-button>
    </FmPageMain>
    <nut-form class="mx-4">
      <nut-form-item label="用户名">
        <nut-input v-model="input" label="文本" placeholder="请输入用户名" />
      </nut-form-item>
    </nut-form>
    <FmPageMain title="Radio">
      <nut-radio-group v-model="radio">
        <nut-radio :label="1">
          单选框 1
        </nut-radio>
        <nut-radio :label="2">
          单选框 2
        </nut-radio>
      </nut-radio-group>
    </FmPageMain>
    <FmPageMain title="Rate">
      <nut-rate v-model="rate" />
    </FmPageMain>
    <FmPageMain title="Switch">
      <nut-switch v-model="toggle" />
    </FmPageMain>
  </FmPageLayout>
</template>
