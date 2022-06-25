# pyspark_instalacao
Guia para instalação do Pyspark no Windows 10

### Tutorial para Instalação e Configuração do PySpark:
```
--- Aula 01 - Conceitos Básicos de PySpark
https://www.youtube.com/watch?v=WpIDLm9ow2o    

--- Aula 02 - Download dos softwares Apache SPARK, Anaconda e Java(JDK)
https://www.youtube.com/watch?v=qtEZXXrGkFk    
  
--- Aula 03 - Instalar os softwares Java JDK, Anaconda, Pyspark
https://www.youtube.com/watch?v=L3oWBs0aMvI    

--- Aula 04 - Configuração das variáveis de ambiente no Windows 
https://www.youtube.com/watch?v=WXnVnwy-Zko    

--- Aula 05 - Executando os softwares Apache SPARK e PYSPARK
https://www.youtube.com/watch?v=xKOSnC2pICo    
```

### Instaladores:
```
  Anaconda: https://www.anaconda.com/products/individual
  Spark:    https://spark.apache.org/downloads.html
  Java JDK: https://www.oracle.com/java/technologies/javase-downloads.html   
  Hadoop:   https://hadoop.apache.org/release/3.2.2.html
```

### Instalações adicionais:
Os arquivos winutils.exe e winutils.pdb não foram baixados com a Hadoop<br>
Neste caso, foi necessário baixar os arquivos a parte

```
Baixar os arquivos winutils.exe e winutils.pdb do Github abaixo e salvar na pasta C:\Hadoop
https://github.com/steveloughran/winutils/tree/master/hadoop-3.0.0/bin  
```

### Notas Importantes:
```
Os programas Anaconda e Java JDK possuem instaladores próprios.
O Spark e o Hadoop devem ser descompactados nos diretórios, C:\Spark e C:\Hadoop respectivamente
A versão do Java que funciona com Spark é a 11.
```

### Codificando no PyCharm
Crie um projeto no PYCharm e inclua o código abaixo:
```
from pyspark.sql import SparkSession

spark = SparkSession.builder.appName("DataFrame").getOrCreate()

df = spark.read.text("dados.txt")

df.selectExpr("split(value, ';') as\
Text_Data_In_Rows_Using_Text").show(4, False)
```
Feito isso, o PyCharm irá sublinhar o pacote pycharm.sql solicitando a instalação<br>
Clique sob este pacote e clique em instalar.
Feito isso, será possível usar o pyspark sem problemas.
