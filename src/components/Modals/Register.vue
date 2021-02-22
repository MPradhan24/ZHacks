<template>
  <mdb-container>
    <mdb-btn color="default" @click.native="register = true">launch register modal <mdb-icon icon="eye" class="ml-1"/></mdb-btn>
    <mdb-modal :show="register" @close="register = false">
    <mdb-modal-header class="text-center">
      <mdb-modal-title tag="h4" bold class="w-100">Sign up</mdb-modal-title>
    </mdb-modal-header>
    <mdb-modal-body class="mx-3 grey-text">
      <mdb-input label="Your name" icon="user" class="mb-5"/>
      <mdb-input label="Your email" icon="envelope" type="email" class="mb-5"/>
      <mdb-input label="Your password" icon="lock" type="password"/>
    </mdb-modal-body>
    <mdb-modal-footer center>
      <mdb-btn @click.native="register = false" color="deep-orange">Sign Up</mdb-btn>
    </mdb-modal-footer>
  </mdb-modal>
</template>

<script>
  import { mdbContainer, mdbBtn, mdbModal, mdbModalHeader, mdbModalBody, mdbModalFooter, mdbInput, mdbIcon } from 'mdbvue';
  export default {
    name: 'ModalExamplesPage',
    components: {
      mdbContainer,
      mdbBtn,
      mdbModal,
      mdbModalHeader,
      mdbModalBody,
      mdbModalFooter,
      mdbInput,
      mdbIcon
    },
    data() {
      return {
        register: false
      }
    }
  }
</script>