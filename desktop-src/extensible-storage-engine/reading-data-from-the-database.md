---
description: 'En savoir plus sur : lecture de données à partir de la base de données'
title: Lecture des données de la base de données
TOCTitle: Reading Data from the Database
ms:assetid: c3c48918-ccd6-4c34-849c-93bd7533ce92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294080(v=EXCHG.10)
ms:contentKeyID: 32765695
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 7d33aa2640c07018186a5516d985fd4e46194d39cd4b12b7254f430f889e2484
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780259"
---
# <a name="reading-data-from-the-database"></a>Lecture des données de la base de données


_**S’applique à :** Windows | Windows Serveurs_

## <a name="reading-data-from-the-database"></a>Lecture des données de la base de données

La lecture des données de la base de données doit être effectuée au sein d’une transaction.

La procédure suivante montre comment effectuer une opération de lecture simple dans la base de données.

### <a name="to-read-data-from-a-database"></a>Pour lire des données à partir d’une base de données

1.  Appelez [JetBeginTransaction](./jetbegintransaction-function.md) ou [JETBEGINTRANSACTION2](./jetbegintransaction2-function.md) avec l’ID de session pour démarrer la transaction.

2.  Déplacez le curseur vers l’enregistrement souhaité en appelant [JetMove](./jetmove-function.md) avec JET_MoveFirst dans le paramètre *cRow* . Pour plus d’informations sur le déplacement du curseur, consultez la rubrique [indexation dans le tableau](./indexing-in-the-table.md) .

3.  Appelez [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) sur l’enregistrement en cours avec JET_ColInfo spécifié dans le paramètre *InfoLevel* pour récupérer l’ID de colonne de la colonne. L’ID de colonne est retourné dans la structure [JET_COLUMNDEF](./jet-columndef-structure.md) .

4.  Lisez les données de la colonne en appelant [JetRetrieveColumn](./jetretrievecolumn-function.md) avec l’ID de colonne récupéré à l’étape 3 dans le paramètre columnid. Le paramètre *pvData* contient le type de données spécifié dans la structure [JET_COLUMNDEF](./jet-columndef-structure.md) Récupérée à l’étape 3.

5.  Appelez [JetCommitTransaction](./jetcommittransaction-function.md) pour valider la transaction dans la base de données.
