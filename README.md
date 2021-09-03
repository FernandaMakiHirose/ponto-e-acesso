# Construindo um sistema de controle de ponto e acesso com Spring Boot
Desenvolvi uma API Rest para controle de ponto e acesso dos usuários de uma empresa. Utilizei Java, Spring Boot, Hibernate Envers e lombok além de documentar toda a API com Swagger.

## Requisitos 
- IntelliJ IDEA. 
- Java com versão 8 ou maior.

## Passo 1 
- No IntelliJ abri o arquivo gerado e configure os mesmos passos para o Spring Initializr: 
- Gradle Project.
- Java.
- Spring 2.3.1.
- Group: com.dio.
- Artifact: live.
- Packaging: .Jar.
- Java: 11.
- Adicionei as dependências: Spring Boot DevTools, Lombok e Spring Configuration Processor.

## Passo 2 
- Todas as dependências estão no build.gradle. <br>
- Em preferences - plugins - plugin Lombok instalado. <br>
- No application.properties dizemos que a aplicação vai subir na porta 8080, o código comentado é sobre o mysql (caso queira fazer sua integração). <br>
- Pacote model criado (dentro se localiza os modelos). <br>
- Pacote repository criado (dentro se localiza o repository). <br>
- Pacote service criado (dentro se localize o service). <br>
- Pacote swagger criado (dentro se localiza o swagger, o qual documenta a API).
- Explicando configurações usadas: <br> <br>

  @Repository: o contêiner Spring entende que é uma class DAO e converte todas as exceções não verificadas (lançadas dos methods DAO) para Spring DataAccessException. Classe DAO é a class em que você escreve methods para executar operações em db.
  @Getter: cria o getter. <br>
  @Setter: cria o setter. <br>
  @AllArgsConstructor: cria um construtor com argumentos. <br>
  @NoArgsConstructor: cria um construtor sem argumentos. <br>
  @EqualsAndHashCode: evita escrever manualmente os métodos equals () e hashcode () nas classes. <br>
  @Builder: ajuda o lombok a traduzir o código durante a compilação. <br>
  @Entity: diz que uma classe também é uma entidade. <br>
  @Audited: rastreaia mudanças em entidades em uma tabela. <br>
  @OnToMany: algo pode fazer parte de muitos. <br>
  @ManyToOne: muitos podem fazer parte de algo. <br>
  @Embeddable: anotação para declarar que uma classe será incorporada por outras entidades. <br>
  @EmbeddedId: é usado para criar uma primary key. <br>
  @GeneratedValue: é utilizada para informar que a geração do valor do identificador único da entidade será gerenciada pelo provedor de persistência. <br>
  @RestController: é uma anotação de conveniência que é anotada com @Controller e @ResponseBody. <br>
  @RequestMapping: mapeia solicitações HTTP para métodos de tratamento de controladores MVC e REST. <br>
  @Autowired: informa ao Spring onde uma injeção deve ocorrer. <br>
  
## Para rodar o projeto
> ```
>gradle bootRun
> ```
## Para abrir o projeto
- Abra o seu navegador e digite: localhost:8082/h2.
- Clique em connect.

![image](https://user-images.githubusercontent.com/72028645/125210423-2897fe00-e276-11eb-8bb5-d963c1d3efa0.png)

- Ou você pode abrir com o <a href="http://localhost:8082/swagger-ui.html">Swager.</a> 
