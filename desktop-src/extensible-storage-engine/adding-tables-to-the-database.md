---
description: 'En savoir plus sur : ajout de tables à la base de données'
title: Ajout de tables à la base de données
TOCTitle: Adding Tables to the Database
ms:assetid: 176d4fea-c856-441b-bd58-165b37c35095
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269195(v=EXCHG.10)
ms:contentKeyID: 32765498
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 67569f8efc164cc7156f346b6754f13b296d3b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950913"
---
# <a name="adding-tables-to-the-database"></a>Ajout de tables à la base de données


_**S’applique à :** Windows | Serveur Windows_

## <a name="adding-tables-to-the-database"></a>Ajout de tables à la base de données

Les tables sont une collection hétérogène d’enregistrements qui regroupent physiquement et logiquement les données dans la base de données. Les tables sont identifiées de manière unique par leur nom. L’ID de table ([JET_TABLEID](./jet-tableid.md)) est un handle de curseur utilisé pour mettre à jour et parcourir les tables. Vous pouvez ouvrir plusieurs [JET_TABLEID](./jet-tableid.md) sur la même table.

Une table existante est ouverte dans l’appel à [JetOpenTable](./jetopentable-function.md), et une nouvelle table est créée sans lignes ou colonnes avec [JetCreateTable](./jetcreatetable-function.md). Pour créer atomiquement une table avec un ensemble initial de colonnes et d’index, appelez [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) ou [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md). La taille initiale de la table est indiquée dans le paramètre *lPages* dans [JetCreateTable](./jetcreatetable-function.md) ou dans le membre **ulPages** de la structure [JET_TABLECREATE](./jet-tablecreate-structure.md) dans l’appel à [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md). Les tables augmentent automatiquement lorsque des données sont ajoutées à la table. La croissance est proportionnelle à la taille initiale de la table. Des colonnes peuvent être ajoutées à la table à tout moment avec [JetAddColumn](./jetaddcolumn-function.md). Lorsque l’application n’a plus besoin d’accéder à la table, le curseur peut être fermé avec [JetCloseTable](./jetclosetable-function.md). La table peut être supprimée via un appel à [JetDeleteTable](./jetdeletetable-function.md).

Les opérations de table doivent être effectuées dans le contexte d’une transaction.

## <a name="see-also"></a>Voir aussi

[Transactions](./transactions.md)
