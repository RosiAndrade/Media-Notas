//Rosilaine
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Resultado de Notas</title>
    <script>
        function calcularMedia() {
            // Recebe as duas notas digitadas pelo usuário
            let nota1 = parseFloat(prompt("Digite a primeira nota:"));
            let nota2 = parseFloat(prompt("Digite a segunda nota:"));

            // Calcula a média das notas
            let media = (nota1 + nota2) / 2;

            // Verifica a situação do aluno
            let situacao;
            if (media <= 4.5) {
                situacao = "Aluno Reprovado";
            } else if (media <= 6.5) {
                situacao = "Aluno de Recuperação";
            } else if (media <= 10) {
                situacao = "Aluno Aprovado";
            } else {
                situacao = "Nota inválida!";
            }

            // Exibe a média e a situação na tela
            document.getElementById("resultado").innerHTML = `
                A média do aluno é: ${media.toFixed(2)}<br>
                Situação: ${situacao}
            `;
        }
    </script>
</head>
<body>
    <h1>Calculadora de Média e Situação do Aluno</h1>
    <button onclick="calcularMedia()">Calcular Média</button>
    <div id="resultado"></div>
</body>
</html>

