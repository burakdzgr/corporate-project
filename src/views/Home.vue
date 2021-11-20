<template>
  <div class="home">
    <h1 class="text-5xl font-bold text-red-500">Anasayfa</h1>
    <CustomText>Merhaba</CustomText>
    <CustomText tag="p">Merhaba</CustomText>
    <CustomText tag="p" size="small">Merhaba</CustomText>
    <CustomText tag="p" size="xsmall">Merhaba</CustomText>
    <CustomText tag="p" size="xxsmall">Merhaba</CustomText>
  </div>
</template>

<script>
// @ is an alias to /src
import CustomText from '@/components/CustomText'
export default {
  name: "Home",
  components : {
    CustomText
  }
};
</script>
