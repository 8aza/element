<template>
  <div class="baza-xls-page-header">
    <div class="baza-xls-page-header__left" @click="$emit('back')">
      <i class="baza-xls-icon-back"></i>
      <div class="baza-xls-page-header__title">
        <slot name="title">{{ title }}</slot>
      </div>
    </div>
    <div class="baza-xls-page-header__content">
      <slot name="content">{{ content }}</slot>
    </div>
  </div>
</template>

<script>
import { t } from 'element-ui/src/locale';
export default {
  name: 'ElPageHeader',

  props: {
    title: {
      type: String,
      default() {
        return t('el.pageHeader.title');
      }
    },
    content: String
  }
};
</script>
