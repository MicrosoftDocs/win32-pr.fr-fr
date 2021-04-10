---
description: Moniteur réseau est un composant de Microsoft Systems Management Server (SMS) utilisé pour détecter et résoudre les problèmes sur les réseaux locaux, les réseaux étendus et les liaisons série qui exécutent le serveur d’accès à distance Microsoft (RAS).
ms.assetid: bd273439-daa2-4263-8f12-28ec988beea0
title: À propos de Moniteur réseau 2,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f447f4763e0c73dc0dcac4cf719a0bad4b61f073
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034480"
---
# <a name="about-network-monitor-21"></a>À propos de Moniteur réseau 2,1

Moniteur réseau est un composant de Microsoft Systems Management Server (SMS) utilisé pour détecter et résoudre les problèmes sur les réseaux locaux, les réseaux étendus et les liaisons série qui exécutent le serveur d’accès à distance Microsoft (RAS). Moniteur réseau fournit une analyse de données réseau après capture.

Dans l’analyse après capture, le trafic réseau est enregistré dans un fichier de capture propriétaire, afin que les données capturées puissent être analysées ultérieurement. Dans ce cas, l’analyse peut se présenter sous la forme d' [*analyseurs*](p.md) de protocole qui sélectionnent des types de trames réseau spécifiques et affichent les données de trame dans l’interface utilisateur Moniteur réseau ; ou l’analyse peut être sous la forme d' [*experts*](e.md) qui examinent les données réseau et affichent un rapport (les experts peuvent également manipuler les données réseau).

Moniteur réseau fournit les types de fonctionnalités suivants :

-   Capture les données réseau en mode en temps réel ou différé.
-   Fournit des fonctionnalités de filtrage lors de la capture de données.
-   Utilise des experts et des analyseurs pour une analyse détaillée de la capture.

Pour plus d’informations sur les fonctionnalités de Moniteur réseau, consultez :

-   [Architecture de l’analyseur et de l’expert](expert-and-parser-architecture.md)
-   [Experts](experts.md)
-   [Analyseurs](parsers.md)
-   [Fournisseurs de paquets réseau](network-packet-providers.md)
-   [Objets BLOB Moniteur réseau](network-monitor-blobs.md)
-   [Page de référence des événements](event-reference-page.md)
-   [Filtres de capture](capture-filters.md)

**Windows Vista :** Moniteur réseau 2,1 et versions antérieures ne sont pas pris en charge sur cette plateforme.

 

 



