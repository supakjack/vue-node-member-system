<template>
  <div>
    <vs-card>
      <div class="flex justify-between">
        <div class="flex justify-between">
          <vs-avatar
            size="40px"
            class="mr-3"
            src="https://i.picsum.photos/id/21/400/400.jpg?hmac=fGXESAhrn1tB0FjFr1unqDHvAwhlgc4LjQElslttyzU"
          />
          <span class="text-xl self-center">ระบบจัดการสมาชิก</span>
        </div>
        <vs-button
          @click="active = !active"
          class="self-center"
          color="dark"
          icon="menu"
          type="flat"
        ></vs-button>
      </div>
    </vs-card>
    <vs-sidebar
      parent="body"
      default-index="1"
      color="primary"
      class="sidebarx"
      spacer
      v-model="active"
    >
      <div
        class="header-sidebar flex flex-col flex-wrap content-center"
        slot="header"
      >
        <vs-avatar
          size="70px"
          src="https://randomuser.me/api/portraits/men/85.jpg"
        />
        <span class="text-center">
          Admin
        </span>
      </div>

      <vs-sidebar-item index="1" icon="question_answer">
        Dashboard
      </vs-sidebar-item>

      <vs-sidebar-item index="2" icon="gavel"> History </vs-sidebar-item>

      <vs-divider icon="person" position="left"> User </vs-divider>

      <vs-sidebar-item index="3" icon="verified_user">
        Configurations
      </vs-sidebar-item>
      <vs-sidebar-item index="4" icon="account_box"> Profile </vs-sidebar-item>
      <vs-sidebar-item index="5"> Card </vs-sidebar-item>

      <div class="footer-sidebar" slot="footer">
        <vs-button icon="reply" color="danger" type="flat">log out</vs-button>
        <vs-button icon="settings" color="primary" type="border"></vs-button>
      </div>
    </vs-sidebar>
  </div>
</template>
<script>
export default {
  data: () => ({
    active: false,
  }),
};
</script>
