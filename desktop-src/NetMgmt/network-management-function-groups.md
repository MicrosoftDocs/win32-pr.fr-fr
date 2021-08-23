---
title: Groupes de fonctions de gestion de réseau
description: Les fonctions de gestion de réseau peuvent être réparties dans les groupes suivants.
ms.assetid: 4b5d3554-f81a-4ecf-bf31-ee4753509f38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e49a8c45c59031a12653f5cb863fef320a33c93bc60cabdd4cd6fb4aece9dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012507"
---
# <a name="network-management-function-groups"></a>Groupes de fonctions de gestion de réseau

Les fonctions de gestion de réseau peuvent être réparties dans les groupes suivants :

-   [Fonctions d’alerte](alert-functions.md)
-   [ApiBuffer, fonctions](apibuffer-functions.md)
-   [Fonctions du service d’annuaire](directory-service-functions.md)
-   [Fonctions de système de fichiers DFS (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions)
-   [Fonctions d’extraction](get-functions.md)
-   [Fonctions de groupe](group-functions.md)
-   [Fonctions de groupe locales](local-group-functions.md)
-   [Fonctions de message](message-functions.md)
-   [Fonctions Netfile](netfile-functions.md)
-   [Fonctions utilitaires distantes](remote-utility-functions.md)
-   [Fonctions de planification](schedule-functions.md)
-   [Fonctions du serveur](server-functions.md)
-   [Fonctions de transport serveur et station de travail](server-and-workstation-transport-functions.md)
-   [Fonctions de session](session-functions.md)
-   [Fonctions de partage](share-functions.md)
-   [Fonctions statistiques](/windows/desktop/NetShare/statistics-functions)
-   [Utiliser les fonctions](use-functions.md)
-   [Fonctions utilisateur](user-functions.md)
-   [Fonctions modales utilisateur](user-modal-functions.md)
-   [Fonctions utilisateur de station de travail et de station de travail](workstation-and-workstation-user-functions.md)

Si vous programmez pour Active Directory, vous pourrez peut-être appeler certaines méthodes d’interface ADSI pour obtenir les mêmes fonctionnalités que celles que vous pouvez obtenir en appelant certaines fonctions de gestion de réseau. Pour plus d’informations, consultez [mappage des interfaces ADSI avec les fonctions de gestion de réseau](mapping-adsi-interfaces-to-the-network-management-functions.md).

Le système fournit également un ensemble de fonctions réseau indépendantes du réseau ([fonctions WNET](/windows/desktop/WNet/wnet-functions)) qui permettent aux fonctions réseau de fonctionner sur différents produits de fournisseurs de réseau. Si votre application peut être convertie pour utiliser une fonction WNet, vous devez effectuer la conversion. Il y a des raisons d’effectuer la modification :

-   Les fonctions WNet sont indépendantes du réseau, tandis que les fonctions de gestion de réseau fonctionnent uniquement sur les réseaux Microsoft.
-   Certaines fonctions peuvent ne pas être prises en charge dans les futures versions des systèmes d’exploitation Microsoft si elles ont été remplacées. Microsoft ne prévoit pas de supprimer des fonctions spécifiques, sauf si des fonctionnalités équivalentes ou supérieures sont disponibles.

 

 