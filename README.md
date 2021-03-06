# B3_daily_historical_data
Historical data on all securities traded on the [Brazilian stock exchange](http://www.b3.com.br/en_us/b3/). Daily data since 2015.

## Contents
This repository contains:
1. A dataset with historical daily data on all securities negotiated on the Brazilian stock exchange (B3) since 2015.
2. A notebook with the code used to generate this dataset

## Source of the data

This data is obtained directly from the Brazilian stock exchange, in [this link](http://www.bmfbovespa.com.br/pt_br/servicos/market-data/historico/mercado-a-vista/series-historicas/). More information about the original dataset (including documentation) can be found [here](http://www.bmfbovespa.com.br/pt_br/servicos/market-data/historico/mercado-a-vista/cotacoes-historicas/). 

The original dataset, however, is not in tidy format. I have processed this data to put it in tidy format.

## Variables

This dataset contains the following variables:

* **BDI**: A code used by B3 to classify the security type. Common stocks, for example, are coded "02". The full list of these codes can be found in the table at the end of this document (in portuguese). This table is itself a copy from the original dataset's documentation. 
* **security**: The security's name. E.g., "PETR4", for Petrobrás PN stock, or "VALE3", for Vale.
* **market type**: The type of market the security is registered in. For example, spot markets are coded "010". The full list of these codes can be found in the table at the end of this document (in portuguese). This table is itself a copy from the original dataset's documentation.
* **company**: The company's nme
* **specification**: A code that offers further description on security type. As usual, I present the table (in potuguese) at the end of this document, copying it from the original documentation.
* **currency**: The currency used to express open, close, high, low and average prices
* **open**: The price at which the security was negotiated when the trading session started
* **high**: The maximum price achieved by the security during the trading session
* **low**: The minimum price achieved by the security during the trading session
* **average**: The average price achieved by the security during the trading session
*  **close**: The price at which the security was negotiated when the trading session ended

At present, this dataset does not contain all variables in the original dataset from B3, only the ones I felt were most important. (If you would like me to add any variable that may be missing, please let me know and I'll incorporate it into future version of this dataset)

## Tables with codes used by B3 (Portuguese)

### BDI codes

02 LOTE PADRAO

05 SANCIONADAS PELOS REGULAMENTOS BMFBOVESPA

06 CONCORDATARIAS

07 RECUPERACAO EXTRAJUDICIAL

08 RECUPERAÇÃO JUDICIAL

09 RAET - REGIME DE ADMINISTRACAO ESPECIAL TEMPORARIA

10 DIREITOS E RECIBOS

11 INTERVENCAO

12 FUNDOS IMOBILIARIOS

14 CERT.INVEST/TIT.DIV.PUBLICA

18 OBRIGACÕES

22 BÔNUS (PRIVADOS)

26 APOLICES/BÔNUS/TITULOS PUBLICOS

32 EXERCICIO DE OPCOES DE COMPRA DE INDICES  

33 EXERCICIO DE OPCOES DE VENDA DE INDICES  

38 EXERCICIO DE OPCOES DE COMPRA

42 EXERCICIO DE OPCOES DE VENDA

46 LEILAO DE NAO COTADOS

48 LEILAO DE PRIVATIZACAO

49 LEILAO DO FUNDO RECUPERACAO ECONOMICA ESPIRITO SANTO

50 LEILAO

51 LEILAO FINOR

52 LEILAO FINAM

53 LEILAO FISET

54 LEILAO DE ACÕES EM MORA

56 VENDAS POR ALVARA JUDICIAL

58 OUTROS

60 PERMUTA POR ACÕES

61 META

62 MERCADO A TERMO

66 DEBENTURES COM DATA DE VENCIMENTO ATE 3 ANOS

68 DEBENTURES COM DATA DE VENCIMENTO MAIOR QUE 3 ANOS

70 FUTURO COM RETENCAO DE GANHOS

71 MERCADO DE FUTURO

74 OPCOES DE COMPRA DE INDICES

75 OPCOES DE VENDA DE INDICES

78 OPCOES DE COMPRA

82 OPCOES DE VENDA

83 BOVESPAFIX

84 SOMA FIX

90 TERMO VISTA REGISTRADO

96 MERCADO FRACIONARIO

99 TOTAL GERAL

### Market type codes

010 VISTA

012 EXERCÍCIO DE OPÇÕES DE COMPRA

013 EXERCÍCIO DE OPÇÕES DE VENDA

017 LEILÃO

020 FRACIONÁRIO

030 TERMO

050 FUTURO COM RETENÇÃO DE GANHO

060 FUTURO COM MOVIMENTAÇÃO CONTÍNUA

070 OPÇÕES DE COMPRA

080 OPÇÕES DE VENDA

### Specification codes

BDR BDR

BNS BÔNUS DE SUBSCRIÇÃO EM ACÕES MISCELÂNEA

BNS B/A BÔNUS DE SUBSCRIÇÃO EM ACÕES PREFERÊNCIA

BNS ORD BÔNUS DE SUBSCRIÇÃO EM ACÕES ORDINÁRIAS

BNS P/A BÔNUS DE SUBSCRIÇÃO EM ACÕES PREFERÊNCIA

BNS P/B BÔNUS DE SUBSCRIÇÃO EM ACÕES PREFERÊNCIA

BNS P/C BÔNUS DE SUBSCRIÇÃO EM ACÕES PREFERÊNCIA

BNS P/D BÔNUS DE SUBSCRIÇÃO EM ACÕES PREFERÊNCIA

BNS P/E BÔNUS DE SUBSCRIÇÃO EM ACÕES PREFERÊNCIA

BNS P/F BÔNUS DE SUBSCRIÇÃO EM ACÕES PREFERÊNCIA

BNS P/G BÔNUS DE SUBSCRIÇÃO EM ACÕES PREFERÊNCIA

BNS P/H BÔNUS DE SUBSCRIÇÃO EM ACÕES PREFERÊNCIA

BNS PRE BÔNUS DE SUBSCRIÇÃO EM ACÕES PREFERÊNCIA

CDA CERTIFICADO DE DEPÓSITO DE ACÕES ORDINÁRIAS

CI FUNDO DE INVESTIMENTO

CPA CERTIF. DE POTENCIAL ADIC. DE CONSTRUÇÃO

DIR DIREITOS DE SUBSCRIÇÃO MISCELÂNEA (BÔNUS)

DIR ORD DIREITOS DE SUBSCRIÇÃO EM ACÕES ORDINÁRIAS

DIR P/A DIREITOS DE SUBSCRIÇÃO EM ACÕES PREFERENCIAIS

DIR P/B DIREITOS DE SUBSCRIÇÃO EM ACÕES PREFERENCIAIS

DIR P/C DIREITOS DE SUBSCRIÇÃO EM ACÕES PREFERENCIAIS

DIR P/D DIREITOS DE SUBSCRIÇÃO EM ACÕES PREFERENCIAIS

DIR P/E DIREITOS DE SUBSCRIÇÃO EM ACÕES PREFERENCIAIS

DIR P/F DIREITOS DE SUBSCRIÇÃO EM ACÕES PREFERENCIAIS

DIR P/G DIREITOS DE SUBSCRIÇÃO EM ACÕES PREFERENCIAIS

DIR P/H DIREITOS DE SUBSCRIÇÃO EM ACÕES PREFERENCIAIS

DIR PR DIREITOS DE SUBSCRIÇÃO EM ACÕES RESGATÁVEIS

DIR PRA DIREITOS DE SUBSCRIÇÃO EM ACÕES RESGATÁVEIS

DIR PRB DIREITOS DE SUBSCRIÇÃO EM ACÕES RESGATÁVEIS

DIR PRC DIREITOS DE SUBSCRIÇÃO EM ACÕES RESGATÁVEIS

DIR PRE DIREITOS DE SUBSCRIÇÃO EM ACÕES PREFERENCIAIS

LFT LETRA FINANCEIRA DO TESOURO

M1 REC RECIBO DE SUBSCRIÇÃO DE MISCELÂNEAS

ON ACÕES ORDINÁRIAS NOMINATIVAS

ON P ACÕES ORDINÁRIAS NOMINATIVAS COM DIREITO

ON REC RECIBO DE SUBSCRIÇÃO EM ACÕES ORDINÁRIAS

OR ACÕES ORDINÁRIAS NOMINATIVAS RESGATÁVEIS

OR P ACÕES ORDINÁRIAS NOMINATIVAS RESGATÁVEIS

PCD POSIÇÃO CONSOLIDADA DA DIVIDA

PN ACÕES PREFERÊNCIAIS NOMINATIVAS

PN P ACÕES PREFERÊNCIAIS NOMINATIVAS COM DIREITO

PN REC RECIBO DE SUBSCRIÇÃO EM ACÕES PREFERENCIAIS

PNA ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE A

PNA P ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE A

PNA REC RECIBO DE SUBSCRIÇÃO EM ACÕES PREFERENCIAIS

PNB ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE B

PNB P ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE B

PNB REC RECIBO DE SUBSCRIÇÃO EM ACÕES PREFERENCIAIS

PNC ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE C

PNC P ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE C

PNC REC RECIBO DE SUBSCRIÇÃO EM ACÕES PREFERENCIAIS

PND ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE D

PND P ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE D

PND REC RECIBO DE SUBSCRIÇÃO EM ACÕES PREFERENCIAIS

PNE ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE E

PNE P ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE E

PNE REC RECIBO DE SUBSCRIÇÃO EM ACÕES PREFERENCIAIS

PNF ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE F

PNF P ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE F

PNF REC RECIBO DE SUBSCRIÇÃO EM ACÕES PREFERENCIAIS

PNG ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE G

PNG P ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE G

PNG REC RECIBO DE SUBSCRIÇÃO EM ACÕES PREFERENCIAIS

PNH ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE H

PNH P ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE H

PNH REC RECIBO DE SUBSCRIÇÃO EM ACÕES PREFERENCIAIS

PNR ACÕES PREFERÊNCIAIS NOMINATIVAS RESGATÁVEIS

PNV ACÕES PREFERÊNCIAS NOMINATIVAS COM DIREITO

PNV P ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE V

PNV REC RECIBO DE SUBSCRIÇÃO EM ACÕES PREFERENCIAIS

PR P ACÕES PREFERÊNCIAIS NOMINATIVAS RESGATÁVEIS

PRA ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE A

PRA P ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE "

PRA REC RECIBO DE SUBSCRIÇÃO EM ACÕES RESGATÁVEIS

PRB ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE B

PRB P ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE "

PRB REC DIREITOS DE SUBSCRIÇÃO EM ACÕES RESGATÁVEIS

PRB REC RECIBO DE SUBSCRIÇÃO EM ACÕES RESGATÁVEIS

PRC ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE C

PRC P ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE "

PRC REC RECIBO DE SUBSCRIÇÃO EM ACÕES RESGATÁVEIS

PRD ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE D

PRD P ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE "

PRE ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE E

PRE P ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE "

PRF ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE F

PRF P ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE "

PRG ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE G

PRG P ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE "

PRH ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE H

PRH P ACÕES PREFERÊNCIAIS NOMINATIVAS CLASSE "

PRV ACÕES PREFERÊNCIAIS NOMINATIVAS COM DIREITO

PRV P ACÕES PREFERÊNCIAIS NOMINATIVAS RESG. C/ DIREITO

R CESTA DE ACÕES NOMINATIVAS

REC RECIBO DE SUBSCRIÇÃO MISCELÂNEA

REC PR RECIBO DE SUBSCRIÇÃO EM PREF RESGATÁVEIS

RON CESTA DE ACÕES ORDINÁRIAS NOMINATIVAS

TPR TIT. PERPETUOS REMUN. VARIAV. ROYALTIES

UNT CERTIFICADO DE DEPÓSITO DE ACÕES - MISCELÂNEAS

UNT UNITS

UP PRECATÓRIO

WRT WARRANTS DE DEBÊNTURES
