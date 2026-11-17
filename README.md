# Quiz da Turma 1002

Site de quiz baseado no documento "Quiz da Turma 1002 – A Inteligência Artificial como Guardiã da Floresta Amazônica".

## Como executar no computador

1. Instale o Node.js (versão 18 ou superior).
2. Extraia a pasta do projeto.
3. Abra o terminal dentro da pasta `quiz_turma_1002_site`.
4. Configure uma senha própria para o operador e inicie:

   **Windows PowerShell**
   ```powershell
   $env:QUIZ_ADMIN_PASSWORD="coloque-uma-senha-forte"
   node server.js
   ```

   **Linux/macOS**
   ```bash
   QUIZ_ADMIN_PASSWORD="coloque-uma-senha-forte" node server.js
   ```

5. Acesse `http://localhost:3000`.

Se não configurar a variável, a senha inicial será `troque-esta-senha`. Troque-a antes de publicar o site.

## Publicar para a turma acessar pela internet

Este projeto precisa ser hospedado em um serviço que execute Node.js e mantenha armazenamento persistente para o arquivo `data.json`. Configure a variável de ambiente `QUIZ_ADMIN_PASSWORD` na hospedagem. Se a hospedagem apagar arquivos locais ao reiniciar ou usar várias instâncias, adapte o armazenamento para um banco de dados persistente antes de usar oficialmente.

## Área do operador

Clique em **Área do operador**, informe a senha e consulte:
- acessos únicos por navegador;
- total de participações;
- média de acertos;
- nome, pontuação, avaliação e data de cada participação.

O botão **Resetar dados** apaga resultados e a contagem de acessos únicos.

## Privacidade e contagem de acessos

Um site comum não consegue ler o endereço MAC de celulares ou computadores visitantes. O sistema usa um identificador aleatório salvo em cookie próprio para contar navegadores distintos. Isso conta navegadores, não pessoas: alguém pode usar mais de um navegador/dispositivo, e várias pessoas podem compartilhar o mesmo aparelho. O identificador não revela o MAC nem identifica fisicamente o visitante.

As seis perguntas de conhecimento são corrigidas no servidor. A pergunta de avaliação é registrada separadamente e não entra na nota.
