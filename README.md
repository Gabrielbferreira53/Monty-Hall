# Monty-Hall
Projeto Monty Hall - Cod3r

# Créditos
Este projeto foi desenvolvido como parte do curso [Curso Web Moderno Completo com JavaScript + Projetos] presente na plataforma de cursos Udemy, pela Cod3r Cursos e ministrado por Leonardo Moura Leitao. 
  
# Modificações e Atualizações
Leves alterações foram realizadas e o código foi atualizado para a versão 3.2 do Vue.

# Requisitos
- instalar o vue de forma global
 npm i -g @vue/cli

- iniciar server
$ cd montyhall
$ npm run serve

- Necessário ter instalado o Node.js e Vue.js 3.2

# Explicação do Problema de Monty Hall
- Há varios numeros de portas e em uma delas contém um prêmio, a qual deverá ser selecionada.
- Após o usuário selecionar a porta o apresentador fecha quase todas as portas restando apenas uma.
- O usuário tem a posibilidade de trocar de porta entre a selecionada ou a ultima não fechada das demais.
- Caso o usuário troque sua porcentagem de chance de acertar a porta que contém o prêmio é maior.
  Exemplo: 
 - 10 portas. 10% de chance em cada.
 - Seleciona uma = 10% de chance de acerto.
 - Apresentador abre 8 portas vazias e sobram apenas a selecionada e mais uma das não selecionadas.
 - Trocar de porta no final lhe dará 90% de chance, já que o apresentador não abrirá a porta com o prêmio antes do final.
 - Manter a mesma ainda terá os 10% de chance, pois ela não participa do conjunto das 9 portas não selecionadas e ainda mantém os 10% de chance de acerto.
# OBSERVAÇÃO: Funciona melhor quando há mais números de portas e apenas para quando o número de portas disponiveis é maior do que 2.

