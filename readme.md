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


## 🧠 Perguntas rápidas

### O que é CD e qual sua relação com CI?  
💡 **Resposta:**  
CD significa *Continuous Delivery* (Entrega Contínua) ou *Continuous Deployment* (Implantação Contínua).  
Ele é o passo seguinte à *Integração Contínua (CI)*.  
Enquanto a CI garante que o código seja constantemente testado e integrado, o CD automatiza o processo de entrega e/ou publicação do software, permitindo que novas versões sejam disponibilizadas rapidamente e com segurança.

---

### Quais são os benefícios da entrega contínua?  
💡 **Resposta:**  
A entrega contínua traz maior agilidade e confiabilidade ao desenvolvimento, pois:  
- Reduz o tempo entre o desenvolvimento e a entrega ao usuário;  
- Diminui a chance de erros humanos no deploy;  
- Facilita a correção rápida de bugs e a entrega de novas funcionalidades;  
- Mantém o software sempre em um estado pronto para produção.



## 🧠 4. Para finalizar

### Qual é a principal diferença prática entre CI e CD?  
💡 **Resposta:**  
A *Integração Contínua (CI)* foca em integrar e testar o código automaticamente a cada modificação.  
Já a *Entrega Contínua (CD)* vai além, automatizando o processo de empacotar e disponibilizar o software para implantação.  
Em resumo: **CI garante que o código funciona**, enquanto **CD garante que ele possa ser entregue rapidamente**.

---

### O que aconteceria se o teste falhasse antes do deploy?  
💡 **Resposta:**  
O pipeline seria interrompido automaticamente, e o deploy não aconteceria.  
Isso evita que código com erros chegue à produção, protegendo a estabilidade do sistema e garantindo que apenas versões validadas sejam publicadas.

---

### Como a entrega contínua aumenta a confiança do time no processo?  
💡 **Resposta:**  
Porque todo o ciclo — integração, testes e deploy — é automatizado e reproduzível.  
O time passa a confiar que cada mudança será testada e implantada de forma consistente, reduzindo riscos, retrabalho e incertezas sobre o estado atual do software.
