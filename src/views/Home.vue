<script>
import InstrucoesConversor from '@/components/InstrucoesConversor.vue';

export default {
  components: {
    InstrucoesConversor
  },
  data() {
    return {
      romano: "",
      arabico: "",
      i: "I",
      x: "X",
      c: "C",
      m: "M"
    }
  },
  watch: {
    romano(novoTexto) {
      this.romano = novoTexto.replace(/[^ivxlcdmIVXLCDM]/g, "");
      if (this.romano != novoTexto) {
        alert("Insira um caractere válido!");
      } else {
        this.romano = novoTexto.toUpperCase();
      }
    },
    arabico(novoNumero) {
      this.arabico = novoNumero.replace(/[^0-9]/g, "");
      if (this.arabico != novoNumero) {
        alert("Insira um caractere válido!");
      }
      if (novoNumero == 0) {
        this.arabico = "";
      }
      if (novoNumero > 3999) {
        alert("Digite um número inteiro entre 1 e 3999.");
      }
    }
  },

  methods: {
    converterRomanoParaArabico() {
      this.arabico = "";
      let calculo = this.romano;
      let resultado = "";

      if (calculo.startsWith("M")) {
        if (calculo.startsWith("MMM")) {
          resultado = resultado.concat(3);
          calculo = calculo.replace(new RegExp("^" + "MMM"), "");
        }

        if (calculo.startsWith("MM")) {
          resultado = resultado.concat(2);
          calculo = calculo.replace(new RegExp("^" + "MM"), "");
        }

        if (calculo.startsWith("M")) {
          resultado = resultado.concat(1);
          calculo = calculo.replace(new RegExp("^" + "M"), "");
        }
      } else {
        resultado = resultado.concat(0);
      }

      if (calculo.startsWith("C") || calculo.startsWith("D")) {
        if (calculo.startsWith("CM")) {
          resultado = resultado.concat(9);
          calculo = calculo.replace(new RegExp("^" + "CM"), "");
        }

        if (calculo.startsWith("DCCC")) {
          resultado = resultado.concat(8);
          calculo = calculo.replace(new RegExp("^" + "DCCC"), "");
        }

        if (calculo.startsWith("DCC")) {
          resultado = resultado.concat(7);
          calculo = calculo.replace(new RegExp("^" + "DCC"), "");
        }

        if (calculo.startsWith("DC")) {
          resultado = resultado.concat(6);
          calculo = calculo.replace(new RegExp("^" + "DC"), "");
        }

        if (calculo.startsWith("D")) {
          resultado = resultado.concat(5);
          calculo = calculo.replace(new RegExp("^" + "D"), "");
        }

        if (calculo.startsWith("CD")) {
          resultado = resultado.concat(4);
          calculo = calculo.replace(new RegExp("^" + "CD"), "");
        }

        if (calculo.startsWith("CCC")) {
          resultado = resultado.concat(3);
          calculo = calculo.replace(new RegExp("^" + "CCC"), "");
        }

        if (calculo.startsWith("CC")) {
          resultado = resultado.concat(2);
          calculo = calculo.replace(new RegExp("^" + "CC"), "");
        }

        if (calculo.startsWith("C")) {
          resultado = resultado.concat(1);
          calculo = calculo.replace(new RegExp("^" + "C"), "");
        }
      } else {
        resultado = resultado.concat(0);
      }

      if (calculo.startsWith("X") || calculo.startsWith("L")) {
        if (calculo.startsWith("XC")) {
          resultado = resultado.concat(9);
          calculo = calculo.replace(new RegExp("^" + "XC"), "");
        }

        if (calculo.startsWith("LXXX")) {
          resultado = resultado.concat(8);
          calculo = calculo.replace(new RegExp("^" + "LXXX"), "");
        }

        if (calculo.startsWith("LXX")) {
          resultado = resultado.concat(7);
          calculo = calculo.replace(new RegExp("^" + "LXX"), "");
        }

        if (calculo.startsWith("LX")) {
          resultado = resultado.concat(6);
          calculo = calculo.replace(new RegExp("^" + "LX"), "");
        }

        if (calculo.startsWith("L")) {
          resultado = resultado.concat(5);
          calculo = calculo.replace(new RegExp("^" + "L"), "");
        }

        if (calculo.startsWith("XL")) {
          resultado = resultado.concat(4);
          calculo = calculo.replace(new RegExp("^" + "XL"), "");
        }

        if (calculo.startsWith("XXX")) {
          resultado = resultado.concat(3);
          calculo = calculo.replace(new RegExp("^" + "XXX"), "");
        }

        if (calculo.startsWith("XX")) {
          resultado = resultado.concat(2);
          calculo = calculo.replace(new RegExp("^" + "XX"), "");
        }

        if (calculo.startsWith("X")) {
          resultado = resultado.concat(1);
          calculo = calculo.replace(new RegExp("^" + "X"), "");
        }
      } else {
        resultado = resultado.concat(0);
      }

      if (calculo.startsWith("I") || calculo.startsWith("V")) {
        if (calculo.startsWith("IX")) {
          resultado = resultado.concat(9);
          calculo = calculo.replace(new RegExp("^" + "IX"), "");
        }

        if (calculo.startsWith("VIII")) {
          resultado = resultado.concat(8);
          calculo = calculo.replace(new RegExp("^" + "VIII"), "");
        }

        if (calculo.startsWith("VII")) {
          resultado = resultado.concat(7);
          calculo = calculo.replace(new RegExp("^" + "VII"), "");
        }

        if (calculo.startsWith("VI")) {
          resultado = resultado.concat(6);
          calculo = calculo.replace(new RegExp("^" + "VI"), "");
        }

        if (calculo.startsWith("V")) {
          resultado = resultado.concat(5);
          calculo = calculo.replace(new RegExp("^" + "V"), "");
        }

        if (calculo.startsWith("IV")) {
          resultado = resultado.concat(4);
          calculo = calculo.replace(new RegExp("^" + "IV"), "");
        }

        if (calculo.startsWith("III")) {
          resultado = resultado.concat(3);
          calculo = calculo.replace(new RegExp("^" + "III"), "");
        }

        if (calculo.startsWith("II")) {
          resultado = resultado.concat(2);
          calculo = calculo.replace(new RegExp("^" + "II"), "");
        }

        if (calculo.startsWith("I")) {
          resultado = resultado.concat(1);
          calculo = calculo.replace(new RegExp("^" + "I"), "");
        }
      } else {
        resultado = resultado.concat(0);
      }
      this.arabico = String(parseInt(resultado, 10));
    },
    converterArabicoParaRomano() {
      this.romano = "";
      let calculo = this.arabico;
      let resultado = "";

      if (calculo >= 1000) {
        calculo = Math.floor(calculo / 1000);

        if (calculo >= 1 && calculo <= 3) {
          resultado += this.m.repeat(calculo);
        }

        calculo = this.arabico % 1000;
      }
      if (calculo >= 100) {
        calculo = Math.floor(calculo / 100);

        if (calculo >= 1 && calculo <= 3) {
          resultado += this.c.repeat(calculo);
        }

        if (calculo == 4) {
          resultado += "CD";
        }

        if (calculo == 5) {
          resultado += "D";
        }

        if (calculo == 6) {
          resultado += "DC";
        }

        if (calculo == 7) {
          resultado += "DCC";
        }

        if (calculo == 8) {
          resultado += "DCCC";
        }

        if (calculo == 9) {
          resultado += "CM";
        }
        calculo = this.arabico % 100;
      }

      if (calculo >= 10) {
        calculo = Math.floor(calculo / 10);

        if (calculo >= 1 && calculo <= 3) {
          resultado += this.x.repeat(calculo);
        }
        if (calculo == 4) {
          resultado += "XL";
        }

        if (calculo == 5) {
          resultado += "L";
        }

        if (calculo == 6) {
          resultado += "LX";
        }

        if (calculo == 7) {
          resultado += "LXX";
        }

        if (calculo == 8) {
          resultado += "LXXX";
        }

        if (calculo == 9) {
          resultado += "XC";
        }

        calculo = this.arabico % 10;
      }

      if (calculo >= 1) {
        calculo = Math.floor(calculo / 1);

        if (calculo >= 1 && calculo <= 3) {
          resultado += this.i.repeat(calculo);
        }
        if (calculo == 4) {
          resultado += "IV";
        }

        if (calculo == 5) {
          resultado += "V";
        }

        if (calculo == 6) {
          resultado += "VI";
        }

        if (calculo == 7) {
          resultado += "VII";
        }

        if (calculo == 8) {
          resultado += "VIII";
        }

        if (calculo == 9) {
          resultado += "IX";
        }
      }
      this.romano = resultado;
    }
  }
}
</script>

<template>
  <div id="conteudo">
    <h1>Conversor de Números Romanos</h1>
    <div id="layout">
      <InstrucoesConversor />
      <div id="conversor">
        <div class="conteudo-input">
          <label for="romano">Número Romano</label>
          <input type="text" id="romano" name="romano" v-model="romano" @input="converterRomanoParaArabico()">
        </div>
        <i class="bi bi-arrow-left-right"></i>
        <div class="conteudo-input">
          <label for="arabico">Número Arábico</label>
          <input type="text" id="arabico" name="arabico" v-model="arabico" @input="converterArabicoParaRomano()">
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
#conteudo {
  height: 100vh;
  width: 50vw;
  display: flex;
  flex-direction: column;
  align-items: center;
}

h1 {
  text-align: center;
}

#layout {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  margin-top: 30px;
}

#conversor {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

.conteudo-input {
  display: flex;
  flex-direction: column;
  align-items: center;
}

input {
  margin: 0 10px 0;
}

i {
  font-size: 20px;
}

h2 {
  color: black;
  margin: 0 10px 0;
}

h2>i {
  margin-right: 10px;
}
</style>
