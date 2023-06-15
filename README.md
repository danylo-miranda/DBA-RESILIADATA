# DBA-RESILIADATA
## Banco de dados que armazena dados importantes.

---

# Entidades:

1° Tabela de empresas parceiras:

* Campos: ID_Empresa (chave primária), nome, endereço, contato, etc.
* Relacionamentos: Nenhum relacionamento direto com outras tabelas.

2° Tabela de tecnologias:

* Campos: ID_Tecnologia (chave primária), nome, descrição, área (webdev, dados, marketing), etc.
* Relacionamentos: Nenhum relacionamento direto com outras tabelas.

3° Tabela de tecnologias utilizadas pelas empresas:

* Campos: ID_Empresa (chave estrangeira referenciando a tabela de empresas), ID_Tecnologia (chave estrangeira referenciando a tabela de tecnologias).
* Relacionamentos: Cada registro nessa tabela representa uma associação entre uma empresa parceira e uma tecnologia utilizada por ela.

4° Tabela de colaboradores:

* Campos: ID_Colaborador (chave primária), nome, cargo, ID_Empresa (chave estrangeira referenciando a tabela de empresas).
* Relacionamentos: Cada registro nessa tabela representa um colaborador e está relacionado com a empresa a qual ele pertence.

# Relacionamentos:

Dessa forma, as tabelas se **relacionam** da seguinte maneira:

* A tabela de empresas parceiras não tem relacionamento direto com as demais tabelas.
* A tabela de tecnologias não tem relacionamento direto com as demais tabelas.
* A tabela de tecnologias utilizadas pelas empresas tem relacionamento com a tabela de empresas parceiras e com a tabela de tecnologias.
* A tabela de colaboradores tem relacionamento com a tabela de empresas parceiras.

Essa estrutura de tabelas permite armazenar e relacionar os dados importantes do sistema RESILIADATA, facilitando a avaliação das tecnologias utilizadas pelas empresas parceiras e a identificação de seus colaboradores.

