# 🖨️ Terminal Elgin i8/i9 em C
### *Controle e Automação de Impressora Térmica Elgin via DLL Nativa*
---

## 📘 Sobre o Projeto

Sistema de linha de comando desenvolvido em **linguagem C** para comunicação, automação e testes de impressão com impressoras térmicas **Elgin i8 e i9** no Windows, utilizando carregamento dinâmico da biblioteca oficial `E1_Impressora01.dll` (via API Win32 `LoadLibraryA` / `GetProcAddress`).

---

## 🧰 Tecnologias Utilizadas

- **Linguagem:** C (C99+)
- **Sistema Operacional:** Windows
- **Compilador:** MinGW (GCC 32 bits / x86)
- **Biblioteca Nativa:** `E1_Impressora01.dll` (arquitetura x86)
- **Arquivos de Teste SAT:** `XMLSAT.xml` e `CANC_SAT.xml` na raiz do projeto

---

## 📁 Estrutura do Projeto

Todos os arquivos ficam na **raiz** do repositório para carregamento direto em tempo de execução:

- `a.c` → Código-fonte principal do sistema
- `E1_Impressora01.dll` → Biblioteca dinâmica da Elgin (x86 / 32 bits)
- `XMLSAT.xml` → Arquivo de exemplo para impressão de cupom fiscal SAT
- `CANC_SAT.xml` → Arquivo de exemplo para impressão de cancelamento SAT
- `.gitignore` → Ignora arquivos compilados (`.exe`)
- `README.md` → Documentação do projeto

---

## ⚙️ Instalação, Compilação e Execução

### 🔽 1. Baixar o Projeto do GitHub
1. Acesse o repositório e clique no botão verde **Code** → **Download ZIP** (ou use `git clone`).
2. Extraia o arquivo ZIP para uma pasta local.

### 🛠️ 2. Compilar o Código em C
1. Abra o terminal (Prompt de Comando, PowerShell ou terminal integrado do VS Code) na pasta raiz do projeto.
2. Compile o arquivo `a.c` utilizando o GCC (MinGW 32 bits):
   ```bash
   gcc a.c -o impressora.exe
