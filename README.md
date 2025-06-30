CRM Banco de Leads - Documentação
Visão Geral
Plataforma web para análise, segmentação e gestão de leads consignados de bancos (inicialmente Banco Master), focada em importação de planilhas (.csv), KPIs, gráficos interativos, filtros dinâmicos e criação de regras personalizadas para tomada de decisão.
Todo processamento é local no navegador — não é necessário backend para uso básico.

Funcionalidades
Login seguro: acesso apenas com usuário e senha (admin / 123456, personalizável).

Página inicial com instruções rápidas (onboarding em cards).

Importação de múltiplas planilhas CSV.

Processamento e análise automática de leads: KPIs, segmentação, gráficos e exportação.

KPIs principais: total de leads, % com margem, % tomadores, negativados.

Gráficos:

Convênio/Produto (barras verticais)

Tipo de Saque

Faixa de Margem

Região (por DDD)

Filtros dinâmicos: convênio, produto, perfil, tipo de saque, faixa de margem, “Não Perturbe”, negativados.

Exportação CSV do segmento filtrado.

Cadastro manual de regras de priorização: por faixa de margem, região e perfil.

Sugestão automática de segmento ideal baseada nas regras e nos dados importados.

Visual moderno, responsivo e intuitivo (TailwindCSS + Chart.js).

Como Usar
1. Login
Acesse a página, preencha usuário e senha (admin / 123456) e clique em “Log in”.

2. Importação de Planilhas
Vá para a aba Resumo da Base.

Clique em “Importar Base Principal” e selecione um ou mais arquivos CSV com os leads.

Clique em “Iniciar Análise”.

3. Visualização de Dados
Veja KPIs e gráficos automaticamente.

Use a aba Segmentação para aplicar filtros e exportar leads segmentados.

4. Cadastro e Análise de Regras
Na aba Regras de Priorização, cadastre novas regras manuais por margem, região e perfil.

Veja a sugestão automática de melhor segmento do dia com base nessas regras.

Requisitos de Arquivo
Formato: .csv separado por vírgula, com cabeçalho.

Campos esperados:

cpf, nome, telefone, convenio, tipo_de_saque, limite_total, limite_disponivel, etc.

Os campos são normalizados automaticamente.

Tecnologias Utilizadas
Front-end: HTML5, TailwindCSS, FontAwesome

Gráficos: Chart.js + chartjs-plugin-datalabels

Leitura CSV: PapaParse.js

Armazenamento local: LocalStorage (para regras)

Sem backend obrigatório (pode evoluir para PHP/MySQL futuramente)

Segurança e Privacidade
Nenhum dado sai do seu computador — todo processamento é local.

Senhas podem ser personalizadas no código.

Não use dados sensíveis reais em ambiente de homologação.

Personalização e Evolução
Integre facilmente um backend em PHP/MySQL (Hostinger) para autenticação real ou armazenamento definitivo.

Permite adicionar novas colunas e KPIs (ex: inclusão de mailing, histórico de vendas etc).

Totalmente adaptável para mobile (só ajustar o CSS se quiser mais responsividade).

Fácil de internacionalizar (basta alterar textos nos cards e menus).

Dicas de Uso
Prefira arquivos CSV salvos como UTF-8.

Limite por arquivo: depende do navegador, mas até 100 mil linhas roda bem.

Faça backup de suas regras antes de limpar cache/localStorage.

Erros Comuns
O botão "Iniciar Análise" só habilita após importar arquivos.

Falta de algum campo obrigatório no CSV pode impedir o cálculo dos KPIs.

Erro de script? Veja o Console do navegador (F12) e confira se todos <script> externos carregaram.
