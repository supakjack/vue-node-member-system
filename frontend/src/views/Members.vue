<template lang="html">
  <div>
    <vs-breadcrumb>
      <li aria-current="page" class="active">จัดการสมาชิก</li>
    </vs-breadcrumb>

    <vs-table
      class="p-5"
      :search="true"
      :max-items="descriptionItems[0]"
      pagination
      :data="users"
      description
      :description-items="descriptionItems"
      description-title="แสดง"
      description-connector="จาก"
      description-body="จำนวนแถว"
    >
      <template slot="header">
        <h3>
          ตารางแสดงสมาชิกทั้งหมด
        </h3>
      </template>
      <template slot="thead">
        <vs-th> รูปประจำตัว </vs-th>
        <vs-th> ชื่อผู้ใช้งาน </vs-th>
        <vs-th> ชื่อ - นามสกุล </vs-th>
        <vs-th> ที่อยู่ </vs-th>
      </template>

      <template slot-scope="{ data }">
        <vs-tr :key="indextr" v-for="(tr, indextr) in data">
          <vs-td :data="data[indextr].imgPath">
            <img
              style="max-width:5rem;"
              class="rounded-2xl"
              :src="data[indextr].imgPath"
            />
          </vs-td>

          <vs-td :data="data[indextr].username">
            {{ data[indextr].username }}
          </vs-td>

          <vs-td :data="data[indextr].fullname">
            {{ data[indextr].fullname }}
          </vs-td>

          <vs-td :data="data[indextr].address">
            {{ data[indextr].address }}
          </vs-td>
        </vs-tr>
      </template>
    </vs-table>
  </div>
</template>

<script>
export default {
  data: () => ({
    descriptionItems: [3, 5, 15],
    users: [
      {
        id: 1,
        fullname: "Leanne Graham",
        username: "Bret",
        address: "Thailand Chonburi",
        imgPath:
          "https://i.picsum.photos/id/1005/5760/3840.jpg?hmac=2acSJCOwz9q_dKtDZdSB-OIK1HUcwBeXco_RMMTUgfY",
      },
      {
        id: 2,
        fullname: "Ervin Howell",
        username: "Antonette",
        address: "Thailand Chonburi",
        imgPath:
          "https://i.picsum.photos/id/1005/5760/3840.jpg?hmac=2acSJCOwz9q_dKtDZdSB-OIK1HUcwBeXco_RMMTUgfY",
      },
      {
        id: 3,
        fullname: "Clementine Bauch",
        username: "Samantha",
        address: "Thailand Chonburi",
        imgPath:
          "https://i.picsum.photos/id/1005/5760/3840.jpg?hmac=2acSJCOwz9q_dKtDZdSB-OIK1HUcwBeXco_RMMTUgfY",
      },
      {
        id: 4,
        fullname: "Patricia Lebsack",
        username: "Karianne",
        address: "Thailand Chonburi.org",
        imgPath:
          "https://i.picsum.photos/id/1005/5760/3840.jpg?hmac=2acSJCOwz9q_dKtDZdSB-OIK1HUcwBeXco_RMMTUgfY",
      },
      {
        id: 5,
        fullname: "Chelsey Dietrich",
        username: "Kamren",
        address: "Thailand Chonburi",
        imgPath:
          "https://i.picsum.photos/id/1005/5760/3840.jpg?hmac=2acSJCOwz9q_dKtDZdSB-OIK1HUcwBeXco_RMMTUgfY",
      },
      {
        id: 6,
        fullname: "Mrs. Dennis Schulist",
        username: "Leopoldo_Corkery",
        address: "Thailand Chonburi",
        imgPath:
          "https://i.picsum.photos/id/1005/5760/3840.jpg?hmac=2acSJCOwz9q_dKtDZdSB-OIK1HUcwBeXco_RMMTUgfY",
      },
      {
        id: 7,
        fullname: "Kurtis Weissnat",
        username: "Elwyn.Skiles",
        address: "Thailand Chonburi.biz",
        imgPath:
          "https://i.picsum.photos/id/1005/5760/3840.jpg?hmac=2acSJCOwz9q_dKtDZdSB-OIK1HUcwBeXco_RMMTUgfY",
      },
      {
        id: 8,
        fullname: "Nicholas Runolfsdottir V",
        username: "Maxime_Nienow",
        address: "Thailand Chonburi",
        imgPath:
          "https://i.picsum.photos/id/1005/5760/3840.jpg?hmac=2acSJCOwz9q_dKtDZdSB-OIK1HUcwBeXco_RMMTUgfY",
      },
      {
        id: 9,
        fullname: "Glenna Reichert",
        username: "Delphine",
        address: "Thailand Chonburi",
        imgPath:
          "https://i.picsum.photos/id/1005/5760/3840.jpg?hmac=2acSJCOwz9q_dKtDZdSB-OIK1HUcwBeXco_RMMTUgfY",
      },
      {
        id: 10,
        fullname: "Clementina DuBuque",
        username: "Moriah.Stanton",
        address: "Thailand Chonburi.biz",
        imgPath:
          "https://i.picsum.photos/id/1005/5760/3840.jpg?hmac=2acSJCOwz9q_dKtDZdSB-OIK1HUcwBeXco_RMMTUgfY",
      },
      {
        id: 11,
        fullname: "Kalolo Rich",
        username: "Kalolo.Rick",
        address: "Thailand Chonburi.io",
        imgPath:
          "https://i.picsum.photos/id/1005/5760/3840.jpg?hmac=2acSJCOwz9q_dKtDZdSB-OIK1HUcwBeXco_RMMTUgfY",
      },
    ],
  }),
};
</script>
