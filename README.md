# rails !

instalando

```
gem install rails
```

criando novo projeto

```
rails new APP
```

rodando server (na pasta do projeto criado)

```
rails s
```

comando para rodar servidor no c9.io

```
rails s -b $IP -p $PORT
```

criando modelos - g de generator, scaffold porque faz todo o trabalho nos diretórios, link é o modelo, title e url são atributos

```
rails g scaffold link title:string utl:string
```

migrate db - sempre que novos modelos forem criados, o migrate deve ser executado.

```
rake db:migrate
```

console rails - console para testes rápidos

```
rails c

# comando no console para verificar usuários cadastrados com o devise
User.count
```





