<template>
  <div>
    <header>
      <img src="@/assets/log.png" alt="Logo SUPPLY AI" class="logo" />
      <h1>SUPPLY AI</h1>
      <p>Conexão entre empresas para garantir suprimentos sem interrupções</p>
    </header>

    <nav>
      <RouterLink to="/home">Início</RouterLink>
      <RouterLink to="/sobre">Sobre</RouterLink>
      <RouterLink to="/contato">Contato</RouterLink>
      <RouterLink to="/suaconta">Sua conta</RouterLink>
    </nav>

    <div class="container">
      <section class="section">
        <h2>🔗 Rede Colaborativa entre Empresas</h2>
        <p>
          A conexão entre empresas da cadeia produtiva permite o compartilhamento de dados sobre demanda,
          disponibilidade de estoque, transporte e produção.
          Essa colaboração resulta em uma resposta mais rápida a imprevistos, melhor uso de recursos e redução da escassez de matéria-prima.
        </p>
      </section>

      <section class="section">
        <h2>📈 Impacto da Conexão na Disponibilidade de Insumos</h2>
        <p>Empresas conectadas conseguem reagir com mais agilidade e planejar melhor seus suprimentos. Veja no gráfico abaixo:</p>
        <canvas ref="graficoCanvas" width="400" height="200"></canvas>
      </section>
    </div>

    <footer>
      <p>&copy; 2025 SUPPLY AI. Todos os direitos reservados.</p>
    </footer>
  </div>
</template>

<script setup>
import { onMounted, ref } from 'vue'
import { Chart, registerables } from 'chart.js'
Chart.register(...registerables)

const graficoCanvas = ref(null)

onMounted(() => {
  const ctx = graficoCanvas.value.getContext('2d')
  new Chart(ctx, {
    type: 'line',
    data: {
      labels: ['Jan', 'Fev', 'Mar', 'Abr', 'Mai', 'Jun'],
      datasets: [
        {
          label: 'Empresas Conectadas',
          data: [70, 78, 85, 90, 94, 97],
          borderColor: '#ff6f00',
          backgroundColor: 'rgba(255, 111, 0, 0.2)',
          fill: true,
          tension: 0.4
        },
        {
          label: 'Empresas Isoladas',
          data: [70, 71, 68, 65, 66, 68],
          borderColor: 'gray',
          backgroundColor: 'rgba(200, 200, 200, 0.2)',
          borderDash: [5, 5],
          fill: true,
          tension: 0.4
        }
      ]
    },
    options: {
      scales: {
        y: {
          beginAtZero: true,
          max: 100,
          title: {
            display: true,
            text: 'Disponibilidade de Insumos (%)'
          }
        },
        x: {
          title: {
            display: true,
            text: 'Meses'
          }
        }
      },
      plugins: {
        legend: {
          labels: {
            color: '#f5f5f5'
          }
        }
      }
    }
  })
})
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, sans-serif;
}

body {
  background: linear-gradient(to right, #000000, #000000);
  color: #f5f5f5;
}

header {
  background-color: #000000;
  color: #ffffff;
  padding: 1.5rem;
  text-align: center;
  position: relative;
}

.logo {
  position: absolute;
  top: 10px;
  left: 10px;
  width: 93px;
  height: auto;
}

nav {
  display: flex;
  justify-content: center;
  gap: 2rem;
  background-color: #f65b08;
  padding: 0.75rem;
}

nav a {
  color: #ffffff;
  text-decoration: none;
  font-weight: bold;
}

nav a:hover {
  text-decoration: underline;
}

.container {
  padding: 2rem;
  max-width: 1200px;
  margin: auto;
}

.section {
  margin-bottom: 2rem;
  background: #1c1c1c;
  padding: 1.5rem;
  border-radius: 10px;
  box-shadow: 0 2px 5px rgba(255, 111, 0, 0.2);
}

canvas {
  margin-top: 2rem;
}

footer {
  text-align: center;
  padding: 1rem;
  background-color: #ff6f00;
  color: #000;
  margin-top: 2rem;
}
</style>
