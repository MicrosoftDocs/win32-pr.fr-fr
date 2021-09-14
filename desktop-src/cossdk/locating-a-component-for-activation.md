---
description: Recherche d’un composant pour l’activation
ms.assetid: 2ba9484a-c646-4a35-8b32-268fe7a9520f
title: Recherche d’un composant pour l’activation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bd90068c34469d61af36e6de8c409cb02e078c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127310998"
---
# <a name="locating-a-component-for-activation"></a>Recherche d’un composant pour l’activation

Lorsque COM+ a localisé la partition correcte (par le biais de l’ensemble de partitions par défaut de l’identité de l’utilisateur, d’un moniker de partition ou de l’ID de partition dans le contexte de l’objet), COM + doit localiser le composant approprié dans cette partition. L’illustration suivante montre comment un composant est trouvé et activé lorsque ce composant réside dans une partition.

> [!Note]  
> Avant toute activation de composant, COM+ effectue une validation pour vérifier que l’identité de l’utilisateur qui tente d’activer le composant dispose des droits d’accès à l’ensemble de partitions dans lequel le composant réside.

 

![Diagramme qui montre une arborescence de résolution des problèmes pour localiser un composant en vue de son activation.](images/26c26a37-ec95-4f9f-aa59-4d84a7bb0fa3.png)

L’illustration ci-dessus montre les éléments suivants :

-   Si le composant appelé réside dans une partition et qu’il se trouve dans la même application que le composant appelant, le composant est activé que le composant appelé soit marqué comme public ou privé.
-   Si le composant appelé réside dans une partition mais n’existe pas dans la même application que le composant appelant, COM+ vérifie si le composant est marqué comme public. Si aucune version publique n’est trouvée, COM+ recherche une version publique du composant dans la partition globale. Si aucune version publique du composant n’est trouvée dans la partition globale ou si l’identité de l’utilisateur n’a pas de droits sur la partition, l’activation échoue.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recherche de partitions pendant l’activation](locating-partitions-during-activation.md)
</dt> </dl>

 

 



