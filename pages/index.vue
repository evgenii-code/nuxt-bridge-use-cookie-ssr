<template>
  <div>
    <h1>Bug with useCookie on SSR</h1>

    <button @click="setCookie">Set cookie to 'foo'</button>

    <p>Cookie value: {{ `${foo}` }}</p>
  </div>
</template>

<script lang="ts" setup>
const foo = useCookie<string | undefined>('foo')

const setCookie = () => (foo.value = 'foo')
</script>
