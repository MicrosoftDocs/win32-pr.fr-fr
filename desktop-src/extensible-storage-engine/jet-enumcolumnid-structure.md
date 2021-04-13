---
description: 'En savoir plus sur : structure JET_ENUMCOLUMNID'
title: Structure JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID Structure
ms:assetid: 5480ebf1-4fc9-49b5-bbb3-12542b86c8f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269251(v=EXCHG.10)
ms:contentKeyID: 32765553
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
ms.openlocfilehash: 356b2a31c682a6ed0392a875c606cfaf20f1aeea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526085"
---
# <a name="jet_enumcolumnid-structure"></a><span data-ttu-id="e3fa1-103">Structure JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="e3fa1-103">JET_ENUMCOLUMNID Structure</span></span>


<span data-ttu-id="e3fa1-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="e3fa1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_enumcolumnid-structure"></a><span data-ttu-id="e3fa1-105">Structure JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="e3fa1-105">JET_ENUMCOLUMNID Structure</span></span>

<span data-ttu-id="e3fa1-106">La structure **JET_ENUMCOLUMNID** énumère un ensemble spécifique de colonnes et, éventuellement, un ensemble spécifique de plusieurs valeurs pour ces colonnes lorsque la fonction [JetEnumerateColumns](./jetenumeratecolumns-function.md) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-106">The **JET_ENUMCOLUMNID** structure enumerates a specific set of columns and, optionally, a specific set of multiple values for those columns when the [JetEnumerateColumns](./jetenumeratecolumns-function.md) function is used.</span></span> <span data-ttu-id="e3fa1-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) retourne un tableau de structures **JET_ENUMCOLUMNID** .</span><span class="sxs-lookup"><span data-stu-id="e3fa1-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) returns an array of **JET_ENUMCOLUMNID** structures.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      unsigned long ctagSequence;
      unsigned long* rgtagSequence;
    } JET_ENUMCOLUMNID;
```

### <a name="members"></a><span data-ttu-id="e3fa1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e3fa1-108">Members</span></span>

<span data-ttu-id="e3fa1-109">**ColumnID**</span><span class="sxs-lookup"><span data-stu-id="e3fa1-109">**columnid**</span></span>

<span data-ttu-id="e3fa1-110">ID de colonne à énumérer.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-110">The column ID to enumerate.</span></span>

<span data-ttu-id="e3fa1-111">Si l’ID de colonne est 0 (zéro), l’énumération de cette colonne est ignorée et un emplacement correspondant dans le tableau de sortie des structures de [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) est généré avec un état de colonne de JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-111">If the column ID is 0 (zero) then the enumeration of this column is skipped and a corresponding slot in the output array of [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) structures will be generated with a column state of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="e3fa1-112">**ctagSequence**</span><span class="sxs-lookup"><span data-stu-id="e3fa1-112">**ctagSequence**</span></span>

<span data-ttu-id="e3fa1-113">Identifie éventuellement un tableau de valeurs de colonne (par index de base un) à énumérer pour l’ID de colonne spécifié.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-113">Optionally identifies an array of column values (by one-based index) to enumerate for the specified column ID.</span></span>

<span data-ttu-id="e3fa1-114">Si **ctagSequence** a la valeur 0 (zéro), **rgtagSequence** est ignoré et toutes les valeurs de colonne pour l’ID de colonne spécifié seront énumérées.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-114">If **ctagSequence** is 0 (zero) then **rgtagSequence** is ignored and all column values for the specified column ID will be enumerated.</span></span>

<span data-ttu-id="e3fa1-115">Si un élément de **rgtagSequence** est 0 (zéro), l’énumération de cette valeur de colonne (par index de base un) sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-115">If an element of **rgtagSequence** is 0 (zero), then the enumeration of that column value (by one-based index) will be skipped.</span></span> <span data-ttu-id="e3fa1-116">Un emplacement correspondant dans le tableau de sortie de la structure **JET_ENUMCOLUMNID** sera généré avec une valeur d’état de colonne de JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-116">A corresponding slot in the output array of the **JET_ENUMCOLUMNID** structure will be generated with a column status value of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="e3fa1-117">**rgtagSequence**</span><span class="sxs-lookup"><span data-stu-id="e3fa1-117">**rgtagSequence**</span></span>

<span data-ttu-id="e3fa1-118">Tableau d’index de base un dans le tableau de valeurs de colonne pour une colonne donnée.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-118">An array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="e3fa1-119">Un élément unique est un **itagSequence** qui est défini dans [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span><span class="sxs-lookup"><span data-stu-id="e3fa1-119">A single element is an **itagSequence** which is defined in [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span></span> <span data-ttu-id="e3fa1-120">Un **itagSequence** de 0 (zéro) signifie « Skip ».</span><span class="sxs-lookup"><span data-stu-id="e3fa1-120">An **itagSequence** of 0 (zero) means "skip".</span></span> <span data-ttu-id="e3fa1-121">Un **itagSequence** de 1 signifie que retourne la première valeur de colonne de la colonne, 2 le second, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-121">An **itagSequence** of 1 means return the first column value of the column, 2 means the second, and so on.</span></span>

### <a name="requirements"></a><span data-ttu-id="e3fa1-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3fa1-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3fa1-123"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e3fa1-123"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e3fa1-124">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-124">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3fa1-125"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="e3fa1-125"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e3fa1-126">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-126">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3fa1-127"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="e3fa1-127"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e3fa1-128">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="e3fa1-128">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="e3fa1-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3fa1-129">See Also</span></span>

[<span data-ttu-id="e3fa1-130">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="e3fa1-130">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="e3fa1-131">JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="e3fa1-131">JET_ENUMCOLUMN</span></span>](./jet-enumcolumn-structure.md)  
[<span data-ttu-id="e3fa1-132">JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="e3fa1-132">JET_ENUMCOLUMNID</span></span>]()  
[<span data-ttu-id="e3fa1-133">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="e3fa1-133">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)  
[<span data-ttu-id="e3fa1-134">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="e3fa1-134">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)
