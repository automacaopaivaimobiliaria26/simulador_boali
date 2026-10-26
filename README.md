# Simulador Boali — pacote de publicação

Pacote para publicar o simulador como um serviço separado no EasyPanel, sem substituir o site principal.

## Configuração no EasyPanel

1. Crie um serviço **App** e envie este pacote ZIP como fonte.
2. Selecione **Dockerfile** como método de build, usando o `Dockerfile` da raiz do pacote.
3. Faça o deploy e confirme que o serviço está ativo.
4. Em **Domains**, configure:
   - **Host:** `www.paivanegociosimobiliarios.com.br`
   - **Path:** `/simuladorboali`
   - **HTTPS:** ativado
   - **Protocolo interno:** HTTP
   - **Porta de destino:** `8080`
5. Salve e teste `https://www.paivanegociosimobiliarios.com.br/simuladorboali`.

O Nginx redireciona o caminho sem barra final para `/simuladorboali/` e serve o HTML somente nesse caminho. A rota `/` deste serviço retorna 404 para não interferir no site principal.

O simulador salva as premissas no armazenamento local do navegador. Os dados ficam separados por navegador/dispositivo e não são compartilhados entre visitantes.
