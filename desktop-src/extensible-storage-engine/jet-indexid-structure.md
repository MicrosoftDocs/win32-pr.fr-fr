---
description: 'En savoir plus sur : structure JET_INDEXID'
title: Structure JET_INDEXID
TOCTitle: JET_INDEXID Structure
ms:assetid: 8b1d90f0-bc93-4b30-90d1-b9e93ad26654
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269327(v=EXCHG.10)
ms:contentKeyID: 32765617
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
ms.openlocfilehash: e1a9c6a971e44604240d750163f0570937f9d4db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522242"
---
# <a name="jet_indexid-structure"></a><span data-ttu-id="4a13c-103">Structure JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="4a13c-103">JET_INDEXID Structure</span></span>


<span data-ttu-id="4a13c-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="4a13c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_indexid-structure"></a><span data-ttu-id="4a13c-105">Structure JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="4a13c-105">JET_INDEXID Structure</span></span>

<span data-ttu-id="4a13c-106">La structure **JET_INDEXID** contient un ID d’index.</span><span class="sxs-lookup"><span data-stu-id="4a13c-106">The **JET_INDEXID** structure holds an index ID.</span></span> <span data-ttu-id="4a13c-107">Un ID d’index est un indicateur utilisé pour accélérer la sélection de l’index actuel à l’aide de [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="4a13c-107">An index ID is a hint that is used to accelerate the selection of the current index using [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span></span> <span data-ttu-id="4a13c-108">Elle est particulièrement utile lorsqu’il existe un très grand nombre d’index sur une table.</span><span class="sxs-lookup"><span data-stu-id="4a13c-108">It is most useful when there is a very large number of indexes over a table.</span></span> <span data-ttu-id="4a13c-109">L’ID d’index peut être récupéré à l’aide de [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="4a13c-109">The index ID can be retrieved using [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

```cpp
    typedef struct tagJET_INDEXID {
      unsigned long cbStruct;
      char rgbIndexId[sizeof(JET_API_PRT) + sizeof(unsigned long) + sizeof(unsigned long)];
    } JET_INDEXID;
```

### <a name="members"></a><span data-ttu-id="4a13c-110">Membres</span><span class="sxs-lookup"><span data-stu-id="4a13c-110">Members</span></span>

<span data-ttu-id="4a13c-111">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="4a13c-111">**cbStruct**</span></span>

<span data-ttu-id="4a13c-112">Taille, en octets, de l’ID d’index.</span><span class="sxs-lookup"><span data-stu-id="4a13c-112">The size, in bytes, of the index ID.</span></span>

<span data-ttu-id="4a13c-113">Il s’agit de la taille réelle de l’ID d’index qui est retourné dans la mémoire tampon de sortie à partir de [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="4a13c-113">This is the actual size of the index ID that is returned in the output buffer from [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

<span data-ttu-id="4a13c-114">**rgbIndexId**</span><span class="sxs-lookup"><span data-stu-id="4a13c-114">**rgbIndexId**</span></span>

<span data-ttu-id="4a13c-115">Objet BLOB opaque d’informations utilisé par le moteur pour identifier rapidement un index dans son cache de schéma.</span><span class="sxs-lookup"><span data-stu-id="4a13c-115">An opaque BLOB of information that is used by the engine to quickly identify an index in its schema cache.</span></span>

<span data-ttu-id="4a13c-116">N’essayez pas d’interpréter l’objet BLOB d’informations.</span><span class="sxs-lookup"><span data-stu-id="4a13c-116">Do not attempt to interpret the BLOB of information.</span></span> <span data-ttu-id="4a13c-117">Il ne s’agit pas d’une taille définie.</span><span class="sxs-lookup"><span data-stu-id="4a13c-117">It is not a set size.</span></span>

### <a name="requirements"></a><span data-ttu-id="4a13c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a13c-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4a13c-119"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="4a13c-119"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4a13c-120">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="4a13c-120">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a13c-121"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="4a13c-121"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4a13c-122">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4a13c-122">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a13c-123"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="4a13c-123"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4a13c-124">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="4a13c-124">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="4a13c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a13c-125">See Also</span></span>

[<span data-ttu-id="4a13c-126">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="4a13c-126">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="4a13c-127">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="4a13c-127">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="4a13c-128">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="4a13c-128">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)  
[<span data-ttu-id="4a13c-129">JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="4a13c-129">JetSetCurrentIndex</span></span>](./jetsetcurrentindex-function.md)
