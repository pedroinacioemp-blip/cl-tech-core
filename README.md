# 🖥️ CL TECH CORE - Hacker IDE

Uma aplicação desktop profissional com interface **hacker futurista** para compilar e executar códigos **C++** e **Java**.

## 🎯 Características

### ✨ Interface Hacker
- **Tema Dark + Neon Verde** com efeito matrix
- Estilo cyberpunk com animações fluidas
- Scanlines e glow neon em botões
- Interface responsiva e intuitiva

### 💻 Editor de Código
- Editor estilo VS Code integrado
- Detecção automática de linguagem
- Syntaxe com fonte monospace (Courier New)
- Suporte a copiar/colar código
- Abrir arquivos .cpp e .java

### ⚙️ Compilação & Execução

#### C++
```bash
g++ arquivo.cpp -o programa.exe
./programa.exe
```

#### Java
```bash
javac arquivo.java
java NomeDaClasse
```

### 🎮 Controles Principais

| Botão | Atalho | Função |
|-------|--------|--------|
| **▶ RUN** | `Ctrl+Enter` | Compila + Executa |
| **⚙ COMPILE** | `Ctrl+Shift+C` | Apenas Compila |
| **🧹 CLEAR** | `Ctrl+L` | Limpa Console |
| **📂 OPEN FILE** | `Ctrl+O` | Abre arquivo |

### 🔧 Console Hacker
- Terminal embutido com logs em tempo real
- Cores inteligentes:
  - 🟢 **Verde**: Sucesso/Output
  - 🔴 **Vermelho**: Erros
  - 🟡 **Amarelo**: Avisos
  - 🔵 **Ciano**: Informações
- Cursor piscando estilo terminal
- Auto-scroll automático

### 🧠 Auto-Run Inteligente
1. Compila automaticamente
2. Se sucesso → Executa
3. Se erro → Mostra erro no console

## 🚀 Instalação

### Pré-requisitos
- **Node.js** (v14+)
- **g++** (para C++)
  ```bash
  # Windows: instalar via MinGW ou MSVC
  choco install mingw  # Se usar Chocolatey
  ```
- **Java JDK** (para Java)
  ```bash
  # Windows: instalar JDK 11+
  choco install openjdk  # Se usar Chocolatey
  ```

### Passos de Instalação

1. **Clone ou descompacte o projeto**
   ```bash
   cd CL-TECH-CORE
   ```

2. **Instale as dependências**
   ```bash
   npm install
   ```

3. **Inicie a aplicação**
   ```bash
   npm start
   ```

## 📦 Estrutura do Projeto

```
CL-TECH-CORE/
├── main.js                 # Processo Principal Electron
├── preload.js             # API Segura (IPC)
├── package.json           # Dependências
├── renderer/
│   ├── index.html         # Interface HTML
│   ├── style.css          # Estilos (Dark+Neon)
│   ├── script.js          # Lógica Principal
│   └── matrix.js          # Efeito Matrix
├── assets/
│   ├── icon.ico           # Ícone da aplicação
│   └── icon.png           # Ícone alternativo
├── dist/                  # Build final
└── README.md             # Este arquivo
```

## 🛠️ Comandos Disponíveis

### Desenvolvimento
```bash
npm start        # Inicia a aplicação
npm run dev      # Mesmo que npm start
```

### Build & Empacotamento
```bash
npm run build           # Cria instalador .exe e .msi
npm run build-win       # Build apenas para Windows
```

## 🎨 Personalização

### Cores
Edite as variáveis CSS em `renderer/style.css`:

```css
:root {
  --color-green: #00ff00;      /* Cor principal */
  --color-red: #ff0033;        /* Cor de erro */
  --color-yellow: #ffff00;     /* Cor de aviso */
  --color-cyan: #00ffff;       /* Cor de info */
}
```

### Fontes
```css
--font-mono: 'Courier New', 'Lucida Console', monospace;
```

## 📋 Tutorial de Uso

### Exemplo: Compilar C++

1. **Abra a aplicação**
   ```bash
   npm start
   ```

2. **Clique em "OPEN FILE"** e selecione um `.cpp`
   - Ou cole código C++ no editor

3. **A linguagem é detectada automaticamente**
   - Badge mostra "C++"

4. **Clique "RUN"** ou pressione `Ctrl+Enter`
   - Compila automaticamente
   - Executa se compilado com sucesso
   - Mostra output no console

### Exemplo: Compilar Java

1. **Abra um arquivo `.java`** ou escreva código
   - Badge mostra "Java"

2. **Clique "COMPILE"** para apenas compilar
   - Ou **RUN** para compilar + executar

3. **Veja o resultado no console**

### Atalhos Rápidos
- `Ctrl+Enter` → Run (Compilar + Executar)
- `Ctrl+Shift+C` → Compile (Apenas compilar)
- `Ctrl+L` → Clear (Limpar console)
- `Ctrl+O` → Open (Abrir arquivo)

## 🐛 Troubleshooting

### g++ não encontrado
```
⚠ Faltando: g++
```
**Solução**: Instale MinGW ou adicione g++ ao PATH do Windows

### javac não encontrado
```
⚠ Faltando: javac
```
**Solução**: Instale JDK e configure a variável `JAVA_HOME`

### Arquivo não compila
- Verifique a sintaxe do código
- Use `Ctrl+L` para limpar o console
- Tente novamente

### Aplicação lenta
- Feche outros programas
- Reinicie a aplicação
- Verifique recursos do sistema

## 📥 Geração de Instalador

Para criar o `.exe` / `.msi`:

```bash
npm run build
```

Os instaladores ficarão em:
- `dist/CL TECH CORE.exe` (NSIS)
- `dist/CL TECH CORE.msi` (MSI)

## 🔒 Segurança

- Uso de **Context Isolation** (Electron)
- **Node Integration desabilitado**
- Comunicação IPC segura via preload.js
- Sem acesso direto ao Node.js da UI

## 📝 Licença

MIT - Livre para usar e modificar

## 👨‍💻 Autor

**CL TECH** - Inovação em Desenvolvimento

---

## 💡 Próximas Melhorias

- [ ] Highlight de sintaxe (Highlighter.js)
- [ ] Histórico de compilações
- [ ] Temas personalizáveis
- [ ] Suporte a mais linguagens
- [ ] Dark/Light mode toggle
- [ ] Integração com versioning

---

**Enjoy coding with style! 🚀💻**
