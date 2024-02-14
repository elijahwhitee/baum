
# Table of Contents

1.  [ProNo.2 | Okonomicus](#orgaeb28ce)
    1.  [Arquitetura](#org24397e7)
        1.  [Interface](#org8e2e1c8):visões:json:
        2.  [Banco de dados](#org422f522)
        3.  [Estrutura dos dados](#org6324683)
    2.  [Analise de negócios](#orgc449929)
        1.  [Concorrentes](#orga9ca03a)
    3.  [Funcionalidades](#org63e539c)
        1.  [Graficos e indíces contidos](#org60c118b)
    4.  [Plano de expansação](#org8fe3d21)
        1.  [Okonomicus para escolas e ensino](#org6c5c0ef)



<a id="orgaeb28ce"></a>

# ProNo.2 | Okonomicus

Análise fundamentalista com API rest e processamento de dados com Python.
A principal ideia é criar uma interface customizável para que o usuário consiga rastrear
os seus valores e dados específicos, tem que ser extensível e focada no power user, uma ferramenta
com potencial para fornecer os mesmos dados na mesma intensidade que um home broker.

O maio objetivo do projeto é se tornar um **verbo** na cultura de investimentos, uma
ferramenta tão atômica e coesa que é amplamente usada pela comunidade de investidores
brasileira.


<a id="org24397e7"></a>

## Arquitetura


<a id="org8e2e1c8"></a>

### Interface     :visões:json:

A interface é customizável, onde o usuário consegue salvar e criar visões, que são
essencialmente vários grafícos e dados que o usuário escolheu rastrear, essas visões
podem ser salvas em abas e em uma lista contendo todas as visões, a ideia é representar
essas visões em **json**.

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">Viz1</td>
</tr>
</tbody>
</table>

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">Viz1</td>
</tr>
</tbody>
</table>

1.  Endpoints

    1.  Live stock data
    
        Connect to stream of stock price data.
    
    2.  Seasonal data with low granularity
    
        The idea is to update every document based data
        about a company every hour.


<a id="org422f522"></a>

### Banco de dados


<a id="org6324683"></a>

### Estrutura dos dados

1.  DFPS

    As dfps são os documentos padronizadas entregues à CVM por parte das empresas
    listadas, o acesso à informação disponibilizada pelo portal de dados é possível
    graças ao incentivo da lei de acesso à informação.
    
    O formato é em CSV.

2.  Grupos das DFPS

3.  Users

4.  Views

    Aqui estruturarei uma forma rudimentar de como as view são expressas dentro do mongodb
    
        View:{
            id: string;
            name: string;
        
            user: {
            //user data
            }
        
            cards:{
                card1:{
                    assets: string;
                    assetid: string;
                    texts:{
        
                    }
                    graphs:{
        
                    }
                    modules?: {
                    //modular components containing extra info about the tracked asset
                    //examples: news module, investor mood module, popularity on the platform
        
                    }
                }
            }
        }


<a id="orgc449929"></a>

## Analise de negócios


<a id="orga9ca03a"></a>

### Concorrentes

Lista de serviços de investimento que visam prover um serviço parecido

1.  Status invest

    -   **Pros:** 1.  Bem estabelicida no mercado
        2.  Oferece muitas ferramentas.
        3.  Preço acessível.
    -   **Cons:** 1.

2.  Google finance

    -   **Pros:** 1.  Gratuito pra primeiro uso.
        2.  Interface simples e amigável.

3.  Fundamentei

    [Fundamentei](https://fundamentei.com/)

4.  Morningstar

    [Morningstar](https://www.morningstar.com/)

5.  The Motley fool

    [The Motley fool](https://www.fool.com/)

6.  Guru focus

    [GuruFocus](https://www.gurufocus.com/)


<a id="org63e539c"></a>

## Funcionalidades


<a id="org60c118b"></a>

### Graficos e indíces contidos

1.D.Y divident yield

1.  P/L
2.  P/EBTIDA
3.  P/VP
4.  P/EBIT
5.  P/SR
6.  P/ATIVO
7.  LPA
8.  P/SR
9.  P/CAP. GIRO
10. P/ATIVO CIRC. LIQ


<a id="org8fe3d21"></a>

## Plano de expansação


<a id="org6c5c0ef"></a>

### Okonomicus para escolas e ensino

Venda de acesso para empresas e escolas

Plano de ensino em etapas.

1- Etapa até crianças de 12 anos
2- Etapa adolescentes
3- Etapa jovens adultos

Atrelar o uso da ferramenta já consolidada ao ensino, tornando assim a plataforma também uma ferramenta de ensino.

1.  Planos empresarias e com parceria

