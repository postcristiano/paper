*Lang: pt-br*
# **Planejamento em Cartas Militares Digital**

### Considerações Iniciais:
- O tutorial tem o objetivo de difundir conhecimentos sobre planejamento tático para operações militares;
- A necessidade do tutorial foi identificada através da realização do Curso de Aperfeiçoamento de Oficiais na [Escola de Aperfeiçoamento de Oficiais](http://www.esao.eb.mil.br/) (EsAO) no ano de 2022. Existia uma demanda pela realização de estudos táticos de maneira digital e produção de produtos do estudo na forma de artefatos digitais (cartas militares de alta resolução, imagens vetorizadas, imagens rasterizadas, desenho de calcos de operações, etc);
- Para execução do planejamento tático em carta digital, foram adotados os softwares **QGIS** e **Inkscape**, ambos softwares de código aberto e de credibilidade alta na comunidade;
- Futuramente as idéias aqui contidas podem fomentar o desenvolvimento de uma solução integrada optimizada para atender os requisitos de uso do planejador tático militar.

> **QGIS**: É um sistema de aplicação para informações geográficas que suporta visualização, edição e análise geospacial de dados.  
  
> **Inkscape**: Editor de imagens vetorizadas.  

---

### **INSTRUÇÕES**

#### PASSO 1: Download e instalação dos softwares
[<img src="./pics/pcmd/pcmd1.png" width="400"/>]() 
##### **Inkscape - Instalação:**
- Windows:
    - Realize o [download](https://inkscape.org/release/1.1.2/windows/64-bit/) do binário e instale seguindo as instruções da interface gráfica. 
- MacOS:
    - Realize o [download](https://inkscape.org/gallery/item/31681/Inkscape-1.1.2.dmg) e arraste o instalador para a pasta de aplicativos.
- GNU/Linux (Debian/ Ubuntu):
    - Encontra-se nos repositórios e também na forma de pacote [Snap](https://snapcraft.io/inkscape) e [Appimage](https://inkscape.org/release/all/gnulinux/appimage/).
```bash
sudo apt update && sudo apt install inkscape -y
```
##### **QGIS - Instalação:**
- Windows:
    - Realize o [download](https://qgis.org/downloads/QGIS-OSGeo4W-3.22.4-1.msi) do binário e instale seguindo as instruções da interface gráfica. 
- MacOS:
    - Realize o [download](https://qgis.org/downloads/macos/qgis-macos-ltr.dmg) e arraste o instalador para a pasta de aplicativos.
- GNU/Linux (Debian/ Ubuntu):
```bash
sudo apt install gnupg software-properties-common -y
```
```bash
wget -qO - https://qgis.org/downloads/qgis-2021.gpg.key | sudo gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/qgis-archive.gpg --import
```
```bash
sudo chmod a+r /etc/apt/trusted.gpg.d/qgis-archive.gpg
```
```bash
sudo add-apt-repository "deb https://qgis.org/ubuntu $(lsb_release -c -s) main"
```
```bash
sudo apt update && sudo apt install qgis qgis-plugin-grass -y
```
> **Observações:** 
> - *Sempre dê preferência para a versão estável.*
> - *O QGIS encontra-se disponível para os Macbooks M1, arquitetura arm proprietária da Apple, apenas através da camada de compatibilidade e virtualização [Rosetta 2](https://support.apple.com/pt-br/HT211861). Sendo necessário instalar a mesma se for o caso.*
> - *No ubuntu 20.04 e posteriores, uma versão estável do QGIS encontra-se no repositório. Não é trata-se da ultima versão do software, porém é funcional e não possui bugs. Para obte-la, basta realizar a instalação a partir do gerenciador de pacotes nativo. Para*

---

#### PASSO 2: Configuração para obtenção de cartas online
- O BDGEx disponibiliza dezenas de camadas de cartas topográficas através de WMS/WMTS; 
- Através de uma conexão é possível consumir diversas cartas GIS topográficas, matriciais e vetorizadas em diferentes escalas.
- Para configurar o QGIS no seu computador e manipular suas cartas, vá no menu superior `camadas`, `adicionar camada`, `adicionar WMS/WMTS layer`, no menu lateral à esquerda selecione `WMS/WMTS`, clique em `novo` e insira os dados:

**Name:** | `EB BDGEx`
--------- | -----------
**URL:** | `http://bdgex.eb.mil.br/mapcache`

[<img src="./pics/pcmd/pcmd2b.gif" width="1024"/>]() 

---

#### PASSO 3: Salvar uma carta em formato de imagem
- Caso necessite uma imagem de sua carta para editar e/ou inserir em uma apresentação de slides, vá em `Projeto`, `Importar/Exportar`, `Exportar mapa para imagem`, atente para quantidade de dpi, a qualidade da carta e o tamanho do arquivo a ser criado estão diretamente relacionados a ela;
- Posteriormente, você também pode carregar a imagem que salvou no QGIS, para trabalhar apenas com ela. Isso pode ser especialmente útil em caso de não possuir uma conexão com a Internet e/ou cache do seu QGIS estiver vazio, como ocorre em novas instalações do software.

[<img src="./pics/pcmd/pcmd3.gif" width="1024"/>]() 

> **Observação:** *É possível utilizar suas credenciais do Geoportal do Exército para obter as cartas, porém isso não é impostivo.*

---

#### PASSO 4: Desenhar um Calco temático como camada no QGIS
- Caso você precise representar um calco temático, por exemplo movimento e manobra, e colocar sobre a carta topográfica, deverá

- Possuir um repositório de Calungas pode facilitar bota no video

colocar os calungas no inks

colocar no qgis

Calungas

---

#### PASSO 5: Salvar planejamento tático em andamento

Todo trabalho em andamento pode ser salvo a qualquer momento, será gerado um arquivo xxxx, que pode ser aberto posteriormente

---

#### PASSO 6: Desenhar um Calco como camada do Inkscape
- De posse de uma carta no formato de imagem podemos representar o planejamento de uma operação tática através de calcos temáticos;
- Abra o Inkscape, adicione a imagem da carta ao documento, crie outras camadas e faça as suas representações de planejamento;
- Com o recursos de camadas você pode desenhar calcos de movimento e manobra, sistema de comunicações de área, posição defensiva, dentre muitos outros;
- Por fim, selecione as camadas de interesse para exportar em um novo arquivo de imagem; 
- Você poderar criar uma nova imagem da carta apenas com as informações táde interesse.

[<img src="./pics/pcmd/pcmd6.gif" width="1024"/>]() 

---

### PASSO 7: Colagem de folhas de Calco (Adicional)
- Esta atividade é uma sugestão para alguma situação de contigência. A idéia é não fazer essa tarefa, já que o objetivo principal é confeccionar todos os artefatos de planejamento da operação de maneira digital, seja por camadas vetorizadas no QGIS ou por imagens simples vetorizadas.
- O procedimento pode ser realizado em qualquer editor de imagem vetorial, utilizamos o Inkscape por ser um software de livre de grande qualidade e de código aberto;
- Inicialmente capture fotos de boa qualidade de todas as folhas de calco a serem coladas, aplicativos de scanner para smartphone podem auxiliar nesta tarefa;
- Crie um número de camadas igual ao número de folhas de calcos, mova cada folha em ordem, para a respectiva camada;
- Aplique transparência nas camadas;
- Realize o alinhamento das "cruzetas" de latitude e longitude;
- Remova a transparência e exporte o calco colado.
- A partir de agora, se tiver interesse, com a imagem vetorizada você pode preparar ela para adicionar como uma nova camada do QGIS, sobre a carta do Teatro de Operações.

[<img src="./pics/pcmd/pcmd7.gif" width="1024"/>]() 

---

### **CONCLUSÃO:** Possibilidades e capacidades
- O QGIS possui inúmeros recursos interessantes, permite salvar os trabalhos em um repositório de rede local com versionamento. Esta funcão pode ser útil para determinadas organizações. Busque suporte com o chefe da Seção de Tecnologia da Informação para se orientar quanto a viabilidade de implementação;
- Integrações com servidores de mapas locais customizados como o [OpenMapTiles do projeto OpenStreetMaps](https://openmaptiles.org/), também são possíveis e podem aumentar substancialmente a capacidade de planejamento tático com a governança dos dados.
- Este tutorial é apenas uma introdução inicial, para aprofundar os conhecimentos, leia as documentações oficiais dos softwares.

Futuramente serão adicionados mais exemplos de caso de uso



### **REFERÊNCIAS**
- EB20-MF-10.102- Manual de Fundamentos Doutrina Militar Terrestre
- [Documentação QGIS](https://docs.qgis.org/3.16/pt_BR/docs/user_manual/)
- [Documentação Inkscape](https://inkscape.org/learn/tutorials/)

---

Author: *Cristiano Monteiro*  
2022 March 4 - version 0.1



