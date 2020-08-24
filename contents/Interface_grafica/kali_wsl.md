# Kali Linux
<p align="center">
    <img src="../../assets/kali_wslfetch.png" width=50%>
</p>

Antes de começar, o Kali Linux no WSL 2 __NÃO__ inclui as
ferramentas para pentest, hacking, etc.

Primeiro vamos rodar o seguinte codigo:
`sudo apt update && sudo apt -y update` para termos tudo atualizado no linux.

Bem feito isso, iremos instalar a inteface **xfce** por ser mais leve e não pesar muito para o seu computador. Para isso, vamos usar o comando:

`sudo apt install xfce4`

Quando estiver instalado, aparecerá a seguinte tela no terminal. Nela, vá para ultima opção("anothers") e aparecerá outros idiomas. Depois, selecione o idioma e o tipo do teclado.

<p align="center">
    <img src="../../assets/install_kali.png"  width=85%>
</p>

Como o xfce instalado, vamos instalar o xrdp:

`sudo apt install xrdp`

O xrdp é o que vai permitir a gente ter a interface. Já que o que ele
faz é permitir que você use o "computador linux" com o acesso remoto.

Então, após instalar, inicie o xrdp com o comando:
`sudo /etc/init.d/xrdp start`.
Em seguida vamos veremos qual o ip do Kali para poder executá-lo com o comando:
`ip add`. No local onde está marcado, é onde estará o seu ip.

<p align="center">
    <img src="../../assets/kali_ip.png" width=85%>
</p>

Feito isso, procure por "acesso remoto" na barra de pesquisa do Windows. Nele, insira o ip do seu Kali e com isso acessar. Ao acessar, aparecerá um tela que pedirá para você inserir o usuário e senha do seu Kali. Pronto, agora temos um interface grafica para o Kali no WSL!

<p align="center">
    <img src="../../assets/kali_desk_xrdp.png" width=85%>
</p>