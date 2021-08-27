---
description: Cette section examine une partie d’un exemple d’application qui fonctionne sur le réseau très lentement. Tout au long de cette section, les modifications sont apportées au code initial pour améliorer ses performances.
ms.assetid: 29b96540-1b45-46b7-871a-e728aa50ad24
title: Amélioration d’une application lente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff8f996267328805dc120d39218784a08383fb68ae9f6927e8983b6e1bec2d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097889"
---
# <a name="improving-a-slow-application"></a>Amélioration d’une application lente

Cette section examine une partie d’un exemple d’application qui fonctionne sur le réseau très lentement. Tout au long de cette section, les modifications sont apportées au code initial pour améliorer ses performances.

L’exemple factice est la partie mise à jour pour un jeu appelé Life. L’application est écrite de telle sorte que le client effectue les calculs pour les mises à jour et les envoie au serveur. Le serveur affiche ensuite le champ vie résultante. La sortie du client est un flux d’octets, regroupés en trois (triples), chaque triplet représentant une seule cellule à mettre à jour. Les octets de l’triplet représentent respectivement la ligne, la colonne et la valeur de la cellule.

Cet exemple commence comme une application intentionnellement médiocre, qui fournit la ligne de base à partir de laquelle les améliorations des performances peuvent être illustrées. À partir de là, le code est amélioré trois fois pour résoudre différents problèmes qui affectent les performances. Ces exemples doivent être lus dans l’ordre, car chaque itération s’améliore sur la version précédente.

Le code de base, ainsi que les révisions qui améliorent ce code, sont les suivantes :

-   [Version de référence : une application très médiocre](the-baseline-version-a-very-poor-performing-application-2.md)
-   [Révision 1 : nettoyage évident](revision-1-cleaning-up-the-obvious-2.md)
-   [Révision 2 : reconception pour des connexions moins nombreuses](revision-2-redesigning-for-fewer-connects-2.md)
-   [Révision 3 : envoi de bloc compressé](revision-3-compressed-block-send-2.md)
-   [Améliorations futures](future-improvements-2.md)

> [!WARNING]
> Les premiers exemples de l’application offrent des performances intentionnellement médiocres, afin d’illustrer les améliorations de performances possibles avec les modifications apportées au code. N’utilisez pas ces exemples de code dans votre application. ils sont fournis à titre d’illustration uniquement.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications de sockets Windows hautes performances](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



