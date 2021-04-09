---
description: Un ensemble d’outils de débogage reposant sur l’API WSDAPI (Web Services on Devices) est disponible dans le SDK Windows et le kit WDK (Windows Driver Kit).
ms.assetid: bd7efa8b-4f12-4b19-a7df-fa34c6a3444a
title: Outils de débogage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29965bb85ccfd2daf00612b09bb013ae170dddcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115707"
---
# <a name="debugging-tools"></a>Outils de débogage

Un ensemble d’outils de débogage reposant sur l’API WSDAPI (Web Services on Devices) est disponible dans le SDK Windows et le kit WDK (Windows Driver Kit). Ces outils peuvent être utilisés pour tester les fonctionnalités des applications personnalisées écrites sur WSDAPI, ou sur les périphériques et les clients écrits à l’aide d’autres piles Device Profile for Web Services (DPWS).

Les outils de débogage WSD (wsddebug \_host.exe) et client de débogage WSD (wsddebug \_client.exe) peuvent être utilisés pour inspecter les caractéristiques des ordinateurs hôtes ou des clients DPWS. Elles peuvent également être utilisées pour résoudre les problèmes de connectivité ou de configuration. Pour plus d’informations, consultez le [Guide de résolution des problèmes wsdapi](wsdapi-troubleshooting-guide.md). Ces outils sont uniquement disponibles dans le kit de développement logiciel (SDK). Les outils du kit de développement logiciel se trouvent dans le répertoire suivant : <Windows SDK Install Folder> \\ bin.

L' [outil wsdapi Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) peut être utilisé pour tester l’interopérabilité au niveau du transport ou au niveau du protocole SOAP (c’est-à-dire s’assurer que les messages sont correctement formés). Cet outil est disponible uniquement dans le kit WDK.

## <a name="the-wsd-debug-client"></a>Client de débogage WSD

Le client de débogage WSD (wsddebug \_client.exe) fournit une console interactive qui peut être utilisée pour envoyer et recevoir des messages WS-Discovery et pour obtenir des métadonnées. Il peut également être utilisé pour générer et consommer des messages de multidiffusion bruts.

Le client de débogage WSD fonctionne dans l’un des trois modes suivants : multidiffusion, Discovery et Metadata.



| Mode      | Description                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Multidiffusion | En mode de multidiffusion, le client de débogage WSD envoie et reçoit des messages de multidiffusion non mis en forme sur le port UDP 3702, comme défini dans WS-Discovery. L’utilisateur peut enregistrer ces messages SOAP dans un fichier texte et peut modifier et rediffuser les messages avec le client de débogage WSD.                                                                                                                                 |
| Découverte | En mode détection, le client de débogage WSD envoie et reçoit des messages WS-Discovery mis en forme. Il peut afficher les messages [Hello](hello-message.md), [Bye](bye-message.md), [messages ProbeMatches](probematches-message.md)et [ResolveMatches](resolvematches-message.md) reçus. Il peut envoyer des messages de [sonde](probe-message.md) via UDP ou http et [résoudre](resolve-message.md) les messages via UDP. |
| Métadonnées  | En plus d’implémenter toutes les fonctionnalités du mode de découverte, le mode métadonnées tente également de récupérer les métadonnées des appareils.                                                                                                                                                                                                                                                                    |



 

Pour plus d’informations, consultez [utilisation d’un hôte et d’un client génériques pour l’échange de métadonnées http](using-a-generic-host-and-client-for-http-metadata-exchange.md), [utilisation d’un hôte et d’un client génériques pour UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md)et [utilisation du client de débogage WSD pour vérifier le trafic de multidiffusion](using-wsddebug-client-to-verify-multicast-traffic.md).

## <a name="the-wsd-debug-host"></a>Hôte de débogage WSD

L’hôte de débogage WSD (wsddebug \_host.exe) fournit une console interactive utilisée pour annoncer l’hôte, répondre aux demandes des clients et imprimer les informations de diagnostic.

L’hôte de débogage WSD fonctionne dans l’un des deux modes suivants : découverte et métadonnées.



| Mode      | Description                                                                                                                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Découverte | En mode détection, l’hôte de débogage WSD imprime les messages mis en forme WS-Discovery. Il envoie également des messages de [salutation](hello-message.md) et de [Bye](bye-message.md) , et répond automatiquement aux messages de [sondage](probe-message.md) et de [résolution](resolve-message.md) . |
| Métadonnées  | En plus d’implémenter toutes les fonctionnalités du mode de découverte, le mode métadonnées publie un service de métadonnées et permet aux clients de se connecter et d’effectuer l’échange de métadonnées.                                                                                       |



 

Pour plus d’informations, consultez [utilisation d’un hôte et d’un client génériques pour l’échange de métadonnées http](using-a-generic-host-and-client-for-http-metadata-exchange.md) et [utilisation d’un hôte et d’un client génériques pour UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement d’applications WSD sur Windows](wsd-application-development-on-windows.md)
</dt> <dt>

[Outils de développement WSDAPI](wsdapi-development-tools.md)
</dt> <dt>

[Guide de résolution des problèmes WSDAPI](wsdapi-troubleshooting-guide.md)
</dt> </dl>

 

 



