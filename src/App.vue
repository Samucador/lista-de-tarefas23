<template>
  <section>
    <cabeca :valor="titulo" />
    <div class="container">
      <adicionar-tarefa @adicionarTarefa="adicionarTarefa" />
      <listar-tarefas :tarefas="tarefas" />
      <footer>
        <em>Altere o nome de sua lista de tarefas: </em>
        <entrada-dados v-model="titulo" type="text" />
      </footer>
    </div>
    <rodape />
  </section>
</template>

<script>
import cabeca from '@/components/cabeca';
import rodape from '@/components/rodape';
import listarTarefas from '@/components/listarTarefas';
import adicionarTarefa from '@/components/adicionarTarefa';
import entradaDados from '@/components/templates/entradaDados';
export default {
  name: 'App',
  components: { cabeca, rodape, listarTarefas, adicionarTarefa, entradaDados },
  data() {
    return {
      titulo: "Minha lista de tarefas",
      tarefas: [
        {titulo: "Acordar", checked: true},
        {titulo: "Comer", checked: false},
        {titulo: "Fazer coisas", checked: false},
        {titulo: "Dormir", checked: false},
      ],
    };
  },
  methods: {
    adicionarTarefa(novaTarefa){
      this.tarefas.push({
        titulo: novaTarefa,
        checked: false,
      });
    }
  }
}
</script>

<style>
.container {
  width: 40%;
  margin: 20px auto 0px auto;
}
ul li {
  list-style: none;
}
.removed {
  color:darkslateblue;
}
.removed label {
  text-decoration: line-through;
}
</style>