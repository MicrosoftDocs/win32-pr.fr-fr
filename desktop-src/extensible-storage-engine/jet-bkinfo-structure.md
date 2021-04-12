---
description: 'En savoir plus sur : structure JET_BKINFO'
title: Structure JET_BKINFO
TOCTitle: JET_BKINFO Structure
ms:assetid: dfaf1d72-1d5f-4777-91c1-6affb735b092
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294120(v=EXCHG.10)
ms:contentKeyID: 32765734
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
ms.openlocfilehash: 6c4849c23e742657d8f5eaba8a030426f7a2a440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210118"
---
# <a name="jet_bkinfo-structure"></a><span data-ttu-id="18a0f-103">Structure JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="18a0f-103">JET_BKINFO Structure</span></span>


<span data-ttu-id="18a0f-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="18a0f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_bkinfo-structure"></a><span data-ttu-id="18a0f-105">Structure JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="18a0f-105">JET_BKINFO Structure</span></span>

<span data-ttu-id="18a0f-106">La structure **JET_BKINFO** contient une collection de données relatives à un événement de sauvegarde spécifique.</span><span class="sxs-lookup"><span data-stu-id="18a0f-106">The **JET_BKINFO** structure holds a collection of data about a specific backup event.</span></span>

```cpp
    typedef struct {
      JET_LGPOS lgposMark;
      union {
        JET_LOGTIME logtimeMark;
        JET_BKLOGTIME bklogtimeMark;
      };
      unsigned long genLow;
      unsigned long genHigh;
    } JET_BKINFO;
```

### <a name="members"></a><span data-ttu-id="18a0f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="18a0f-107">Members</span></span>

<span data-ttu-id="18a0f-108">**lgposMark**</span><span class="sxs-lookup"><span data-stu-id="18a0f-108">**lgposMark**</span></span>

<span data-ttu-id="18a0f-109">ID de cette sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="18a0f-109">The ID of this backup.</span></span>

<span data-ttu-id="18a0f-110">**logtimeMark**</span><span class="sxs-lookup"><span data-stu-id="18a0f-110">**logtimeMark**</span></span>

<span data-ttu-id="18a0f-111">Heure de l’événement de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="18a0f-111">The time of this backup event.</span></span>

<span data-ttu-id="18a0f-112">**bklogtimeMark**</span><span class="sxs-lookup"><span data-stu-id="18a0f-112">**bklogtimeMark**</span></span>

<span data-ttu-id="18a0f-113">L’heure de cet événement de sauvegarde, avec des bits supplémentaires pour indiquer une sauvegarde d’instantané.</span><span class="sxs-lookup"><span data-stu-id="18a0f-113">The time of this backup event, with additional bits to indicate a snapshot backup.</span></span>

<span data-ttu-id="18a0f-114">**Windows Vista : bklogtimeMark** est introduit dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="18a0f-114">**Windows Vista:  bklogtimeMark** is introduced in Windows Vista.</span></span>

<span data-ttu-id="18a0f-115">**genLow**</span><span class="sxs-lookup"><span data-stu-id="18a0f-115">**genLow**</span></span>

<span data-ttu-id="18a0f-116">Numéro de génération de journal faible associé à cet événement de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="18a0f-116">The low log generation number associated with this backup event.</span></span>

<span data-ttu-id="18a0f-117">**genHigh**</span><span class="sxs-lookup"><span data-stu-id="18a0f-117">**genHigh**</span></span>

<span data-ttu-id="18a0f-118">Numéro de génération de journal élevé associé à cet événement de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="18a0f-118">The high log generation number associated with this backup event.</span></span>

### <a name="remarks"></a><span data-ttu-id="18a0f-119">Notes</span><span class="sxs-lookup"><span data-stu-id="18a0f-119">Remarks</span></span>

<span data-ttu-id="18a0f-120">Cette structure est utilisée à l’intérieur de la structure [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) pour représenter des données relatives à l’événement de sauvegarde de la base de données.</span><span class="sxs-lookup"><span data-stu-id="18a0f-120">This structure is used inside the [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) structure to represent data about the database backup event.</span></span>

### <a name="requirements"></a><span data-ttu-id="18a0f-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18a0f-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18a0f-122"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="18a0f-122"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="18a0f-123">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="18a0f-123">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18a0f-124"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="18a0f-124"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="18a0f-125">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="18a0f-125">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18a0f-126"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="18a0f-126"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="18a0f-127">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="18a0f-127">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="18a0f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18a0f-128">See Also</span></span>

[<span data-ttu-id="18a0f-129">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="18a0f-129">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="18a0f-130">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="18a0f-130">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="18a0f-131">JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="18a0f-131">JET_BKLOGTIME</span></span>](./jet-bklogtime-structure.md)  
[<span data-ttu-id="18a0f-132">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="18a0f-132">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
