# Anotações Usadas nas Classes de Teste



- `@SpringBootTest`: Carrega o contexto da aplicação. Usado para testes de integração. 🔄



- `@AutoConfigureMockMvc`: Carrega o contexto da aplicação e trata as requisições sem subir o servidor. Usado para testes de integração e web. 🤖



- `@WebMvcTest(Classe.class)`: Carrega o contexto, porém somente da camada web. Usado para testes de unidade do controlador. 🌐



- `@ExtendWith(SpringExtension.class)`: Não carrega o contexto, mas permite usar os recursos do Spring com JUnit. Usado para testes de unidade de service/component. 🧪



- `@DataJpaTest`: Carrega somente os componentes relacionados ao Spring Data JPA. Cada teste é transacional e dá rollback ao final. Usado para testes de unidade do repository. 📊



## Fixtures



Fixtures é uma forma de organizar melhor o código dos testes e evitar repetições. 🛠️



## JUnit 5 vs JUnit 4



| JUnit 5 | JUnit 4 | Objetivo |

|---------|---------|----------|

| `@BeforeAll` | `@BeforeClass` | Preparação antes de todos testes da classe (método estático) |

| `@AfterAll` | `@AfterClass` | Preparação depois de todos testes da classe (método estático) |

| `@BeforeEach` | `@Before` | Preparação antes de cada teste da classe |

| `@AfterEach` | `@After` | Preparação depois de cada teste da classe |



## Mockito vs @MockBean



- `@Mock` ou `myComp = Mockito.mock(MyComp.class)`: Usar quando a classe de teste não carrega o contexto da aplicação. É mais rápido e enxuto. 🧩



- `@MockBean`: Usar quando a classe de teste carrega o contexto da aplicação e precisa mockar algum bean do sistema. 🤖



Para mais detalhes, consulte a referência do Stack Overflow: [link](https://stackoverflow.com/questions/44200720/difference-between-mock-mockbean-and-mockito-mock) 📚

