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
