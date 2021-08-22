---
description: Cette rubrique décrit la prise en charge des appareils multirésidents dans WSDAPI et fournit des recommandations d’implémentation pour les développeurs de clients et d’appareils.
ms.assetid: d30ed536-d477-4f50-8c80-aacc35f948b9
title: Implémentation d’un périphérique WSD multirésident
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ac83b0fe3b951e02e77ef9efc6241ce5a7e1780106b1e85e4f00b987bbbe05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991739"
---
# <a name="implementing-a-multi-homed-wsd-device"></a>Implémentation d’un périphérique WSD multirésident

[WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) et le [profil de périphériques pour les services Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) ne décrivent pas l’implémentation des appareils multirésidents. Cette rubrique décrit la prise en charge des appareils multirésidents dans WSDAPI et fournit des recommandations d’implémentation pour les développeurs de clients et d’appareils. Dans cette rubrique, on suppose que les messages de découverte sont envoyés sur IPv4 et IPv6 (le cas échéant) avec le même ID de message et les mêmes informations de séquencement d’application.

## <a name="discovery-in-a-multi-homed-environment"></a>Découverte dans un environnement multirésident

Comme mentionné dans la section [Hello](hello-message.md) et [XAddrs](xaddr-validation-rules.md) de la [fonctionnalité WS-Discovery supplémentaire](additional-ws-discovery-functionality.md), wsdapi ne fournit jamais XAddrs dans un message Hello. Cela signifie que le même message Hello peut être envoyé sur toutes les interfaces réseau avec le même ID de message et les mêmes informations de séquencement d’application. Il est ainsi plus facile pour la détection de collision client d’ignorer plusieurs messages de salutation du même appareil lorsqu’un client et l’appareil partagent plusieurs sous-réseaux.

Étant donné que les [XAddrs](xaddr-validation-rules.md) ne sont pas envoyés dans le message [Hello](hello-message.md) , les implémentations clientes doivent envoyer un message de [résolution](resolve-message.md) pour obtenir l’adresse d’appareil appropriée. La résolution doit être envoyée sur toutes les interfaces clientes avec le même ID de message, et l’appareil doit filtrer les messages en double en fonction des besoins. L’utilisation du même ID de message pour le message de résolution permet à l’appareil de choisir une interface préférée pour communiquer avec les clients, si nécessaire.

Lors de l’envoi d’un message [ResolveMatch](resolvematches-message.md) , un appareil doit fournir des [XAddrs](xaddr-validation-rules.md) qui se rapportent à l’interface réseau sur laquelle il diffuse le message. Cette pratique permet d’éviter plusieurs tentatives de connexion au client et une logique de nouvelle tentative compliquée.

## <a name="metadata-exchange-in-a-multi-homed-environment"></a>Échange de métadonnées dans un environnement multirésident

Il est plus difficile d’implémenter l’échange de métadonnées dans un environnement multirésident que d’implémenter la découverte en raison du contrôle de version des métadonnées. Si un client demande des métadonnées sur plusieurs interfaces, le client peut recevoir plusieurs messages [GetResponse](getresponse--metadata-exchange--message.md) sur différentes interfaces. Ces messages GetResponse peuvent contenir différentes sections de métadonnées de **relation** avec la même version de métadonnées. Cela réduit la valeur du numéro de version des métadonnées.

Il existe une autre approche, où un seul message [GetResponse](getresponse--metadata-exchange--message.md) est envoyé en réponse à toutes les adresses du service. L’inconvénient de cette méthode est que des informations privées, telles que la topologie de réseaux indirectement accessibles, peuvent être divulguées.

sur Windows Vista, les métadonnées fournies par WSDAPI contiennent uniquement les adresses valides pour l’interface sur laquelle la demande de métadonnées a été reçue.

 

 



