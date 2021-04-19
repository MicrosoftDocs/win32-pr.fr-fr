---
description: Répertorie les procédures de diagnostic à utiliser lors du dépannage de l’Assistant Ajout d’imprimante.
ms.assetid: 3ffee09b-e980-4a14-97ad-270444457dd7
title: Résolution des problèmes liés à l’Assistant Ajout d’imprimante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b0054758e3ec721598ad279a073a32862af368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521504"
---
# <a name="troubleshooting-the-add-printer-wizard"></a>Résolution des problèmes liés à l’Assistant Ajout d’imprimante

Assistant Ajout d’imprimante :

-   Utilise toujours le WS-Discovery UDP pour la découverte des appareils
-   Lance toujours une connexion HTTP ou HTTPs pour l’échange de métadonnées
-   Utilise parfois la découverte dirigée
-   Utilise parfois un canal sécurisé (HTTPs) pour l’échange de métadonnées

Les procédures de diagnostic suivantes doivent être utilisées (dans l’ordre) pour aider à identifier les problèmes liés à l’Assistant Ajout d’imprimante.

**Pour résoudre les problèmes liés à l’Assistant Ajout d’imprimante**

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
</dt> <dt>

[Dépannage des applications à l’aide de la découverte dirigée](troubleshooting-applications-using-directed-discovery.md)
</dt> </dl>

 

 



