## App Video Aula YouTube - Pokedex Flutter

### "Flutter Pokedex: Aula 1 - Utilizando Stack e Positioned"

1. Crie um projeto pelo Visual Studio

2. Após criado, reabra a pasta do projeto usando o VSCode (questão de preferência)

3. Delete o conteúdo de Main.dart, deixando apenas a primeira Widget Build

4. Altere o title para o `Pokedex - Youtube`

5. Adicione `debugShowCheckedModeBanner` para retirar a faixa de debug do App

6. Crie a pasta assets/fonts e assets/images

7. Adicione as duas fontes usadas e as imagens de logo

8. Já deixe adicionado o conjunto de dependências abaixo em `pubspec.yaml`

```yaml
dependencies:
  mobx:
  flutter_mobx:
  cached_network_image: ^2.0.0
  md2_tab_indicator: ^1.0.2
  provider: ^4.0.4
  flutter_staggered_animations: ^0.1.2
  sliding_sheet: ^0.2.6
  flutter_icons: ^1.0.0+1
  intl: ^0.16.1
```

9. Adicione também as seguintes dependências de desenvolvimento

```yaml
dev_dependencies:
  flutter_test:
    sdk: flutter
  mobx_codegen:
  build_runner:
```

10. Também adicione as imagens de assets no arquivo

```yaml
assets:
  - assets/images/pokeball.png
  - assets/images/pokeball_dark.png
```

11. Também adicione as fontes

```yaml
fonts:
  - family: Google
    fonts:
      - asset: assets/fonts/ProductSans-Regular.ttf
      - asset: assets/fonts/ProductSans-Bold.ttf
        weight: 700
```

12. Crie o arquivo `pages/home_page/home_page.dart` com stateless

13. Importe home_page como `Home` em main.dart

14. Crie o arquivo `consts/const_app.dart` e adicione as constantes de acesso as imagens

15. Na build Trabalhe usando Stacks() que permite que você trabalhe com varias camadas sobrepostas
    tal qual o nome sugere, pilhas.

16. Na Stack() desenvolva o conteúdo do App_Bar da tela

17. Após feito, componentize copiando o conteúdo e colocando no arquivo
    `pages/home_page/widgets/app_bar_home.dart`

18. Na `home_page.dart` importe e coloque no lugar a chamada para o `AppBarHome()` na `Stack()`

### "Flutter Pokedex: Aula 2 - Consumindo API com MobX"

19. Criar o arquivo `stores/pokeapi_store.dart`

20. Instalar a extensão flutter_mobx no VSCode

21. Aplicar o snippet mobx no `pokeapi_store.dart`

22. Rodar o comando abaixo para trabalhar com o Mobx
    `flutter packages pub run build_runner build`

23. Após a geração do `pokeapi_store.g.dart`, rode o comando abaixo para o console
    ficar monitorando as alterações do arquivo `pokeapi_store.dart`
    `flutter packages pub run build_runner watch`

24. Entre na URL abaixo e copie o conteúdo JSON da pokedex
    `https://raw.githubusercontent.com/Biuni/PokemonGO-Pokedex/master/pokedex.json`

25. Entre no site abaixo, cole o conteúdo do Json e transforme para uma Dart Class com nome de PokeAPI
    `https://javiercbk.github.io/json_to_dart/`

26. Crie o arquivo `models/pokeapi.dart` e cole o conteúdo da PokeAPI

27. Duplique a classe NextEvolution e a nomeie como PrevEvolution para corrigir os erros

28. Adicionar a dependência http em `pubspec.yaml`

```yaml
dependencies:
  http: ^0.12.0+4
```

29. Criar o arquivo `consts/consts_api.dart` e colocar a URL do pokedex JSON

30. Importar a pokeapiURL no Store, dentro da loadPokeAPI()

31. Preparar a fetchPokemonList para carregar e receber o conteúdo da loadPokeAPI()

32. Ir em home_page.dart e criar um Observer para consumir a pokeapi_store.dart

33.
