# Jogo de Cara ou Coroa para Android

Este é um aplicativo simples de jogo de cara ou coroa para dispositivos Android. O aplicativo permite que os usuários joguem e acompanhem estatísticas simples sobre os resultados.

## Capturas de Tela

<img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjAHY7Tivk7d8uwDp8FPKmYQVcErzOa9BN0Labbe3TbjRKXJpRKw2yTpkomQUjCulaJekb0dov11zIl2-9TCvEToZCih7jzdowDMK0cM5bwcJWjeVbiwNEc8lb04fzMJHblHn8sUoW4a2SkfoyGxVglxfV_OVPVIaqfwZFzW_TapbwXnAksuVpT9ZDjMBZe/s1440/tela%20do%20jogo.jpg" alt="Captura de Tela 1" width="400">

<img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjzTf_N7HySu0WrFVAjOHfT_qyK8tnnl8GoxZ024KLGCrrysGrOVIcvcBAC4ehbrJqDEy7ZTXpRyImJRNxX3j6sfrUYGQglQiW2I49941N5m2iKuHJd_N1kd-rW_uJa9V-WwvVPhNeGbsCNRPWhef8sUxE4_UHYOrItBedaXpSHPFENJli6fRAin-lMVqEx/s1440/tela%202%20do%20jogo.jpg" alt="Captura de Tela 2" width="400">

<img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEglyplt8b337gsM30yUKz8TGufSeMe5jelHSX7WTfqD8HVDd3eB45hfnXrpXgiKLmaaH-3-O2ip9DPY9y7oA2z1kENKqUoDiKxVCHrDEXki7N721W-Q6CyWR2UiKQRwuO7LoeyBUiiHkseGS73ru50yJ8F_1o097b43ygMc6yB0VixxUBVock-9trRxruAL/s1440/tela%203%20do%20jogo.jpg" alt="Captura de Tela 3" width="400">

## Funcionalidades

- **Botão "JOGAR"**: Ao ser pressionado, simula o lançamento de uma moeda e exibe o resultado (cara ou coroa).
- **Botão "ZERAR"**: Reinicia o jogo, zerando as contagens de caras, coroas e o número de vezes jogadas.
- **Estatísticas**: Mostra o número de vezes que cada lado da moeda apareceu e a quantidade total de jogadas.

## Componentes do Aplicativo

O aplicativo é composto por:
- Interface de usuário simples com botões e textos para exibir informações.
- Uso de imagens (cara e coroa) para representar o resultado do jogo.
- Sons reproduzidos para dar feedback durante o jogo.
- Utilização de uma WebView para exibir um GIF da moeda.

## Descrição da Classe `telaRealBr`

### Variáveis da Classe `telaRealBr`:
- `moedaView`: Uma `ImageView` para exibir a imagem da moeda.
- `btnJogar`: O botão que o usuário pressiona para jogar.
- `som1`, `som2`, `somEgg`: Objetos `MediaPlayer` para reproduzir diferentes sons durante o jogo.
- `numeroDeCara`, `numeroDeCoroa`, `numeroDeVezesJogadas`, `numeroAleatrorios`, `egg`: Variáveis para controlar o número de caras, coroas, vezes jogadas, números aleatórios gerados e um contador especial ("egg").
- `numerosAleatoriosView`, `numeroDeVezesJogadasView`, `viewNumeroDeCara`, `viewNumeroDeCoroa`: `TextViews` para exibir informações na interface do usuário.
- `moedaGif`: Uma `WebView` para mostrar um GIF da moeda.

### Método `onCreate`:
- Configura a Activity quando é criada:
  - Define o layout usando `setContentView`.
  - Associa elementos de interface do usuário a variáveis usando `findViewById`.
  - Carrega um arquivo HTML contendo um GIF da moeda na `WebView`.
  - Esconde a barra de ação usando `getSupportActionBar().hide()`.

### Método `Jogar`:
- É chamado quando o botão "JOGAR" é pressionado.
- Inicia um som de moeda (`som1.start()`).
- Oculta o GIF da moeda.
- Incrementa o número de vezes jogadas e exibe esse número.
- Gera um número aleatório de 0 a 999.
- Exibe o número aleatório gerado e atualiza a interface para mostrar se é cara ou coroa.

### Método `Zera`:
- É chamado quando o botão "ZERAR" é pressionado.
- Inicia um som de reinicialização (`som2.start()`).
- Zera o número de vezes jogadas e exibe isso na interface.
- Verifica um contador especial ("egg") para exibir um texto específico após três vezes de zerar seguidas.
- Reinicia as contagens de caras e coroas.
- Limpa a imagem da moeda.
- Torna visível o GIF da moeda novamente.

## Como Usar

1. Faça o download ou clone este repositório.
2. Abra o projeto em um ambiente de desenvolvimento Android, como o Android Studio.
3. Execute o aplicativo em um emulador ou dispositivo Android.

## Contribuindo

Contribuições são bem-vindas! Se você deseja melhorar este jogo, sinta-se à vontade para fazer um fork deste repositório, fazer suas alterações e criar um pull request.

## Créditos

- Desenvolvido por [João Marcos](https://grupo.jm7087.com)
