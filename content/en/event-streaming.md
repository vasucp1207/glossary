---
título: Transmissão de eventos
estado: Concluído
categoria: conceito
---

## O que é isso

O streaming de eventos é uma abordagem em que o software envia dados de eventos de um aplicativo para outro para comunicar continuamente o que eles estão fazendo.
Imagine um serviço transmitindo tudo o que faz para todos os outros serviços.
Cada atividade realizada por um serviço é chamada de evento, daí o fluxo de eventos.
Por exemplo, a NASDAQ recebe atualizações sobre preços de ações e commodities a cada segundo.
Se você tivesse um aplicativo que monitorasse um conjunto específico de ações, gostaria de receber essas informações quase em tempo real.
Yahoo! O Finance fornece uma [API](https://glossary.cncf.io/application-programming-interface/) que extrai do NASDAQ e envia (ou transmite) as informações (ou eventos) de seu aplicativo para qualquer aplicativo que se inscreva nele .
Os dados enviados, bem como as alterações nesses dados (preços das ações) são os eventos, enquanto o processo de entregá-los a um aplicativo é o fluxo de eventos.

## Problema que resolve

Tradicionalmente, o Yahoo! Finanças usaria solicitações TCP únicas.
Isso seria muito ineficiente, pois exigiria que uma conexão fosse criada para cada evento.
À medida que os dados se tornam mais em tempo real por natureza, dimensionar essa solução se torna ineficiente.
Abrir uma conexão uma vez e permitir que os eventos fluam é ideal para coleta em tempo real.
A quantidade de dados sendo gerados está crescendo exponencialmente e com isso, o estado dos dados está em constante fluxo. Desenvolvedores e usuários precisam ver esses dados quase em tempo real.

## Como isso ajuda

A transmissão de eventos permite que as alterações de dados sejam comunicadas da fonte para o receptor.
Em vez de esperar que os serviços solicitem informações, o serviço transmite continuamente todos os seus eventos (ou atividades).
Não está preocupado com o que acontece com a informação.
Ele apenas faz o que precisa fazer e o transmite, permanecendo completamente independente de qualquer outro serviço.