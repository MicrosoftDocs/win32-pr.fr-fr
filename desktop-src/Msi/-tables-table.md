---
description: La \_ table tables est une table système en lecture seule qui répertorie toutes les tables de la base de données. Interrogez cette table pour savoir si une table existe.
ms.assetid: d064855b-8c10-476e-9570-cc3ab48ae998
title: Table _Tables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2dc3ebafd969a07676f64f674f76c3e16ebe059
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864545"
---
# <a name="_tables-table"></a><span data-ttu-id="28503-104">\_Table tables</span><span class="sxs-lookup"><span data-stu-id="28503-104">\_Tables Table</span></span>

<span data-ttu-id="28503-105">La \_ table tables est une table système en lecture seule qui répertorie toutes les tables de la base de données.</span><span class="sxs-lookup"><span data-stu-id="28503-105">The \_Tables table is a read-only system table that lists all the tables in the database.</span></span> <span data-ttu-id="28503-106">Interrogez cette table pour savoir si une table existe.</span><span class="sxs-lookup"><span data-stu-id="28503-106">Query this table to find out if a table exists.</span></span>

<span data-ttu-id="28503-107">La \_ table tables contient la colonne suivante.</span><span class="sxs-lookup"><span data-stu-id="28503-107">The \_Tables Table has the following column.</span></span>



| <span data-ttu-id="28503-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="28503-108">Column</span></span> | <span data-ttu-id="28503-109">Type</span><span class="sxs-lookup"><span data-stu-id="28503-109">Type</span></span>             | <span data-ttu-id="28503-110">Clé</span><span class="sxs-lookup"><span data-stu-id="28503-110">Key</span></span> | <span data-ttu-id="28503-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="28503-111">Nullable</span></span> |
|--------|------------------|-----|----------|
| <span data-ttu-id="28503-112">Nom</span><span class="sxs-lookup"><span data-stu-id="28503-112">Name</span></span>   | [<span data-ttu-id="28503-113">Text</span><span class="sxs-lookup"><span data-stu-id="28503-113">Text</span></span>](text.md) | <span data-ttu-id="28503-114">O</span><span class="sxs-lookup"><span data-stu-id="28503-114">Y</span></span>   | <span data-ttu-id="28503-115">N</span><span class="sxs-lookup"><span data-stu-id="28503-115">N</span></span>        |



 

## <a name="column"></a><span data-ttu-id="28503-116">Colonne</span><span class="sxs-lookup"><span data-stu-id="28503-116">Column</span></span>

<dl> <dt>

<span data-ttu-id="28503-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme</span><span class="sxs-lookup"><span data-stu-id="28503-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="28503-118">Nom de l’une des tables.</span><span class="sxs-lookup"><span data-stu-id="28503-118">Name of one of the tables.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28503-119">Notes</span><span class="sxs-lookup"><span data-stu-id="28503-119">Remarks</span></span>

<span data-ttu-id="28503-120">Étant donné que la \_ table tables est une table système qui ne peut pas être modifiée par le biais de requêtes SQL, vous ne pouvez pas obtenir les clés primaires avec la fonction [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) ou la [**propriété PrimaryKeys**](database-primarykeys.md).</span><span class="sxs-lookup"><span data-stu-id="28503-120">Because the \_Tables table is a system table that cannot be modified through SQL queries, you cannot obtain the primary keys with the [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) function or the [**PrimaryKeys property**](database-primarykeys.md).</span></span>

 

 



