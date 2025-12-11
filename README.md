# **OBS Studio Ultimate Controller (GC & Holyrics Bible)**

Este projeto é um conjunto de ferramentas web para controlar Lower Thirds (GCs) e exibir versículos da Bíblia (integrado ao Holyrics) diretamente no OBS Studio, tudo através de um Painel de Controle unificado.

## **🚀 Funcionalidades**

### **📺 Lower Thirds (GC)**

* **Controle Totaal:** Exibir, Ocultar e Limpar GCs.  
* **Personalização:** Altere nomes, títulos/cargos, logotipos e fontes individualmente.  
* **Temas Globais:** Defina cores, animações (Slide, Fade, Zoom, etc.) e tempos para todos os GCs de uma vez.  
* **Auto-Save:** Todas as configurações e textos são salvos automaticamente no navegador.

### **📖 Bíblia Holyrics Live**

* **Integração Automática:** Monitora o Holyrics e exibe o versículo na tela automaticamente assim que você clica no slide.  
* **Temas Exclusivos:** Personalize cores, fontes e temas (Gradientes, Sólido, Transparente) especificamente para a Bíblia.  
* **Filtro Inteligente:** Exibe apenas conteúdo bíblico, ocultando automaticamente músicas ou anúncios para não poluir a transmissão.  
* **Sem API Complexa:** Funciona lendo diretamente a saída de visualização local do Holyrics.

## **📦 Arquivos do Projeto**

1. obs\_control\_panel.html: O painel administrativo onde você controla tudo. Pode ser aberto no navegador ou como uma Doca Customizada no OBS.  
2. obs\_lower\_thirds\_source.html: O arquivo de design dos GCs. Adicione como "Navegador" no OBS.  
3. obs\_bible\_source.html: O arquivo de design da Bíblia. Adicione como "Navegador" no OBS.

## **🛠️ Instalação e Configuração**

### **Passo 1: Configurar o OBS Studio**

1. Baixe os arquivos para uma pasta no seu computador.  
2. No OBS, crie uma **Cena** para seus GCs (ou use a atual).  
3. Adicione uma nova fonte do tipo **Navegador (Browser Source)**:  
   * **Nome:** GC Source  
   * **Arquivo Local:** Marque a caixa e selecione o arquivo obs\_lower\_thirds\_source.html.  
   * **Largura/Altura:** 1920 x 1080 (ou a resolução da sua stream).  
   * **CSS Personalizado:** Limpe tudo (deixe vazio).  
4. Adicione outra fonte do tipo **Navegador**:  
   * **Nome:** Bible Source  
   * **Arquivo Local:** Marque a caixa e selecione o arquivo obs\_bible\_source.html.  
   * **Largura/Altura:** 1920 x 1080\.  
   * **CSS Personalizado:** Limpe tudo.

### **Passo 2: Configurar o Painel de Controle**

Opção A: Doca Customizada (Recomendado)  
Esta é a melhor opção pois evita bloqueios de segurança do navegador (CORS) ao conectar com o Holyrics.

1. No OBS, vá em **Ver (View) \-\> Docas (Docks) \-\> Docas de Navegador Personalizadas (Custom Browser Docks)**.  
2. **Nome da Doca:** Controlador Ultimate  
3. **URL:** Cole o caminho do arquivo no seu PC.  
   * *Dica:* Abra o arquivo obs\_control\_panel.html no Chrome, copie o endereço da barra (ex: file:///C:/Users/SeuNome/Downloads/obs\_control\_panel.html) e cole no OBS.  
4. Clique em **Aplicar**. A doca vai aparecer, você pode arrastá-la e fixá-la na interface do OBS.

**Opção B: Navegador Externo (Chrome/Edge)**

1. Abra o arquivo obs\_control\_panel.html no seu navegador.  
2. **Importante:** Para a integração com Holyrics funcionar via navegador externo, você pode precisar instalar uma extensão que permita CORS (Cross-Origin Resource Sharing) ou usar a opção A.

## **🔗 Conectando ao Holyrics**

1. No Holyrics, certifique-se que o servidor de visualização está ativo.  
2. No Painel de Controle (seção Bíblia), insira o endereço local do Holyrics.  
   * Geralmente é algo como: http://192.168.x.x:2020/view/text3  
3. Clique em **"SINCRONIZAR COM HOLYRICS"**.  
4. Se a "bolinha" ficar verde, está conectado\! Ao mudar um versículo no Holyrics, ele aparecerá no OBS.

## **🎨 Personalização**

* **Logos:** Você pode carregar imagens locais para os GCs.  
* **Fontes:** O sistema utiliza Google Fonts. As fontes são carregadas da internet, então o computador do OBS precisa estar online.  
* **Cores:** Use os seletores de cor no painel para criar temas personalizados.

*Desenvolvido para agilizar transmissões ao vivo de cultos e eventos.*