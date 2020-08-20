# WSL - Windows Subsystem for Linux
<p align="center">
    <img src="../../assets/wsl2.jpeg" width=75%>
</p>

# Sobre

O WSL é um recurso para windows que permite executar inários e scripts em Linux diretamente no Windows, basicamete, seria rodar o linux dentro do windows, só que sem a interface gráfica.

Ele é uma boa alternativa pra quem não quer fazer dual boot com o linux ou que não quer ficar criando um ambiente separado com uma virtual machine, ou também pra poder algo que não conseguiu instalar no windows por exempro.

Atualmete ele está na sua segunda versão, que está sendo até que bem recebido em comparação à primeira versão.

# Preparação do ambiente

Para poder usar o WSL, você precisa abilitar a virtulização no seu pc, seja com o AMD-V ou com o Intel VR, que precisa ser feito pela bios.

### Intel VR
  
Para entrar na bios, vai depender de cada computador/placa mãe, mas após entrar na bios, você vai em `ADVANCED`, nessa aba vai ter a opção `Inter Virtualization Technology` é só colocar como `Enable` após isso, salvar e sair.

Exemplo:

<img src="../../assets/intel_exemple.jpg" width=75%>

### AMD-V

Para entrar na bios, vai depender de cada computador/placa mãe, mas após entrar na bios, você vai em `ADVANCED`, estando em `ADVANCED`, você vai na opção `CPU Configuration`, estando nela você vai ter a opção `SVM Mode` aí é só colocar como `Enable` após isso, salvar e sair.

Exemplo:

<img src="../../assets/amd_exemple.jpg" width=75%>

# Instalando o WSL

Primeiro, iremos abrir o powershell como administrador e executar o seguinte codigo:

`dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart`

Após isso, você irá reiniciar o pc e pronto o wsl está instalado. Mas agora a gente vai atualizar pro WSL 2. Então tendo reiniciado o computador, você vai ativar o recurso "Plataforma de Máquina Virtual".

Para isso você vai abrir o Recursos do Windows, você vai achar como "Ativar ou Desabilitar os recursos do windows" quando procurar usando a barra de pesquisa do windows. Bem, feito isso rodamos esse codigo no powershell como admin: 

`dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart`

E reiniciamos o computador novamete, após isso passamos o codigo:

`wsl --set-default-version 2`

Assim quando for instalar uma nova distribuição, ela já vai entender que vai ser usada a versão 2 e não a primeira.

# Instalando a distro Linux

Para a gente instalar um distro, a gente vai abrir a [Microsoft Store](https://aka.ms/wslstore) e vai pesquisar "linux", ou você pode entrar pelo link que já vai aparecer as versões disponiveis.

<img src="../../assets/win_stores.png" width=75%>

Você vai clicar no icone da distro da sua escolha e depois em instalar, sem muito segredo. Estando instalado, você vai executar e esperar um tempo, aí vai pedir pra você colocar um nome e a senha, feito isso, você já pode usar o terminal do linux normalmente.

<img src="../../assets/terminal.png" width=75%>

Caso você tenha instalado o wsl pra aprender linux ainda, na he4rt temos o [linux4noobs](https://github.com/lucashe4rt/linux4noobs) que vai te ajudar nessa jornada no mundo linux.