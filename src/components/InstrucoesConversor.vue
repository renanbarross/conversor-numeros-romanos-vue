<template>
  <div id="instrucoes">
    <p>
      <span id="titulo-instrucoes">INSTRUÇÕES:</span>
      <br><br>
      Para converter um número romano para um número arábico, basta digitá-lo na ordem correta no campo "Número Romano"
      que o resultado da conversão será imediatamente observado no campo "Número Arábico".
      <br><br>
      Para fazer o caminho contrário, isto é, converter um número arábico para um número romano, basta digitá-lo no campo
      "Número Arábico" e, da mesma forma, observar o resultado da conversão no campo "Número Romano".
      <br><br>
      Os caracteres permitidos no campo "Número Romano" são as letras "I", "V", "X", "L", "C", "D" e "M". A digitação de
      quaisquer caracteres não correspondentes a essas letras não é permitida. As letras que compõem os números romanos
      podem ser digitadas em sua forma minúscula que automaticamente aparecerão em sua forma maiúscula. Se elas
      não estiverem na ordem correta você receberá uma conversão incorreta no campo "Número Arábico".
      <br><br>
      Os caracteres permitidos no campo "Número Arábico" são os algarismos de "0" a "9". A digitação de quaisquer
      caracteres diferentes desses algarismos não é permitida. A digitação do número "0" em sua forma unitária também
      não é permitida, porém, esse tipo de ação não gera nenhum alerta. Além disso, devem ser digitados somente números
      inteiros entre 1 e 3999, que é o conjunto de números arábicos com representação possível em números romanos.
    </p>
  </div>
</template>
<style>
#instrucoes {
  height: fit-content;
  width: 490px;
  margin-right: 80px;
  padding: 10px;
  border: 4px double black;
  font-size: 12px;
}

p {
  text-align: center;
}

#titulo-instrucoes {
  font-weight: bold;
}
</style>