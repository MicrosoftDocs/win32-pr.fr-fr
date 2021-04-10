---
description: Répertorie les procédures de diagnostic à utiliser lors du dépannage de l’Explorateur réseau.
ms.assetid: 56052a82-d3a6-4749-9010-6796558dcb17
title: Résolution des problèmes de l’Explorateur réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09afe7acbcb20d706c8645d84c68014b0e33d799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951167"
---
# <a name="troubleshooting-the-network-explorer"></a>Résolution des problèmes de l’Explorateur réseau

Explorateur réseau :

-   Utilise toujours le WS-Discovery UDP pour la découverte des appareils
-   Lance toujours une connexion HTTP ou HTTPs pour l’échange de métadonnées
-   Utilise parfois un canal sécurisé (HTTPs) pour l’échange de métadonnées

Les procédures de diagnostic suivantes doivent être utilisées (dans l’ordre) pour aider à identifier les problèmes liés à l’Explorateur réseau.

**Pour résoudre les problèmes de l’Explorateur réseau**

1.  [Inspectez les paramètres de l’adaptateur et du pare-feu](inspecting-adapter-and-firewall-settings.md).
2.  [Utilisez un hôte et un client génériques pour UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Utilisez le client de débogage WSD pour vérifier le trafic de multidiffusion](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Inspectez les suivis réseau pour le service WS-Discovery UDP](inspecting-network-traces-for-udp-ws-discovery.md).
5.  [Utilisez un hôte et un client génériques pour l’échange de métadonnées http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
6.  [Utilisez la journalisation WinHTTP pour vérifier le trafic d’extraction](using-winhttp-logging-to-verify-get-traffic.md).
7.  [Inspectez les traces réseau pour l’échange de métadonnées http](inspecting-network-traces-for-http-metadata-exchange.md).

L’Explorateur réseau utilise la [détection de fonction](/previous-versions/windows/desktop/fundisc/fd-portal) pour énumérer les périphériques réseau. Pour plus d’informations sur le dépannage, consultez [Dépannage des clients de découverte de fonctions](troubleshooting-function-discovery-clients.md).

Si la source du problème ne peut pas être identifiée à l’aide des procédures de diagnostic ci-dessus, suivez les instructions de la procédure d' [activation du suivi wsdapi](enabling-wsdapi-tracing.md) et contactez le support Microsoft.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes de Prise en main avec WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Résolution des problèmes des clients de découverte des fonctions](troubleshooting-function-discovery-clients.md)
</dt> </dl>

 

 
