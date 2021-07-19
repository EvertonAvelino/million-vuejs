<template>
  <main class="bd-masthead" id="content" role="main">
    <div class="container">
      <div class="row">
        <div class="col-6 mx-auto col-md-4 order-md-2">
          <svg
            width="512"
            height="430"
            xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink"
            class="img-fluid mb-3 mb-md-0"
            viewBox="0 0 1024 860"
            focusable="false"
            role="img"
          >
            <title>Million</title>
            <defs>
              <path
                d="m355.967,242.807l-322,216.395c-44.275,29.754 -44.275,78.443 0,108.197l322,216.395c44.275,29.754 116.725,29.754 161,0l322,-216.395c44.275,-29.754 44.275,-78.443 0,-108.197l-322,-216.395c-44.275,-29.754 -116.725,-29.754 -161,0z"
                id="b"
              />
              <filter
                filterUnits="objectBoundingBox"
                y="-4.3%"
                x="-4%"
                height="112%"
                width="108%"
                id="a"
              >
                <feGaussianBlur stdDeviation="10" />
              </filter>
              <path
                d="m355.967,132.807l-322,216.395c-44.275,29.754 -44.275,78.443 0,108.197l322,216.395c44.275,29.754 116.725,29.754 161,0l322,-216.395c44.275,-29.754 44.275,-78.443 0,-108.197l-322,-216.395c-44.275,-29.754 -116.725,-29.754 -161,0z"
                id="e"
              />
              <filter
                filterUnits="objectBoundingBox"
                y="-4.3%"
                x="-4%"
                height="112%"
                width="108%"
                id="d"
              >
                <feGaussianBlur stdDeviation="10" />
              </filter>
              <path
                d="m355.967,22.807l-322,216.395c-44.275,29.754 -44.275,78.443 0,108.197l322,216.395c44.275,29.754 116.725,29.754 161,0l322,-216.395c44.275,-29.754 44.275,-78.443 0,-108.197l-322,-216.395c-44.275,-29.754 -116.725,-29.754 -161,0z"
                id="h"
              />
              <filter
                filterUnits="objectBoundingBox"
                y="-4.3%"
                x="-4%"
                height="112%"
                width="108%"
                id="g"
              >
                <feGaussianBlur stdDeviation="10" />
              </filter>
              <linearGradient y2="100%" y1="0%" x2="50%" x1="50%" id="c">
                <stop stop-color="#5c24ae" offset="0%" />
                <stop stop-color="#30135a" offset="100%" />
              </linearGradient>
              <linearGradient y2="100%" y1="-17.303%" x2="50%" x1="50%" id="f">
                <stop stop-color="#7331d4" offset="0%" />
                <stop stop-color="#461b84" offset="100%" />
              </linearGradient>
              <linearGradient y2="100%" y1="0%" x2="50%" x1="50%" id="i">
                <stop stop-color="#905bdd" offset="0%" />
                <stop stop-color="#5521a0" offset="100%" />
              </linearGradient>
            </defs>
            <g>
              <title>background</title>
              <rect
                fill="none"
                id="canvas_background"
                height="602"
                width="802"
                y="-1"
                x="-1"
              />
            </g>
            <g>
              <title>Million</title>
              <g id="svg_2">
                <use
                  id="svg_3"
                  x="42"
                  y="51"
                  xlink:href="#b"
                  filter="url(#a)"
                  fill="#000"
                />
                <use id="svg_4" x="42" y="51" xlink:href="#b" fill="url(#c)" />
              </g>
              <g id="svg_5">
                <use
                  id="svg_6"
                  x="42"
                  y="51"
                  xlink:href="#e"
                  filter="url(#d)"
                  fill="#000"
                />
                <use id="svg_7" x="42" y="51" xlink:href="#e" fill="url(#f)" />
              </g>
              <g id="svg_8">
                <use
                  id="svg_9"
                  x="42"
                  y="50"
                  xlink:href="#h"
                  filter="url(#g)"
                  fill="#000"
                />
                <use id="svg_10" x="42" y="50" xlink:href="#h" fill="url(#i)" />
              </g>
              <text
                stroke="#000"
                transform="matrix(18.55555534362793,0,0,7.303030490875244,-11867.55541229248,-2549.772803261876) "
                xml:space="preserve"
                text-anchor="start"
                font-family="Helvetica, Arial, sans-serif"
                font-size="24"
                id="svg_12"
                y="399.4375"
                x="662.5"
                stroke-width="0"
                fill="#000000"
              />
              <image
                xlink:href="data:image/png;"
                id="svg_18"
                height="255"
                width="385"
                y="193.5"
                x="279.5"
              />
            </g>
          </svg>
        </div>
        <div class="col-md-8 order-md-1 text-center text-md-left pr-md-5">
          <h1 class="mb-3">Ações - Cadastro</h1>
          <p class="lead mb-4"></p>
          <form method="" action="">
            <label>Código</label>
            <input
              class="form-control"
              v-model="acao.cod_empresa"
              id="codigo"
              type="text"
            />
            <label>Nome</label>
            <input
              class="form-control"
              v-model="acao.nome_empresa"
              id="nome"
              type="text"
            />
            <label>Taxa</label>
            <input
              class="form-control"
              v-model="acao.taxa_juros"
              type="number"
              id="taxa"
            />
            <label>Tipo</label>
            <select class="form-control" v-model="acao.tipo" id="tipo">
              <option value="ON">ON</option>
              <option value="PN">PN</option>
            </select>
            <br />
            <div v-if="erro" class="alert alert-danger">
              {{ erro }}
            </div>
            <button type="button" v-on:click="salvar()" class="btn btn-success">
              Salvar</button
            >&nbsp; &nbsp;
            <router-link to="/acoes" tag="button" class="btn btn-danger"
              >Voltar</router-link
            >
          </form>
        </div>
      </div>
    </div>
  </main>
</template>


<script>
import axios from "axios";

export default {
  data: () => {
    return {
      erro: "",
      acao: {
        nome_empresa: "",
        cod_empresa: "",
        taxa_juros: "",
        tipo: "",
      },
    };
  },
  methods: {
    salvar() {
      if (!this.acao._id) {
        axios
          .post("http://localhost:3000/acoes.json", this.acao, {
            headers: { token: "123456" },
          })
          .then(() => {
            this.$router.push("/acoes");
          })
          .catch((err) => {
            this.erro = JSON.stringify(err);
          });
      } else {
        axios
          .put(`http://localhost:3000/acoes/${this.acao._id}.json`, this.acao, {
            headers: { token: "123456" },
          })
          .then(() => {
            this.$router.push("/acoes");
          })
          .catch((err) => {
            this.erro = JSON.stringify(err);
          });
      }
    },
  },
  created() {
    window.scrollTo(500, 0);
    let id = this.$route.params.id;
    axios
      .get(`http://localhost:3000/acoes/${id}.json`, {
        headers: { token: "123456" },
      })
      .then((res) => {
        this.acao = res.data;
      })
      .catch((err) => {
        console.log(err);
      });
  },
};
</script>

