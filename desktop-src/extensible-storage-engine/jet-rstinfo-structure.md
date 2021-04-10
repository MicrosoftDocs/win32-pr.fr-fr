---
description: 'En savoir plus sur : structure JET_RSTINFO'
title: Structure JET_RSTINFO
TOCTitle: JET_RSTINFO Structure
ms:assetid: 2f144d68-dcd9-4d0d-9d9e-a7d2a5c350fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269216(v=EXCHG.10)
ms:contentKeyID: 32765519
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
ms.openlocfilehash: 3a776c84d89dfc97272c65bb0c0684faba814fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112550"
---
# <a name="jet_rstinfo-structure"></a><span data-ttu-id="f4f81-103">Structure JET_RSTINFO</span><span class="sxs-lookup"><span data-stu-id="f4f81-103">JET_RSTINFO Structure</span></span>


<span data-ttu-id="f4f81-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="f4f81-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_rstinfo-structure"></a><span data-ttu-id="f4f81-105">Structure JET_RSTINFO</span><span class="sxs-lookup"><span data-stu-id="f4f81-105">JET_RSTINFO Structure</span></span>

<span data-ttu-id="f4f81-106">La structure **JET_RSTINFO** contient les informations de contrôle du processus de récupération, telles que les informations de réadressage de la base de données et la possibilité de contrôler l’arrêt de la récupération.</span><span class="sxs-lookup"><span data-stu-id="f4f81-106">The **JET_RSTINFO** structure contains control information for the recovery process like database relocation information and ability to control stopping recovery.</span></span>

<span data-ttu-id="f4f81-107">**Windows Vista :** La structure **JET_RSTINFO** est introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f4f81-107">**Windows Vista:** The **JET_RSTINFO** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_RSTMAP* rgrstmap;
      long crstmap;
      JET_LGPOS lgposStop;
      JET_LOGTIME logtimeStop;
      JET_PFNSTATUS pfnStatus;
    } JET_RSTINFO;
```

### <a name="members"></a><span data-ttu-id="f4f81-108">Membres</span><span class="sxs-lookup"><span data-stu-id="f4f81-108">Members</span></span>

<span data-ttu-id="f4f81-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="f4f81-109">**cbStruct**</span></span>

<span data-ttu-id="f4f81-110">Taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="f4f81-110">The size of the structure.</span></span>

<span data-ttu-id="f4f81-111">**rgrstmap**</span><span class="sxs-lookup"><span data-stu-id="f4f81-111">**rgrstmap**</span></span>

<span data-ttu-id="f4f81-112">Structure qui décrit l’ancien et le nouveau chemin d’accès d’une base de données restaurée.</span><span class="sxs-lookup"><span data-stu-id="f4f81-112">The structure that describes the old and new path of a restored database.</span></span>

<span data-ttu-id="f4f81-113">**crstmap**</span><span class="sxs-lookup"><span data-stu-id="f4f81-113">**crstmap**</span></span>

<span data-ttu-id="f4f81-114">Nombre d’entrées de tableau dans le rgrstmap.</span><span class="sxs-lookup"><span data-stu-id="f4f81-114">Count of array entries in the rgrstmap.</span></span>

<span data-ttu-id="f4f81-115">**lgposStop**</span><span class="sxs-lookup"><span data-stu-id="f4f81-115">**lgposStop**</span></span>

<span data-ttu-id="f4f81-116">Position du journal sur laquelle arrêter la récupération.</span><span class="sxs-lookup"><span data-stu-id="f4f81-116">The log position to stop recovery at.</span></span> <span data-ttu-id="f4f81-117">Aucune annulation n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="f4f81-117">No undo will be done.</span></span>

<span data-ttu-id="f4f81-118">**logtimeStop**</span><span class="sxs-lookup"><span data-stu-id="f4f81-118">**logtimeStop**</span></span>

<span data-ttu-id="f4f81-119">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="f4f81-119">Reserved for future use.</span></span>

<span data-ttu-id="f4f81-120">**pfnStatus**</span><span class="sxs-lookup"><span data-stu-id="f4f81-120">**pfnStatus**</span></span>

<span data-ttu-id="f4f81-121">Fonction d’État pour signaler l’état de la récupération.</span><span class="sxs-lookup"><span data-stu-id="f4f81-121">A status function for reporting status of recovery.</span></span>

### <a name="requirements"></a><span data-ttu-id="f4f81-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4f81-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4f81-123"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f4f81-123"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f4f81-124">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="f4f81-124">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4f81-125"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="f4f81-125"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f4f81-126">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f4f81-126">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4f81-127"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="f4f81-127"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f4f81-128">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="f4f81-128">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4f81-129"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="f4f81-129"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="f4f81-130">Implémenté comme <strong>JET_RSTINFO_W</strong> (Unicode) et <strong>JET_RSTINFO_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f4f81-130">Implemented as <strong>JET_RSTINFO_W</strong> (Unicode) and <strong>JET_RSTINFO_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="f4f81-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4f81-131">See Also</span></span>

[<span data-ttu-id="f4f81-132">JetInit3</span><span class="sxs-lookup"><span data-stu-id="f4f81-132">JetInit3</span></span>](./jetinit3-function.md)
