---
description: 'En savoir plus sur : utilisation de colonnes dans une table'
title: Utilisation de colonnes dans une table
TOCTitle: Using Columns in a Table
ms:assetid: 064ac59e-d306-4335-a623-754a003f5ebc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269178(v=EXCHG.10)
ms:contentKeyID: 32765481
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 332cca1c64c851ded44951fc9bb7f68ebd9f6818030cefeb8406f965a1bd5d6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471299"
---
# <a name="using-columns-in-a-table"></a>Utilisation de colonnes dans une table


_**S’applique à :** Windows | Windows Serveurs_

## <a name="using-columns-in-a-table"></a>Utilisation de colonnes dans une table

Une table peut être créée avec un ensemble initial de colonnes en appelant [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) ou sans colonnes en appelant [JetCreateTable](./jetcreatetable-function.md). Lorsque la table est créée avec un ensemble initial de colonnes dans l’appel à [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) ou [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), elle contient une structure [JET_TABLECREATE](./jet-tablecreate-structure.md) (ou [JET_TABLECREATE2](./jet-tablecreate2-structure.md)). Ces structures contiennent un tableau de [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures qui définissent l’ensemble des colonnes de la table. Le membre **Grbit** définit les options sur la colonne et le membre **coltyp** définit le type de données qui peut être défini dans la colonne.

Lorsque la table est créée sans colonnes, vous devez l’ajouter en appelant [JetAddColumn](./jetaddcolumn-function.md) avec la structure [JET_COLUMNDEF](./jet-columndef-structure.md) . Le membre **Grbit** de la structure [JET_COLUMNDEF](./jet-columndef-structure.md) définit les options sur la colonne et le membre **coltyp** définit le type de données qui peut être défini dans la colonne. Les valeurs de colonne par défaut sont définies dans l’appel à [JetAddColumn](./jetaddcolumn-function.md) en spécifiant une valeur dans le paramètre *pvDefault* et la taille dans le paramètre *cbDefault* . Une colonne sans valeur par défaut a effectivement une valeur par défaut NULL.

Les valeurs de la table peuvent uniquement être définies dans le contexte d’une transaction. La transaction commence dans l’appel à [JetBeginTransaction](./jetbegintransaction-function.md) et se termine dans l’appel à [JetCommitTransaction](./jetcommittransaction-function.md). Au sein de la transaction, une seule valeur de colonne peut être définie en appelant [JetSetColumn](./jetsetcolumn-function.md), ou plusieurs valeurs de colonnes peuvent être définies en appelant [JetSetColumns](./jetsetcolumns-function.md). [JetSetColumns](./jetsetcolumns-function.md) utilise un tableau de structures [JET_SETCOLUMN](./jet-setcolumn-structure.md) pour définir plusieurs colonnes dans la table. Les données sont contenues dans le paramètre *pvData* de [JetSetColumn](./jetsetcolumn-function.md), ou le membre **pvData** dans [JET_SETCOLUMN](./jet-setcolumn-structure.md) structure.

Les structures [JET_COLUMNBASE](./jet-columnbase-structure.md), [JET_COLUMNLIST](./jet-columnlist-structure.md)et [JET_COLUMNDEF](./jet-columndef-structure.md) sont retournées dans les appels à [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)et [JetGetColumnInfo](./jetgetcolumninfo-function.md) selon le type de colonne récupéré. La structure [JET_COLUMNBASE](./jet-columnbase-structure.md) décrit les paramètres de la colonne de base, et la [JET_COLUMNLIST](./jet-columnlist-structure.md) contient les informations nécessaires pour parcourir la table temporaire créée par les fonctions [JetGetColumnInfo](./jetgetcolumninfo-function.md) et [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) .
