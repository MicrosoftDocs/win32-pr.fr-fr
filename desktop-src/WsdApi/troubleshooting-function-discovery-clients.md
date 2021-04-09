---
description: Répertorie les procédures de diagnostic à utiliser lors du dépannage des clients de découverte de fonctions.
ms.assetid: e488882a-fadd-4150-89ef-b958c3df34c6
title: Résolution des problèmes des clients de découverte des fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a44c17b269a604efa1f5f999dff22211cee24f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753668"
---
# <a name="troubleshooting-function-discovery-clients"></a>Résolution des problèmes des clients de découverte des fonctions

Clients de découverte de fonction :

-   Toujours utiliser les WS-Discovery UDP pour la découverte des appareils
-   Toujours initier des connexions HTTP ou HTTPs pour l’échange de métadonnées
-   Utilisez parfois la découverte dirigée
-   Utilisez parfois un canal sécurisé (HTTPs) pour l’échange de métadonnées

La liste suivante présente la séquence classique des messages envoyés et reçus par les clients de détection de fonction. Tous les messages ne sont pas obligatoires.

1.  Le client envoie un message de [sondage](probe-message.md) pour détecter les appareils et les services. Si le client utilise la découverte dirigée, ce message est envoyé via HTTP ou HTTPs ; dans le cas contraire, le message est envoyé par la multidiffusion UDP au port 3702.
2.  Le client reçoit des messages [messages ProbeMatches](probematches-message.md) à partir des appareils ou services correspondants. Les messages de découverte dirigée sont envoyés via HTTP ou HTTPs. dans le cas contraire, ces messages sont envoyés par la monodiffusion UDP et proviennent du port 3702.
3.  Si aucun XAddrs n’a été inclus dans le message messages ProbeMatches, le client enverra un message de [résolution](resolve-message.md) par multidiffusion UDP au port 3702.
4.  Si un message de [résolution](resolve-message.md) a été envoyé, le client reçoit un message [ResolveMatches](resolvematches-message.md) à partir de services correspondants. Ce message est envoyé par la monodiffusion UDP du port 3702 vers le port d’origine du message de résolution.
5.  Le client envoie un message d' [extraction](get--metadata-exchange--http-request-and-message.md) pour demander des métadonnées à partir de l’appareil ou du service. Ce message est envoyé par HTTP ou HTTPs.
6.  Le client reçoit un message [GetResponse](getresponse--metadata-exchange--message.md) avec les métadonnées du périphérique ou du service. Ce message est envoyé par HTTP ou HTTPs.

Les procédures de diagnostic suivantes doivent être utilisées (dans l’ordre) pour aider à identifier les problèmes liés à un client de découverte de fonctions.

**Pour dépanner un client de découverte de fonctions**

1.  Si la découverte dirigée est utilisée, [résolvez les problèmes de détection dirigée](troubleshooting-applications-using-directed-discovery.md).
2.  [Inspectez les paramètres de l’adaptateur et du pare-feu](inspecting-adapter-and-firewall-settings.md).
3.  [Utilisez un hôte et un client génériques pour UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
4.  [Utilisez le client de débogage WSD pour vérifier le trafic de multidiffusion](using-wsddebug-client-to-verify-multicast-traffic.md).
5.  [Inspectez les suivis réseau pour le service WS-Discovery UDP](inspecting-network-traces-for-udp-ws-discovery.md).
6.  [Utilisez un hôte et un client génériques pour l’échange de métadonnées http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
7.  [Utilisez la journalisation WinHTTP pour vérifier le trafic d’extraction](using-winhttp-logging-to-verify-get-traffic.md).
8.  [Inspectez les traces réseau pour l’échange de métadonnées http](inspecting-network-traces-for-http-metadata-exchange.md).

Si la source du problème ne peut pas être identifiée à l’aide des procédures de diagnostic ci-dessus, suivez les instructions de la procédure d' [activation du suivi wsdapi](enabling-wsdapi-tracing.md) et contactez le support Microsoft.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes de Prise en main avec WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



