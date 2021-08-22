---
title: Ce qui se passe lors d’une requête
description: Cette section décrit comment le réseau gère la requête lorsqu’un client 32 bits recherche un nom dans son propre domaine.
ms.assetid: a8a88743-a245-4258-af05-9261c214ab50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7377df4ced562bc166fedbf489724a2a4a042855391db45841b5de5cf5af906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010427"
---
# <a name="what-happens-during-a-query"></a>Ce qui se passe lors d’une requête

Cette section décrit comment le réseau gère la requête lorsqu’un client 32 bits recherche un nom dans son propre domaine.

Lorsque votre application cliente appelle [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), le localisateur résidant sur votre ordinateur client tente de répondre à cette demande. S’il n’y a rien dans le cache, il transfère la demande par RPC à un localisateur maître. Si le localisateur maître ne trouve rien dans son cache, il envoie la demande à tous les ordinateurs du domaine à l’aide d’une diffusion de l’emplacement de messagerie. En cas de correspondance, le localisateur sur chaque ordinateur répondra à l’aide d’un emplacement de messagerie dirigée. (Par exemple, si un processus sur cet ordinateur a exporté l’interface.) Les réponses sont assemblées et le RPC est terminé à partir du localisateur de processus du client, qui répondra au processus client lui-même.

Dans un domaine, le localisateur du client recherche un localisateur maître aux emplacements suivants :

-   Sur le contrôleur de domaine principal
-   Sur chaque contrôleur de domaine de sauvegarde

Si aucune correspondance n’est trouvée, le localisateur client déclare lui-même pour être le localisateur maître. Ainsi, les requêtes sont diffusées si elles ne peuvent pas être satisfaites localement.

Dans un groupe de travail, le localisateur client conserve un cache des ordinateurs dont les localisateurs ont une diffusion. Elle utilise celle qui a exécuté le plus long que le localisateur maître. Si cet ordinateur n’est pas disponible, l’ordinateur de diffusion suivant, le plus long est utilisé, et ainsi de suite. Si le client a besoin d’un localisateur maître et que le cache est vide, il réapprovisionne le cache en envoyant une diffusion d’emplacement de courrier spéciale qui demande à des localisateurs principaux de répondre. S’il n’y a aucune réponse, le localisateur du client se déclare être le localisateur maître et diffuse des requêtes s’ils ne peuvent pas être satisfaits localement.

Cela change si votre application cliente est un programme 16 bits ou MS-DOS. Dans ce cas, aucun localisateur n’est en cours d’exécution sur l’ordinateur client et Rpcns1.dll ou Rpcnslm. RPC contient le code permettant de trouver un localisateur maître. Toutes les demandes sont transférées directement au localisateur maître.

Ces instructions sont valides pour les noms dans le domaine du client, tels que les noms de « /.:/ » entryname». Si le client demande un nom dans un autre domaine par le biais de l’utilisation de « /.../DOMAIN/entryname ; », le localisateur du client transfère la demande au domaine spécifié, qui la diffuse si elle n’a pas la réponse. Si le domaine est en panne ou est en fait un groupe de travail, la demande échoue.

> [!Note]  
> N’oubliez pas les points suivants lorsque vous utilisez des entrées dans le service de noms :

 

-   Un client ne peut pas utiliser la syntaxe « /.../DOMAIN/entryname » pour rechercher une entrée dans son propre domaine. Utilisez la syntaxe «/.:/ entryname». Toutefois, vous pouvez utiliser « /.../DOMAIN/entryname » pour rechercher une entrée dans un autre domaine.
-   Le nom de domaine dans « /.../DOMAIN/entryname » doit être en majuscules. Lorsque vous recherchez une correspondance, le localisateur respecte la casse.
-   Les noms d’entrée de localisateur respectent également la casse, mais ils n’ont pas besoin d’être en majuscules.
-   Quand le client utilise le « /.:/ » entryname», le localisateur ne recherche pas d’entrées dans d’autres domaines, même s’ils ont une relation d’approbation avec le domaine d’ouverture de session.
-   Les diffusions ne traversent pas les segments de réseau local (par exemple, les sous-réseaux). Ainsi, l’utilité du localisateur est limitée dans une organisation avec plusieurs sous-réseaux.

 

 




