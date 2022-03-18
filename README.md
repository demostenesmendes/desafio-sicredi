## Requisitos

Necessário ter **Docker** e **Python 3** instalados na máquina.

## Etapas

 1. Abrir terminal/CMD na pasta raiz;
 2. Executar `docker-compose up -d` no diretório onde o arquivo **Dockerfile** se encontra;
 3. Executar `pip install -r requirements.txt`
 4. Avaliar se os serviços já estão disponíveis no contêiner;
 5. Executar `python3 runner.py {caminho_onde_salvar_csv_sem_aspas}`

Seguinto essas etapas, o script irá provisionar um cluster **Spark**, com um **Worker** , e o banco de dados MySQL, que irá ser preenchido com os dados iniciais. O script `runner.py` irá se conectar com o banco através do **Spark** e executar o cruzamento das tabelas em formato de **DF** para agregar num único arquivo. Quanto ao **Spark** decidi usar o **PySpark** como encapsulador da engine por ter muita familiaridade com a linguagem **Python**. E todo desenvolvimento foi feito com **Spark SQL**.