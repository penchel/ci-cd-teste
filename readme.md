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

## 🧠 4. Para finalizar

### Como o GitHub Actions ajuda a detectar erros cedo?  
💡 **Resposta:**  
O GitHub Actions executa automaticamente o pipeline de testes e verificação a cada *push* ou *pull request*.  
Isso permite identificar falhas logo após uma alteração no código, evitando que erros cheguem à versão principal do projeto e garantindo maior qualidade e estabilidade no desenvolvimento.

---

### Quais seriam exemplos reais de CI/CD em projetos web ou mobile?  
💡 **Resposta:**  
- **Projetos Web:** execução de testes automatizados e deploy automático para serviços como **Vercel**, **Netlify**, **AWS** ou **Heroku** após cada *push* na branch principal.  
- **Projetos Mobile:** geração automática de *builds* Android/iOS e envio para **Firebase App Distribution** ou **TestFlight** sempre que novas alterações são publicadas.

---

### Como o deploy automático poderia ser feito a partir deste pipeline?  
💡 **Resposta:**  
Bastaria adicionar uma etapa extra no workflow usando *actions* específicas para deploy, como:  
- `peaceiris/actions-gh-pages` → para publicar sites estáticos no GitHub Pages;  
- `appleboy/scp-action` → para enviar arquivos para um servidor remoto via SSH;  
- Integrações com **AWS**, **Vercel**, **Docker Hub** ou **Firebase Hosting**, permitindo que o código atualizado seja automaticamente implantado após passar pelos testes.
