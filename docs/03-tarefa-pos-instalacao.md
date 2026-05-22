# Etapa 3: Pós-Instalação e Integração com o VirtualBox

## 🎯 Objetivo
Instalar os drivers de virtualização do pacote Guest Additions do VirtualBox para habilitar aceleração de vídeo, redimensionamento de tela automática e integração nativa do mouse.

---

## 📑 Roteiro de Execução

1.  **Instalação dos Adicionais de Convidado (VirtualBox Guest Additions):**
    *   Com a máquina virtual do Windows XP ligada e logada na área de trabalho, vá até o menu superior da janela do VirtualBox e clique em **Dispositivos** -> **Inserir Imagem de CD dos Adicionais de Convidado...**.
    *   Se a execução automática não abrir, clique no Menu Iniciar do Windows XP, abra o **Meu Computador** e dê dois cliques no drive de `CD-ROM (D:) VirtualBox Guest Additions`.
    *   O assistente de instalação será iniciado. Clique em **Next** em todas as etapas.
    *   Durante a instalação, o Windows XP exibirá janelas de aviso informando que o software que está sendo instalado "Não passou no teste de logotipo do Windows" (falta de assinatura digital retrô). Clique em **Continuar assim mesmo** em todas as notificações que surgirem.
    *   Certifique-se de que a opção de instalar suporte experimental a Direct3D/Aceleração Gráfica seja marcada se for solicitada.
    *   Ao concluir, selecione a opção `Reboot Now` e clique em **Finish** para reiniciar a VM.

2.  **Otimização Gráfica e de Desempenho:**
    *   Após o reinício, verifique se a tela da VM pode ser redimensionada livremente ou se o mouse se desloca para fora da tela da VM sem travar.
    *   Vá em `Painel de Controle` -> `Vídeo` -> `Configurações` e ajuste a resolução para pelo menos `1024x768` com qualidade de cor em `Máxima (32 bits)`.
    *   Clique com o botão direito em `Meu Computador` -> `Propriedades` -> aba `Avançado` -> Seção Desempenho clique em `Configurações` -> Escolha **Ajustar para obter um melhor desempenho** para otimizar o consumo de ciclos de CPU do sistema hospedeiro.

---

## 📝 Entregáveis desta Etapa

### 📸 [EVIDÊNCIA]
*Insira aqui uma captura de tela do Windows XP em "Modo Janela Redimensionada" ou em "Tela Cheia" dentro do VirtualBox, demonstrando que os drivers de vídeo e integração do mouse estão ativos de forma fluida.*
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/0ee8b1b6-71bd-41fb-9080-f02ad635a47a" />

### ❓ [QUESTÃO 3]
Quais recursos técnicos específicos passam a funcionar entre o sistema operacional real (hospedeiro) e a máquina virtual do Windows XP (convidado) após a instalação correta dos "Adicionais de Convidado" (Guest Additions)?

**Sua Resposta:**
> Integração do Mouse: O cursor se move livremente entre a máquina virtual e o seu computador real, sem ficar "preso" dentro da janela.

Tela Automática: A resolução do Windows XP se ajusta sozinha quando você estica ou maximiza a janela do VirtualBox.

Copiar e Colar (Ctrl+C / Ctrl+V): Permite copiar textos e arquivos do seu computador e colar direto dentro do Windows XP (e vice-versa).

Arrastar e Soltar: Você pode puxar arquivos com o mouse do seu computador e soltá-los dentro da máquina virtual.

Pastas Compartilhadas: Cria uma pasta comum entre os dois sistemas para trocar arquivos facilmente.

Aceleração de Vídeo: Melhora o desempenho visual e ativa o suporte a jogos e programas antigos em 3D.

Relógio Sincronizado: O horário do Windows XP fica sempre igual ao do seu computador real.

---
[⬅️ Voltar para a Etapa 2](02-tarefa-instalacao.md) | [Ir para a Etapa 4 ➡️](04-tarefa-troubleshooting-seguranca.md)
