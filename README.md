## BEM VINDO AO SDK!! 

Primeiramente gostaria de dar as boas vindas ao time SDK da eletra energy solutions, nesse primeiro momento vamos gastar o tempo necessário
em projetos simples de integração para aumentar seu nível de conhecimentos básicos em C++ e P.O.O. . Abaixo temos 3 projetos para serem
desenvolvidos pelos membros récem chegados, esses projetos devem ser feitos em sequência e só podem ser começados após o anterior ter sido aprovado por um membro sênior do time. Bom trabalho mãos a obra!


## PROJETO N°1

O primeiro projeto tem o objetivo avaliar o nível de domínio com a linguagem C++, e as estratégias de resolução de problemas. 

### Objetivo Final

- Montar uma aplicação utilizando o Console para iteração com o usuário. Nesta aplicação o objetivo principal é mostrar as listas de equipamentos de medição que existem hoje na Eletra.
- Segue a lista de medidores definida na montagem deste manual, caso haja algum modelo novo deve ser incluído na lista:
    - **Zeus 8021** - **Zeus 8023** - **Zeus 8031**
    - **Apolo 6031**
    - **Cronos 6001-A** - **Cronos 6021-A** - **Cronos 6021L**
    - **Cronos 6003** - **Cronos 7023** - **Cronos 7023L** - **Cronos 7023 2,5**
    - **Ares 7021** - **Ares 7031** - **Ares 7023**
    - **Ares 8023** - **Ares 8023 15** - **Ares 8023 200**

    - Funcionalidades no Menu
        1) Exibir todas as linhas disponíveis
        2) Exibir todos modelos de Medidores de Energia
        3) Exibir todos os modelos da Linha Ares
        4) Exibir todos os modelos da Linha Apolo
        5) Exibir todos os modelos da Linha Cronos
        6) Exibir todos os modelos da Linha Zeus
        7) Sair da Aplicação

    - Requisitos
        1) Utilizar classes
        2) Organização dos arquivos (header/cpp)
        3) Utilizar compilador via Terminal do Visual Studio

        Abaixo segue o modelo de um projeto 1 realizado na última integração:

        ![alt text](https://raw.githubusercontent.com/RaulSouza27/Intregracao_ELETRA_SDK/master/imagens/Resultado%20Final%20projeto%201.jpg)

## PROJETO N°2

O objetivo deste projeto, além de otimizar tudo que foi feito no projeto anterior, é que o novo integrante conheça todas as tecnologias, alguns dos padrões de projetos que são utilizados no EletraSDK.

### Objetivo Final

- Esta aplicação tem a mesma ideia da anterior, mas conterá algumas novas funcionalidades. Essa aplicação deverá armazenar em uma única lista, todos os modelos de medidores existentes, como também os novos que serão adicionados, atrelando cada um deles ao ID. Cada Linha específica deverá ser implementada em classes diferentes, a partir de uma interface pré-definida pelo programador.

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

    - Requisistos
        1. Utilizar Interface para os medidores
        2. Utilizar o Padrão de Projeto Factory para a criação dos novos modelos.
        3. Utilizar alguma das estruturas de dados disponíveis (Lista, fila ou pilha)
        4. Utilizar CMake

        Abaixo segue o modelo de um projeto 2 realizado na última integração:

        ![alt text](https://raw.githubusercontent.com/RaulSouza27/Intregracao_ELETRA_SDK/master/imagens/Resultado%20Final%20projeto%202.jpg)


## PROJETO 03

Com esse projeto estaremos avançando mais um passo no conhecimento das tecnologias usadas no time SDK. Neste projeto, alem de aprofundar tudo que foi feito no projeto 2 iremos implementar o uso do gRPC e vcpkg. 

### Objetivo Final

Implementações importantes para o dia a dia dos membros do time do SDK. O objetivo do Projeto 3 é fazer um Servidor se comunicando com o BloomRPC e os métodos da aplicação serem exibidos lá. O servidor tem que disponibilizar os seguintes métodos:

- Funcionalidades do Menu

    1. Exibir as linhas disponíveis
    2. Exibir as linhas disponíveis na lista de medidores
    3. Exibir todos os medidores disponíveis na lista baseado na linha escolhida pelo usuário
    4. Exibir todos os modelos de medidores na lista
    5. Adiconar um novo medidor na lista de medidores
    6. Excluir um medidor baseado no seu ID
       
- Requisitos

    1. Criar arquivo .proto 
    2. Criar os arquivos services linkando o gRPC 
    3. Fazer testes apropriados em todos os métodos usados na aplicação
    4. Utilizar gRPC para fazer a exibição dos comandos

    Abaixo segue o modelo de um projeto 3 realizado na última integração:

    ![alt text](https://raw.githubusercontent.com/RaulSouza27/Intregracao_ELETRA_SDK/master/imagens/Resultado%20Final%20projeto%203%20-%20Server.jpg)


    ![alt text](https://raw.githubusercontent.com/RaulSouza27/Intregracao_ELETRA_SDK/master/imagens/Resultado%20Final%20projeto%203%20-%20gRPC.jpg)

