<template>
  <FormulateForm class="formulate_form" v-model="formValues">
    <div class="row">
      <div class="col-6">
        <div>
          <FormulateInput class="name_surname"
            v-for="name in name_"
            :key="name.name"
            v-bind="name"
          />
        </div>
      </div>
      <div class="col-6">
        <div class="name_surname">
          <FormulateInput
            v-for="surname in surname_"
            :key="surname.name"
            v-bind="surname"
          />
        </div>
      </div>
    </div>
    <div class="address">
      <FormulateInput
        v-for="address in address_"
        :key="address.name"
        v-bind="address"
      />
    </div>
    <div class="row">
      <div class="col-4">
        
          <FormulateInput
            v-model="value"
            v-for="radio in radio_"
            :key="radio.name"
            v-bind="radio"
          />
       
      </div>
      <div class="col-8">
        <div class="info">
          <FormulateInput
            v-for="info in info_"
            :key="info.name"
            v-bind="info"
          />
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-12 button ">
            <FormulateInput type="submit" label="SEND" />

      </div>
    </div>
  </FormulateForm>
</template>
<script>
export default {
  data() {
    return {
      name_: [
        {
          type: 'text',
          name: "name",
          label: "Name",
        },
      ],
      surname_: [
        {
          type: 'text',
          name: "surname",
          label: "Surname",
        },
      ],
      address_: [
        {
          type: 'text',
          name: "address",
          label: "Address",
        },
      ],
      radio_: [
        {
          
          options: [
            { value: "first", id: "first", label: "First" },
            { value: "second", id: "second", label: "Second" },
          ],
          type: "radio",
        },
      ],
      info_: [
        {
          type: "textarea",
          name: "info",
          label: "İnfo",
        },
      ],
      button_: [
        {
          type: "button",
          name: "Send",
          
        }
      ]
    };
  },
};
</script>
<style>
.info {
  width: 98%;
  margin-top: 1rem;
}
.form {
  display: flex;
  width: 40%;
  margin: auto;
  margin-top: 1rem;
}
.address {
  width: 98% !important;
  margin: auto;
}
.formulate_form {
  width: 70%;
  margin: auto;
}

.formulate_form{
  margin-top: 3rem;
}
.name_surname {
  width: 95%;
  justify-content: space-between;
  margin: auto;
}
.button{
  text-align: end;
  margin-top: 1rem;
}
</style>