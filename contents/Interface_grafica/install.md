

Para fazer a instalação, será necessário duas coisas:

- O windows 10 insider Preview build 21362+  [link](https://insider.windows.com/)

- Driver instalado para vGPU

  > "Para executar aplicativos de GUI do Linux, você deve primeiro instalar o driver de visualização correspondente ao sistema abaixo. Isso permitirá que você use uma vGPU (GPU virtual) para que você possa se beneficiar da renderização openGL acelerada por hardware."
  >
  > [fonte, e também acesso aos links pros driver](https://docs.microsoft.com/pt-br/windows/wsl/tutorials/gui-apps#prerequisites)

Após isso, temos duas situações, se você já ter o WSL instalado ou não.

### WSL nova instalação

Se você não instalou o wsl ainda, você pode fazer o seguinte:

1. Abrir um prompt de comando como administrador.
2. Executar o comando ```wsl --install -d DistroQueForUsar*``` e reinicie o computador quando for pedido
3. Após a reinicialização, a instalação continuará e será pedido colocar um usuário e uma senha pro Linux

> [* caso necessário leia essa parte](../Intro/wsl_first)

### WSL existente

Se você já ter o WSL, você só precisará abrir o prompt de comando como administrador

executar o comando `wsl --update`

e depois reiniciar o WSL com o comando `wsl --shutdown`

e tchadam! está pronto o WSL com GUI.

___

### versões anteriores a essa build.

Bem, temos dois casos se o seu windows ainda não suporta a interface por conta da versão

que é o caso do Kali Linux, em que temos o Win-Kex feita para ser uma forma de termos a interface gráfica no Kali Linux. você pode seguir por esse [link](./kali_wsl.md). E o caso do ubuntu em que é uma pura gambiarra, que você pode ver nesse [link](./ubuntu_wsl.md)

