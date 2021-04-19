---
description: La \_ Table Columns est une table système en lecture seule qui contient le catalogue de colonnes. Elle répertorie les colonnes de toutes les tables. Vous pouvez interroger cette table pour savoir si une colonne donnée existe.
ms.assetid: 1ddde4e2-90a9-4dd8-a4f9-b6802d0b11cf
title: Table _Columns
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d896f330e5fc2e13b5f172581341eb11a09617d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534224"
---
# <a name="_columns-table"></a><span data-ttu-id="1ff4e-105">\_Table colonnes</span><span class="sxs-lookup"><span data-stu-id="1ff4e-105">\_Columns Table</span></span>

<span data-ttu-id="1ff4e-106">La \_ Table Columns est une table système en lecture seule qui contient le catalogue de colonnes.</span><span class="sxs-lookup"><span data-stu-id="1ff4e-106">The \_Columns table is a read-only system table that contains the column catalog.</span></span> <span data-ttu-id="1ff4e-107">Elle répertorie les colonnes de toutes les tables.</span><span class="sxs-lookup"><span data-stu-id="1ff4e-107">It lists the columns for all the tables.</span></span> <span data-ttu-id="1ff4e-108">Vous pouvez interroger cette table pour savoir si une colonne donnée existe.</span><span class="sxs-lookup"><span data-stu-id="1ff4e-108">You can query this table to find out if a given column exists.</span></span>

<span data-ttu-id="1ff4e-109">La \_ Table Columns contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="1ff4e-109">The \_Columns table has the following columns.</span></span>



| <span data-ttu-id="1ff4e-110">Colonne</span><span class="sxs-lookup"><span data-stu-id="1ff4e-110">Column</span></span> | <span data-ttu-id="1ff4e-111">Type</span><span class="sxs-lookup"><span data-stu-id="1ff4e-111">Type</span></span>                   | <span data-ttu-id="1ff4e-112">Clé</span><span class="sxs-lookup"><span data-stu-id="1ff4e-112">Key</span></span> | <span data-ttu-id="1ff4e-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="1ff4e-113">Nullable</span></span> |
|--------|------------------------|-----|----------|
| <span data-ttu-id="1ff4e-114">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="1ff4e-114">Table</span></span>  | [<span data-ttu-id="1ff4e-115">Text</span><span class="sxs-lookup"><span data-stu-id="1ff4e-115">Text</span></span>](text.md)       | <span data-ttu-id="1ff4e-116">O</span><span class="sxs-lookup"><span data-stu-id="1ff4e-116">Y</span></span>   | <span data-ttu-id="1ff4e-117">N</span><span class="sxs-lookup"><span data-stu-id="1ff4e-117">N</span></span>        |
| <span data-ttu-id="1ff4e-118">Number</span><span class="sxs-lookup"><span data-stu-id="1ff4e-118">Number</span></span> | [<span data-ttu-id="1ff4e-119">Integer</span><span class="sxs-lookup"><span data-stu-id="1ff4e-119">Integer</span></span>](integer.md) | <span data-ttu-id="1ff4e-120">O</span><span class="sxs-lookup"><span data-stu-id="1ff4e-120">Y</span></span>   | <span data-ttu-id="1ff4e-121">N</span><span class="sxs-lookup"><span data-stu-id="1ff4e-121">N</span></span>        |
| <span data-ttu-id="1ff4e-122">Nom</span><span class="sxs-lookup"><span data-stu-id="1ff4e-122">Name</span></span>   | [<span data-ttu-id="1ff4e-123">Text</span><span class="sxs-lookup"><span data-stu-id="1ff4e-123">Text</span></span>](text.md)       | <span data-ttu-id="1ff4e-124">N</span><span class="sxs-lookup"><span data-stu-id="1ff4e-124">N</span></span>   | <span data-ttu-id="1ff4e-125">N</span><span class="sxs-lookup"><span data-stu-id="1ff4e-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="1ff4e-126">Colonnes</span><span class="sxs-lookup"><span data-stu-id="1ff4e-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="1ff4e-127"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tableau</span><span class="sxs-lookup"><span data-stu-id="1ff4e-127"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="1ff4e-128">Nom de la table qui contient la colonne.</span><span class="sxs-lookup"><span data-stu-id="1ff4e-128">The name of the table that contains the column.</span></span>

</dd> <dt>

<span data-ttu-id="1ff4e-129"><span id="Number"></span><span id="number"></span><span id="NUMBER"></span>Certain</span><span class="sxs-lookup"><span data-stu-id="1ff4e-129"><span id="Number"></span><span id="number"></span><span id="NUMBER"></span>Number</span></span>
</dt> <dd>

<span data-ttu-id="1ff4e-130">Ordre de la colonne dans la table.</span><span class="sxs-lookup"><span data-stu-id="1ff4e-130">The order of the column within the table.</span></span>

</dd> <dt>

<span data-ttu-id="1ff4e-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme</span><span class="sxs-lookup"><span data-stu-id="1ff4e-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="1ff4e-132">Nom de la colonne.</span><span class="sxs-lookup"><span data-stu-id="1ff4e-132">The name of the column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ff4e-133">Notes</span><span class="sxs-lookup"><span data-stu-id="1ff4e-133">Remarks</span></span>

<span data-ttu-id="1ff4e-134">Étant donné que la \_ table de colonnes est une table système qui ne peut pas être modifiée par le biais de requêtes SQL, vous ne pouvez pas obtenir les clés primaires avec la fonction [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) ou la [**propriété PrimaryKeys**](database-primarykeys.md).</span><span class="sxs-lookup"><span data-stu-id="1ff4e-134">Because the \_Columns table is a system table that cannot be modified through SQL queries, you cannot obtain the primary keys with the [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) function or the [**PrimaryKeys property**](database-primarykeys.md).</span></span>

<span data-ttu-id="1ff4e-135">Seules les colonnes persistantes sont stockées dans la \_ Table Columns.</span><span class="sxs-lookup"><span data-stu-id="1ff4e-135">Only persistent columns are stored in the \_Columns table.</span></span> <span data-ttu-id="1ff4e-136">Pour déterminer s’il existe une colonne temporaire, vous devez créer une vue à l’aide d’une \* instruction SELECT sur la table, puis parcourir tous les champs d’un enregistrement retourné par la fonction [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) avec l' \_ option MSICOLINFO Names.</span><span class="sxs-lookup"><span data-stu-id="1ff4e-136">To determine if a temporary column exists one would need to create a view using a SELECT \* statement against the table, then loop through all fields in a record returned by the [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) function with the MSICOLINFO\_NAMES option.</span></span>

 

 



