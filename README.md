# Simulador Boali — XLSX corrigido

A exportação gera um arquivo `.xlsx` Open XML válido, não um XML renomeado para `.xls`. A aba Premissas alimenta projeções mensais, DRE anual (valor e percentual por ano e total do período) e indicadores por fórmulas. O Excel recalcula as fórmulas ao abrir ou recalcular a pasta.

A aplicação continua estática; o Nginx atende `/simuladorboali` na porta interna 8080. As premissas da página são salvas no localStorage do navegador. O fluxo considera CAPEX e giro pagos no mês zero e abate parcelas sem entrada do principal financiado. A DRE não inclui depreciação, juros segregados ou IR/CSLL.
