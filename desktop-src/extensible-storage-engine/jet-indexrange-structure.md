---
description: 'En savoir plus sur : structure JET_INDEXRANGE'
title: Structure JET_INDEXRANGE
TOCTitle: JET_INDEXRANGE Structure
ms:assetid: 8e437f7d-1e21-4a0b-a5a5-1c78235a4f80
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269335(v=EXCHG.10)
ms:contentKeyID: 32765624
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
ms.openlocfilehash: ecbd8151be8ef278fc1bddc12323f41abd05b09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544985"
---
# <a name="jet_indexrange-structure"></a><span data-ttu-id="29459-103">Structure JET_INDEXRANGE</span><span class="sxs-lookup"><span data-stu-id="29459-103">JET_INDEXRANGE Structure</span></span>


<span data-ttu-id="29459-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="29459-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_indexrange-structure"></a><span data-ttu-id="29459-105">Structure JET_INDEXRANGE</span><span class="sxs-lookup"><span data-stu-id="29459-105">JET_INDEXRANGE Structure</span></span>

<span data-ttu-id="29459-106">La structure **JET_INDEXRANGE** identifie une plage d’index lorsqu’elle est utilisée avec la fonction [JetIntersectIndexes](./jetintersectindexes-function.md) .</span><span class="sxs-lookup"><span data-stu-id="29459-106">The **JET_INDEXRANGE** structure identifies an index range when it is used with the [JetIntersectIndexes](./jetintersectindexes-function.md) function.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      JET_GRBIT grbit;
    } JET_INDEXRANGE;
```

### <a name="members"></a><span data-ttu-id="29459-107">Membres</span><span class="sxs-lookup"><span data-stu-id="29459-107">Members</span></span>

<span data-ttu-id="29459-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="29459-108">**cbStruct**</span></span>

<span data-ttu-id="29459-109">Taille, en octets, de la **JET_INDEXRANGE**.</span><span class="sxs-lookup"><span data-stu-id="29459-109">The size, in bytes, of the **JET_INDEXRANGE**.</span></span>

<span data-ttu-id="29459-110">**TableID**</span><span class="sxs-lookup"><span data-stu-id="29459-110">**tableid**</span></span>

<span data-ttu-id="29459-111">Un curseur ayant précédemment une plage d’index définie avec [JetSetIndexRange](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="29459-111">A cursor that has previously had an index range set with [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

<span data-ttu-id="29459-112">**grbit**</span><span class="sxs-lookup"><span data-stu-id="29459-112">**grbit**</span></span>

<span data-ttu-id="29459-113">Masque de masque composé exactement d’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="29459-113">A bitmask composed of exactly one of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="29459-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="29459-114">Value</span></span></p></th>
<th><p><span data-ttu-id="29459-115">Signification</span><span class="sxs-lookup"><span data-stu-id="29459-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="29459-116">JET_bitRecordInIndex</span><span class="sxs-lookup"><span data-stu-id="29459-116">JET_bitRecordInIndex</span></span></p></td>
<td><p><span data-ttu-id="29459-117">Spécifie que la plage d’index doit être traitée normalement.</span><span class="sxs-lookup"><span data-stu-id="29459-117">Specifies that the index range should be treated normally.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29459-118">JET_bitRecordNotInIndex</span><span class="sxs-lookup"><span data-stu-id="29459-118">JET_bitRecordNotInIndex</span></span></p></td>
<td><p><span data-ttu-id="29459-119">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="29459-119">Reserved for future use.</span></span> <span data-ttu-id="29459-120">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="29459-120">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a><span data-ttu-id="29459-121">Notes</span><span class="sxs-lookup"><span data-stu-id="29459-121">Remarks</span></span>

<span data-ttu-id="29459-122">Chaque **JET_INDEXRANGE** structure transmise à [JetIntersectIndexes](./jetintersectindexes-function.md) représente une plage d’index, qui sera croisée par l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="29459-122">Each **JET_INDEXRANGE** structure that is passed to [JetIntersectIndexes](./jetintersectindexes-function.md) represents an index range, which will be intersected by the API call.</span></span> <span data-ttu-id="29459-123">Le curseur fourni dans **JET_INDEXRANGE** doit avoir une plage d’index valide déjà définie, avec un appel réussi à [JetSetIndexRange](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="29459-123">The cursor that is given in **JET_INDEXRANGE** must have a valid index range set on it already, with a successful call to [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="29459-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29459-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="29459-125"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="29459-125"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="29459-126">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="29459-126">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29459-127"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="29459-127"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="29459-128">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="29459-128">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29459-129"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="29459-129"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="29459-130">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="29459-130">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="29459-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29459-131">See Also</span></span>

[<span data-ttu-id="29459-132">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="29459-132">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="29459-133">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="29459-133">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="29459-134">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="29459-134">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="29459-135">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="29459-135">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="29459-136">JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="29459-136">JetIntersectIndexes</span></span>](./jetintersectindexes-function.md)  
[<span data-ttu-id="29459-137">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="29459-137">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
