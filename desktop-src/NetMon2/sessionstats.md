---
description: La structure SESSIONSTATS fournit des statistiques sur une session.
ms.assetid: 51a6a601-634e-4d97-8c85-d3961400a2d1
title: SESSIONSTATS, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4eddfa6b0a45627c59e61fd083eb11b8d5f26caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202307"
---
# <a name="sessionstats-structure"></a><span data-ttu-id="9c60e-103">SESSIONSTATS, structure</span><span class="sxs-lookup"><span data-stu-id="9c60e-103">SESSIONSTATS structure</span></span>

<span data-ttu-id="9c60e-104">La structure **SESSIONSTATS** fournit des statistiques sur une [*session*](s.md).</span><span class="sxs-lookup"><span data-stu-id="9c60e-104">The **SESSIONSTATS** structure provides statistics about a [*session*](s.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9c60e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c60e-105">Syntax</span></span>


```C++
typedef struct _SESSIONSTATS {
  DWORD NextSession;
  DWORD StationOwner;
  DWORD StationPartner;
  DWORD Flags;
  DWORD TotalPacketsSent;
} SESSIONSTATS, *LPSESSIONSTATS;
```



## <a name="members"></a><span data-ttu-id="9c60e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="9c60e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9c60e-107">**NextSession**</span><span class="sxs-lookup"><span data-stu-id="9c60e-107">**NextSession**</span></span>
</dt> <dd>

<span data-ttu-id="9c60e-108">Index de la session suivante du propriétaire de la station.</span><span class="sxs-lookup"><span data-stu-id="9c60e-108">Index of the station owner's next session.</span></span>

</dd> <dt>

<span data-ttu-id="9c60e-109">**StationOwner**</span><span class="sxs-lookup"><span data-stu-id="9c60e-109">**StationOwner**</span></span>
</dt> <dd>

<span data-ttu-id="9c60e-110">Index d’une station propriétaire dans le tableau de structures [STATIONSTATS](stationstats.md) associées.</span><span class="sxs-lookup"><span data-stu-id="9c60e-110">Index of a owner station within the associated [STATIONSTATS](stationstats.md) structure array.</span></span> <span data-ttu-id="9c60e-111">La station propriétaire est la station qui a initié la session, la station qui a envoyé les paquets de la session.</span><span class="sxs-lookup"><span data-stu-id="9c60e-111">The owner station is the station that initiated the session, the station that sent the packets of the session.</span></span>

</dd> <dt>

<span data-ttu-id="9c60e-112">**StationPartner**</span><span class="sxs-lookup"><span data-stu-id="9c60e-112">**StationPartner**</span></span>
</dt> <dd>

<span data-ttu-id="9c60e-113">Index de l’autre station dans le tableau de structures [STATIONSTATS](stationstats.md) associé.</span><span class="sxs-lookup"><span data-stu-id="9c60e-113">Index of the other station within the associated [STATIONSTATS](stationstats.md) structure array.</span></span> <span data-ttu-id="9c60e-114">La station partenaire est la station qui a reçu les paquets de la session.</span><span class="sxs-lookup"><span data-stu-id="9c60e-114">The partner station is the station that received the packets of the session.</span></span>

</dd> <dt>

<span data-ttu-id="9c60e-115">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="9c60e-115">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="9c60e-116">Ce membre est obsolète.</span><span class="sxs-lookup"><span data-stu-id="9c60e-116">This member is obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="9c60e-117">**TotalPacketsSent**</span><span class="sxs-lookup"><span data-stu-id="9c60e-117">**TotalPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="9c60e-118">Nombre de paquets envoyés dans la session.</span><span class="sxs-lookup"><span data-stu-id="9c60e-118">Number of packets sent in the session.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c60e-119">Notes</span><span class="sxs-lookup"><span data-stu-id="9c60e-119">Remarks</span></span>

<span data-ttu-id="9c60e-120">Moniteur réseau stocke les informations de session et de station dans deux tableaux associés, dont les éléments sont respectivement des structures **SESSIONSTATS** et [STATIONSTATS](stationstats.md) .</span><span class="sxs-lookup"><span data-stu-id="9c60e-120">Network Monitor stores session and station information in two associated arrays, whose elements are **SESSIONSTATS** and [STATIONSTATS](stationstats.md) structures respectively.</span></span> <span data-ttu-id="9c60e-121">Les membres de ces structures peuvent être utilisés pour naviguer entre eux.</span><span class="sxs-lookup"><span data-stu-id="9c60e-121">The members of these structures can be used to navigate between them.</span></span> <span data-ttu-id="9c60e-122">Par exemple, pour passer à la session suivante pour un propriétaire de station spécifique, utilisez **NextSession**.</span><span class="sxs-lookup"><span data-stu-id="9c60e-122">For example, to move to the next session for a specific station owner, use **NextSession**.</span></span> <span data-ttu-id="9c60e-123">Pour accéder au propriétaire et à la station partenaire de la session dans le tableau STATIONSTATS, utilisez l’index fourni dans **StationOwner** et **StationPartner**.</span><span class="sxs-lookup"><span data-stu-id="9c60e-123">To jump to the owner and partner station of the session in the STATIONSTATS array, use the index provided in **StationOwner** and **StationPartner**.</span></span>

> [!Note]  
> <span data-ttu-id="9c60e-124">Le tableau SESSIONSTATS contient un élément pour chaque session dans la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="9c60e-124">The SESSIONSTATS array contains an element for each session in the current capture.</span></span> <span data-ttu-id="9c60e-125">L’algorithme Moniteur réseau utilise pour ajouter des éléments au tableau SESSIONSTATS est basé sur l’enregistrement efficace des informations lorsque la capture est en cours.</span><span class="sxs-lookup"><span data-stu-id="9c60e-125">The algorithm Network Monitor uses to add elements to the SESSIONSTATS array is based on efficiently recording information while the capture is in progress.</span></span> <span data-ttu-id="9c60e-126">Par conséquent, la session suivante pour une station propriétaire spécifique n’est pas toujours l’élément suivant dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="9c60e-126">Consequently, the next session for a specific owner station is not always the next element in the array.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9c60e-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c60e-127">Requirements</span></span>



| <span data-ttu-id="9c60e-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c60e-128">Requirement</span></span> | <span data-ttu-id="9c60e-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c60e-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9c60e-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c60e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9c60e-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c60e-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9c60e-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c60e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9c60e-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c60e-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9c60e-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="9c60e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c60e-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c60e-135"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c60e-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c60e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c60e-137">IDelaydC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="9c60e-137">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="9c60e-138">IRTC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="9c60e-138">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="9c60e-139">IStats::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="9c60e-139">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> </dl>

 

 




