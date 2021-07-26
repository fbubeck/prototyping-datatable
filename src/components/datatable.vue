<template>
    <v-data-table
        v-model="selected"
        :headers="headers"
        :items="desserts"
        :single-select="singleSelect"
        item-key="name"
        show-select
        class="elevation-1"
        :items-per-page="5"
    >
    <template v-slot:top>
      <v-switch
        v-model="singleSelect"
        label="Single select"
        class="pa-3"
      ></v-switch>
    </template>
    <template v-slot:item.category="{ item }">
      <v-chip
        :color="getColor(item.category)"
        dark
      >
        {{ item.category }}
      </v-chip>
    </template>
    <template v-slot:item.status="{ item }">
      <v-chip
        :color="getColor2(item.status)"
        dark
      >
        {{ item.status }}
      </v-chip>
    </template>
  </v-data-table>
</template>

<script>
  export default {
    data () {
      return {
        headers: [
          {
            text: 'ID',
            align: 'start',
            sortable: false,
            value: 'id',
          },
          { text: 'Process Name', value: 'processName' },
          { text: 'Category', value: 'category' },
          { text: 'Responsible User', value: 'responsibleUser' },
          { text: 'Creation Date', value: 'creationDate' },
          { text: 'Status', value: 'status' },
          { text: 'Description', value: 'description' },
        ],
        desserts: [
          {
            id: '001',
            processName: 'Test-Process',
            category: 'internal',
            responsibleUser: 'Max Mustermann',
            creationDate: '2021/07/13',
            status: 'running',
            description: 'This is a Test Process',
          },
                    {
            id: '002',
            processName: 'Test-Process',
            category: 'Project xy',
            responsibleUser: 'Max Mustermann',
            creationDate: '2021/07/13',
            status: 'failed',
            description: 'This is a Test Process',
          },
          {
            id: '003',
            processName: 'Test-Process',
            category: 'internal',
            responsibleUser: 'Max Mustermann',
            creationDate: '2021/07/13',
            status: 'stopped',
            description: 'This is a Test Process',
          },
          {
            id: '004',
            processName: 'Test-Process',
            category: 'Project xy',
            responsibleUser: 'Max Mustermann',
            creationDate: '2021/07/13',
            status: 'running',
            description: 'This is a Test Process',
          },
          {
            id: '005',
            processName: 'Test-Process',
            category: 'Project xy',
            responsibleUser: 'Max Mustermann',
            creationDate: '2021/07/13',
            status: 'stopped',
            description: 'This is a Test Process',
          },
          {
            id: '006',
            processName: 'Test-Process',
            category: 'internal',
            responsibleUser: 'Max Mustermann',
            creationDate: '2021/07/13',
            status: 'finished',
            description: 'This is a Test Process',
          },
          {
            id: '007',
            processName: 'Test-Process',
            category: 'Project xy',
            responsibleUser: 'Max Mustermann',
            creationDate: '2021/07/13',
            status: 'running',
            description: 'This is a Test Process',
          },
          {
            id: '008',
            processName: 'Test-Process',
            category: 'internal',
            responsibleUser: 'Max Mustermann',
            creationDate: '2021/07/13',
            status: 'finished',
            description: 'This is a Test Process',
          },
          {
            id: '009',
            processName: 'Test-Process',
            category: 'internal',
            responsibleUser: 'Max Mustermann',
            creationDate: '2021/07/13',
            status: 'failed',
            description: 'This is a Test Process',
          },
        ],
      }
    },
    methods: {
      getColor (category) {
        if (category == 'internal') return 'purple'
        else return 'cyan'
      },
      getColor2 (status) {
        if (status == 'running') return 'blue'
        else if (status == 'failed') return 'red'
        if (status == 'stopped') return 'orange'
        else return 'green'
      },
    },
  }
</script>
