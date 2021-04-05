<template>
  <v-app class="imgIndex">
    <form class="index-padding">
      <h1 class="contact-text">CONTACT</h1>
      <p>
        ADDRESS:

      </p>
      <p>
        12th Street,Berge 50 60 NORWEY
      </p>
      <p>
        MAIL:
      </p>
      <p>
        contact@yourcompany.com
      </p>
      <p>
        PHONE:
      </p>
      <p>
        +0(800)-123-654, +0(800)-123-654
      </p>
      <p>
        YOUR MESSAGE
      </p>
      <v-row class="pr-10">
        <v-col cols="12" md="6" sm="6">
          <v-text-field
            v-model="name"
            :error-messages="nameErrors"
            label="Name"
            required
            color="red"
          ></v-text-field>
        </v-col>
        <v-col cols="12" md="6" sm="6">
          <v-text-field
            v-model="email"
            :error-messages="emailErrors"
            label="E-mail"
            required

          ></v-text-field>
        </v-col>
        <v-col cols="12" md="12" sm="12">
          <v-text-field
            v-model="select"
            :error-messages="selectErrors"
            label="Item"
            required
            style="width: 800px"
          ></v-text-field>
        </v-col>
      </v-row>
      <v-btn
        small
        class="batten2"
        @click="submit"
      >
        SEND
      </v-btn>
    </form>
  </v-app>
</template>

<script>
import {validationMixin} from 'vuelidate'
import {required, maxLength, email} from 'vuelidate/lib/validators'


export default {
  name: "contact",
  mixins: [validationMixin],

  validations: {
    name: {required, maxLength: maxLength(10)},
    email: {required, email},
    select: {required},
    checkbox: {
      checked(val) {
        return val
      },
    },
  },

  data: () => ({
    name: '',
    email: '',
    select: null,
    items: [
      'Item 1',
      'Item 2',
      'Item 3',
      'Item 4',
    ],
    checkbox: false,
  }),

  computed: {
    checkboxErrors() {
      const errors = []
      if (!this.$v.checkbox.$dirty) return errors
      !this.$v.checkbox.checked && errors.push('You must agree to continue!')
      return errors
    },
    selectErrors() {
      const errors = []
      if (!this.$v.select.$dirty) return errors
      !this.$v.select.required && errors.push('Item is required')
      return errors
    },
    nameErrors() {
      const errors = []
      if (!this.$v.name.$dirty) return errors
      !this.$v.name.maxLength && errors.push('Name must be at most 10 characters long')
      !this.$v.name.required && errors.push('Name is required.')
      return errors
    },
    emailErrors() {
      const errors = []
      if (!this.$v.email.$dirty) return errors
      !this.$v.email.email && errors.push('Must be valid e-mail')
      !this.$v.email.required && errors.push('E-mail is required')
      return errors
    },
  },

  methods: {
    submit() {
      this.$v.$touch()
    },
    clear() {
      this.$v.$reset()
      this.name = ''
      this.email = ''
      this.select = null
      this.checkbox = false
    },
  },
}
</script>

<style scoped>
.imgIndex {
  background-image: url("https://3dnews.ru/assets/external/illustrations/2018/11/26/978705/sm.intro.800.jpg");
  background-size: cover;
  background-repeat: no-repeat;
}


.batten2 {
  border-radius: 10rem;
  text-transform: uppercase;
  border: 1px solid white;
  box-shadow: none;
  width: 0;
  transition: all 0.5s ease-in-out;
  background-color: transparent !important;
}

.batten2:hover {
  background-color: white !important;
  color: black;
}
@media (max-width: 1300px) {
.index-padding{
  padding-left: 30px!important;
}
  .contact-text{
    text-align: center;
    font-size: 50px;
  }
}

.index-padding {

  padding-top: 30px;
  padding-left: 70px;
  background: rgba(190, 104, 107, 0.97);
  height: 100%;
  width: 100%;

}
</style>
