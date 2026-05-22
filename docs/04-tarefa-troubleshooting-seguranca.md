# Etapa 4: Troubleshooting e Redes no VirtualBox

## 🎯 Objetivo
Solucionar travamentos comuns do VirtualBox ao lidar com sistemas legados e mitigar riscos de segurança através do isolamento de placas de rede virtuais.

---

## 📑 Roteiro de Execução

1.  **Troubleshooting de Integração (Se necessário):**
    *   Se o mouse travar ou sumir após a instalação, vá nas configurações da VM no VirtualBox, aba **Sistema** -> **Dispositivo de Apontamento** e mude de `Multi-touch Tablet` para `Mouse PS/2`.
2.  **Configuração de Rede Segura (Isolamento de Vulnerabilidades):**
    *   O Windows XP é vulnerável a ataques modernos de rede distribuída (como o exploit *EternalBlue* / *WannaCry*).
    *   Abra as configurações da VM no VirtualBox com ela desligada. Vá na aba **Rede**.
    *   No campo **Conectado a:** altere a opção padrão `NAT` para **Não Conectado** ou **Rede Interna (Internal Network)**.
    *   Isso garante que o sistema compartilhe arquivos com outras VMs do laboratório (se necessário), mas fique totalmente blindado e invisível contra varreduras e ataques vindos da Internet real.

---

## 📝 Entregáveis desta Etapa

### 📸 [EVIDÊNCIA]
*Insira uma captura de tela da aba "Rede" do painel de controle do VirtualBox da sua VM demonstrando a modificação e isolamento do adaptador de rede para o modo seguro.*
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/c89cdefd-8314-47bb-bb22-039b4513a718" />

### ❓ [QUESTÃO 4]
Se mantivéssemos o adaptador de rede da máquina virtual do Windows XP configurado no modo "Placa em modo Bridge (Bridged Adapter)" conectada à rede Wi-Fi/cabeada pública da instituição, quais seriam as consequências imediatas em termos de segurança cibernética para o laboratório e para a VM?

**Sua Resposta:**
> Em modo Bridge, a VM fica exposta diretamente na rede física com um IP próprio, gerando duas graves consequências: a máquina virtual seria invadida e infectada por malwares em poucos minutos, pois o Windows XP não recebe atualizações desde 2014 e possui brechas de rede críticas (como a EternalBlue) que são alvos fáceis de varreduras automáticas; e o laboratório correria risco de contaminação em massa, já que a VM infectada funcionaria como um "trampolim" para criminosos ou vírus atacarem os computadores reais dos outros alunos e os servidores da instituição que compartilham a mesma rede.

---
### 🏁 FIM DA ATIVIDADE
Com todas as seções preenchidas e imagens anexadas à pasta `/assets` do seu repositório local, execute os comandos do Git para registrar e subir sua atividade:

```bash
git add .
git commit -m "feat: conclusao do laboratorio de instalacao do winxp no virtualbox"
git push origin main
