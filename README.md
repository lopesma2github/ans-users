Para gerar as senha criptografadas que ficam na variável ansible_ssh_password

pip install passlib

python -c "from passlib.hash import sha512_crypt; import getpass; print(sha512_crypt.using(rounds=5000).hash(getpass.getpass()))"

Irá solicitar a digitação da senha

copie a senha gerada no console e insira na variável que está no arquivo
roles/users/tasks/main.yaml -> variável "password"


Para utilizar