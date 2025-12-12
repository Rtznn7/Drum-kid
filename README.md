DRUM KIT – Projeto Interativo de Sons

Este projeto é um Drum Kit virtual, onde cada tecla do teclado corresponde a um som diferente, simulando uma bateria digital. Basta pressionar as teclas exibidas na tela ou clicar nos blocos para disparar os sons. O projeto combina HTML, CSS e JavaScript para criar uma experiência rápida, visual e responsiva.

 Como funciona
 Interface Principal

A interface contém:

Um título estilizado com gradiente colorido.

Um contêiner onde cada tecla (A, S, D, F, G, H, J, K, L) aparece como um bloco clicável.

Fundo com imagem personalizada para reforçar o ambiente musical.

 Teclas Interativas

Cada bloco na tela:

representa uma letra do teclado,

está associado a um arquivo de som,

aumenta de tamanho e recebe brilho quando ativado.

O efeito visual acontece através da classe active, aplicada e removida automaticamente.

 Sistema de Áudio

O JavaScript controla todos os sons.
Cada letra corresponde a um arquivo MP3 dentro da pasta /sounds.

Exemplo:

const sons = {
    'A': '1.mp3',
    'S': '2.mp3',
    ...
}


Quando o usuário:

clica em uma tecla na tela, ou

pressiona a tecla no teclado,

o script carrega e toca o som correto com:

new Audio(`./sounds/${sons[letra]}`).play();

 Funcionalidades do JavaScript

O JS responsável pelo kit faz:

1️ Renderização Automática das Teclas

Ele cria as div.key dinamicamente com base no objeto sons.

2️ Detecção de Eventos

Clique na tela

Teclas do teclado (keyup)

3️ Animação das Teclas

Quando uma tecla é acionada:

É aplicada a classe .active

Após o fim da animação (transitionend), a classe é removida

4️ Sistema Limpo e Modular

Cada função tem uma responsabilidade:

criar tecla

tocar som

aplicar efeito

remover efeito

validar tecla

 Estilo (CSS)

O visual usa:

Fundo com imagem de bateria,

Título colorido com gradiente e recorte de texto,

Teclas com bordas brancas e fundo preto translúcido,

Escala animada quando ativadas,

Sombras fortes para dar efeito de impacto.

O layout também é flexível, se adaptando à largura da tela.

 Objetivo do Projeto

Este Drum Kit serve como:

treino de manipulação de áudio no navegador,

prática de eventos de teclado,

criação de interfaces dinâmicas com DOM,

base para jogos musicais simples.

É um ótimo projeto para aprender interação em tempo real usando JavaScript puro.
