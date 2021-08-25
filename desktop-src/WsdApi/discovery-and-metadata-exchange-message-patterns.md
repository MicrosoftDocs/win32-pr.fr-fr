---
description: Profil d’appareil pour les hôtes de services Web (DPWS) et les clients communiquent sur le réseau à l’aide d’une série de messages SOAP sur UDP et HTTP.
ms.assetid: 52282990-d993-4034-a791-2ee7c9c1663d
title: détection et schémas de Message Exchange de métadonnées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1b41267e86358a9d6e263f4bc8971632f1061eb1c94d1e64cc76d65020ce255
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856792"
---
# <a name="discovery-and-metadata-exchange-message-patterns"></a>détection et schémas de Message Exchange de métadonnées

Profil d’appareil pour les hôtes de services Web (DPWS) et les clients communiquent sur le réseau à l’aide d’une série de messages SOAP sur UDP et HTTP.

Le diagramme suivant présente une vue d’ensemble du trafic UDP et HTTP attendu entre un hôte et un client DPWS.

![Diagramme montrant le trafic UDP et HTTP entre un hôte et un client DPWS.](images/ws-discovery-and-metadata-exchange-message-patterns.png)

Les messages [Hello](hello-message.md), [Bye](bye-message.md), [Probe](probe-message.md), [Resolve](resolve-message.md)et [obtient](get--metadata-exchange--http-request-and-message.md) sont tous générés sans sollicitation du réseau ; ces messages sont utilisés pour annoncer l’état de l’appareil ou pour émettre une demande de recherche. Les messages [messages ProbeMatches](probematches-message.md), [ResolveMatches](resolvematches-message.md)et [GetResponse](getresponse--metadata-exchange--message.md) sont générés en réponse à des messages de sondage, de résolution et de récupération.

Les messages [Hello](hello-message.md), [Bye](bye-message.md), [Resolve](resolve-message.md)et [ResolveMatches](resolvematches-message.md) sont toujours exécutés sur UDP. De même, les messages de métadonnées d' [extraction](get--metadata-exchange--http-request-and-message.md) et [GetResponse](getresponse--metadata-exchange--message.md) sont toujours exécutés sur http ou HTTPS. Les messages [Probe](probe-message.md) et [messages ProbeMatches](probematches-message.md) sont normalement transmis via UDP, mais ils ont lieu sur une connexion http ou https dans un scénario de découverte dirigée. Pour plus d’informations sur les modèles de message de découverte dirigée, consultez [Dépannage des applications à l’aide de la découverte dirigée](troubleshooting-applications-using-directed-discovery.md).

La liste suivante indique la séquence typique de messages sur le réseau. Tous les messages ne sont pas obligatoires.

1.  [Bonjour](hello-message.md)
2.  [Sonde](probe-message.md)
3.  [Messages ProbeMatches](probematches-message.md)
4.  [Résoudre](resolve-message.md)
5.  [ResolveMatches](resolvematches-message.md)
6.  [Obtenir](get--metadata-exchange--http-request-and-message.md) (demande d’échange de métadonnées)
7.  [GetResponse](getresponse--metadata-exchange--message.md)
8.  [Adieu](bye-message.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des services Web sur les appareils](about-web-services-for-devices.md)
</dt> </dl>

 

 



