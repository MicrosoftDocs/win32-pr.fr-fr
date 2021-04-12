---
description: L’activation JIT COM+ fait essentiellement un compromis entre les clients gourmands et les serveurs gourmands afin d’obtenir des performances optimales. Les clients sont en mesure de conserver les références d’objets, tandis que les serveurs peuvent mieux gérer l’utilisation de la mémoire.
ms.assetid: 125d39f5-af38-4a87-a649-2f77a3e77c27
title: Mise en pool d’objets et activation JIT COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8042d838aaaae62eace6f61a8fe1aa820e17d079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393223"
---
# <a name="object-pooling-and-com-jit-activation"></a>Mise en pool d’objets et activation JIT COM+

L’activation JIT COM+ fait essentiellement un compromis entre les clients gourmands et les serveurs gourmands afin d’obtenir des performances optimales. Les clients sont en mesure de conserver les références d’objets, tandis que les serveurs peuvent mieux gérer l’utilisation de la mémoire.

Vous pouvez affiner cette amélioration en utilisant le [regroupement d’objets com+](com--object-pooling.md). En regroupant les objets qui sont activés juste-à-temps, vous pouvez dédier une certaine quantité de mémoire pour contenir un certain nombre d’objets actifs en mémoire, prêts à être réutilisés immédiatement. Cela est plus clair lorsque les objets sont coûteux à créer, comme dans le cas où ils détiennent plusieurs ressources.

En regroupant les objets activés juste-à-temps de cette manière, vous pouvez bénéficier des avantages suivants :

-   Délais de réactivation d’objets accélérés.
-   Réutilisation des ressources coûteuses que les objets détiennent.
-   Administration plus précise de la mémoire et de l’utilisation des ressources pour les objets regroupés.
-   Rétention de la flexibilité administrative afin que votre application puisse être mise à l’échelle pour utiliser les ressources disponibles et s’adapter à l’évolution des besoins en performances.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts d’activation juste-à-temps de COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Mise en pool d’objets COM+](com--object-pooling.md)
</dt> <dt>

[Activation de l’activation JIT pour un composant](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Transactions et activation JIT COM+](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



