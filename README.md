# Cronograma PRF + PMPE Offline

Aplicativo PWA estático para celular, preservando o visual clássico. Contém: cronograma PRF + PMPE de 15 horas efetivas por semana, prioridades da PRF, registros de questões e erros separados para cada concurso, gráficos semanais, backup JSON e menu de três pontinhos.

## Plano semanal
- Segunda: Português (base comum) — 1h30.
- Terça: História de Pernambuco (PMPE) — 1h45.
- Quarta: Raciocínio Lógico (base comum) — 1h45.
- Quinta: Direito Administrativo / Administração (PRF; uma matéria por sessão) — 1h45.
- Sexta: Direito Constitucional (base comum) — 1h45.
- Sábado: Informática + Direitos Humanos/Legislação PMPE — 3h15.
- Domingo: Redação PMPE + Legislação PRF / Ética / Arquivologia (uma matéria por sessão) — 3h15.

Nas quintas e domingos, a escolha da matéria fica com o estudante, sem rodízio automático. O bloco de 40 minutos de questões corresponde sempre à matéria estudada naquela sessão. As pausas são adicionais aos tempos indicados. A distribuição é uma organização de estudo, não uma garantia de conclusão de todos os tópicos dos editais.

## Publicação no GitHub + Vercel
1. Extraia o ZIP.
2. Envie **todos os 7 arquivos**, incluindo `index.html`, `app.js`, `sw.js`, `manifest.webmanifest` e ícones, à **raiz** de um repositório GitHub.
3. No Vercel, importe esse repositório. Framework **Other**, sem build command, output directory padrão/raiz.
4. Abra o domínio HTTPS da Vercel no Chrome do celular. Após carregar pela primeira vez, tente abrir com a internet desligada. Para instalar, utilize o menu do navegador → **Adicionar à tela inicial** ou **Instalar app**.

## Armazenamento e backup
O histórico de questões fica em **localStorage**:
- PRF: chave antiga `prf-questoes-v1`, preservada.
- PMPE: chave independente `pmpe-questoes-v1`.

Resultados de Português e das outras matérias comuns registrados na PRF não aparecem automaticamente na PMPE (e vice-versa). Redação PMPE não é contada como questão objetiva. Não há conta, sincronização com GitHub/Vercel ou armazenamento no servidor. Faça backups pelo menu **Backup dos dados** antes de limpar o navegador, trocar de aparelho ou domínio.

## Atualização
Esta revisão mantém o histórico da PRF no mesmo domínio e navegador. O backup novo, versão 2, inclui registros de PRF e PMPE. Backups antigos, versão 1, ainda podem ser importados: atualizam apenas a PRF e preservam os registros PMPE atuais. A primeira atualização deve ser aberta com internet, para renovar o cache offline.

## Observações
Prioridades da PRF baseadas no edital de 2014; não representam edital novo. Para a PMPE, o plano usa o edital de Soldado publicado em 2026. Páginas da apostila vêm das referências do planejamento anterior. O funcionamento em Android precisa ser testado no aparelho após publicar.
