---
description: 'En savoir plus sur : lecture de données à partir de la base de données'
title: Lecture des données de la base de données
TOCTitle: Reading Data from the Database
ms:assetid: c3c48918-ccd6-4c34-849c-93bd7533ce92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294080(v=EXCHG.10)
ms:contentKeyID: 32765695
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 176cd3189dd1c2701331eff0ef5387827da19b94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521219"
---
# <a name="reading-data-from-the-database"></a><span data-ttu-id="a1ba4-103">Lecture des données de la base de données</span><span class="sxs-lookup"><span data-stu-id="a1ba4-103">Reading Data from the Database</span></span>


<span data-ttu-id="a1ba4-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="a1ba4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="reading-data-from-the-database"></a><span data-ttu-id="a1ba4-105">Lecture des données de la base de données</span><span class="sxs-lookup"><span data-stu-id="a1ba4-105">Reading Data from the Database</span></span>

<span data-ttu-id="a1ba4-106">La lecture des données de la base de données doit être effectuée au sein d’une transaction.</span><span class="sxs-lookup"><span data-stu-id="a1ba4-106">Reading data from the database should be performed within a transaction.</span></span>

<span data-ttu-id="a1ba4-107">La procédure suivante montre comment effectuer une opération de lecture simple dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="a1ba4-107">The following procedure shows how to perform a simple read operation in the database.</span></span>

### <a name="to-read-data-from-a-database"></a><span data-ttu-id="a1ba4-108">Pour lire des données à partir d’une base de données</span><span class="sxs-lookup"><span data-stu-id="a1ba4-108">To read data from a database</span></span>

1.  <span data-ttu-id="a1ba4-109">Appelez [JetBeginTransaction](./jetbegintransaction-function.md) ou [JETBEGINTRANSACTION2](./jetbegintransaction2-function.md) avec l’ID de session pour démarrer la transaction.</span><span class="sxs-lookup"><span data-stu-id="a1ba4-109">Call [JetBeginTransaction](./jetbegintransaction-function.md) or [JetBeginTransaction2](./jetbegintransaction2-function.md) with the session ID to start the transaction.</span></span>

2.  <span data-ttu-id="a1ba4-110">Déplacez le curseur vers l’enregistrement souhaité en appelant [JetMove](./jetmove-function.md) avec JET_MoveFirst dans le paramètre *cRow* .</span><span class="sxs-lookup"><span data-stu-id="a1ba4-110">Move the cursor to the desired record by calling [JetMove](./jetmove-function.md) with JET_MoveFirst in the *cRow* parameter.</span></span> <span data-ttu-id="a1ba4-111">Pour plus d’informations sur le déplacement du curseur, consultez la rubrique [indexation dans le tableau](./indexing-in-the-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a1ba4-111">For more information on how to move the cursor, see the [Indexing in the Table](./indexing-in-the-table.md) topic.</span></span>

3.  <span data-ttu-id="a1ba4-112">Appelez [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) sur l’enregistrement en cours avec JET_ColInfo spécifié dans le paramètre *InfoLevel* pour récupérer l’ID de colonne de la colonne.</span><span class="sxs-lookup"><span data-stu-id="a1ba4-112">Call [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) on the current record with JET_ColInfo specified in the *InfoLevel* parameter to retrieve the column ID for the column.</span></span> <span data-ttu-id="a1ba4-113">L’ID de colonne est retourné dans la structure [JET_COLUMNDEF](./jet-columndef-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="a1ba4-113">The column ID is returned in the [JET_COLUMNDEF](./jet-columndef-structure.md) structure.</span></span>

4.  <span data-ttu-id="a1ba4-114">Lisez les données de la colonne en appelant [JetRetrieveColumn](./jetretrievecolumn-function.md) avec l’ID de colonne récupéré à l’étape 3 dans le paramètre columnid.</span><span class="sxs-lookup"><span data-stu-id="a1ba4-114">Read the data from the column by calling [JetRetrieveColumn](./jetretrievecolumn-function.md) with the column ID retrieved in step 3 in the columnid parameter.</span></span> <span data-ttu-id="a1ba4-115">Le paramètre *pvData* contient le type de données spécifié dans la structure [JET_COLUMNDEF](./jet-columndef-structure.md) Récupérée à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="a1ba4-115">The *pvData* parameter contains the type of data specified in the [JET_COLUMNDEF](./jet-columndef-structure.md) structure retrieved in step 3.</span></span>

5.  <span data-ttu-id="a1ba4-116">Appelez [JetCommitTransaction](./jetcommittransaction-function.md) pour valider la transaction dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="a1ba4-116">Call [JetCommitTransaction](./jetcommittransaction-function.md) to commit the transaction to the database.</span></span>
