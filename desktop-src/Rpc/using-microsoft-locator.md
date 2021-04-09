---
title: Utilisation de Microsoft Locator
description: Le localisateur Microsoft est le service de nom par défaut. La bibliothèque Runtime RPC l’utilise pour rechercher des programmes serveur sur les systèmes hôtes serveur.
ms.assetid: 8481de50-4e72-432d-aef7-524f18f5c9c4
keywords:
- Appel de procédure distante RPC, tâches, à l’aide de Microsoft Locator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 236dce18b9286150581af925935222f3c9b3f862
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840021"
---
# <a name="using-microsoft-locator"></a>Utilisation de Microsoft Locator

Le localisateur Microsoft est le service de nom par défaut. La bibliothèque Runtime RPC l’utilise pour rechercher des programmes serveur sur les systèmes hôtes serveur.

**Remarque**    Le localisateur Microsoft RPC n’est pas pris en charge dans Windows Vista et les systèmes d’exploitation ultérieurs.

Avant Windows 2000, le localisateur Microsoft ne fournissait pas d’entrées de service de noms persistantes. Toutes les entrées dans le service de noms ont été stockées dans un cache mémoire sur l’ordinateur hôte du programme serveur. Le localisateur a utilisé un mécanisme de diffusion pour découvrir l’emplacement des serveurs demandés par les clients. Chaque fois que le système hôte s’arrête, toutes les entrées de service de noms ont été perdues.

Depuis la sortie de Windows 2000, Microsoft Locator prend désormais en charge les entrées de service de noms persistantes. Pour ce faire, le système utilise un service d’annuaire distribué pour stocker les entrées de service de noms. Ce mécanisme présente plusieurs avantages :

-   **Persistance.** Les programmes serveur ne sont plus nécessaires pour exporter leurs informations de liaison vers le service de noms à chaque démarrage. Le service de noms stocke désormais les informations jusqu’à ce que le programme serveur de l’administrateur réseau le supprime explicitement.
-   **Performance.** En éliminant la majorité de la diffusion pour les entrées de service de nom, le localisateur réduit le trafic réseau. Il recherche également les entrées de service de nom plus rapidement.
-   **Interopérabilité inter-domaines.** Les clients sont désormais en mesure d’effectuer des requêtes de service de noms sur plusieurs domaines.

Les versions actuelles de Microsoft Locator sont à compatibilité descendante. Par exemple, un système hôte serveur exécutant le localisateur fourni avec Windows 2000 peut fonctionner correctement sur un réseau qui contient des systèmes hôtes serveur exécutant le localisateur fourni avec Windows NT 4,0.

Avec la sortie de Windows 2000, Microsoft Locator prend désormais en charge les entrées de service de nom pour les groupes d’utilisateurs. Il offre également la possibilité de créer des profils utilisateur.

En outre, la version actuelle de Microsoft Locator prend en charge l’utilisation de listes de Access Control dans les entrées de service de nom. Cette capacité améliore la sécurité du réseau.

La prise en charge de Plug-and-Play est désormais incluse dans le localisateur Microsoft. Par conséquent, il peut gérer en toute transparence les événements de Plug-and-Play, tels que les modifications de domaine. Pour plus d’informations, consultez [**RpcNsBindingExportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexportpnpa) et [**RpcNsBindingUnexportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexportpnpa).

 

 




