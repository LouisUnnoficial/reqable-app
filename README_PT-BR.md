# Reqable

[Inglês](README.md) | [Chinês](README_CN.md) | [Chinês Tradicional](README_ZH-HANT.md) | [Japonês](README_JA.md) | [Coréia do Sul](README_KO.md) | [Espanhol](README_ES.md) | [Francês](README_FR.md) | [Alemão](README_DE.md) | [Russo](README_RU.md) | [Português-Brasil](README_PT-BR.md) |

⚠️ **Observação: Reqable não é um projeto de código aberto. Este repositório é usado exclusivamente para rastreamento de problemas, solicitações de recursos e feedback do usuário.**

## Sobre

[Reqable](https://reqable.com/) é uma plataforma de depuração e teste de APIs de última geração e completa. Oferece suporte multiplataforma, arquitetura sem necessidade de login, tamanho reduzido, alta taxa de transferência e uma experiência sem anúncios.

O Reqable combina uma ferramenta de captura de tráfego de API com um cliente de teste de API completo em um único ambiente profundamente integrado — permitindo fluxos de trabalho de captura e teste contínuos e substituindo várias soluções independentes.

![](arts/products_en.png)

A maioria dos recursos do Reqable está disponível gratuitamente, sem período de teste. A edição Community atende às necessidades da maioria dos desenvolvedores individuais; usuários avançados e equipes podem se beneficiar de atualizações.

Visite nosso site oficial: https://reqable.com

## Conteúdo

- [Sobre](#about)
- [Depuração de API](#api-debugging)
- [Teste de API](#api-testing)
- [Suporte MCP](#mcp-support)
- [Desempenho extremo](#extreme-performance)
- [Aplicativo móvel](#mobile-app)
- [Instalação](#installation)
- [Documentação](#documentation)
- [Agradecimentos](#thanks)

# Depuração de API

A Reqable emprega uma estratégia clássica de MITM (Homem no Meio) para interceptar o tráfego HTTP(S). Em plataformas desktop, ela captura o tráfego por meio da configuração de proxy em nível de sistema; em dispositivos móveis, ela utiliza um proxy local.
O tráfego capturado pode ser inspecionado e manipulado por meio de um conjunto abrangente de ferramentas de depuração: reprodução de solicitações, edição em linha, pontos de interrupção, reescrita de URLs, scripts personalizados e muito mais.

![](arts/screenshot_en_01.png)

# Teste de API

O Reqable oferece um cliente de API completo para compor, enviar e organizar requisições HTTP, WebSocket, SSE e gRPC (em breve). Inclui coleções de API com organização baseada em pastas.

![](arts/screenshot_en_02.png)

# Suporte MCP

O Reqable vem com um servidor MCP (Model Context Protocol) integrado, permitindo que assistentes de IA como Claude e GitHub Copilot interajam diretamente com o Reqable. Isso desbloqueia fluxos de trabalho orientados por IA para APIs.

![](arts/screenshot_en_03.png)

A implementação do servidor MCP é totalmente de código aberto. Consulte o [repositório do servidor MCP](https://github.com/reqable/reqable-mcp-server) para obter detalhes.

# Desempenho extremo

O Reqable foi desenvolvido com Flutter e C++, evitando deliberadamente um ambiente de execução de navegador embutido. Essa escolha arquitetônica fortalece a segurança, reduzindo a superfície de ataque e, ao mesmo tempo, proporcionando uma melhoria substancial. 

- Tempo de inicialização a frio em nível de milissegundos.
- Tamanho da instalação inferior a 100 MB.
- Consumo típico de memória inferior a 300 MB durante uso ativo.
Testes de desempenho de captura de pacotes

![](arts/benchmark_en_02.png)

Benchmarks de desempenho do cliente API

![](arts/benchmark_en_01.png)

> Os testes de desempenho foram realizados em um MacBook Pro da Apple com o chip M5. Em hardware com especificações inferiores, a diferença de desempenho do Reqable é ainda mais acentuada.

# Aplicativo móvel

A versão para dispositivos móveis mantém a paridade de recursos com a versão para desktop, oferecendo funcionalidades de depuração e teste de API em qualquer lugar. Ele permite adicionar um computador remoto através da leitura de um código QR, possibilitando que o tráfego móvel seja encaminhado para o computador para uma inspeção e manipulação mais detalhadas.

Com um login de conta opcional, a sincronização na nuvem pode ser ativada para replicar automaticamente os dados em todos os dispositivos conectados.

![](arts/screenshot_en_04.png)

> Os recursos de ponto de interrupção, reescrita e criação de scripts estão indisponíveis no momento em plataformas móveis devido às políticas de segurança de cada plataforma.

# Instalação

| Plataforma | Arquitetura | Formato | Download e Instalação | Observações |
| ---- | ---- | ---- | ---- | ---- |
| **Windows** | x86_64 | exe | [Download](https://app.reqable.com/download?platform=windows&arch=x86_64&ext=exe&locale=en-US) | Versão do instalador (recomendada), compatível com Windows 7 e versões posteriores.`. |
| **Windows** | x86_64 | zip | [Download](https://app.reqable.com/download?platform=windows&arch=x86_64&ext=zip&locale=en-US) | Versão portátil, compatível com Windows 7 e versões posteriores.`. |
| **Mac** | universal | - | instalação de cerveja reqable | Requer macOS `11.0` ou posterior. |
| **Mac** | Intel Chip | dmg | [Download](https://app.reqable.com/download?platform=macos&arch=x86_64&ext=dmg&locale=en-US) | Chip Intel, requer macOS 11.0 ou posterior. |
| **Mac** | Apple Silicon | dmg | [Download](https://app.reqable.com/download?platform=macos&arch=arm64&ext=dmg&locale=en-US) | Chip da série M, requer macOS 11.0 ou posterior. |
| **Linux** | x86_64 | deb | [Download](https://app.reqable.com/download?platform=linux&arch=x86_64&ext=deb&locale=en-US) | Compatível com `Ubuntu`, `Debian` e outras distribuições. Requer `GTK 3.0`. |
| **Linux** | x86_64 | AppImage | [Download](https://app.reqable.com/download?platform=linux&arch=x86_64&ext=AppImage&locale=en-US) | Compatível com `Ubuntu`, `Debian` e outras distribuições. Requer `GTK 3.0`. |
| **Android** | universal | - | [Google Play](https://play.google.com/store/apps/details?id=com.reqable.android) | Requer Android 5.0 ou posterior. |
| **Android** | arm64-v8a | apk | [Download](https://app.reqable.com/download?platform=android&arch=arm64&ext=apk&locale=en-US) | Requer Android 5.0 ou posterior. |
| **Android** | armeabi-v7a | apk | [Download](https://app.reqable.com/download?platform=android&arch=arm&ext=apk&locale=en-US) | Requer Android 5.0 ou posterior. |
| **Android** | x86_64 | apk | [Download](https://app.reqable.com/download?platform=android&arch=x86_64&ext=apk&locale=en-US) | Requer Android 5.0 ou posterior. |
| **iOS** | arm64 | - | [App Store](https://apps.apple.com/cn/app/id6473166828) | Requer iOS 13.0 ou posterior. |

## Documentação
https://reqable.com/en-US/docs/introduction

## Agradecimentos

<p align="left">
  <a href="https://github.com/RonaldinhoL" title="RonaldinhoL (51 issues)"><img src="https://avatars.githubusercontent.com/u/1797392?v=4&amp;s=80" width="40" height="40" alt="RonaldinhoL" /></a>
  <a href="https://github.com/cesuproxy" title="cesuproxy (49 issues)"><img src="https://avatars.githubusercontent.com/u/195559109?v=4&amp;s=80" width="40" height="40" alt="cesuproxy" /></a>
  <a href="https://github.com/zclovelyj" title="zclovelyj (23 issues)"><img src="https://avatars.githubusercontent.com/u/38125286?v=4&amp;s=80" width="40" height="40" alt="zclovelyj" /></a>
  <a href="https://github.com/xiuluoshendaren" title="xiuluoshendaren (21 issues)"><img src="https://avatars.githubusercontent.com/u/160598517?v=4&amp;s=80" width="40" height="40" alt="xiuluoshendaren" /></a>
  <a href="https://github.com/hhs66317" title="hhs66317 (18 issues)"><img src="https://avatars.githubusercontent.com/u/3916247?v=4&amp;s=80" width="40" height="40" alt="hhs66317" /></a>
  <a href="https://github.com/DemonZD" title="DemonZD (14 issues)"><img src="https://avatars.githubusercontent.com/u/91039854?v=4&amp;s=80" width="40" height="40" alt="DemonZD" /></a>
  <a href="https://github.com/xuennai" title="xuennai (13 issues)"><img src="https://avatars.githubusercontent.com/u/63104635?v=4&amp;s=80" width="40" height="40" alt="xuennai" /></a>
  <a href="https://github.com/NavinChen" title="NavinChen (12 issues)"><img src="https://avatars.githubusercontent.com/u/11780577?v=4&amp;s=80" width="40" height="40" alt="NavinChen" /></a>
  <a href="https://github.com/ejfkdev" title="ejfkdev (12 issues)"><img src="https://avatars.githubusercontent.com/u/152914458?v=4&amp;s=80" width="40" height="40" alt="ejfkdev" /></a>
  <a href="https://github.com/QuanTum2088" title="QuanTum2088 (12 issues)"><img src="https://avatars.githubusercontent.com/u/158152582?v=4&amp;s=80" width="40" height="40" alt="QuanTum2088" /></a>
  <a href="https://github.com/DreamlingBig" title="DreamlingBig (11 issues)"><img src="https://avatars.githubusercontent.com/u/44178151?v=4&amp;s=80" width="40" height="40" alt="DreamlingBig" /></a>
  <a href="https://github.com/cesaryuan" title="cesaryuan (10 issues)"><img src="https://avatars.githubusercontent.com/u/35998162?v=4&amp;s=80" width="40" height="40" alt="cesaryuan" /></a>
  <a href="https://github.com/am3k0" title="am3k0 (10 issues)"><img src="https://avatars.githubusercontent.com/u/71699483?v=4&amp;s=80" width="40" height="40" alt="am3k0" /></a>
  <a href="https://github.com/xvhuan" title="xvhuan (10 issues)"><img src="https://avatars.githubusercontent.com/u/50939413?v=4&amp;s=80" width="40" height="40" alt="xvhuan" /></a>
  <a href="https://github.com/picture-j" title="picture-j (10 issues)"><img src="https://avatars.githubusercontent.com/u/62652474?v=4&amp;s=80" width="40" height="40" alt="picture-j" /></a>
  <a href="https://github.com/cxplay" title="cxplay (9 issues)"><img src="https://avatars.githubusercontent.com/u/62034099?v=4&amp;s=80" width="40" height="40" alt="cxplay" /></a>
  <a href="https://github.com/SugarFatFree" title="SugarFatFree (9 issues)"><img src="https://avatars.githubusercontent.com/u/30424828?v=4&amp;s=80" width="40" height="40" alt="SugarFatFree" /></a>
  <a href="https://github.com/ghost" title="ghost (9 issues)"><img src="https://avatars.githubusercontent.com/u/10137?v=4&amp;s=80" width="40" height="40" alt="ghost" /></a>
  <a href="https://github.com/Lehcok" title="Lehcok (9 issues)"><img src="https://avatars.githubusercontent.com/u/63954316?v=4&amp;s=80" width="40" height="40" alt="Lehcok" /></a>
  <a href="https://github.com/19774279" title="19774279 (9 issues)"><img src="https://avatars.githubusercontent.com/u/3414408?v=4&amp;s=80" width="40" height="40" alt="19774279" /></a>
  <a href="https://github.com/Jingle-Pan" title="Jingle-Pan (9 issues)"><img src="https://avatars.githubusercontent.com/u/75921710?v=4&amp;s=80" width="40" height="40" alt="Jingle-Pan" /></a>
  <a href="https://github.com/nullCode666" title="nullCode666 (9 issues)"><img src="https://avatars.githubusercontent.com/u/82703497?v=4&amp;s=80" width="40" height="40" alt="nullCode666" /></a>
  <a href="https://github.com/gyunlyun" title="gyunlyun (9 issues)"><img src="https://avatars.githubusercontent.com/u/111403418?v=4&amp;s=80" width="40" height="40" alt="gyunlyun" /></a>
  <a href="https://github.com/Arcticlyc" title="Arcticlyc (8 issues)"><img src="https://avatars.githubusercontent.com/u/94273547?v=4&amp;s=80" width="40" height="40" alt="Arcticlyc" /></a>
  <a href="https://github.com/TopMaps" title="TopMaps (8 issues)"><img src="https://avatars.githubusercontent.com/u/163238823?v=4&amp;s=80" width="40" height="40" alt="TopMaps" /></a>
  <a href="https://github.com/pansy1110" title="pansy1110 (8 issues)"><img src="https://avatars.githubusercontent.com/u/118948488?v=4&amp;s=80" width="40" height="40" alt="pansy1110" /></a>
  <a href="https://github.com/cry980285208" title="cry980285208 (8 issues)"><img src="https://avatars.githubusercontent.com/u/46832863?v=4&amp;s=80" width="40" height="40" alt="cry980285208" /></a>
  <a href="https://github.com/Toskysun" title="Toskysun (8 issues)"><img src="https://avatars.githubusercontent.com/u/88605463?v=4&amp;s=80" width="40" height="40" alt="Toskysun" /></a>
  <a href="https://github.com/Acheng97" title="Acheng97 (7 issues)"><img src="https://avatars.githubusercontent.com/u/65265814?v=4&amp;s=80" width="40" height="40" alt="Acheng97" /></a>
  <a href="https://github.com/lsdlh" title="lsdlh (7 issues)"><img src="https://avatars.githubusercontent.com/u/45959509?v=4&amp;s=80" width="40" height="40" alt="lsdlh" /></a>
  <a href="https://github.com/CAI5201314" title="CAI5201314 (7 issues)"><img src="https://avatars.githubusercontent.com/u/155355247?v=4&amp;s=80" width="40" height="40" alt="CAI5201314" /></a>
  <a href="https://github.com/86523553" title="86523553 (7 issues)"><img src="https://avatars.githubusercontent.com/u/72677878?v=4&amp;s=80" width="40" height="40" alt="86523553" /></a>
  <a href="https://github.com/Jesn" title="Jesn (7 issues)"><img src="https://avatars.githubusercontent.com/u/5728274?v=4&amp;s=80" width="40" height="40" alt="Jesn" /></a>
  <a href="https://github.com/zsh2517" title="zsh2517 (7 issues)"><img src="https://avatars.githubusercontent.com/u/30528671?v=4&amp;s=80" width="40" height="40" alt="zsh2517" /></a>
  <a href="https://github.com/CHINA-T" title="CHINA-T (7 issues)"><img src="https://avatars.githubusercontent.com/u/54023741?v=4&amp;s=80" width="40" height="40" alt="CHINA-T" /></a>
  <a href="https://github.com/1002753959" title="1002753959 (7 issues)"><img src="https://avatars.githubusercontent.com/u/31638769?v=4&amp;s=80" width="40" height="40" alt="1002753959" /></a>
  <a href="https://github.com/hyt65098631" title="hyt65098631 (6 issues)"><img src="https://avatars.githubusercontent.com/u/83172030?v=4&amp;s=80" width="40" height="40" alt="hyt65098631" /></a>
  <a href="https://github.com/yinsel" title="yinsel (6 issues)"><img src="https://avatars.githubusercontent.com/u/91541985?v=4&amp;s=80" width="40" height="40" alt="yinsel" /></a>
  <a href="https://github.com/xx299x" title="xx299x (6 issues)"><img src="https://avatars.githubusercontent.com/u/23482348?v=4&amp;s=80" width="40" height="40" alt="xx299x" /></a>
  <a href="https://github.com/wuewill" title="wuewill (6 issues)"><img src="https://avatars.githubusercontent.com/u/136971925?v=4&amp;s=80" width="40" height="40" alt="wuewill" /></a>
  <a href="https://github.com/jinshuqishi2019" title="jinshuqishi2019 (6 issues)"><img src="https://avatars.githubusercontent.com/u/57516638?v=4&amp;s=80" width="40" height="40" alt="jinshuqishi2019" /></a>
  <a href="https://github.com/TopChina" title="TopChina (6 issues)"><img src="https://avatars.githubusercontent.com/u/11971348?v=4&amp;s=80" width="40" height="40" alt="TopChina" /></a>
  <a href="https://github.com/Dawnnnnnn" title="Dawnnnnnn (6 issues)"><img src="https://avatars.githubusercontent.com/u/24506421?v=4&amp;s=80" width="40" height="40" alt="Dawnnnnnn" /></a>
  <a href="https://github.com/Mrqqeat" title="Mrqqeat (6 issues)"><img src="https://avatars.githubusercontent.com/u/12445017?v=4&amp;s=80" width="40" height="40" alt="Mrqqeat" /></a>
  <a href="https://github.com/Soujer" title="Soujer (6 issues)"><img src="https://avatars.githubusercontent.com/u/43666892?v=4&amp;s=80" width="40" height="40" alt="Soujer" /></a>
  <a href="https://github.com/fankuiz6" title="fankuiz6 (6 issues)"><img src="https://avatars.githubusercontent.com/u/156877102?v=4&amp;s=80" width="40" height="40" alt="fankuiz6" /></a>
  <a href="https://github.com/airline233" title="airline233 (6 issues)"><img src="https://avatars.githubusercontent.com/u/70080598?v=4&amp;s=80" width="40" height="40" alt="airline233" /></a>
</p>
