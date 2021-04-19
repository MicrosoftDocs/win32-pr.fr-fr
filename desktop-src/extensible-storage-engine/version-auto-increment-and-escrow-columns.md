---
description: 'En savoir plus sur les colonnes : version, incrément automatique et tiers de confiance'
title: Colonnes version, incrémentation automatique et tiers de confiance
TOCTitle: Version, Auto-Increment and Escrow Columns
ms:assetid: b12724a4-6846-49a7-9223-43895f91427e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294059(v=EXCHG.10)
ms:contentKeyID: 32765674
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: e5966990a51e87b90946416161e20d677116f8c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515881"
---
# <a name="version-auto-increment-and-escrow-columns"></a>Colonnes version, incrémentation automatique et tiers de confiance


_**S’applique à :** Windows | Serveur Windows_

## <a name="version-auto-increment-and-escrow-columns"></a>Colonnes version, incrémentation automatique et tiers de confiance

ESE offre des types de colonne de mise à jour de version, d’incrémentation automatique et de dépôt qui ont des capacités particulières. Les options de colonne définies dans le membre **Grbit** de la structure [JET_COLUMNDEF](./jet-columndef-structure.md) utilisée dans l’appel à [JetAddColumn](./jetaddcolumn-function.md) indiquent si la colonne est l’un des types spécialisés indiqués ici.

### <a name="version-jet_bitcolumnversion"></a>Version (JET_bitColumnVersion)

L’option de colonne version, appliquée uniquement aux colonnes JET_coltypLong, indique que la colonne contient des informations de version sur l’enregistrement qui peuvent être utilisées pour déterminer si une copie en mémoire d’un enregistrement donné doit être actualisée. Les colonnes de version sont automatiquement incrémentées par ESE lorsque la colonne est modifiée par l’application via [JetUpdate](./jetupdate-function.md).

### <a name="auto-increment-jet_bitcolumnautoincrement"></a>Incrément automatique (JET_bitColumnAutoincrement)

Les colonnes d’incrémentation automatique sont automatiquement incrémentées par ESE lorsqu’un nouvel enregistrement est inséré dans la table. La valeur contenue dans la colonne d’incrémentation automatique est unique pour chaque enregistrement de la table et n’est pas nécessairement continue. Ces valeurs ne sont pas recyclées, mais peuvent être réutilisées dans certains cas. Seules les colonnes de type JET_coltypLong et JET_coltypLongLong peuvent être des colonnes d’incrémentation automatique.

### <a name="escrow-jet_bitcolumnescrowupdate"></a>Tiers de confiance (JET_bitColumnEscrowUpdate)

Les colonnes de dépôt peuvent être modifiées dans l’appel à [JetEscrowUpdate](./jetescrowupdate-function.md). Les mises à jour dans le tiers de confiance sont des opérations Delta numériques qui ne souffrent pas de conflits d’écriture. Cela signifie que tout nombre de sessions peut mettre à jour simultanément une colonne du tiers de confiance dans un enregistrement via [JetEscrowUpdate](./jetescrowupdate-function.md) sans conflits. Notez que toute autre opération de mise à jour peut toujours entraîner un conflit d’écriture avec une opération de mise à jour de tiers de confiance. Les mises à jour de tiers de confiance ne peuvent être apportées qu’à des colonnes de type JET_coltypLong qui ont une valeur par défaut. Ces colonnes doivent également être ajoutées à une table avant d’être chargées avec des lignes. Enfin, les lignes contenant une colonne de mise à jour de dépôt peuvent être configurées pour prendre en charge un rappel de finalisation de ligne (JET_bitColumnFinalize) ou être automatiquement supprimées si le nombre de références atteint zéro (JET_bitColumnDeleteOnZero). Pour plus d’informations, consultez la structure [JET_COLUMNDEF](./jet-columndef-structure.md) .
