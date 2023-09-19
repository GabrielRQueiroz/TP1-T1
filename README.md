# TP1-T1
Trabalho n. 1 de Técnicas de programação, UnB, 2023/2

## Requisitos funcionais
- [ ] O sistema proverá suporte ao uso do método Kanban no gerenciamento de projetos.
- [ ] Para usar o sistema, o usuário deve criar uma conta.
- [ ] Para criar uma conta, deve informar nome, endereço de correio eletrônico e senha.
- [ ] O usuário precisa ser autenticado para ter acesso a outros serviços.
- [ ] Para ser autenticado, deve informar endereço de correio eletrônico e senha.
- [ ] Após ser autenticado, tem acesso aos seguintes serviços relacionados à sua conta:
  - [ ] visualizar,
  - [ ] editar e
  - [ ] eliminar conta.
- [ ] A visualização de conta resulta na apresentação dos dados da conta.
- [ ] A edição de conta possibilita alterar nome e/ou senha da conta.
- [ ] Após ser autenticado, o usuário tem também acesso aos seguintes serviços:
  - [ ] criar quadro (board),
  - [ ] visualizar quadro,
  - [ ] eliminar quadro,
  - [ ] criar cartão (card),
  - [ ] visualizar cartão,
  - [ ] mover cartão,
  - [ ] eliminar cartão.
- [ ] Ao criar quadro ou cartão, deve informar os dados necessários.
- [ ] A visualização de quadro resulta na apresentação dos dados do quadro e dos códigos dos cartões associados ao quadro.
- [ ] A visualização de cartão resulta na apresentação dos dados do cartão.
- [ ] Para visualizar quadro ou cartão, o usuário deve informar código de quadro ou de cartão.
- [ ] O serviço mover cartão possibilita alterar nome da coluna onde está o cartão.
- [ ] O sistema deve assegurar as seguintes regras:
  - [ ] usuário só pode eliminar quadro por ele criado;
  - [ ] eliminar quadro resulta na eliminação dos cartões associados;
  - [ ] número máximo de cartões na coluna trabalho em progresso é igual ao limite do trabalho em progresso (work in progress limit) informado no quadro.


## Requisitos não funcionais
- [ ] Adotar o estilo de arquitetura em camadas (layers).
- [ ] A arquitetura do software deve ser composta por camada de apresentação e por camada de serviço.
- [ ] A camada de apresentação deve ser responsável pela interface com o usuário e pela validação dos dados de entrada.
- [ ] A camada de serviço deve ser responsável pela lógica de negócio e por armazenar dados.
- [ ] Cada camada deve ser decomposta em módulos de software.
- [ ] Módulos de software devem interagir por meio de serviços especificados em interfaces.
- [ ] Módulos de software devem ser decompostos em classes.
- [ ] Devem ser implementadas classes que representem domínios, entidades e controladoras.
- [ ] Implementar o código na linguagem de programação C++.
- [ ] Prover projeto compatível com o ambiente de desenvolvimento Code::Blocks.

