---
description: 'En savoir plus sur : structure JET_RECORDLIST'
title: Structure JET_RECORDLIST
TOCTitle: JET_RECORDLIST Structure
ms:assetid: 6b4d97a0-4b42-4f7c-bb18-b6db3c92668a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269287(v=EXCHG.10)
ms:contentKeyID: 32765579
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
ms.openlocfilehash: 16aca3a13bbae7c61bfe03aca49acea775820d39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868373"
---
# <a name="jet_recordlist-structure"></a><span data-ttu-id="fb606-103">Structure JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="fb606-103">JET_RECORDLIST Structure</span></span>


<span data-ttu-id="fb606-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="fb606-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recordlist-structure"></a><span data-ttu-id="fb606-105">Structure JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="fb606-105">JET_RECORDLIST Structure</span></span>

<span data-ttu-id="fb606-106">La structure **JET_RECORDLIST** trouve les enregistrements qui se trouvent à l’intersection des plages d’index spécifiées lorsqu’elles sont utilisées avec la fonction [JetIntersectIndexes](./jetintersectindexes-function.md) .</span><span class="sxs-lookup"><span data-stu-id="fb606-106">The **JET_RECORDLIST** structure finds records that are in the intersection of specified index ranges when they are used with the [JetIntersectIndexes](./jetintersectindexes-function.md) function.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidBookmark;
    } JET_RECORDLIST;
```

### <a name="members"></a><span data-ttu-id="fb606-107">Membres</span><span class="sxs-lookup"><span data-stu-id="fb606-107">Members</span></span>

<span data-ttu-id="fb606-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="fb606-108">**cbStruct**</span></span>

<span data-ttu-id="fb606-109">Taille de la structure **JET_RECORDLIST** , en octets.</span><span class="sxs-lookup"><span data-stu-id="fb606-109">The size of the **JET_RECORDLIST** structure, in bytes.</span></span>

<span data-ttu-id="fb606-110">**TableID**</span><span class="sxs-lookup"><span data-stu-id="fb606-110">**tableid**</span></span>

<span data-ttu-id="fb606-111">Identificateur de table d’une table temporaire qui contient les signets pour les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="fb606-111">The table identifier of a temporary table that contains the bookmarks for the results of the query.</span></span> <span data-ttu-id="fb606-112">La table est automatiquement fermée si la transaction en cours est restaurée avec [JetRollback](./jetrollback-function.md); dans le cas contraire, il doit être fermé avec [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="fb606-112">The table will automatically be closed if the current transaction is rolled back with [JetRollback](./jetrollback-function.md); otherwise, it must be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="fb606-113">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="fb606-113">**cRecord**</span></span>

<span data-ttu-id="fb606-114">Nombre de lignes dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="fb606-114">The number of rows in the temporary table.</span></span>

<span data-ttu-id="fb606-115">**columnidBookmark**</span><span class="sxs-lookup"><span data-stu-id="fb606-115">**columnidBookmark**</span></span>

<span data-ttu-id="fb606-116">Identificateur de colonne de la colonne de signets dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="fb606-116">The column identifier of the bookmark column in the temporary table.</span></span>

### <a name="remarks"></a><span data-ttu-id="fb606-117">Notes</span><span class="sxs-lookup"><span data-stu-id="fb606-117">Remarks</span></span>

<span data-ttu-id="fb606-118">La table temporaire qui est identifiée par **TableID** a une seule colonne.</span><span class="sxs-lookup"><span data-stu-id="fb606-118">The temporary table that is identified by **tableid** has a single column.</span></span> <span data-ttu-id="fb606-119">Cette colonne unique contient des signets et chaque enregistrement doit tenir dans une mémoire tampon de taille JET_cbBookmarkMost octets.</span><span class="sxs-lookup"><span data-stu-id="fb606-119">That single column holds bookmarks, and each record should fit in a buffer of size JET_cbBookmarkMost bytes.</span></span>

### <a name="requirements"></a><span data-ttu-id="fb606-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb606-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb606-121"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="fb606-121"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fb606-122">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="fb606-122">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb606-123"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="fb606-123"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fb606-124">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="fb606-124">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb606-125"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="fb606-125"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fb606-126">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="fb606-126">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="fb606-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb606-127">See Also</span></span>

[<span data-ttu-id="fb606-128">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="fb606-128">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="fb606-129">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="fb606-129">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="fb606-130">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="fb606-130">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="fb606-131">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="fb606-131">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="fb606-132">JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="fb606-132">JetIntersectIndexes</span></span>](./jetintersectindexes-function.md)  
[<span data-ttu-id="fb606-133">JetRollback</span><span class="sxs-lookup"><span data-stu-id="fb606-133">JetRollback</span></span>](./jetrollback-function.md)
