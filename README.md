## BEM VINDO AO SDK!! 

Primeiramente gostaria de dar as boas vindas ao time SDK da Eletra Energy Solution, nesse primeiro momento vamos gastar o tempo necessário
em projetos simples de integração para aumentar seu nível de conhecimentos básicos em C++, POO, CMake, Catch2, gRPC entre outras tecnologias. Abaixo temos 3 projetos para serem desenvolvidos pelos membros récem chegados, esses projetos devem ser feitos em sequência e só podem ser começados após o anterior ter sido aprovado por um membro sênior do time. Bom trabalho!


## PROJETO N° 1

Montagem do ambiente de programação C++. Para iniciar os projetos subsequentes os novos membros devem ser capazes de montar o ambiente de programação para ter o conhecimento de como essas ferramentas funcionam e o funcionamento básico dessas tecnologias. Dentro da pasta *files* desse repositório há um guia de quais softwares baixar e onde baixá-los.
- #### Requisitos:
    1. Instalar o CMake
    2. Instalar o Visual Studio 2019 (community)
    3. Visual Studio Code
    4. bloom gRPC
    5. Git
    6. Tortoise
    7. VCPKG
    8. COM0COM
    9. ComByTCP
- #### Entregas:
    Todos os softwares instalados e funcionando permitindo assim o uso do ambiente C++.    

## PROJETO N°2

Este projeto tem o objetivo de avaliar o nível de domínio com a linguagem C++, e as estratégias de resolução de problemas. O objetivo é montar uma aplicação utilizando o Console para iteração com o usuário. Nesta aplicação o objetivo principal é mostrar as listas de equipamentos de medição que existem hoje na Eletra.
- Segue a lista de medidores definida na montagem deste manual, caso haja algum modelo novo deve ser incluído na lista:
    - **Zeus 8021** - **Zeus 8023** - **Zeus 8031**
    - **Apolo 6031**
    - **Cronos 6001-A** - **Cronos 6021-A** - **Cronos 6021L**
    - **Cronos 6003** - **Cronos 7023** - **Cronos 7023L** - **Cronos 7023 2,5**
    - **Ares 7021** - **Ares 7031** - **Ares 7023**
    - **Ares 8023** - **Ares 8023 15** - **Ares 8023 200**

    - #### Requisitos:
      - Deve conter um menu no console com as seguintes funcionalidades
        1. Exibir todas as linhas disponíveis
        2. Exibir todos modelos de Medidores de Energia
        3. Exibir todos os modelos da Linha Ares
        4. Exibir todos os modelos da Linha Apolo
        5. Exibir todos os modelos da Linha Cronos
        6. Exibir todos os modelos da Linha Zeus
        7. Sair da Aplicação

    - #### Entregas:
        1. Utilizar classes
        1. Utilizar CMake
        2. Organização dos arquivos (header/cpp)
        3. Utilizar compilador via Terminal do Visual Studio
        4. Ultilizar a biblioteca Catch2 para testes

## PROJETO N°3

O objetivo deste projeto, além de otimizar tudo que foi feito no projeto anterior, é que o novo integrante conheça todas as tecnologias, alguns dos padrões de projetos que são utilizados no EletraSDK. Esta aplicação tem a mesma ideia da anterior, mas conterá algumas novas funcionalidades. Essa aplicação deverá armazenar em uma única lista, todos os modelos de medidores existentes, como também os novos que serão adicionados, atrelando cada um deles um ID único. Cada Linha específica deverá ser implementada em classes diferentes, a partir de uma interface pré-definida pelo programador:
- #### Requisitos 
    - Funcionalidades do Menu
        1. Exibir todas as linhas disponíveis
        2. Exibir todos modelos de Medidores de Energia
        3. Exibir todos os modelos da Linha Ares
        4. Exibir todos os modelos da Linha Apolo
        5. Exibir todos os modelos da Linha Cronos
        6. Exibir todos os modelos da Linha Zeus
        7. Adicionar um novo modelo a uma linha específica
        8. Remover o modelo informando o seu id
        9. Sair da Aplicação

- #### Entregas:
    1. Utilizar Interface para os medidores
    2. Não é permitido ID iguais
    3. Tratamento de exceções
    4. Utilizar alguma das estruturas de dados disponíveis (Lista, fila ou pilha)
    5. Utilizar o Padrão de Projeto Factory(no mínimo) para a criação dos novos modelos.
    6. Utilizar CMake
    7. Ultilizar a biblioteca Catch2 para testes
    8. Medir a cobertura de testes (O projeto só será aprovado com 100% de cobertura)

## PROJETO N°4

Com esse projeto estaremos avançando mais um passo no conhecimento das tecnologias usadas no time SDK. Neste projeto, alem de aprofundar tudo que foi feito nos projetos anteriores iremos implementar o uso do gRPC e vcpkg. Implementações importantes para o dia a dia dos membros do time do SDK. O objetivo do Projeto N°4 é fazer um Servidor se comunicando com o BloomRPC e os métodos da aplicação serem exibidos lá. O servidor tem que disponibilizar os seguintes métodos:

- #### Requisitos
  - Funcionalidades do Menu
    1. Exibir as linhas disponíveis
    2. Exibir as linhas disponíveis na lista de medidores
    3. Exibir todos os medidores disponíveis na lista baseado na linha escolhida pelo usuário
    4. Exibir todos os modelos de medidores na lista
    5. Adiconar um novo medidor na lista de medidores
    6. Excluir um medidor baseado no seu ID
       
- #### Entregas:
    1. Criar arquivos .proto 
    2. Criar os arquivos services linkando o gRPC 
    3. Fazer testes apropriados em todos os métodos usados na aplicação
    4. Utilizar gRPC para fazer a exibição dos comandos
    5. Utilizar o Bloom como interfaçe de exibição
    6. Medir a cobertura de testes (O projeto só será aprovado com 100% de cobertura)
    7. Implementar CI do Projeto

## PROJETO N°5

Este projeto sai do trabalho com listas de medidores e visa introduzir os novos membros a respeito dos protocolos de comunicação dos dispositivos usados na Eletra. 
Os protocolos usados nesse projeto serão DLMS, ABNT, HXD822 e MODBUS. Como desenvolvedor backend você terá que fazer uso desses protocolos constantemente e por tanto deve conhecer eles bem, e entender como a informação está contida ou deve ser enviada ao medidor por via de frames.

- #### Requisitos
  - Este projeto deve funcionar da seguinte maneira:
    1. Pelo bloom o usuário irá colocar um frame e a sua aplicação deve reconhecer se é um frame do tipo DLMS, ABNT, HXD822 e MODBUS.
    2. Uma lista de comandos dos protocolos será lhe fornecida e a aplicação deverá traduzir a informação contida no frame.
    3. Deve ser feita a verificação se o frame é valido, em algum formato de protocolos.
    
- #### Entregas
  1. Software funcional atendendo os requisitos.
  2. Demais entregas dos projetos anteriores. 