## Domínios
| NOME        | FORMATO VÁLIDO                                           |
|-------------|---------------------------------------------------------|
| **CODIGO**      | Formato LLDD                                           |
|             | L é letra maiúscula (A - Z)                            |
|             | D é dígito (0 – 9)                                     |
| **COLUNA**      | SOLICITADO, EM EXECUCAO, CONCLUIDO                     |
| **EMAIL**       | Formato: nome@domínio                                  |
|             | nome é composto por 2 a 10 caracteres                  |
|             | domínio é composto por 2 a 20 caracteres               |
|             | Cada caractere é letra (A-Z ou a-z), dígito (0 – 9) ou ponto (.) |
|             | Caractere @ não pode ser imediatamente precedido ou sucedido por ponto (.) |
|             | Não há pontos (.) em sequência                         |
| **LIMITE**      | 5, 10, 15, 20                                          |
| **SENHA**       | Formato: XXXXX                                         |
|             | X é um dos seguintes caracteres: letra (A - Z, a - z), dígito (0 - 9), sinal de pontuação ( . , ; ? !) |
|             | Pelo menos um caractere é letra maiúscula              |
|             | Pelo menos um caractere é letra minúscula              |
|             | Pelo menos um caractere é dígito                       |
|             | Pelo menos um caracter é sinal de pontuação            |
|             | Não há caractere duplicado                             |
| **TEXTO**       | 5 a 30 caracteres                                       |
|             | Cada caractere é letra (A - Z, a - z), dígito (0-9), sinal de pontuação ( . , ; ? !) ou espaço em branco |
|             | Não há espaços em branco em sequência                   |
|             | Não há sinais de pontuação em sequência                 |
|             | Não há acentuação                                      |
|             | Primeiro caractere é letra maiúscula                    |
|             | Primeiro caractere após sinal de pontuação (exceto vírgula ou ponto-e-vírgula) é letra maiúscula |

## Avaliação final

### Atividades
- [ ] Projetar e codificar classe para cada domínio (domain).
- [ ] Projetar e codificar classe para cada entidade (entity).
- [ ] Projetar, codificar e executar teste de unidade (unit test) para cada classe domínio.
- [ ] Projetar, codificar e executar teste de unidade (unit test) para cada classe entidade.
- [ ] Documentar classes que representam domínios e entidades por meio de texto em formato HTML.

### Requisitos
- [ ] Trabalho pode ser realizado individualmente ou por equipe com até quatro participantes.
- [ ] Preencher os documentos com clareza e atentar para a ortografia.
- [ ] Adotar um padrão de codificação (coding standard).
- [ ] Fornecer os códigos em formato fonte e em formato executável.
- [ ] Em cada classe, identificar por comentários, a matrícula do aluno responsável pela implementação da classe.
- [ ] Cada classe domínio deve conter atributo que seja instância de tipo suportado pela linguagem de programação.
- [ ] Cada classe domínio deve permitir acesso ao atributo por meio de métodos públicos set e get.
- [ ] Método set de cada classe domínio deve lançar exceção em caso de formato inválido.
- [ ] Cada classe de entidade deve conter atributos onde cada atributo é instância de classe domínio.
- [ ] Cada classe de entidade deve permitir acesso aos atributos por meio de métodos públicos set e get.
- [ ] Nesse trabalho, associações entre entidades não são implementadas.
- [ ] Cada teste de unidade deve ser classe com diferentes métodos para diferentes casos de teste.
- [ ] Cada teste de domínio deve exercitar o domínio por meio de um cenário com valor válido e um com valor inválido.
- [ ] Execução de cada teste de domínio deve resultar em sucesso.
- [ ] Cada teste de entidade deve invocar cada método público da entidade pelo menos uma vez.
- [ ] Cada teste de entidade deve comprovar que métodos invocados resultam no comportamento esperado.
- [ ] Execução de cada teste de entidade deve resultar em sucesso.
- [ ] Fornecer projeto Code::Blocks que possibilite compilar e executar códigos sem erros na plataforma de correção.
- [ ] Gerar documentação dos domínios e das entidades em formato HTML por meio da ferramenta Doxygen.
- [ ] Escrever documentação das classes em formato HTML segundo perspectiva dos usuários das classes.
- [ ] Incluir todos os artefatos construídos em um arquivo zip.
- [ ] Atribuir o nome T1-TP1-X-Y-Z.ZIP ao arquivo zip.
- [ ] No nome do arquivo zip, X, Y e Z devem ser os números de matrícula dos autores do trabalho.
- [ ] Testar se o arquivo pode ser descompactado com sucesso e se não há vírus no mesmo.
- [ ] Enviar o arquivo dentro do prazo.
- [ ] Não cumprimento de requisitos resulta em redução de nota do trabalho.

## 
