## 🧠 Perguntas rápidas

### O que é CI/CD e por que é importante?  
💡 **Resposta:**  
CI/CD significa *Integração Contínua* (Continuous Integration) e *Entrega/Implantação Contínua* (Continuous Delivery/Deployment).  
A CI garante que o código seja constantemente integrado e testado a cada alteração, evitando falhas e conflitos.  
O CD automatiza o processo de entrega e deploy, tornando o desenvolvimento mais rápido, confiável e com menos erros.

---

### Em qual pasta os workflows do GitHub ficam armazenados?  
💡 **Resposta:**  
Os workflows do GitHub Actions ficam armazenados na pasta **`.github/workflows/`** dentro do repositório.

## 🧩 Etapa 3 – Verificando o pipeline

No GitHub:

- Vá em **Actions → Teste CI**  
- Veja o workflow em execução após o *push*

---

### O que aparece no log do GitHub Actions após a execução?  
💡 **Resposta:**  
O log mostra todas as etapas executadas do workflow, como o checkout do código, configuração do Python e execução do script.  
Na saída final, aparece o resultado do comando indicando que o script foi executado com sucesso.  
Isso confirma que o pipeline foi concluído corretamente e que o GitHub Actions rodou o programa automaticamente.

---

### O que acontece se alterar o código e fizer novo push?  
💡 **Resposta:**  
Sempre que você faz uma nova alteração e executa `git push`, o GitHub Actions detecta o novo *push* e executa novamente o workflow automaticamente.  
Assim, ele roda todas as etapas novamente — build, configuração do ambiente e execução dos testes — garantindo que o código atualizado continue funcionando corretamente.

