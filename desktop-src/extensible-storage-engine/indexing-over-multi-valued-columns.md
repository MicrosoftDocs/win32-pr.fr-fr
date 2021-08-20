---
description: En savoir plus sur l’indexation des colonnes à valeurs multiples
title: Indexation sur des colonnes à valeurs multiples
TOCTitle: Indexing over Multi-Valued Columns
ms:assetid: 90e31df2-2f5b-47a8-84c1-ece6bcc40858
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269341(v=EXCHG.10)
ms:contentKeyID: 32765630
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 5b825a687c1771fae7d01526fbb7e8e0f56e87fccdfa8b43fcab2c202d87df1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117705910"
---
# <a name="indexing-over-multi-valued-columns"></a>Indexation sur des colonnes à valeurs multiples


_**S’applique à :** Windows | Windows Serveurs_

## <a name="indexing-over-multi-valued-columns"></a>Indexation sur des colonnes à valeurs multiples

L’indexation sur des colonnes à valeurs multiples est effectuée uniquement sur la première colonne à valeurs multiples de l’index. La première colonne à valeurs multiples est développée afin que chaque valeur de la colonne soit indexée. Toutes les autres colonnes à valeurs multiples sont indexées uniquement sur la première valeur de la colonne. Par exemple, un index est défini sur la colonne A, et la colonne B, où ces deux colonnes sont à valeurs multiples. Dans un enregistrement donné, la colonne a a les valeurs rouge et bleu, et la colonne B a les valeurs 1, 2 et 3. L’index obtenu donne des entrées pour Red-1 et Blue-1. Les valeurs de la deuxième colonne, colonne B, ne sont pas développées. Notez que même si chaque colonne avec balises peut être à valeurs multiples, seules les colonnes avec balises explicitement marquées comme étant à valeurs multiples via JET_bitColumnMultiValued sont développées de cette façon. En outre, en raison du fait que les entrées d’index primaire contiennent des enregistrements, il n’est pas autorisé d’avoir un index primaire sur une colonne à valeurs multiples, car cela entraînerait l’index de plusieurs emplacements dans lesquels l’enregistrement devrait résider. Pour plus d’informations, consultez la rubrique [colonnes avec balises, fixes et variables](./tagged-fixed-and-variable-columns.md) .

à partir de Windows Vista, les utilisateurs ont la possibilité de définir l’option JET_bitIndexCrossProduct lors de la création de l’index avec [JetCreateIndex](./jetcreateindex-function.md) ou [JetCreateIndex2](./jetcreateindex2-function.md) à l’aide de la structure [JET_INDEXCREATE](./jet-indexcreate-structure.md) . Lorsque cette option est définie sur un index, toutes les colonnes clés à valeurs multiples de l’index sont développées et un produit croisé est créé dans l’index pour chaque valeur dans ces colonnes. L’exemple ci-dessus produit désormais des entrées pour rouge-1, rouge-2, rouge-3, bleu-1, bleu-2, bleu-3. Là encore, chaque colonne clé doit être explicitement déclarée comme étant à valeurs multiples via JET_bitColumnMultiValued pour être développée dans l’index.
