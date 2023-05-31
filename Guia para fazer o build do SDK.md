# Guia para fazer o build do SDK

## Para fazer o primeiro build

Para fazer o build do projeto do SDK é necessário ter feito toda a configuração inicial que também está nesse repositório, somente depois podemos seguir com o próximo passo que é o build do SDK

Vamos lá:

## Integrção a organização da Eletra

1. Primeiramente devemos solicitar a autorização necessária a um membro da eletra para que você possa acessar ao repositório do SDK. Uma vez com o devido acesso faça um clone do repositorio do Eletra-SDK no Eletra-PeD-Software-Team. Recomendo que seja feita uma pasta Dev dentro do disco C:/ pois alguns compiladores tem certos problemas em localizar paths com espaços ou caracteres especiais. 

2. Feito isso dê um switch/checkout para a branch mais atual do SDK (no presente momento da escrita desse guia a branch era a eletraSDK_v0.58.0, mas basta se informar com alguem do time para saber a branch mais atual) logo após dê um submodule Update.

3. O próximo passo consiste em abrir a pasta do SDK no VS code, dentro da pasta crie a pasta build. Abra o arquivo README, nele há as instruções de build que devem ser seguidas bem como os presets e as tags de compilação.