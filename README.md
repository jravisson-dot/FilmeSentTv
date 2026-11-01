# FilmesSent TV — projeto Android WebView

Aplicativo Android/Fire TV que abre https://filmessent.com/ em tela cheia.

## O que faz
- Mantém a navegação principal em `filmessent.com` e seus subdomínios.
- Bloqueia navegações principais para outros domínios e esquemas externos.
- Recusa janelas pop-up.
- Bloqueia requisições a uma lista inicial de domínios publicitários/rastreadores.
- Permite conteúdo incorporado em iframes, inclusive players externos, para não quebrar automaticamente os vídeos.
- Usa o botão Voltar do controle para voltar na navegação.

## Limitações importantes
- Não é um bloqueador universal. Anúncios servidos pelo próprio domínio, overlays em HTML e publicidade dentro do player podem continuar aparecendo.
- O site pode alterar seus domínios e a lista de bloqueio pode precisar de manutenção.
- Alguns players podem abrir uma página externa como navegação principal; ela será bloqueada por projeto.
- O projeto não remove anúncios de dentro do vídeo nem contorna login, DRM ou restrições de acesso.

## Como gerar o APK no Windows
1. Instale o Android Studio e o Android SDK Platform 35.
2. Extraia o ZIP.
3. No Android Studio, escolha **Open** e selecione a pasta `FilmesSentTV`.
4. Aguarde a sincronização do Gradle.
5. Selecione **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
6. O APK de teste ficará em `app/build/outputs/apk/debug/app-debug.apk`.

## Instalar no Fire TV
Ative as opções de desenvolvedor e a instalação de aplicativos desconhecidos. Transfira o APK por Downloader ou ADB e instale.

## Observação
Este é o código-fonte do aplicativo, não um APK já compilado. A compilação precisa do Android SDK/Gradle.

## Gerar APK sem Android Studio (GitHub Actions)
1. Crie uma conta gratuita no GitHub, se ainda não tiver.
2. Crie um repositório novo e envie todos os arquivos deste projeto, incluindo a pasta `.github`.
3. Abra a aba **Actions** do repositório.
4. Aguarde o workflow **Build FilmesSent TV APK** terminar com sucesso.
5. Abra a execução concluída e baixe **FilmesSentTV-debug-apk** em Artifacts.
