# Scanner-de-portas
Como executar o scanner de portas:

    Salvar o código em um arquivo Python: Copie o código fornecido e cole em um arquivo com a extensão .py, como scanner_de_portas.py.

    Executar o script: Após salvar o arquivo, abra o terminal ou prompt de comando, navegue até o diretório onde o arquivo está salvo e execute o script com o comando:

    Você deve ter o python instalado para executar o script

python scanner_de_portas.py

Inserir o IP do alvo: O script pedirá para você digitar o IP do alvo, que pode ser o IP de um roteador ou servidor que você deseja escanear. Exemplo:

Digite o IP do alvo: 192.168.1.1

Resultados: O script vai verificar se as portas listadas (como 21, 22, 23, 25, 53, 80, 443, 8080) estão abertas ou fechadas no IP especificado. Ele irá exibir uma mensagem indicando o estado de cada porta, por exemplo:

    Escaneando 192.168.1.1...
    [+] Porta 21 está ABERTA
    [-] Porta 22 está fechada
    [+] Porta 80 está ABERTA
    [-] Porta 8080 está fechada

Explicação do código:

    socket.socket(socket.AF_INET, socket.SOCK_STREAM): Cria um socket TCP para a comunicação.

    sock.settimeout(1): Define o tempo limite de 1 segundo para a tentativa de conexão.

    sock.connect_ex((target, port)): Tenta conectar ao IP e à porta especificados. O método retorna 0 se a conexão for bem-sucedida (porta aberta) e outro valor caso contrário (porta fechada).

    Lista de portas: O código verifica portas comuns, mas você pode adicionar ou remover portas da lista portas conforme necessário.

Atenção:

    Certifique-se de ter permissão para escanear o IP de destino. Escanear redes ou dispositivos sem permissão pode ser considerado ilegal.

    Esse código é para fins educacionais e deve ser usado de maneira responsável.
