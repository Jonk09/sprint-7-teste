<template>
  <div>
    <header>
      <img src="@/assets/log.png" alt="Logo SUPPLY AI" class="logo" />
      <h1>SUPPLY AI</h1>
      <p>Inovação que mantém sua produção em movimento</p>
    </header>

    <nav>
      <a href="/home">Início</a>
      <a href="/contato">Contato</a>
      <a href="/suaconta">Sua conta</a>
    </nav>

    <div class="">
      <section id="sobre" class="section">
        <h2>O que é o SUPPLY AI?</h2>
        <p>
          O SUPPLY AI é uma solução inteligente e acessível de gestão de insumos e fornecedores, desenvolvida especialmente para pequenas e médias indústrias.
          Nosso sistema automatiza o controle de estoque, prevê demandas futuras e ajuda sua empresa a evitar atrasos, reduzir custos e se tornar mais resiliente a imprevistos.
        </p>

        <h2>Por que criamos o SUPPLY AI?</h2>
        <p>
          Muitas PMEs enfrentam problemas sérios por falta de matéria-prima na hora certa.
          As ferramentas disponíveis hoje são caras, complexas e feitas para grandes empresas.
          O SUPPLY AI surge como uma alternativa simples, eficaz e sob medida para empresas que precisam de eficiência sem complicação.
        </p>

        <h2>Como o SUPPLY AI ajuda sua empresa?</h2>
        <ul>
          <li>Evita atrasos na produção com alertas automáticos e previsões inteligentes.</li>
          <li>Reduz custos ao minimizar compras emergenciais.</li>
          <li>Facilita decisões com dashboards simples e relatórios personalizados.</li>
          <li>Monitora estoques em tempo real com sensores IoT.</li>
          <li>Se adapta ao seu ritmo, com módulos que crescem junto com sua operação.</li>
          <li>Integra com os sistemas que você já usa (ERP, CRM etc.).</li>
          <li>Conecta empresas para troca de dados e boas práticas na cadeia de suprimentos.</li>
        </ul>

        <h2>É pra minha empresa?</h2>
        <p>
          Se você é gestor de uma pequena ou média indústria e busca uma forma prática, moderna e acessível de controlar insumos e fornecedores,
          o SUPPLY AI é pra você. Menos burocracia, mais controle, e resultados reais.
        </p>

        <h2>Quer saber mais?</h2>
        <p>
          Fale com a gente e descubra como o SUPPLY AI pode transformar a gestão da sua produção!
        </p>
      </section>
    </div>

    <footer>
      <p>&copy; 2025 supplyai. Todos os direitos reservados.</p>
    </footer>
  </div>
</template>

<script>
import { useRouter } from 'vue-router'

const router = useRouter()

function goTo(page) {
  router.push(`/${page}`)
}
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
  background-color: #ff6f00;
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

.section h2 {
  color: #ff6f00;
  margin-bottom: 1rem;
}

.section p,
.section li {
  margin-bottom: 1rem;
  line-height: 1.6;
}

footer {
  text-align: center;
  padding: 1rem;
  background-color: #ff6f00;
  color: #000;
  margin-top: 2rem;
}
</style>