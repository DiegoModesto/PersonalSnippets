# Snippets and Tools

Este repositório contém Snippets e Ferramentas para uso do dia a dia para ambientes.



## Snippets :: Visual Studio Code


Seguindo a documentação [Visual Studio Code]("https://code.visualstudio.com/docs/editor/userdefinedsnippets")

### Windows

```path
  File -> Preferences 
```

ou

```path
  Ctrl + Shift + P
  [Digite] Snippets: Configure Snippets
  New global snippets file...
```

### MacOS

```path
  Code -> Preferences
```
ou
```path
  Code -> Settings
```

ou

```path
  Command + Shift + P
  [Digite] Snippets: Configure Snippets
  New global snippets file...
```

### Snippets personalizados

```path
  Copie o código 'Snippets/NetSuiteSnippets.json'
```

## Snippets :: Webstorm


Seguindo a documentação [Jetbrains Webstorm]("https://blog.jetbrains.com/webstorm/2018/01/using-and-creating-code-snippets/#work_with_live_templates")

Lembrando que dentro do Webstorms, os auxiliadores de código se chamam Live Template, e o mesmo foi exportado para pasta ZIP contida na pasta Snippets.

### Windows ou MacOS

```path
  File -> Manage IDE Settings -> Import Settings
  [Selecione o arquivo settgins.zip] 
```

## Tasks :: Visual Studio Code



Visual Studio Code trabalha com Tasks personalisáveis, que auxiliam nas tarefas.


### Instalação

```path
  Windows: CTRL + SHIFT + P
  MacOS: Command + SHIFT + P

  [Digite] Task: Configure Task
  [Selecione] Create tasks.json

  Copie e cole o conteúdo do arquivo Tasks/tasks.json

```

### Explicação
#### Typescript Compile Watch

Script para iniciar o comando TSC dinacimante com Watch ativo. Isso irá garantir que que toda alteração no código fonte seja imediatamente compilada para os arquivos de saída do seu ```outDir``` dentro do arquivo ```tsconfig```

#### Upload JavaScript to NetSuite

Esta task irá automaticamente subir um arquivo seguindo a estrutura de pastas.
Por exemplo, ao editar um arquivo no caminho:

```bash
src/FileCabinet/SuiteScripts/<Nome do Projeto>/_EntryPoints/<Nome do Arquivo>.js
```

O compilador irá utilizar o CLI do Netsuite para enviar o arquivo para o caminho:

```bash
suitecloud file:upload --path "/SuiteScripts/<Nome do Projeto>/_EntryPoints/<Nome do Arquivo>.js"
```

#### Upload TypeScript to NetSuite

Esta task irá automaticamente subir um arquivo seguindo a estrutura de pastas, porém, irá converter o caminho Typescript para o caminho do arquivo compilado.

Por exemplo:
```bash
src/Source/<Nome do Projeto>/_EntryPoints/<Nome do Arquivo>.ts
```

O compilador irá utilizar o CLI do Netsuite para enviar o arquivo para o caminho:

```bash
suitecloud file:upload --path "/SuiteScripts/<Nome do Projeto>/_EntryPoints/<Nome do Arquivo>.js"