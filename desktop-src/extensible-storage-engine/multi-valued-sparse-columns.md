---
description: En savoir plus sur les colonnes éparses à valeurs multiples
title: Colonnes éparses à valeurs multiples
TOCTitle: Multi-Valued Sparse Columns
ms:assetid: 36e82a73-aad4-4e0d-a743-a2182c41fe9c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269225(v=EXCHG.10)
ms:contentKeyID: 32765527
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 21448d50e17881517086c1b258dcce02e84286a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915852"
---
# <a name="multi-valued-sparse-columns"></a>Colonnes éparses à valeurs multiples


_**S’applique à :** Windows | Windows Serveurs_

## <a name="multi-valued-sparse-columns"></a>Colonnes éparses à valeurs multiples

Les colonnes éparses peuvent être fixes ou de longueur variable, et sont uniques en ce qu’elles n’occupent pas d’espace dans un enregistrement s’ils ont une valeur NULL ou sont laissées à leur valeur par défaut. Les colonnes éparses, également appelées colonnes avec balises, peuvent contenir plusieurs valeurs dans un seul enregistrement. Les colonnes avec balises peuvent correspondre à l’un des types de colonnes décrits dans la [JET_coltyp](./jet-coltyp.md) constantes. Ils sont créés lors de l’ajout de la colonne à la table en définissant l’indicateur JET_bitColumnTagged dans la structure [JET_COLUMNDEF](./jet-columndef-structure.md) de l’appel à [JetAddColumn](./jetaddcolumn-function.md), ou dans la structure [JET_COLUMNCREATE](./jet-columncreate-structure.md) utilisée dans l’appel à [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) ou [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md). Les colonnes de type JET_coltypLongText et JET_coltypLongBinary sont automatiquement créées en tant que colonnes avec balises.

Seules les colonnes avec balises peuvent contenir plusieurs valeurs dans un enregistrement, les colonnes de longueur fixe ou variable ne peuvent pas contenir plusieurs valeurs. Il existe deux types de colonnes à plusieurs valeurs :

  - Par défaut, les colonnes avec balises sont à valeurs multiples. Lorsqu’une deuxième valeur est ajoutée à la colonne, elle devient automatiquement à valeurs multiples.

  - Colonnes avec balises créées avec l’option JET_bitColumnMultiValued dans la structure [JET_COLUMNDEF](./jet-columndef-structure.md) de l’appel à [JetAddColumn](./jetaddcolumn-function.md).

L’option JET_bitColumnMultiValued modifie la façon dont la colonne est indexée. Les colonnes à valeurs multiples avec l’option JET_bitColumnMultiValued sont indexées plus largement que les colonnes à valeurs multiples balisées. Ces colonnes sont indexées sur toutes les valeurs de la colonne à valeurs multiples, alors que les colonnes à valeurs multiples balisées sont uniquement indexées sur la première valeur de la colonne à valeurs multiples. Par exemple, considérez une colonne à valeurs multiples dans laquelle l’option JET_bitColumnMultiValued est définie et il s’agit de la première colonne à valeurs multiples d’un index. Cette colonne contient trois valeurs : A, B et C. Un index sur cette colonne contient des entrées pour les trois valeurs, A, B et C. Si l’option JET_bitColumnMultiValued n’a pas été définie, l’index sur cette colonne contient uniquement la première valeur, A, dans l’index.
