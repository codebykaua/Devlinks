# Devlinks
Resumo do Projeto DevLinks - Kauã França

Neste projeto, recriei a aplicação DevLinks do programa Discover da Rocketseat, aplicando personalizações avançadas para aprimorar o design, a interatividade e a experiência do usuário.

Abaixo, detalho as tecnologias, as técnicas de estilização e as bibliotecas utilizadas para alcançar o resultado final.

1. Tecnologias Utilizadas

HTML5: Estruturação semântica do conteúdo.

CSS3: Estilização avançada, utilizando variáveis (Custom Properties) para gerenciar os temas (Claro e Escuro) e animações baseadas em Keyframes e Transições.

JavaScript Vanilla: Lógica para a alternância do tema (Light/Dark mode) e inicialização das interações 3D.

Ionicons: Biblioteca de ícones utilizada para as redes sociais (GitHub, Instagram, LinkedIn).

Vanilla Tilt (JavaScript Library): Biblioteca externa leve utilizada para criar efeitos de inclinação 3D suaves e interativos.

2. Modificações e Melhorias no Design

A. Estilização da Foto de Perfil (Premium Look)

O objetivo foi dar um destaque maior à foto de perfil, garantindo que ela ficasse perfeitamente alinhada e interativa.

Recorte Circular Perfeito: Utilizei width: 112px; e height: 112px; combinados com object-fit: cover; e border-radius: 50%;. Isso assegura que a imagem se torne um círculo exato, sem esticar ou achatar a foto original (image.png).

Borda Dinâmica: Adicionei uma border: 2px solid var(--stroke-color); que acompanha as cores do tema atual (claro ou escuro).

Sombra Profunda: Apliquei box-shadow: 0 8px 24px rgba(0, 0, 0, 0.2); para criar a ilusão de que a foto está suspensa sobre o fundo.

B. Efeito Glassmorphism (Efeito Vidro)

Para modernizar os botões e os links, apliquei a técnica de Glassmorphism, que cria a ilusão de um vidro fosco flutuando sobre o plano de fundo.

Implementação: Utilizei a propriedade backdrop-filter: blur(12px); (e -webkit-backdrop-filter para compatibilidade). Isso faz com que o plano de fundo por trás dos botões fique embaçado.

Ajuste de Cores: Ajustei as variáveis --surface-color e --surface-color-hover para garantir que o "vidro" tenha a opacidade ideal, destacando os botões sem perder a textura da imagem de fundo.

3. Animações e Interatividade

A. Animação de Entrada (Fade Up)

Para que o site não apareça de forma abrupta ao carregar, criei uma animação de entrada suave.

Técnica: Utilizei @keyframes fadeUp. O container principal inicia com opacity: 0; e transform: translateY(20px);, subindo e revelando o conteúdo suavemente em 0.8 segundos (animation: fadeUp 0.8s ease-out forwards;).

B. Interatividade 3D e Reflexos de Luz (Vanilla Tilt)

Esta foi a principal adição para elevar o nível do projeto. Utilizei o JavaScript da biblioteca Vanilla Tilt para dar vida aos elementos:

Nos Botões (Links): Configurei a biblioteca para reagir ao movimento do mouse (max: 10, speed: 400), fazendo com que o botão se incline na direção do cursor. Adicionei também a propriedade glare: true (reflexo de luz), o que reforça muito a sensação de um objeto de vidro real e brilhante.

Na Foto de Perfil: A foto recebeu um efeito Tilt ainda mais pronunciado (max: 20), além de um scale: 1.05, que faz a imagem dar um leve "pulo" (zoom in) quando o mouse passa por cima. Isso substituiu as transições CSS mais simples, garantindo um efeito fluido e tridimensional.

C. Transições Suaves (Hover e Mudança de Tema)

Hover nos Ícones Sociais: Adicionei um transform: scale(1.15) translateY(-2px); nos ícones do rodapé. Ao interagir, eles crescem levemente e sobem, simulando botões de aplicativos móveis.

Mudança de Tema (Switch): A transição do botão que alterna entre claro e escuro recebeu um cubic-bezier no CSS (transition: transform 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);). Isso cria um efeito elástico e natural quando a "bolinha" desliza de um lado para o outro. Todo o fundo do site (Background Color e Image) também altera de forma suave através da propriedade transition: background 0.5s ease.

4. Funcionalidade Extra (JavaScript)

Saudação Dinâmica: Adicionei um pequeno script (window.onload) que lê a hora do sistema do usuário e injeta uma saudação automática ("Bom dia!", "Boa tarde!" ou "Boa noite!") logo acima do nome de usuário, tornando a interface mais amigável e personalizada.
