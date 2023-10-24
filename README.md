# Conversor de Números Romanos

Trata-se de um conversor de números romanos em que o usuário pode inserir números romanos em um campo do lado esquerdo e imediatamente observar sua conversão para números arábicos do lado direito. O caminho inverso também pode ser feito, ou seja, o usuário inserir números arábicos no campo a direita e ver sua conversão para números romanos no campo a esquerda.

## Descrição do projeto

Para converter um número romano para um número arábico, basta que o usuário digite o número na ordem correta no campo "Número Romano" que o resultado da conversão será imediatamente observado no campo "Número Arábico".

Para fazer o caminho contrário, isto é, converter um número arábico para um número romano, basta digitá-lo no campo
"Número Arábico" e, da mesma forma, observar o resultado da conversão no campo "Número Romano".

Os caracteres permitidos no campo "Número Romano" são as letras "I", "V", "X", "L", "C", "D" e "M". A digitação de
quaisquer caracteres não correspondentes a essas letras não é permitida. As letras que compõem os números romanos
podem ser digitadas em sua forma minúscula que automaticamente aparecerão em sua forma maiúscula. Se elas
não estiverem na ordem correta o usuário receberá uma conversão incorreta no campo "Número Arábico".

Os caracteres permitidos no campo "Número Arábico" são os algarismos de "0" a "9". A digitação de quaisquer
caracteres diferentes desses algarismos não é permitida. A digitação do número "0" em sua forma unitária também
não é permitida, porém, esse tipo de ação não gera nenhum alerta. Além disso, devem ser digitados somente números
inteiros entre 1 e 3999, que é o conjunto de números arábicos com representação possível em números romanos.

Essas instruções também estão presentes na interface do conversor.

## Tecnologia utilizada

Framework Vue.js 3 (Options API).

## Configuração Recomendada da IDE

VSCode + Volar (e desative o Vetur)

## Personalização da Configuração
Consulte Referência de Configuração do Vite.

## Configuração do Projeto
```sh
npm install
```

### Compilação e Recarga Automática para Desenvolvimento
```sh
npm run dev
```

### Compilação e Minificação para Produção
```sh
npm run build
```