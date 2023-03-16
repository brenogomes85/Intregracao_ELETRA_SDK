# Preparação de ambiente de trabalho Eletra SDK

## Configuração inicial 

Nesse arquivo iremos indicar quais os principais softwares que serão necessários para trabalhar no time SDK:
Esses softwares são importantes para o trabalho em equipe e para a atividades desempenhadas no dia a dia.

Vamos lá:

## Ferramentas para uso de trabalho

1. **CMake**
	Disponível em: https://cmake.org/download/
	recomendado baixar o windows x64installer
2. **Sublime**
	Disponível em: https://www.sublimetext.com/3
	recomendado baixar o windows 64 bit
3. **Visual Studio 2019**
	Disponível em: https://visualstudio.microsoft.com/pt-br/vs/older-downloads/
	Ao fazer a instalação instale o máximo de pacotes possível(de preferência todos com C++)
4. **Visual Studio Code**
	Disponível em: https://code.visualstudio.com/download
	Após a instalação se faz necessário configurar todo o ambiente para a programação em C++. Para isso é necessário instalar algumas extensões pois o VS code é um editor de texto. As extensões a serem instaladas são as seguintes: 
	- 4.1. **C/C++** extensão da microsoft responsável por interpretar os códigos em C++;
	- 4.2. **C/C++ Extension Pack** extensão da microsoft.
	- 4.3. **C/C++ Themes** extensão da microsoft responsável pelos temas do visual studio na hora de desenvolver o código. Estes temas trazem organização e dinâmica ao código. 
	Para isso acesse o Text com o nome "Configuração VS Code"
    - 4.4. **CMake** Extensão muito importante
    - 4.5. **CMake Tools** 
    - 4.6. **vscode-icons** extensão com a função estética que mostra os ícones dos arquivos que estão sendo usados, ajuda muito na organização do que está sendo usado.
    - 4.7 **vscode-proto3** extensão que tarbalha com arquivos do tipo '.proto' que são essenciais no trabalho do dia a dia do SDK.

5. **Bloom gRPC**
	Disponível em: https://github.com/bloomrpc/bloomrpc/releases
	Instalação padrão, nesse aplicativo que serão incluídos os arquivos .proto muito utilizados para identificar se os metódos estão em funcionamento.

6. **VCPKG**
	Disponível em: https://github.com/microsoft/vcpkg 
	(Necessário já ter instalado o tortoise pois será por ele que faremos o clone da pasta)
	Após o clone e ter rodado o projeto do vcpkg é necessário instalar as variaveis de ambiente, são elas:
		-VCPKG_ROOT -> ${Diretório onde vcpkg foi clonado}

7. **SDK**
	

    Configurando:
    - Configurando o terminal do VS code:
	Setings (Ctrl+,) -> Features -> Terminal 
	no canto superior direito clique em "show source", irá aparecer um código do tipo json. Apague o que tiver lá e substitua pelo código no bloco de notas com o nome de "VS code Terminal"

	
O código acima tem o objetivo de alterar o terminal do VS code para que ele fique execuntando o compilador do Visual studio 2019, instalado na parte de ferramentas de trabalho.
	
O seguinte comando deve ser usado para aplicar caracteres especiais no compilador ->chcp 65001 & cmd

## Ferramentas de Equipe

1. **Discord**
	Disponível em: https://discord.com/download
	Acesse, faça seu login e depois adicione os membros do time.
2. **Trello**
    Algum membro sênior do time irá adicionar vc e explicar quais cartões devem ser preenchidos e como preeencher, para mais dúvidas 
3. **Glossário**
	Dentro do mundo da programação há uma infinidade de termos especificos para a programação, segue o link de um glossário englobando vários deles:
	https://blog.cubos.academy/dicionario-programacao-do-zero-entenda-os-termos-da-area-de-programacao/# 	

O presente arquivo tem o intuito de ensinar o passo a passo de configuração do software Visual Studio Code (VS code)
para servir como ambiente de programação para as aplicações de C++.

## ATIVIDADES
Todos os dias há os ***Dailys***, que tem o objetivo de compartilhar suas atividades para a equipe o que foi feito

Quinzenalmente as terças há as ***Sprints***, que são as atividades que tem que ser desempenhadas nesse periodo passadas pela equipe.

## Etapas da configuração do Ambiente de programação C++.

Após terem sidos instaladas as ferramentas de trabalho siga o passo a passo abaixo para fazer a preparção de todo o ambiente de trabalho e suas configurações para que seja possivél realizar o desenvolvimento em C++ dos programas e dos testes.

