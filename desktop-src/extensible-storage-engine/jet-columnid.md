---
description: 'En savoir plus sur : JET_COLUMNID'
title: JET_COLUMNID
TOCTitle: JET_COLUMNID
ms:assetid: d6c74c5c-ba61-4e1c-a1b1-495e925b6b68
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294104(v=EXCHG.10)
ms:contentKeyID: 32765719
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be5b8bb64dc9e0fc42055cf5e4d4f67caa7654bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861962"
---
# <a name="jet_columnid"></a><span data-ttu-id="73dd0-103">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="73dd0-103">JET_COLUMNID</span></span>


<span data-ttu-id="73dd0-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="73dd0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columnid"></a><span data-ttu-id="73dd0-105">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="73dd0-105">JET_COLUMNID</span></span>

<span data-ttu-id="73dd0-106">Le type de données **JET_COLUMNID** identifie une colonne dans une table.</span><span class="sxs-lookup"><span data-stu-id="73dd0-106">The **JET_COLUMNID** data type identifies a column within a table.</span></span>

```cpp
    typedef unsigned long JET_COLUMNID;
```

### <a name="data-types"></a><span data-ttu-id="73dd0-107">Types de données</span><span class="sxs-lookup"><span data-stu-id="73dd0-107">Data Types</span></span>

<span data-ttu-id="73dd0-108">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="73dd0-108">JET_COLUMNID</span></span>

<span data-ttu-id="73dd0-109">Identifie une colonne dans une table.</span><span class="sxs-lookup"><span data-stu-id="73dd0-109">Identifies a column within a table.</span></span>

### <a name="remarks"></a><span data-ttu-id="73dd0-110">Notes</span><span class="sxs-lookup"><span data-stu-id="73dd0-110">Remarks</span></span>

<span data-ttu-id="73dd0-111">Les ID de colonne sont uniques dans une table unique.</span><span class="sxs-lookup"><span data-stu-id="73dd0-111">Column IDs are unique within a single table.</span></span> <span data-ttu-id="73dd0-112">Une fois qu’une colonne est connue pour avoir un certain ID de colonne, elle aura toujours cet ID de colonne.</span><span class="sxs-lookup"><span data-stu-id="73dd0-112">Once a column is known to have a certain column ID, it will always have that column ID.</span></span> <span data-ttu-id="73dd0-113">La restauration à partir d’une sauvegarde ne modifie pas la valeur d’un ID de colonne.</span><span class="sxs-lookup"><span data-stu-id="73dd0-113">Restore from backup will not change the value of a column ID.</span></span> <span data-ttu-id="73dd0-114">Toutefois, si une ou plusieurs colonnes de table, antérieures à une colonne de table spécifique, sont supprimées, une base de données compacte peut alors modifier la valeur d’un ID de colonne.</span><span class="sxs-lookup"><span data-stu-id="73dd0-114">However, if one or more table columns, prior to a specific table column, are deleted, a compact database can then change the value of a column ID.</span></span>

<span data-ttu-id="73dd0-115">Dans certains cas, les ID de colonne sont le seul moyen d’identifier les colonnes.</span><span class="sxs-lookup"><span data-stu-id="73dd0-115">In some cases, column IDs are the only means of identifying columns.</span></span> <span data-ttu-id="73dd0-116">Lorsqu’une table temporaire est créée, ses colonnes n’ont pas de noms, mais un tableau d’ID de colonne est retourné par la fonction Create.</span><span class="sxs-lookup"><span data-stu-id="73dd0-116">When a temporary table is created, its columns do not have names, but an array of column IDs is returned by the create function.</span></span>

<span data-ttu-id="73dd0-117">Les colonnes de différentes tables peuvent avoir le même ID de colonne.</span><span class="sxs-lookup"><span data-stu-id="73dd0-117">Columns in different tables can have the same column ID.</span></span>

### <a name="requirements"></a><span data-ttu-id="73dd0-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73dd0-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73dd0-119"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="73dd0-119"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="73dd0-120">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="73dd0-120">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73dd0-121"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="73dd0-121"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="73dd0-122">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="73dd0-122">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73dd0-123"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="73dd0-123"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="73dd0-124">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="73dd0-124">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

