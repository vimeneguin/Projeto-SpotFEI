Spotfei
Projeto Spotfei — um sistema de música estilo Spotify feito em Java com interface gráfica Swing. Permite gerenciamento de usuários, playlists, músicas e histórico de reprodução.

Descrição
O Spotfei é um aplicativo desktop desenvolvido em Java com Swing que oferece funcionalidades para criação e gerenciamento de playlists, cadastro e login de usuários, controle de músicas e histórico de reprodução. Utiliza acesso a banco de dados por meio de DAOs para persistência e manipulação dos dados.

Funcionalidades principais
Cadastro e login de usuários com autenticação segura.

Criação, edição e exclusão de playlists.

Inclusão, remoção e reprodução de músicas.

Registro do histórico das músicas tocadas pelo usuário.

Interface gráfica intuitiva e responsiva utilizando Swing.

Persistência dos dados com acesso a banco via DAOs.

Controle de operações com tratamento de exceções.

Tecnologias utilizadas
Java 8+ (JDK)

Swing para interface gráfica

JDBC para conexão com banco de dados (ex: MySQL, SQLite)

DAO (Data Access Object) para abstração do acesso a dados

SQL para manipulação das tabelas: usuario, playlists, musicas, historico_musicas

Estrutura do projeto
model: Classes que representam as entidades do sistema (Usuario, Playlist, Musica, HistoricoMusicas).

dao: Classes DAO responsáveis pela comunicação com o banco de dados.

view: Interfaces gráficas Swing (JFrames, JPanels).

controller: Lógica do sistema para conectar a interface com os dados.

util: Classes utilitárias (ex: conexão com banco, tratamento de erros).

Banco de dados
O projeto utiliza um banco de dados relacional com as seguintes tabelas principais:

usuario (id, nome, email, senha, etc.)

playlists (id, nome, id_usuario, etc.)

musicas (id, titulo, artista, duracao, etc.)

historico_musicas (id, id_usuario, id_musica, data_hora, etc.)

Como executar
Clone o repositório:

bash
Copiar
Editar
git clone https://github.com/seuusuario/spotfei.git
Configure seu banco de dados (MySQL, SQLite ou outro) e ajuste o arquivo de conexão (ex: Conexao.java).

Importe o projeto na sua IDE preferida (Eclipse, IntelliJ, NetBeans).

Compile e execute a classe principal (Main.java ou similar).

Use a interface para cadastrar usuários, criar playlists e ouvir músicas.

Problemas conhecidos
Alguns erros na manipulação das DAOs podem ocorrer se as conexões não forem fechadas corretamente.

Validar melhor a entrada de dados nos formulários para evitar erros.

Implementar melhorias na usabilidade e design da interface gráfica.
