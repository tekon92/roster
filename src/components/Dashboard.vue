<template>
  <v-container>
    <v-layout text-center wrap>
      <v-flex xs12>
        <v-data-table :headers="headers" :items="desserts" :items-per-page="5" class="elevation-1">

            <!-- <div v-for="i in 2" :key="i">
                <template v-slot:item.date1="{ item }">
                    <div v-if="item.date1 === 1">test1</div>
                    <div v-else-if="item.date1 === 2">test2</div>
                    <div v-else-if="item.date1 === 3">test3</div>
                </template>
            </div> -->
          <template v-slot:item.date1="{ item }">
            <div v-if="item.date1 === 1">test1</div>
            <div v-else-if="item.date1 === 2">test2</div>
            <div v-else-if="item.date1 === 3">test3</div>
          </template>

          <template v-slot:item.date2="{ item }">
            <div v-if="item.date2 === 1">test1</div>
            <div v-else-if="item.date2 === 2">test2</div>
            <div v-else-if="item.date2 === 3">test3</div>
          </template>

          <!-- <template v-slot:item.date1="{ item }">
                {{ Object.keys(item).length-2 }}
          </template>-->
        </v-data-table>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      headers: [
        {
          text: "Employe ID",
          align: "left",
          sortable: true,
          value: "eid"
        },
        {
          text: "Name",
          align: "left",
          sortable: true,
          value: "name"
        },
        { text: "date1", value: "date1" },
        { text: "date2", value: "date2" }
      ],
      desserts: [
        {
          eid: "RP12345",
          name: "Frozen Yogurt",
          date1: 1,
          date2: 2
        },
        {
          eid: "RP23456",
          name: "Ice cream sandwich",
          date1: 2,
          date2: 1
        },
        {
          eid: "RP34567",
          name: "Eclair",
          date1: 3,
          date2: 2
        },
        {
          eid: "RP45678",
          name: "Cupcake",
          date1: 1,
          date2: 1
        }
      ]
    };
  }
};
</script>
