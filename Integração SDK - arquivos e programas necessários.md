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
	Ao fazer a instalação instale o máximo de pacotes possível(de preferência todos com C++). É importante frizar que o que deve ser instalado é a versão da comunidade (visual studio community) pois as versões profissional e enterprise tbm irão funcionar mas durante o build elas informam cada arquivo que é criado tornando muito díficil encontrar os erros.
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

	Algumas coisas devem ser feitas no VS Code para poder usá-lo como ambiente de programação, tais como o arquivo de Debug e os settings do json para integrar o  compilador do visual studio 2019 com o VS Code
	- primeiro o arquivo de Debug
		Dentro da pasta do VScode crie um arquivo "launch.json" e nele cole o seguinte:
	```
	{
	// Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "name": "debug",
            "type": "cppvsdbg",
            "request": "launch",
            "program": "${workspaceFolder}/caminho até o executável",
            "args": [],
            "stopAtEntry": false,
            "cwd": "${workspaceFolder}/build/",
            "environment": [],
            "console": "integratedTerminal"
        }]}
	```
		Na linha onde tem program é necessário colocar o caminho até o executável gerado após a compilação
		Na linha que tem name é onde vc pode definir um nome pro Debug
		Na linha que tem args é onde devem ser passados os argumentos, se necessário, para funcionamento do do executável. (Como por exemplo a porta do servidor)

	- segundo o terminal de uso
		O terminal que deve ser usado é o do Visual studio, para compilação. Para tanto vá em settings->features->edit in settings json. Irá abrir um arquivo do tipo json, apague o que tiver nele e insira o texto abaixo:
	```
		{   
    "terminal.integrated.defaultProfile.windows": "Command Prompt",
    "terminal.integrated.profiles.windows": {
        "PowerShell": {
            "source": "PowerShell",
            "icon": "terminal-powershell"
        },
        "Command Prompt": {
            "path": [
                "${env:windir}\\Sysnative\\cmd.exe",
                "${env:windir}\\System32\\cmd.exe"
            ],
            "args": [
                "/k", "C:\\**Caminho até o arquivo VsDevCmd.bat que deve estar dentro da pasta do visual studio**\\VsDevCmd.bat"        
            ],
            "icon": "terminal-cmd"
        },
        "Git Bash": {
            "source": "Git Bash"
        }
    },
    "workbench.colorTheme": "Default Dark+",
    "workbench.iconTheme": "vscode-icons",
    "editor.unicodeHighlight.nonBasicASCII": false,
    "terminal.integrated.automationProfile.linux": {
    }
    "workbench.colorCustomizations" : 
    {
        "terminal.foreground" : "#ff6600",
        "terminal.background" : "#000000"
    }

}
```
	Na linha onde tem "workbench.colorCustomizations": é uma customização adicional, não é necesserária, serve para mudar a cor do fundo do terminal e a cor das letras.


5. **Bloom gRPC**
	Disponível em: https://github.com/bloomrpc/bloomrpc/releases
	Instalação padrão, nesse aplicativo que serão incluídos os arquivos .proto muito utilizados para identificar se os metódos estão em funcionamento.

7. **Tortoise**
	Disponível em: https://tortoisegit.org/download/
	Instalação padrão, aplicativo  responsável por fazer a clonagem das pastas e o commit dos  arquivos para salvar no GitHub.

8. **GitBash**
	Disponível em: https://git-scm.com/download/win


9. **VCPKG**
	Disponível em: https://github.com/microsoft/vcpkg 
	(Necessário já ter instalado o tortoise pois será por ele que faremos o clone da pasta)
	Após o clone e ter rodado o projeto do vcpkg é necessário instalar as variaveis de ambiente, são elas:
		-VCPKG_ROOT -> ${Diretório onde vcpkg foi clonado}

10. **COM0COM**
	Disponível em: https://sourceforge.net/projects/com0com/
	Instalação padrão, após instalar crie pelo menos 1 par de portas e depois reinicie o computador, para que o computador reconheça as portas.

11. **ComByTCP**
	Disponível em: https://sourceforge.net/projects/combytcp/
	Instalação padrão, aplicativo serve para fazer a conecção com os medidores.

12. **AnyDesk**
	Disponível em: https://anydesk.com/pt/downloads/windows
	Executável padrão serve tanto para comunicação com o time quanto para facilitar a passagem de arquivos.

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
