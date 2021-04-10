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
# <a name="adding-tables-to-the-database"></a><span data-ttu-id="e8cf1-103">Ajout de tables à la base de données</span><span class="sxs-lookup"><span data-stu-id="e8cf1-103">Adding Tables to the Database</span></span>


<span data-ttu-id="e8cf1-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="e8cf1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="adding-tables-to-the-database"></a><span data-ttu-id="e8cf1-105">Ajout de tables à la base de données</span><span class="sxs-lookup"><span data-stu-id="e8cf1-105">Adding Tables to the Database</span></span>

<span data-ttu-id="e8cf1-106">Les tables sont une collection hétérogène d’enregistrements qui regroupent physiquement et logiquement les données dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="e8cf1-106">Tables are a heterogeneous collection of records that physically and logically group the data in the database.</span></span> <span data-ttu-id="e8cf1-107">Les tables sont identifiées de manière unique par leur nom.</span><span class="sxs-lookup"><span data-stu-id="e8cf1-107">Tables are uniquely identified by their name.</span></span> <span data-ttu-id="e8cf1-108">L’ID de table ([JET_TABLEID](./jet-tableid.md)) est un handle de curseur utilisé pour mettre à jour et parcourir les tables.</span><span class="sxs-lookup"><span data-stu-id="e8cf1-108">The table ID ([JET_TABLEID](./jet-tableid.md)) is a handle to a cursor that is used to update and navigate tables.</span></span> <span data-ttu-id="e8cf1-109">Vous pouvez ouvrir plusieurs [JET_TABLEID](./jet-tableid.md) sur la même table.</span><span class="sxs-lookup"><span data-stu-id="e8cf1-109">You may open multiple [JET_TABLEID](./jet-tableid.md) on the same table.</span></span>

<span data-ttu-id="e8cf1-110">Une table existante est ouverte dans l’appel à [JetOpenTable](./jetopentable-function.md), et une nouvelle table est créée sans lignes ou colonnes avec [JetCreateTable](./jetcreatetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="e8cf1-110">An existing table is opened in the call to [JetOpenTable](./jetopentable-function.md), and a new table is created without rows or columns with [JetCreateTable](./jetcreatetable-function.md).</span></span> <span data-ttu-id="e8cf1-111">Pour créer atomiquement une table avec un ensemble initial de colonnes et d’index, appelez [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) ou [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span><span class="sxs-lookup"><span data-stu-id="e8cf1-111">To atomically create a table with an initial set of columns and indices, call [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) or [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span></span> <span data-ttu-id="e8cf1-112">La taille initiale de la table est indiquée dans le paramètre *lPages* dans [JetCreateTable](./jetcreatetable-function.md) ou dans le membre **ulPages** de la structure [JET_TABLECREATE](./jet-tablecreate-structure.md) dans l’appel à [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="e8cf1-112">The initial size of the table is given in the *lPages* parameter in [JetCreateTable](./jetcreatetable-function.md) or the **ulPages** member of the [JET_TABLECREATE](./jet-tablecreate-structure.md) structure in the call to [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="e8cf1-113">Les tables augmentent automatiquement lorsque des données sont ajoutées à la table.</span><span class="sxs-lookup"><span data-stu-id="e8cf1-113">Tables grow automatically when data is added to the table.</span></span> <span data-ttu-id="e8cf1-114">La croissance est proportionnelle à la taille initiale de la table.</span><span class="sxs-lookup"><span data-stu-id="e8cf1-114">The growth is proportional to the initial size of the table.</span></span> <span data-ttu-id="e8cf1-115">Des colonnes peuvent être ajoutées à la table à tout moment avec [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="e8cf1-115">Columns may be added to the table at any time with [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="e8cf1-116">Lorsque l’application n’a plus besoin d’accéder à la table, le curseur peut être fermé avec [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="e8cf1-116">When the application no longer needs to access the table, the cursor can be closed with [JetCloseTable](./jetclosetable-function.md).</span></span> <span data-ttu-id="e8cf1-117">La table peut être supprimée via un appel à [JetDeleteTable](./jetdeletetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="e8cf1-117">The table may be deleted via a call to [JetDeleteTable](./jetdeletetable-function.md).</span></span>

<span data-ttu-id="e8cf1-118">Les opérations de table doivent être effectuées dans le contexte d’une transaction.</span><span class="sxs-lookup"><span data-stu-id="e8cf1-118">Table operations should be performed within the context of a transaction.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8cf1-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8cf1-119">See Also</span></span>

[<span data-ttu-id="e8cf1-120">Transactions</span><span class="sxs-lookup"><span data-stu-id="e8cf1-120">Transactions</span></span>](./transactions.md)
