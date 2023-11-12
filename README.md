# Intalando serviço http no ubunto
<h3>Atualizando o índice de pacote local</h3>
<pre> sudo apt update </pre>
<h3>Instalando o apache</h3>
<pre> sudo apt install apache2 </pre>
<h3>Versão do Apache</h3>
<pre> sudo apache2ctl -v </pre>
<h3>Apache → Este perfil apenas abra a porta 80 (tráfego da web normal não criptografado)</h3>
<pre> sudo ufw app list </pre>
<h3>Escolhendo o perfil apache</h3>
<pre> sudo ufw allow 'Apache'</pre>
<h3>Verificando se o serviço estar ativo</h3>
<pre> sudo systemctl status apache2 </pre>
<h3>Verificando o ip do serviço<h3>
<pre> hostname -I </pre>

# Instalando o fpt no ubunto
<h3>Instalando o daemon FTP</h3>
<pre> sudo apt-get install vsftpd </pre>
<h3>Startando o serviço</h3>
<pre> sudo service vsftpd start  </pre>
<h3>Configurando serviço<h3/>
<pre> nano /etc/vsftpd.conf </pre>
<h7> anonymous_enable=YES <br>
     local_enable=YES <br>
     write_enable=YES <br>
     anon_upload_enable=YES <br> </h7>
<h3>Criando úsuario</h3>
<pre> sudo adduser joaovitor73 </pre>
<h3>Criando usuário ftp</h3>
<pre> sudo usermod -aG ftp joaovitor73 </pre>
<h3>Restartando o serviço</h3>
<pre> sudo service vsftpd restart </pre>

## Enviando arquivo
### Movendo todos os arquivos
<pre> sudo mv * /var/www/html </pre>
### Removendo todos os arquivos
<pre> sudo rm -rf * </pre>
### Alterando as permissões de todos os arquivos
<pre> sudo chmod -R +rX /var/www/html </pre>
###  Restartando o serviço
<pre> sudo service apache2 restart </pre>
