# Orbis — Operação Comercial v0.2.0

Aplicativo desktop de treinamento em vendas ativas (PF e PJ). Funciona localmente, sem telefonia externa, sem clientes reais e sem serviços pagos.

## Entrar

Informe seu nome, matrícula `OP-1042` e senha inicial `123456`. Esta é uma senha local de demonstração, **não um mecanismo de segurança**. O nome pode ser atualizado em Meu perfil.

## Novos recursos

- Discador progressivo de treinamento: seleção, discagem, resposta, conversa representada por texto, resultado e pós-atendimento (TPA), com distribuição contínua enquanto o operador estiver disponível.
- Mailing inicial com 72 contatos; recebe **18 a 32 novos registros por dia útil** nas configurações padrão. Configurável de 1 a 200; dias sem abrir são repostos no máximo por 5 dias úteis. Não faz trabalho em segundo plano com o app fechado.
- CRM de clientes PF/PJ com código de cliente, telefone parcialmente oculto, CPF/CNPJ ocultos, região, histórico, responsável, origem, interesse, registros de negócio e anotações.
- Metas, descontos, preços dos produtos, probabilidade de atendimento, intervalo entre chamadas e tempo de TPA personalizáveis.
- Relógio em tempo real, tempo conectado, cronômetro de ligação e pausas.
- Propostas, aprovações, cancelamentos, relatórios CSV e backup JSON.

## Origem dos dados

Banco de perfis gerado offline com [Python Faker](https://faker.readthedocs.io/en/master/locales/pt_BR.html), localização brasileira. O banco é distribuído em `data/profiles.json`; nenhum cadastro é obtido de pessoas reais. CPF/CNPJ e telefones são deliberadamente mascarados, e e-mails usam o domínio `example.com`, reservado para exemplos.

## Executar

Para usar sem instalar, abra `demo.html` em um navegador atualizado. Para desenvolvimento, Node.js 22+ e Rust com toolchain do Tauri 2:

```bash
npm install
npm run dev
```

## Windows 10

No GitHub: **Actions → Build Windows → Run workflow**. Se a execução concluir com sucesso, baixe o artefato `Orbis-Windows-Installer` (NSIS `.exe`). O workflow também dispara automaticamente após alterações na branch main.

## Limitações

- O discador **simula** tentativas e atendimentos em software; não disca números reais, não faz áudio SIP/VoIP e não conversa com IA.
- As taxas de atendimento e os tempos são ajustáveis e não se propõem a representar médias oficiais de mercado.
- Os clientes e empresas são gerados para testes. Dados ficam em localStorage; faça backup antes de limpar o navegador, reinstalar ou mudar o perfil do Windows.
- Build/testes manuais em Windows dependem da execução do GitHub Actions e de validação posterior no computador.
