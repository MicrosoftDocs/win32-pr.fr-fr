---
description: 'En savoir plus sur : structure JET_RECPOS'
title: Structure JET_RECPOS
TOCTitle: JET_RECPOS Structure
ms:assetid: 7c335120-4b84-4095-8f13-e5315d4996b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269308(v=EXCHG.10)
ms:contentKeyID: 32765598
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
ms.openlocfilehash: e24e16aaac4228f35350f55f57a14f2820add0cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522105"
---
# <a name="jet_recpos-structure"></a><span data-ttu-id="9a830-103">Structure JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="9a830-103">JET_RECPOS Structure</span></span>


<span data-ttu-id="9a830-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="9a830-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recpos-structure"></a><span data-ttu-id="9a830-105">Structure JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="9a830-105">JET_RECPOS Structure</span></span>

<span data-ttu-id="9a830-106">La structure **JET_RECPOS** contient une collection d’entiers représentant une position fractionnaire dans un index.</span><span class="sxs-lookup"><span data-stu-id="9a830-106">The **JET_RECPOS** structure contains a collection of integers that represent a fractional position within an index.</span></span> <span data-ttu-id="9a830-107">**centriesLT** est le nombre d’entrées d’index inférieures à la clé d’index actuelle.</span><span class="sxs-lookup"><span data-stu-id="9a830-107">**centriesLT** is the number of index entries less than the current index key.</span></span> <span data-ttu-id="9a830-108">**centriesInRange** est le nombre d’entrées d’index égales à la clé actuelle.</span><span class="sxs-lookup"><span data-stu-id="9a830-108">**centriesInRange** is the number of index entries equal to the current key.</span></span> <span data-ttu-id="9a830-109">**centriesInRange** n’est pas pris en charge et est toujours retourné en tant que 1.</span><span class="sxs-lookup"><span data-stu-id="9a830-109">**centriesInRange** is not supported and is always returned as 1.</span></span> <span data-ttu-id="9a830-110">**centriesTotal** est le nombre d’entrées d’index dans l’index.</span><span class="sxs-lookup"><span data-stu-id="9a830-110">**centriesTotal** is the number of index entries in the index.</span></span> <span data-ttu-id="9a830-111">Toutes les valeurs sont des approximations sans garantie de précision.</span><span class="sxs-lookup"><span data-stu-id="9a830-111">All values are approximations with no guarantee of accuracy.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long centriesLT;
      unsigned long centriesInRange;
      unsigned long centriesTotal;
    } JET_RECPOS;
```

### <a name="members"></a><span data-ttu-id="9a830-112">Membres</span><span class="sxs-lookup"><span data-stu-id="9a830-112">Members</span></span>

<span data-ttu-id="9a830-113">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="9a830-113">**cbStruct**</span></span>

<span data-ttu-id="9a830-114">Taille de la structure [JET_RETINFO](./jet-retinfo-structure.md) , en octets.</span><span class="sxs-lookup"><span data-stu-id="9a830-114">The size of the [JET_RETINFO](./jet-retinfo-structure.md) structure, in bytes.</span></span> <span data-ttu-id="9a830-115">Cette valeur confirme la présence des champs suivants.</span><span class="sxs-lookup"><span data-stu-id="9a830-115">This value confirms the presence of the following fields.</span></span>

<span data-ttu-id="9a830-116">**centriesLT**</span><span class="sxs-lookup"><span data-stu-id="9a830-116">**centriesLT**</span></span>

<span data-ttu-id="9a830-117">Nombre approximatif d’entrées d’index inférieures à la clé actuelle.</span><span class="sxs-lookup"><span data-stu-id="9a830-117">The approximate number of index entries less than the current key.</span></span>

<span data-ttu-id="9a830-118">**centriesInRange**</span><span class="sxs-lookup"><span data-stu-id="9a830-118">**centriesInRange**</span></span>

<span data-ttu-id="9a830-119">Nombre approximatif d’entrées d’index égales à la clé actuelle.</span><span class="sxs-lookup"><span data-stu-id="9a830-119">The approximate number of index entries equal to the current key.</span></span> <span data-ttu-id="9a830-120">Ce champ a toujours la valeur 1, quel que soit le nombre d’entrées d’index qui sont réellement égales à la clé actuelle.</span><span class="sxs-lookup"><span data-stu-id="9a830-120">This field is always set to 1, regardless of the number of index entries that are actually equal to the current key.</span></span>

<span data-ttu-id="9a830-121">**centriesTotal**</span><span class="sxs-lookup"><span data-stu-id="9a830-121">**centriesTotal**</span></span>

<span data-ttu-id="9a830-122">Nombre approximatif d’entrées dans l’index.</span><span class="sxs-lookup"><span data-stu-id="9a830-122">The approximate number of entries in the index.</span></span>

### <a name="requirements"></a><span data-ttu-id="9a830-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a830-123">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a830-124"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="9a830-124"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9a830-125">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="9a830-125">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a830-126"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="9a830-126"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9a830-127">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9a830-127">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a830-128"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="9a830-128"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9a830-129">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="9a830-129">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="9a830-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a830-130">See Also</span></span>

[<span data-ttu-id="9a830-131">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="9a830-131">JET_RETINFO</span></span>](./jet-retinfo-structure.md)  
[<span data-ttu-id="9a830-132">JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="9a830-132">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)
