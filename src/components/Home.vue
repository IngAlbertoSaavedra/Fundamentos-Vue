<template>
  <Layout>
    <template #header>
      <Header/>
    </template>
    <template #resume>
      <Resume
        :label="label"
        :totalLabel = "'Ahorro Total'"
        :amount="amount"
        :totalAmount="65536"
      >
        <template #graphic>
          graphic
        </template>
        <template #action>
          <Action/>
        </template>
      </Resume>
    </template>
    <template #movements>
      <Movements
        :movements="movements"
      /> 

    </template>
  </Layout>
</template>
<script>
  import Layout from './Layout.vue';
  import Header from './Header.vue';
  import Resume from './Resume/Index.vue';
  import Movements from './Movements/Index.vue';
  import Action from './Action.vue';

  export default {
    components: {
      Layout,
      Header,
      Resume,
      Action, 
      Movements
    },
    data() {
      return {
        amount: null,
        label: null, 
        movements: [{
          id: 0,
          title: "Movimiento 1",
          description: "descripcion del movimiento",
          amount: 1001,
        },
        {
          id: 1,
          title: "Movimiento 2",
          description: "descripcion del movimiento",
          amount: 1002,
        },
        {
          id: 2,
          title: "Movimiento 3",
          description: "descripcion del movimiento",
          amount: -1003,
        },
        {
          id: 3,
          title: "Movimiento 4",
          description: "descripcion del movimiento",
          amount: 1003,
        },
        {
          id: 4,
          title: "Movimiento 5 ",
          description: "descripcion del movimiento",
          amount: 1004,
        },
      ]
      }
    }
  };
</script>
