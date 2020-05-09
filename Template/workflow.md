<img src="https://i.ibb.co/DtHQ3FG/802x265-Logo-GT.png" width="500">

## Grupo Turing
# Workflow para subir material

0) Se sua pasta estiver desatualizada em relação ao GitHub, faça:
**git pull**

1) Navegar até a pasta certa, criando as pastas necessárias para igualar ao caminho da árvore

2) Incluir os arquivos correspondentes na pasta

3) Mudar para uma nova branch, já que não é possível fazer um commit pela master: **git checkout -b "(nome da branch)"**

    - Padrão de nome de branch:
        - "add/[nome do arquivo/pasta]" para adicionar
        - "fix/[nome do arquivo/pasta]" para arrumar
        - "del/[nome do arquivo/pasta]" para apagar

4) Adicionar arquivo: **git add (nome/caminho do arquivo)** 

5) Fazer o commit: **git commit -m "(Mensagem em portugues)"**
    
    - Para a mensagem de commit, informar o que for criado/alterado, em letras maiúsculas
    - Padrão: "ESTE COMMIT ADICIONA/ALTERA ..."


6) Mandar para o github: **git push origin HEAD**

7) No GitHub, vá em "pull requests", crie um novo pull request com a sua branch e adicione uma descrição das suas adições/alterações

    - Neste texto, seja mais descritivo do que a mensagem do commit

8) Crie seu "pull request" e espere a aprovação de outra pessoa

9) Para aprovar outros "pull requests", abra as abertas, veja as alterações e confirme se estiver tudo correto

10) Faça o "merge" com a master; a outra branch é removida automaticamente.