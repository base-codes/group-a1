<template>
  <cv-modal
    close-aria-label="closeAriaLabel"
    size="md"
    :visible="modalFormVisible"
    primary-button-disabled="primaryButtonDisabled"
    @modal-hidden="CLOSE_MODAL_FORM()"
  >
    <template slot="label">
      Каталог
    </template>
    <template slot="title">
      Заказать продукт
    </template>
    <template slot="content">
      <div class="bx--form-item">
        <label
          for="text-input-3h9mddk235a"
          class="bx--label"
        >Введите ваш Email</label>
        <input
          id="text-input-3h9mddk235a"
          type="text"
          class="bx--text-input"
          placeholder="Optional placeholder text"
          data-modal-primary-focus
        >
      </div>
    </template>
    <template slot="secondary-button">
      Закрыть
    </template>
    <template slot="primary-button">
      Отпаравить
    </template>
  </cv-modal>
</template>

<script>
import { mapMutations, mapState } from 'vuex'
export default {
  methods: {
    ...mapMutations('poductItem', ['CHANGE_MODAL_FORM']),
    ...mapMutations('poductItem', ['CLOSE_MODAL_FORM'])

  },
  computed: {
    ...mapState('poductItem', ['modalFormVisible'])
  }

}
</script>
