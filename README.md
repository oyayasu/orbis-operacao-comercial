# Orbis — Operação Comercial

Simulador **fictício e offline** de telemarketing ativo, com campanhas de vendas para pessoa física (PF) e pessoa jurídica (PJ).

## Entrar
- Informe qualquer nome de exibição: ele aparece no painel, e pode ser alterado em **Meu perfil**.
- A matrícula fictícia inicial é **OP-1042**.
- Senha demonstrativa: **123456** (não é autenticação real).

## Funcionalidades da versão 0.1
- Discador simulado e campanhas PF/PJ;
- Estados do operador, chamadas, pausas e resultados;
- CRM: mailing, histórico, notas e bloqueio de contato;
- Portal comercial: produtos fictícios, descontos e propostas;
- Relatórios CSV, backup JSON e persistência local.

Nenhum número é discado de verdade. Não use cadastros reais ou dados sensíveis. O simulador usa `localStorage`.

## Testar sem instalar
Abra [demo.html](demo.html) em um navegador atualizado. Tudo funciona localmente.

## Executar o projeto
Instale Node.js 22+ e, no diretório do repositório, execute:

```bash
npm install
npm run dev
```

## Compilar para Windows 10
O workflow em **Actions → Build Windows** tenta compilar um instalador Tauri 2/NSIS em Windows. Também é executado após push na branch `main`.

Quando a execução terminar com sucesso, abra o workflow e baixe o artefato **Orbis-Windows-Installer**, contendo o arquivo de instalação `.exe`.

A compilação exige dependências Rust, MSVC e WebView2 no ambiente de build, preparadas pelo runner Windows do GitHub Actions. O aplicativo ainda **não** foi validado em todas as versões do Windows 10.

## Escopo
A versão atual não possui telefonia SIP/VoIP real, transcrição de voz nem cliente com IA. Dados, produtos e históricos são fictícios.
