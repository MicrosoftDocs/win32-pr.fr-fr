---
description: Cette section examine une partie d’un exemple d’application qui fonctionne sur le réseau très lentement. Tout au long de cette section, les modifications sont apportées au code initial pour améliorer ses performances.
ms.assetid: 29b96540-1b45-46b7-871a-e728aa50ad24
title: Amélioration d’une application lente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae5bbec57791155852a41b1413e0d863f8704c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516872"
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

[Applications Windows Sockets hautes performances](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



