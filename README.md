### 1. **História do Usuário**  

**Estimativa**: 1 hora  

 

**Justificativa**: Escrever uma história do usuário é uma tarefa relativamente rápida, embora história deva ser clara e concisa, refletindo a necessidade do usuário em gerenciar tarefas de forma eficiente.  

 

---  

### 2. **Critérios de Aceitação**  

**Estimativa**: 4 horas  

 

**Justificativa**: Criar critérios de aceitação requer um entendimento profundo das funcionalidades da aplicação. Devemos identificar as condições que devem ser atendidas para que uma funcionalidade seja considerada completa, e essa tarefa pode incluir revisões para garantir que os critérios estejam alinhados com a visão do produto.  

 

---  

### 3. **Casos de Teste**  

**Estimativa**: 4 horas  

 

**Justificativa**: Elaborar casos de teste envolve detalhar os diferentes cenários que devem ser testados para cada funcionalidade. Isso inclui não apenas os casos positivos, mas também os negativos e isso pode levar tempo para garantir a cobertura completa.  

 

--- 

### 3. **Teste exploratório**  

**Estimativa**: 2 horas  

 

**Justificativa**: Esse tempo permite uma análise abrangente e cuidadosa da aplicação, garantindo uma boa cobertura de testes. Também permite uma familiarização com a aplicação e a execução de diversos cenários. 

 

---  

### 5. **Testes Automatizados com Cypress, JavaScript e Cucumber**  

**Estimativa**: 12 horas  

 

**Justificativa**: A implementação de testes automatizados com Cypress, JavaScript e Cucumber envolve não apenas escrever os testes, mas também configurar o ambiente e garantir que todos os testes sejam executados corretamente. Isso inclui a criação de cenários de teste em Gherkin (Cucumber) e a codificação de testes em Cypress, além da necessidade de revisões e ajustes.   

 

--- 

**Gerenciamento de Tarefas em uma Aplicação To-Do**  

 

**Como** usuário que preciso organizar minhas atividades diárias    

**Quero** utilizar uma aplicação de gerenciamento de tarefas    

**Para** que eu possa adicionar, visualizar, editar e remover tarefas de forma prática e rápida.  

 

### **Critérios de Aceitação**:  

  

 

1. **Adicionar Tarefas**:  

 

   - O usuário pode inserir uma nova tarefa digitando no campo de texto e pressionando "Enter".  

   - A nova tarefa é exibida na lista de tarefas, e o campo de texto é limpo automaticamente.  

   

2. **Marcar Tarefas como Concluídas**:  

 

   - O usuário pode marcar uma tarefa como concluída clicando em uma caixa de seleção ao lado de cada tarefa.  

   - Quando marcada como concluída, a tarefa aparece com um texto riscado.  

   

3. **Visualizar Tarefas Pendentes e Concluídas**:  

 

   - O usuário pode visualizar todas as tarefas.  

   - O usuário pode filtrar a lista de tarefas para exibir apenas as pendentes, as concluídas ou todas.  

 

  4. **Editar Tarefas**:  

 

   - O usuário pode editar uma tarefa clicando duas vezes sobre o texto da tarefa.  

   - O campo de texto para edição aparece, e o usuário pode modificar o conteúdo da tarefa.  

   - Após a edição, o usuário pode pressionar "Enter" para salvar as alterações.  

   

5. **Excluir Tarefas**:  

 

   - O usuário pode excluir uma tarefa clicando no ícone de lixeira ou na área dedicada à exclusão ao lado da tarefa.  

   - A tarefa é removida permanentemente da lista.  

   

 

6. **Contador de Tarefas Pendentes**:  

 

   - O usuário pode ver o número de tarefas que ainda não foram concluídas em um contador localizado na parte inferior da aplicação.  

   

7. **Remover Tarefas Concluídas**:  

 

   - O usuário pode clicar em um botão para remover todas as tarefas que foram marcadas como concluídas.  

   

8. **Salvar Estado**:  

 

   - A aplicação deve manter as tarefas salvas mesmo após recarregar a página, utilizando armazenamento local (localStorage).  

  

---  

### **Definição de Pronto (DoD)**:  

  

- A interface do usuário está intuitiva e responsiva, permitindo que o usuário realize todas as ações de maneira fluida.  

- A funcionalidade de CRUD (Create, Read, Update, Delete) está funcionando conforme descrito.  

- Testes automatizados foram implementados para garantir a integridade das funcionalidades.  

- O estado das tarefas é salvo entre sessões, utilizando o armazenamento local.  

 

--- 

### **Cenários de Testes**:  

 

 

### **1. Adicionar Tarefas**  

 

