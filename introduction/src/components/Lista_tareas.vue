<template>
    <div class="container">
        
        <h1>Lista de Quehaceres</h1>
        <ul>
            <li v-for="tarea in tareas" :key="tarea.id">{{ tarea.descripcion }}</li>
        </ul>
        <input v-model="nuevaTarea" @keyup.enter="añadir" placeholder="Añadir nueva tarea">
        <button @click="añadir">Agregar Tarea</button>
        
    </div>
</template>

<script>
export default{
    data() {
        return {
            tareas: [
                {
                    id: 1,
                    descripcion: 'Limpiar la casa'
                },
                {
                    id: 2,
                    descripcion: 'Hacer el almuerzo'
                }
            ],
            nuevaTarea: ''
        };
    },
    methods: {
        añadir() {
      if (this.nuevaTarea.trim() !== '') {
        const nuevaId = this.tareas.length + 1;
        this.tareas.push({ id: nuevaId, descripcion: this.nuevaTarea });
        this.nuevaTarea = '';
      }
    },
 }
    
};

</script>

