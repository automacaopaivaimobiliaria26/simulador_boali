# Simulador Boali — versão revisada

Pacote estático para EasyPanel: index.html, Dockerfile e nginx.conf. Nginx atende em `/simuladorboali` pela porta interna 8080.

A exportação Excel (`.xls`, SpreadsheetML) possui aba Premissas editável. A projeção mensal, DRE anual e indicadores de VPL, TIR e MTIR usam fórmulas vinculadas às premissas para recálculo no Excel. A DRE anual mostra valor e percentual sobre a receita de cada ano, mais total do período e percentual sobre a receita total.

As premissas salvas na página ficam no localStorage do navegador e não são sincronizadas entre dispositivos. O modelo considera CAPEX e capital de giro desembolsados no mês zero; subtrai as parcelas sem lançar o principal financiado como entrada. A DRE não contempla depreciação, juros segregados ou IR/CSLL.
