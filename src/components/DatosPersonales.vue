<script setup>
import linkedin from '/src/assets/linkedin_icon.svg';
import Instagram from '/src/assets/instagram_icon.svg';
import github from '/src/assets/github_icon.svg';


const title = 'Gonzalo Bucca';
const descripcion = 'Estudio en la Universidad Tecnologica Nacional (UTN)';
const residencia = 'Actualmente vivo en San Rafael, Mendoza, Argentina';
const presentacion = 'Bienvenido a mi portafolio, soy estudiante de Programación de la cohorte 2024 y pertenezco al grupo Los Magios.';
const redesSociales = [
  { id: 1, name: 'linkedin', src: linkedin, url: 'https://www.linkedin.com/in/gonza-bucca-68103331b/' },
  { id: 2, name: 'instagram', src: Instagram, url: 'https://www.instagram.com/gonzabbucca/' },
  { id: 3, name: 'github', src: github, url: 'https://github.com/GonzaloBucca' },
];
const telefono = '+54 9 2604-401498';
</script>

<template>
  <section class="datos-personales">
    <div class="card">
      <h1>{{ title }}</h1>
      <h2>{{ descripcion }}</h2>
      <p>{{ presentacion }}</p>
      <ul class="container-lista">
        <li v-for="red in redesSociales" :key="red.id">
          <a :href="red.url"><img class="icon-redsocial" :src="red.src" width="35rem" :alt="red.name"></a>
        </li>
      </ul>
      <h3>☎ Mi Teléfono personal: {{ telefono }}</h3>
      <h4>{{ residencia }}</h4>
    </div>
  </section>
</template>

<style scoped>
h1 {
  font-size: 2.5rem;
}

p {
  font-size: 1.2rem;
  font-weight: 600;
  margin-bottom: 1rem;
}

.card {
  background-color: rgb(59, 59, 59);
  border-radius: 10px;
  padding: 10px;
  margin: 10px;
  text-align: center;
}

.container-lista {
  display: flex;
  justify-content: center;
  list-style: none;
  padding: 0;
  margin: 0;
  text-align: center;
}

.icon-redsocial {
  align-items: center;
  background-color: aliceblue;
  border-radius: 50%;
  padding: 2px;
  margin: 5px;
  box-shadow: 0 0 5px rgba(95, 124, 205, 0.934);
}

.icon-redsocial:hover {
  background-color: rgb(255, 255, 255);
  box-shadow: 0 0 5px rgba(251, 249, 249, 0.934);
}

h3 {
  font-size: 1.2rem;
  font-weight: 600;
}
</style>
