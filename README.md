# 🎹 Piano Virtual

<div align="center">
  
  ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
  ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
  ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
  
  <p>Um simulador de piano virtual interativo desenvolvido com tecnologias web puras</p>
  
</div>

---

## 📋 Sobre o Projeto

Este é um projeto de piano virtual desenvolvido como parte do desafio de projeto do **Bootcamp de Front-end da [DIO (Digital Innovation One)](https://dio.me)**. O simulador permite tocar notas musicais tanto clicando nas teclas quanto usando o teclado do computador, oferecendo uma experiência interativa e divertida.

## ✨ Funcionalidades

- 🎵 **17 teclas funcionais** (combinação de teclas brancas e pretas)
- ⌨️ **Suporte para teclado físico** - toque as notas usando as teclas do seu computador
- 🖱️ **Clique nas teclas** - interação via mouse
- 🔊 **Controle de volume** - ajuste o volume através de um slider
- 👁️ **Toggle de visibilidade** - mostre ou oculte as letras das teclas
- 🎨 **Feedback visual** - animação ao pressionar as teclas

## 🎮 Como Usar

### Teclado do Computador

As seguintes teclas correspondem às notas do piano:

**Teclas Brancas:** `A`, `S`, `D`, `F`, `T`, `Y`, `U`, `K`, `L`, `;`

**Teclas Pretas:** `W`, `E`, `F`, `G`, `H`, `J`, `O`, `P`

### Controles

- **Volume:** Use o controle deslizante para ajustar o volume de 0 a 100%
- **Teclas:** Clique no toggle para mostrar/ocultar as letras nas teclas do piano

## 🚀 Tecnologias Utilizadas

- **HTML5** - Estrutura semântica da página
- **CSS3** - Estilização e animações
  - Flexbox para layout
  - Gradientes lineares
  - Transições e animações
  - Custom checkbox styling
- **JavaScript (Vanilla)** - Lógica e interatividade
  - Manipulação do DOM
  - Event Listeners
  - Web Audio API
  - Dataset API

## 📁 Estrutura do Projeto

```
piano-virtual/
│
├── index.html                 # Página principal
├── README.md                  # Documentação
│
├── src/
│   ├── scripts/
│   │   └── engine.js         # Lógica do piano
│   │
│   ├── styles/
│   │   ├── reset.css         # Reset de estilos padrão
│   │   └── main.css          # Estilos principais
│   │
│   └── tunes/                # Arquivos de áudio (.wav)
│       ├── a.wav
│       ├── w.wav
│       ├── s.wav
│       └── ...
```

## 🎯 Conceitos Aplicados

### HTML
- Estruturação semântica
- Data attributes (`data-key`)
- Inputs customizados (range e checkbox)

### CSS
- CSS Reset para consistência entre navegadores
- Flexbox para alinhamento e distribuição
- Pseudo-elementos (`::before`)
- Gradientes lineares para efeito de profundidade
- Box-shadow para feedback visual
- Transições suaves

### JavaScript
- `querySelector` e `querySelectorAll` para seleção de elementos
- Event Listeners (`click`, `keydown`, `input`)
- Manipulação de classes (`classList.add`, `classList.remove`, `classList.toggle`)
- Web Audio API para reprodução de sons
- `setTimeout` para animações temporais
- Array methods (`forEach`, `includes`, `push`)

## 💡 Destaques do Código

### Reprodução de Som Dinâmica
```javascript
const playTune = (key) => {
    audio.src = `src/tunes/${key}.wav`;
    audio.play();
    // Feedback visual
    const clickedKey = document.querySelector(`[data-key="${key}"]`);
    clickedKey.classList.add('active');
    setTimeout(() => {
        clickedKey.classList.remove('active');
    }, 150);
};
```

### Mapeamento de Teclas
```javascript
pianoKeys.forEach((key) => {
    key.addEventListener('click', () => playTune(key.dataset.key));
    mapedKeys.push(key.dataset.key);
});
```

## 🎨 Design

O projeto apresenta um design moderno e elegante com:
- Fundo azul claro (`#e3f2fd`)
- Container preto com bordas arredondadas
- Teclas brancas e pretas realistas com gradientes
- Animações suaves ao pressionar
- Interface minimalista e intuitiva

## 📦 Como Executar

1. Clone este repositório:
```bash
git clone [url-do-repositorio]
```

2. Navegue até a pasta do projeto:
```bash
cd piano-virtual
```

3. Abra o arquivo `index.html` no seu navegador preferido

**Nota:** Certifique-se de que os arquivos de áudio (.wav) estejam na pasta `src/tunes/` para o funcionamento correto do piano.

## 🎓 Aprendizados

Este projeto permitiu praticar e consolidar conhecimentos em:
- Manipulação avançada do DOM
- Event handling em JavaScript
- Web Audio API
- CSS moderno e técnicas de layout
- Criação de componentes interativos
- Boas práticas de organização de código

## 🤝 Contribuições

Contribuições são sempre bem-vindas! Sinta-se à vontade para:
- Reportar bugs
- Sugerir novas funcionalidades
- Melhorar a documentação
- Enviar pull requests

## 📄 Licença

Este projeto foi desenvolvido para fins educacionais como parte do Bootcamp de Front-end da DIO.

---

<div align="center">
  
  Desenvolvido com 💜 durante o Bootcamp de Front-end da **[Digital Innovation One](https://www.dio.me/)**
  
</div>