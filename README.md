# 🖨️ Terminal Elgin i8/i9 em C
### *Controle e Automação de Impressora Térmica Elgin i8/i9 em C*
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
2. Compile o arquivo `a.c` utilizando o GCC (MinGW 32 bits): `gcc a.c -o impressora.exe`

### ▶️ 3. Executar e Fazer Login
1. Execute o programa gerado: `.\impressora.exe`
2. Informe as credenciais de acesso (limite de **3 tentativas**):
   - **Usuário:** `admin`
   - **Senha:** `1234`

---

## 🧪 Funcionalidades e Testes Disponíveis no Menu

- **1 - Configurar Conexão:** Define tipo de conexão (`1` = USB), modelo (`i8` ou `i9`), porta (`USB`) e parâmetro adicional (`0`).
- **2 - Abrir Conexão:** Estabelece comunicação com a impressora configurada.
- **3 - Fechar Conexão:** Encerra a comunicação ativa com a impressora.
- **4 - Imprimir Texto:** Imprime texto personalizado com quantidade definida de cópias e corte automático.
- **5 - Imprimir QR Code:** Gera e imprime um QR Code a partir do conteúdo digitado.
- **6 - Imprimir Código de Barras:** Imprime código de barras padrão Code 128 com corte automático.
- **7 - Imprimir XML SAT:** Lê o arquivo `XMLSAT.xml` e imprime o cupom fiscal SAT.
- **8 - Imprimir XML de Cancelamento SAT:** Lê o arquivo `CANC_SAT.xml` e imprime o comprovante de cancelamento SAT.
- **9 - Abrir Gaveta (Elgin):** Aciona a abertura da gaveta conectada via comando específico Elgin.
- **10 - Abrir Gaveta:** Aciona a abertura da gaveta via comando padrão.
- **11 - Sinal Sonoro:** Emite bipes sonoros na impressora conforme a quantidade informada.
- **0 - Sair:** Fecha a conexão, libera a DLL da memória e encerra o programa.

---

## 📚 Documentação Adicional

- Manual da Impressora Térmica **Elgin i8 / i9**
- Documentação da biblioteca nativa **E1_Impressora01.dll (Elgin)**

---

## 👥 Autores  

- Leandro Silva Santos
- Nicolas Gabriel Alves Ramalho
