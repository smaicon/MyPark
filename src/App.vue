<template>
  <form v-on:submit.prevent="save">
    <div class="container">
      <my-header :title="title">teste</my-header>

      <div class="row" g2>
        <div class="col-md-3">
          <label for="">Nome</label>
          <input
            type="text"
            class="form-control"
            v-model="reserva.nome"
            required
          />
        </div>
        <div class="col-md-3">
          <label for="">Data Reserva</label>
          <input
            type="date"
            class="form-control"
            v-model="reserva.dataReserva"
          />
        </div>
        <div class="col-md-3">
          <label for="">Hora Entrada</label>
          <input
            type="time"
            class="form-control"
            v-model="reserva.horaEntrada"
          />
        </div>
        <div class="col-md-3">
          <label for="">Qtd Horas</label>
          <input
            type="number"
            class="form-control"
            v-model="reserva.qtdHoras"
          />
        </div>
        <div class="col-md-4">
          <label for="">Placa</label>
          <input type="text" class="form-control" v-model="reserva.placa" />
        </div>
        <div class="col-md-4">
          <label for="">Modelo</label>
          <input type="text" class="form-control" v-model="reserva.modelo" />
        </div>
        <div class="col-md-3">
          <label for="">Ano</label>
          <input type="number" class="form-control" v-model="reserva.ano" />
        </div>
      </div>
      <div class="sm-12">
        <button class="btn btn-primary" type="submit">Save</button>
        <button class="btn btn-danger" type="button" @click="clear">
          Clear
        </button>

        {{ reserva }}
      </div>
    </div>
  </form>
</template>

<script>
import Header from "./components/Header/Header.vue";
export default {
  components: {
    "my-header": Header,
  },
  data() {
    return {
      title: "Cadastro e Listagem de Veiculos",
      reserva: {},
      reservas: [],
    };
  },
  methods: {
    save() {
      this.reservas.push(this.reserva);
      console.log(reserva);
    },
    clear() {
      this.reserva = {};
    },
  },
};
</script>

<style>
</style>