**Cenário**: Adicionar uma nova tarefa  

 

- **Dado** que o usuário está na página inicial da aplicação,  

- **Quando** o usuário digitar uma nova tarefa no campo de entrada e pressionar "Enter",  

- **Então** a nova tarefa deve aparecer na lista de tarefas,  

- **E** o campo de entrada deve ser limpo.  

 

**Cenário**: Adicionar tarefa em branco  

 

- **Dado** que o usuário está na página inicial da aplicação,  

- **Quando** o usuário pressionar "Enter" sem digitar nada no campo de entrada,  

- **Então** nenhuma nova tarefa deve ser adicionada à lista.  

   

   

### **2. Marcar Tarefas como Concluídas**  

 

**Cenário**: Marcar uma tarefa como concluída  

 

- **Dado** que o usuário tem uma tarefa pendente na lista,  

- **Quando** o usuário clicar na caixa de seleção ao lado da tarefa,  

- **Então** a tarefa deve ser marcada como concluída,  

- **E** o texto da tarefa deve ser exibido com uma linha riscada.  

   

**Cenário**: Desmarcar uma tarefa concluída  

 

- **Dado** que o usuário tem uma tarefa marcada como concluída,  

- **Quando** o usuário clicar na caixa de seleção novamente,  

- **Então** a tarefa deve ser desmarcada,  

- **E** o texto riscado deve ser removido.  

   

   

### **3. Filtrar Tarefas**  

 

**Cenário**: Filtrar para visualizar tarefas pendentes  

 

- **Dado** que o usuário tem tarefas pendentes e concluídas na lista,  

- **Quando** o usuário clicar na opção "Ativas" para filtrar as tarefas,  

- **Então** apenas as tarefas pendentes devem ser exibidas.  

 

**Cenário**: Filtrar para visualizar tarefas concluídas  

 

- **Dado** que o usuário tem tarefas pendentes e concluídas na lista,  

- **Quando** o usuário clicar na opção "Concluídas" para filtrar as tarefas,  

- **Então** apenas as tarefas concluídas devem ser exibidas.  

   

**Cenário**: Exibir todas as tarefas  

 

- **Dado** que o usuário está filtrando as tarefas,  

- **Quando** o usuário clicar na opção "Todas",  

- **Então** todas as tarefas, tanto pendentes quanto concluídas, devem ser exibidas.  

 

   

### **4. Editar Tarefas**  

 

**Cenário**: Editar uma tarefa existente  

 

- **Dado** que o usuário tem uma tarefa na lista,  

- **Quando** o usuário clicar duas vezes no texto da tarefa,  

- **Então** o campo de entrada deve aparecer para edição,  

- **E** o usuário deve poder modificar o texto da tarefa.  

   

**Cenário**: Salvar a edição da tarefa  

 

- **Dado** que o usuário está editando uma tarefa,  

- **Quando** o usuário pressionar "Enter" após fazer alterações,  

- **Então** a tarefa deve ser atualizada com o novo texto,  

- **E** o campo de entrada deve ser ocultado.  

 

**Cenário**: Cancelar edição de uma tarefa  

 

- **Dado** que o usuário está editando uma tarefa,  

- **Quando** o usuário pressionar "Esc",  

- **Então** a edição deve ser cancelada,  

- **E** o texto original da tarefa deve ser mantido.  

   

   

### **5. Excluir Tarefas**  

 

**Cenário**: Excluir uma tarefa  

 

- **Dado** que o usuário tem uma tarefa na lista,  

- **Quando** o usuário clicar no ícone de lixeira ao lado da tarefa,  

- **Então** a tarefa deve ser removida permanentemente da lista.  

 

   

### **6. Remover Tarefas Concluídas**  

 

**Cenário**: Remover todas as tarefas concluídas  

- **Dado** que o usuário tem tarefas concluídas na lista,  

- **Quando** o usuário clicar no botão "Limpar Concluídas",  

- **Então** todas as tarefas marcadas como concluídas devem ser removidas.  

   

 

### **7. Contador de Tarefas Pendentes**  

 

**Cenário**: Ver o número de tarefas pendentes  

 

- **Dado** que o usuário tem uma lista de tarefas,  

- **Quando** o usuário visualiza a lista,  

- **Então** o contador de tarefas pendentes deve mostrar o número correto de tarefas não concluídas.  

 

   

### **8. Persistência de Dados**  

 

**Cenário**: Verificar a persistência de tarefas após recarregar a página  

 

- **Dado** que o usuário adicionou várias tarefas e algumas foram marcadas como concluídas,  

- **Quando** o usuário recarregar a página,  

- **Então** todas as tarefas devem ser exibidas como estavam antes do recarregamento. 

 