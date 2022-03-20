# gitconfigssh
Passo a passo de configuração da chave ssh no git.

1) Gere suas chaves SSH (Pública e Privada) com o seguinte comando no terminal:
> ssh-keygen -t ed25519 -C seuemail@email.com

2) Escolha o caminho para salvar as chaves ou use o diretório padrão.

3) Defina uma senha para a sua chave.

4) Vá até o diretório onde suas chaves foram salvas e use o comando 'cat' para visualizar o arquivo 'id_ed25519.pub':
> cat id_ed25519.pub

5) Copie o conteúdo da chave e adicione ao github.

6) Ative o processo de validação do ssh:
> eval $(ssh-agent -s)

7) Adicione sua chave privada na validação:
> ssh-add id_ed25519

8) Faça o git-clone através da URL ssh.

9) Pronto, seu dispositivo será reconhecido pelo github e já poderá fazer seus envios normalmente.
