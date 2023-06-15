# DBA-RESILIADATA
## Banco de dados que armazena dados importantes.

---

# Entidades

1° Tabela de empresas parceiras: Essa tabela irá armazenar as informações das empresas parceiras, como nome, endereço, contato, entre outros detalhes relevantes.

2° Tabela de tecnologias: Nessa tabela, serão registradas as diferentes tecnologias disponíveis, com opções para selecionar a área específica, como webdev, dados, marketing, etc. Cada tecnologia terá um identificador único e possivelmente outros atributos, como descrição ou nível de experiência necessário.

3° Tabela de relacionamento entre empresas e tecnologias: Essa tabela servirá para registrar as tecnologias utilizadas por cada empresa parceira. Pode ser uma tabela de relacionamento muitos-para-muitos, onde cada registro inclui o ID da empresa e o ID da tecnologia.

4° Tabela de colaboradores: Nessa tabela, serão cadastrados os colaboradores das empresas parceiras. As informações podem incluir nome, cargo, dados de contato, entre outros campos relevantes para identificação e gerenciamento dos colaboradores.

---

# Relacionamentos

As tabelas se relacionam por meio de chaves primárias e chaves estrangeiras. Esse relacionamento permite estabelecer conexões entre os registros das diferentes tabelas. Vou explicar como ocorre o relacionamento entre as tabelas mencionadas:

1° Tabela de empresas parceiras:

* Possui uma chave primária, por exemplo, "ID_Empresa".

2° Tabela de tecnologias:

* Possui uma chave primária, por exemplo, "ID_Tecnologia".

3° Tabela de relacionamento entre empresas e tecnologias:

* Contém duas chaves estrangeiras: "ID_Empresa" e "ID_Tecnologia".
* As chaves estrangeiras referenciam as chaves primárias das tabelas de empresas parceiras e tecnologias, estabelecendo uma relação entre elas.
* Cada registro nessa tabela representa uma associação entre uma empresa parceira e uma tecnologia utilizada por ela.

4° Tabela de colaboradores:

* Pode conter uma chave estrangeira, por exemplo, "ID_Empresa".
* A chave estrangeira "ID_Empresa" se relaciona com a chave primária da 
* Tabela de empresas parceiras, permitindo identificar a qual empresa cada 
* Colaborador pertence.

Dessa forma, os relacionamentos entre as tabelas são estabelecidos por meio das chaves primárias e chaves estrangeiras, permitindo consultar e conectar informações de diferentes tabelas com base nas associações definidas. Essa estrutura de relacionamento é fundamental para garantir a integridade dos dados e facilitar consultas e operações entre as tabelas.
