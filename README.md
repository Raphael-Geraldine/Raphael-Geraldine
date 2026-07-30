# Raphael Geraldine aqui :)

<div align="center">
  <em>Estudante de Engenharia de Computação (UTFPR) | Desenvolvedor Back-end & macOS</em>
</div>
<br>

Gosto de entender sistemas em profundidade e construir soluções que vão muito além do "apenas funciona". Sou apaixonado por arquitetura de software, otimização de baixo nível e por desbravar os bastidores dos sistemas operacionais, especialmente o **macOS**. 

### 👨‍💻 Sobre mim
- 🎓 Estudante de **Engenharia de Computação** na Universidade Tecnológica Federal do Paraná (UTFPR).
- ⚙️ Experiência prática com **Python, C e C++** (incluindo manipulação de registradores, pthreads e gerenciamento de memória em embarcados).
- 🇺🇸 **Inglês Avançado** (Leitura técnica, documentação e conversação).
- 🥋 Pratico **Jiu-Jitsu há 14 anos** — o que moldou minha disciplina, resiliência e capacidade de atuar sob pressão.
- 🎸 Nas horas vagas, a música é meu hobby: toco guitarra, violão, piano, synth e harmônica.

---

## 🍎 Destaque Principal: macOS, C++ & UX

### O Equilíbrio da Força
*Um jogo de plataforma 2D em C++ utilizando programação orientada a objetos avançada, SFML e concorrência (POSIX Threads).*

<a href="https://github.com/Raphael-Geraldine/O-Equilibrio-da-Forca" target="_blank">
  <img src="https://img.shields.io/badge/Acessar_Repositório-181717?style=for-the-badge&logo=github&logoColor=white" alt="Acessar Repositório" />
</a>
<a href="https://github.com/Raphael-Geraldine/O-Equilibrio-da-Forca/releases" target="_blank">
  <img src="https://img.shields.io/badge/Baixar_App_macOS-000000?style=for-the-badge&logo=apple&logoColor=white" alt="Baixar DMG" />
</a>
<br><br>

> **Por que este projeto está em destaque?**  
> Originalmente um trabalho acadêmico de POO em C++, decidi levar o projeto muito além do escopo exigido, focando tanto na excelência técnica quanto na experiência do usuário final. Assumi o desafio de desenvolver a versão nativa do jogo para a arquitetura **ARM64 (Apple Silicon)**, garantindo máximo desempenho e fluidez.
> 
> Para entregar uma **experiência de uso (UX)** polida e alinhada aos padrões da plataforma, não me limitei a gerar um executável. Construí uma aplicação autônoma (`.app`) com as dependências dinâmicas da biblioteca gráfica embutidas no seu _bundle_ interno e distribuí o pacote via imagem de disco (`.dmg`). Além disso, documentei o processo de _bypass_ do Gatekeeper, pois esse projeto educacional é distribuído sem um certificado pago de desenvolvedor. 
>
> Esse esforço reflete minha capacidade de unir engenharia de baixo nível (manipulação de binários e bibliotecas dinâmicas) com um cuidado minucioso com a interface e a jornada do usuário na plataforma Apple.

<table border="0" style="width: 100%;">
  <tr>
    <td width="50%" align="center">
      <img src="https://github.com/user-attachments/assets/19fd3fa7-1bf5-41b8-91b1-ef3d5466fa11" width="100%" alt="Fase 2" />
    </td>
    <td width="50%" align="center">
      <img src="https://github.com/user-attachments/assets/c9d7a13e-1f61-4d91-984b-b8b06e35ec4c" width="100%" alt="Menu Principal" />
    </td>
  </tr>
</table>

---

## Outros Projetos Relevantes

### 🐧 Intel Quartus Prime no Apple Silicon
Engenharia reversa e virtualização avançada para rodar com alta performance uma ferramenta legada x86_64, com uma teia de bibliotecas legadas em 32-bits, diretamente em um **MacBook Air M4**.

<a href="https://github.com/Raphael-Geraldine/Intel-Quartus-Prime-macOS-Apple-Silicon" target="_blank">
  <img src="https://img.shields.io/badge/Acessar_Repositório-181717?style=for-the-badge&logo=github&logoColor=white" alt="Acessar Repositório" />
</a>

- **Virtualização & Rosetta 2:** Implementação de uma VM Debian ARM64 via UTM com integração do **Rosetta 2** diretamente no kernel do Linux (`binfmt_misc` e VirtioFS), viabilizando a tradução e execução de binários x86_64 em alta performance no Apple Silicon.
- **Resolução de Dependências Legadas (32-bit/i386):** Superação de incompatibilidades profundas em ferramentas como o ModelSim por meio de compilação cruzada, reconstrução de fontes legadas (como o FreeType 2.4.12) e desenvolvimento de um *wrapper* em C para interceptar e estabilizar chamadas da `libsqlite3`.

### 📡 Arquitetura de Comunicação Óptica via Laser (FSO)
Desenvolvimento da camada de software, ponta a ponta, para um sistema de comunicação sem fio bidirecional por meio de feixes de _laser_ em ESP32. Alcance validado de **37,4 metros sem perda de pacotes**.

<a href="https://github.com/Raphael-Geraldine/Arquitetura-de-Comunicacao-Optica-Laser" target="_blank">
  <img src="https://img.shields.io/badge/Acessar_Repositório-181717?style=for-the-badge&logo=github&logoColor=white" alt="Acessar Repositório" />
</a>

- **Baixo Nível & Registradores:** Abandonei as abstrações do Arduino (`digitalWrite`) para implementar o controle de I/O escrevendo diretamente nos **registradores** do ESP32, eliminando o *jitter* na modulação do feixe de luz.
- **Gerenciamento de Memória (Chunklist):** Para evitar o esgotamento de Heap ao transmitir imagens em um microcontrolador, desenvolvi uma estrutura de dados customizada em C chamada *Chunklist*. Ela aloca e encadeia pequenos blocos dispersos na RAM sob demanda, contornando a fragmentação.
- **Determinismo com FreeRTOS:** Isolei o início transmissão óptica utilizando *FreeRTOS Tasks* com prioridade máxima fixadas em um núcleo (*core*) dedicado, garantindo que o tráfego de rede (Wi-Fi AP e Servidor HTTP) não interferisse na temporização crítica de alinhamento temporal do laser.
- **Pilha Full-Stack:** O firmware hospeda um painel web completo, onde o usuário pode enviar textos ou arquivos de imagem (JPG/PNG).

---

## Tecnologias e Ferramentas

<div align="left">
  <!-- Back-end & Linguagens -->
  <img src="https://img.shields.io/badge/C++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white" alt="C++" height="28" /><img src="https://img.shields.io/badge/c-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white" alt="C" height="28" /><img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54" alt="Python" height="28" />
  <br>
  <!-- OS & Ferramentas -->
  <img src="https://img.shields.io/badge/mac%20os-000000?style=for-the-badge&logo=macos&logoColor=F0F0F0" alt="macOS" height="28" /><img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux" height="28" /><img src="https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white" alt="Git" height="28" />
</div>

---

## Onde me encontrar também
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/raphael-geraldine/)
