> HTML
````HTML
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fatorial e Número Primo</title>
</head>
<body>
    <h2>Calculadora de Fatorial e Verificador de Número Primo</h2>
    
    <!-- Campo para entrada do número -->
    <label for="numero">Digite um número:</label>
    <input type="number" id="numero">
    <button onclick="calcular()">Calcular</button>
    
    <!-- Local onde será exibido o resultado -->
    <p id="resultado"></p>
````
  > FUNÇÃO CALCULAR FATORIAL
```` JAVASCRIPT
        
         * @param {number} n - Número para calcular o fatorial.
         * @returns {number} - Resultado do fatorial.
         */
        function calcularFatorial(n) {
            if (n === 0) {
                return 1;
            } else {
                return n * calcularFatorial(n - 1);
            }
        }
````
> FUNÇÃO DE VERIFIAR NÚMEROS PRIMOS
```` JAVASCRIPT
         
         * @param {number} numero - Número a ser verificado.
         * @returns {boolean} - Retorna true se for primo, false caso contrário.
         */
        function verificarNumeroPrimo(numero) {
            if (numero <= 1) {
                return false;
            }
            for (let i = 2; i < numero; i++) {
                if (numero % i === 0) {
                    return false;
                }
            }
            return true;
        }
````
> FUÇAÕ QUE LÊ NÚMERO DA ENTRADA
```` JAVASCRIPT
         * Função principal que lê o número da entrada, calcula o fatorial e verifica se é primo.
         */
        function calcular() {
            let numero = parseInt(document.getElementById("numero").value);
            let fatorial = calcularFatorial(numero);
            let primo = verificarNumeroPrimo(numero);
            
            // Exibição do resultado na página
            document.getElementById("resultado").innerHTML =
                `O fatorial de ${numero} é ${fatorial} <br> ` +
                `O número ${numero} ${primo ? "é primo." : "não é primo."}`;
        }
````

</body>
</html>


## QUESTÕES PARA REFLEXÃO

## 1.
  A indentação foi corrigida para melhorar a legibilidade.

Foram adicionados comentários explicativos em cada função para facilitar o entendimento.

A estrutura do código foi mantida, mas agora está mais organizada e intuitiva.


## 2. 
A rastreabilidade permite que desenvolvedores entendam rapidamente o propósito de cada parte do código.

Com um código bem documentado, futuras manutenções e correções podem ser feitas com mais eficiência.

Ajuda a identificar a origem de possíveis erros e a entender a lógica aplicada.

## 3.
Uso de indentação adequada.

Adição de comentários explicativos.

Nomeação clara e descritiva de variáveis e funções.

Separação lógica das responsabilidades dentro do código.

Uso de padrões de desenvolvimento para facilitar a colaboração.

## 4.
O Markdown permite criar documentações estruturadas de forma simples e legível.

É um formato amplamente utilizado e compatível com diversas plataformas.

Facilita a organização de informações, incluindo código-fonte, listas e explicações detalhadas.

## 5.
A padronização permite que diferentes desenvolvedores compreendam o código sem dificuldade.

Boas práticas reduzem erros e tornam o código mais eficiente e seguro.

Um código bem estruturado pode ser expandido e adaptado sem comprometer sua funcionalidade original.
