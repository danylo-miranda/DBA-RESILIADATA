# DBA-RESILIADATA
## 🏦 Banco de dados que armazena dados importantes.

---

# 📅 Entidades:

1° Tabela de empresas parceiras:

* Campos: 🔑 ID_Empresa (chave primária), nome, endereço, contato, etc.
* Relacionamentos: (1,N) com a tabela Colaboradores e (1,N) com a tabela Tec_utilizadas.

2° Tabela de tecnologias:

* Campos: 🔑 ID_Tecnologia (chave primária), nome, descrição, área (webdev, dados, marketing, etc).
* Relacionamentos: (1,N) com a tabela Tec_utilizadas. 

3° Tabela de colaboradores:

* Campos: 🔑 ID_Colaborador (chave primária), nome, cargo, 🔐 ID_Empresa (chave estrangeira referenciando a tabela de empresas).
* Relacionamentos: (N,1) Cada registro nessa tabela representa um colaborador e está relacionado com a empresa a qual ele pertence.

4° Tabela de tecnologias utilizadas pelas empresas:

* Campos: 🔐 ID_Empresa (chave estrangeira referenciando a tabela de empresas), 🔐 ID_Tecnologia (chave estrangeira referenciando a tabela de tecnologias).
* Relacionamentos: (N,1) Cada registro nessa tabela representa uma associação entre uma empresa parceira e uma tecnologia utilizada por ela.


# 🔃 Relacionamentos:

Dessa forma, as tabelas se **relacionam** da seguinte maneira:

* A tabela de Stakeholders (empresas parceiras) tem relacionamento de (1,N) com as tabelas Colaboradores e Tec_utilizadas .
* A tabela de tecnologias tem relacionamento (1,N) com a tabela Tec_utilizadas.
* A tabela de colaboradores tem relacionamento (N,1) com a tabela de empresas parceiras.
* A tabela de tecnologias utilizadas pelas empresas tem relacionamento (N,1) com a tabela de empresas parceiras e com a tabela de tecnologias.

# 📑 Tipos de Dados:

1° Tabela de Stakeholders (empresas parceiras):

ID_Empresa = INT PRIMARY KEY 🔑
nome = VARCHAR 🔤
endereço = VARCHAR 🔤
telefone = INT 1️⃣
e-mail = VARCHAR 🔤
cnpj = INT 1️⃣

2° Tabela de tecnologias:

ID_tecnologia = INT PRIMARY KEY 🔑
descrição = VARCHAR 🔤
área = VARCHAR 🔤
nome = VARCHAR 🔤

3° Tabela de colaboradores:

ID-Colaborador = INT PRIMARY KEY 🔑
nome = VARCHAR 🔤
cargo = VARCHAR 🔤
ID_Empresa = FOREST KEY 🔐

4° Tabela de tecnologias utilizadas pelas empresas:

ID_Empresa = FOREST KEY 🔐
ID_Tecnologia =  FOREST KEY 🔐



Essa estrutura de tabelas permite armazenar e relacionar os dados importantes do sistema RESILIADATA, facilitando a avaliação das tecnologias utilizadas pelas empresas parceiras e a identificação de seus colaboradores.

