<template>
  <div class="home">
    <div class="container">
      <v-card>
        <div class="header-block">
          <div class="table">
            <div class="filters-wrap">
              <div class="filters">
                <v-autocomplete class="motive" placeholder="Rejection motive"></v-autocomplete>
                <v-autocomplete class="code" placeholder="Code"></v-autocomplete>
                <v-autocomplete class="region" placeholder="Region"></v-autocomplete>
                <v-autocomplete class="ddc" placeholder="DDC"></v-autocomplete>
              </div>
              <v-text-field
                v-model="search"
                append-icon="mdi-magnify"
                label="Search"
                single-line
                hide-details
                class="search"
              ></v-text-field>
            </div>
              <v-spacer></v-spacer>
              <v-data-table
              :headers="headers"
              :items="items"
              :search="search"
              :items-per-page= 5
              class="tbl"
            >
            </v-data-table>
          </div>
          <div class="buttons">
            <v-btn
            class="notify_all"
            color="primary"
            >Notify all</v-btn>
            <v-btn
            class="notify_select"
            color="primary"
            >Notify select</v-btn>
            <v-switch  label="Send SMS"></v-switch>
            <v-switch  label="Send Email"></v-switch>
            <v-switch  label="Auto send at:"></v-switch>
          </div>
        </div>
      </v-card>
        <div class="footer-block">
          <div class="textfields">
            <v-text-field
              height="60px"
              placeholder="Write E-mail to send..."
            ></v-text-field>
            <v-text-field
              height="60px"
              placeholder="Write Phone to send..."
            ></v-text-field>
            <!-- <label for="email">E-mail to send:</label>
            <input type="text" class="email"> -->
          </div>
          <v-row>
            <v-col cols="12" md="6">
              <v-textarea
                outlined
                name="input-7-4"
                height="120px"
                label="Internal notification preview:"
                no-resize="false"
                value="..."
              ></v-textarea>
            </v-col>
          </v-row>
        </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Home',

  data: () => ({
    search: '',
    headers: [
      {
        text: 'Order number',
        sortable: false,
        value: 'orderNumber'
      },
      {
        text: 'Customer Code',
        sortable: false,
        value: 'customerCode'
      },
      {
        text: 'Rejection code',
        sortable: false,
        value: 'rejCode'
      },
      {
        text: 'First POC Nam',
        sortable: false,
        value: 'firstPOC'
      },
      {
        text: 'First Owner',
        sortable: false,
        value: 'firstOwner'
      },
      {
        text: 'First phone number',
        sortable: false,
        value: 'firstPhone'
      },
      {
        text: 'First E-mail',
        sortable: false,
        value: 'firstEmail'
      },
      {
        text: 'Count SKU',
        sortable: false,
        value: 'countSKU'
      }
    ],

    items: [
      {
        orderNumber: 9153180887,
        customerCode: 12509687,
        rejCode: null,
        firstPOC: 'La Esquina',
        firstOwner: 'Torres Velandi',
        firstPhone: 33102458479,
        firstEmail: 'Haswelvc@yandex.ru',
        countSKU: 6
      },
      {
        orderNumber: 9153180888,
        customerCode: 12509687,
        rejCode: null,
        firstPOC: 'La Esquina',
        firstOwner: 'Torres Velandi',
        firstPhone: 33102458479,
        firstEmail: 'Haswelvc@yandex.ru',
        countSKU: 6
      },
      {
        orderNumber: 9153180889,
        customerCode: 12509687,
        rejCode: null,
        firstPOC: 'La Esquina',
        firstOwner: 'Torres Velandi',
        firstPhone: 33102458479,
        firstEmail: 'Haswelvc@yandex.ru',
        countSKU: 6
      },
      {
        orderNumber: 9153180880,
        customerCode: 12509687,
        rejCode: null,
        firstPOC: 'La Esquina',
        firstOwner: 'Torres Velandi',
        firstPhone: 33102458479,
        firstEmail: 'Haswelvc@yandex.ru',
        countSKU: 6
      },
      {
        orderNumber: 9153180890,
        customerCode: 12509687,
        rejCode: null,
        firstPOC: 'La Esquina',
        firstOwner: 'Torres Velandi',
        firstPhone: 33102458479,
        firstEmail: 'Haswelvc@yandex.ru',
        countSKU: 6
      },
      {
        orderNumber: 9153180887,
        customerCode: 12509687,
        rejCode: null,
        firstPOC: 'La Esquina',
        firstOwner: 'Torres Velandi',
        firstPhone: 33102458479,
        firstEmail: 'Haswelvc@yandex.ru',
        countSKU: 6
      },
      {
        orderNumber: 9153180887,
        customerCode: 12509687,
        rejCode: null,
        firstPOC: 'La Esquina',
        firstOwner: 'Torres Velandi',
        firstPhone: 33102458479,
        firstEmail: 'Haswelvc@yandex.ru',
        countSKU: 6
      },
      {
        orderNumber: 9153180887,
        customerCode: 12509687,
        rejCode: null,
        firstPOC: 'La Esquina',
        firstOwner: 'Torres Velandi',
        firstPhone: 33102458479,
        firstEmail: 'Haswelvc@yandex.ru',
        countSKU: 6
      },
      {
        orderNumber: 9153180887,
        customerCode: 12509687,
        rejCode: null,
        firstPOC: 'La Esquina',
        firstOwner: 'Torres Velandi',
        firstPhone: 33102458479,
        firstEmail: 'Haswelvc@yandex.ru',
        countSKU: 6
      }
    ]
  })
}
</script>

<style scoped>
  .home{
    max-width: 100vw;
    max-height: 100vh;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
  }
  .container{
    max-width: 68.75rem;
    width: 100%;
    height: 100%;
    margin-left: 30px;
    margin-right: 30px;
  }

  .search{
    /* margin-top: 30px; */
    /* margin-bottom: 30px; */
    width: 40%;
  }

  .table{
    display: flex;
    align-items: flex-end;
    flex-direction: column;
    max-width: 55.438rem;
    width: 100%;
    margin-left: 30px;
  }

  .tbl{
    min-width: 22.375rem;
    height: 100%;
  }

  .header-block{
    display: flex;
  }

  .buttons{
    min-width: 13.875rem;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .footer_block{
    display: flex;
  }
  .textfields{
    margin-top: 60px;
    display: flex;
    width: 48%;
  }

  .v-text-field{
    padding: 5px;
  }

  .filters-wrap{
    display: flex;
    flex-direction: row;
  }

  .filters{
    display: flex;
    flex-direction: row;
  }

  .notify_select{
    margin-top: 10px;
  }
</style>
