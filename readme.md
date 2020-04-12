Nubank - Clone Course

Curso ministrado pelo Diego da Rocketset.  

Esta aplicação foi desenvolvida como treinametno para replicar a a interface iniciar o aplicativo do Nubank.

Utilizei o Expo para a criação do aplicativo, saindo um pouco da orientação do curso que era para criar uma aplicação através do react-native. Como não tenho um emulador utilizei o Expo, mantendo todas as caracteristicas do curso original mas com recursos do Expo como simulador.

- [ ]  Vamos usar o template do React-Native-Template-Basic da Rocktseat que já vem com bastante coisa pronta e configurada como axios, styled components, gesture handler, etc. (docs.rocketseat.dev)

## CRIAR PROJETO USANDO REACT-NATIVE

TEMPLATE ROCKETSEAT - já traz diversas dependências instaladas

- [ ]  **react-native init nubank --template rocketseat-basic**

## CRIAR PROJETO USANDO O EXPO

- [ ]  **expo init**
- [ ]  selecionar blank template

## INICIAR O GIT

- [ ]  Acessar a pasta da aplicação criada e rodar o comando "**git init**" para criar o git master para a aplicação e fazer o controle de versionamento.
- [ ]  git init
- [ ]  git add .
- [ ]  git commit -m "First commit"

## CONFIGURAR O **GESTURE HANDLER**

- [ ]  **No projeto do Expo vamos ter que instalar manualmente todas as dependências usando o NPM.**
    - [ ]  npm install --save react-native-gesture-handler
    - [ ]  react-native link react-native-gesture-handler

- [ ]  Acessar a documentação do React Native Gesture Handler, [https://software-mansion.github.io/react-native-gesture-handler/docs/getting-started.html](https://software-mansion.github.io/react-native-gesture-handler/docs/getting-started.html),  para completar a configuração após a criação da aplicação no VScode. Seguir conforme abaixo:

Update your `MainActivity.java` file (or wherever you create an instance of `ReactActivityDelegate`), so that it overrides the method responsible for creating `ReactRootView` instance and then use the root view wrapper provided by this library. Do not forget to import `ReactActivityDelegate`, `ReactRootView`, and `RNGestureHandlerEnabledRootView`:

    package com.swmansion.gesturehandler.react.example;
    
    import com.facebook.react.ReactActivity;
    + import com.facebook.react.ReactActivityDelegate;
    + import com.facebook.react.ReactRootView;
    + import com.swmansion.gesturehandler.react.RNGestureHandlerEnabledRootView;
    
    public class MainActivity extends ReactActivity {
    
      @Override
      protected String getMainComponentName() {
        return "Example";
      }
    
    +  @Override
    +  protected ReactActivityDelegate createReactActivityDelegate() {
    +    return new ReactActivityDelegate(this, getMainComponentName()) {
    +      @Override
    +      protected ReactRootView createRootView() {
    +       return new RNGestureHandlerEnabledRootView(MainActivity.this);
    +      }
    +    };
    +  }
    }

- [ ]  Rodar o projeto dentro do emulador **"react-native run-android"** se tiver um emulador instalado. Se não tiver, usar o expo. Para isso realizar a instalação do expo usando 
**"npm install -g expo-cli"** e **"npm install expo".** Instalar também o aplicativo do expo em seu smartphone. Toda a documentação do Expo está em [https://docs.expo.io/versions/v37.0.0/](https://docs.expo.io/versions/v37.0.0/).

    Lembre-se que a versão do aplicativo do Expo no smartphone deve ser compativel com a versão do cli instalada em seu ambiente de desenvolvimento.

# DEPENDÊNCIAS

- [ ]  npm install --save-dev babel-plugin-styled-components
- [ ]  npm install --save styled-components
- [ ]  npm install react-native-vector-icons
- [ ]  react-native link react-native-vector-icons
- [ ]  npm install react-native-qrcode (não funciona no Expo, só no projeto criado com react-native)
    - [ ]  Para rodar no Expo usar o react-native-svg ()

            npm install react-native-svg --save
            react-native link react-native-svg
            npm install react-native-qrcode-svg --save

        [react-native-qrcode-svg](https://www.npmjs.com/package/react-native-qrcode-svg)

- [ ]  Dentro do **react-native-vector-icons/material-icons,**  usamos os ícones que podem ser consultados no site:

[Material Icons](https://material.io/resources/icons/?style=baseline)
