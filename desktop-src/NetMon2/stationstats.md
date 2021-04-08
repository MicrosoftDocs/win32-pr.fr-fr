---
description: La structure STATIONSTATS fournit des statistiques sur une station spécifique décrite par la capture en cours.
ms.assetid: f85d53d6-f496-4242-875f-e173c76b046a
title: STATIONSTATS, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0b37d4570fe8f4c27ea66e6350b79e14a10e544e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034322"
---
# <a name="stationstats-structure"></a><span data-ttu-id="b5010-103">STATIONSTATS, structure</span><span class="sxs-lookup"><span data-stu-id="b5010-103">STATIONSTATS structure</span></span>

<span data-ttu-id="b5010-104">La structure **STATIONSTATS** fournit des statistiques sur une [*station*](s.md) spécifique décrite par la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="b5010-104">The **STATIONSTATS** structure provides statistics about a specific [*station*](s.md) described by the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5010-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5010-105">Syntax</span></span>


```C++
typedef struct _STATIONSTATS {
  DWORD NextStationStats;
  DWORD SessionPartnerList;
  DWORD Flags;
  BYTE  StationAddress[6];
  WORD  Pad;
  DWORD TotalPacketsReceived;
  DWORD TotalDirectedPacketsSent;
  DWORD TotalBroadcastPacketsSent;
  DWORD TotalMulticastPacketsSent;
  DWORD TotalBytesReceived;
  DWORD TotalBytesSent;
} STATIONSTATS, *LPSTATIONSTATS;
```



## <a name="members"></a><span data-ttu-id="b5010-106">Membres</span><span class="sxs-lookup"><span data-stu-id="b5010-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b5010-107">**NextStationStats**</span><span class="sxs-lookup"><span data-stu-id="b5010-107">**NextStationStats**</span></span>
</dt> <dd>

<span data-ttu-id="b5010-108">Index de la station suivante enregistrée dans le tableau de structures **STATIONSTATS** .</span><span class="sxs-lookup"><span data-stu-id="b5010-108">Index of the next station recorded in the **STATIONSTATS** structure array.</span></span>

</dd> <dt>

<span data-ttu-id="b5010-109">**SessionPartnerList**</span><span class="sxs-lookup"><span data-stu-id="b5010-109">**SessionPartnerList**</span></span>
</dt> <dd>

<span data-ttu-id="b5010-110">Index de la liste des partenaires de station.</span><span class="sxs-lookup"><span data-stu-id="b5010-110">Index of the station partner list.</span></span>

</dd> <dt>

<span data-ttu-id="b5010-111">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="b5010-111">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="b5010-112">Ce membre est obsolète.</span><span class="sxs-lookup"><span data-stu-id="b5010-112">This member is obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="b5010-113">**StationAddress**</span><span class="sxs-lookup"><span data-stu-id="b5010-113">**StationAddress**</span></span>
</dt> <dd>

<span data-ttu-id="b5010-114">Adresse MAC de la station.</span><span class="sxs-lookup"><span data-stu-id="b5010-114">The MAC address of the station.</span></span>

</dd> <dt>

<span data-ttu-id="b5010-115">**Remplir**</span><span class="sxs-lookup"><span data-stu-id="b5010-115">**Pad**</span></span>
</dt> <dd>

<span data-ttu-id="b5010-116">Alignement **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="b5010-116">**DWORD** alignment.</span></span>

</dd> <dt>

<span data-ttu-id="b5010-117">**TotalPacketsReceived**</span><span class="sxs-lookup"><span data-stu-id="b5010-117">**TotalPacketsReceived**</span></span>
</dt> <dd>

<span data-ttu-id="b5010-118">Nombre total de paquets envoyés à la station.</span><span class="sxs-lookup"><span data-stu-id="b5010-118">Total number of packets sent to the station.</span></span>

</dd> <dt>

<span data-ttu-id="b5010-119">**TotalDirectedPacketsSent**</span><span class="sxs-lookup"><span data-stu-id="b5010-119">**TotalDirectedPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="b5010-120">Nombre total de paquets dirigés envoyés par la station.</span><span class="sxs-lookup"><span data-stu-id="b5010-120">Total number of directed packets sent by the station.</span></span>

</dd> <dt>

<span data-ttu-id="b5010-121">**TotalBroadcastPacketsSent**</span><span class="sxs-lookup"><span data-stu-id="b5010-121">**TotalBroadcastPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="b5010-122">Nombre total de paquets dirigés par diffusion (adresse MAC FF FF FF FF FF FF) envoyés par la station.</span><span class="sxs-lookup"><span data-stu-id="b5010-122">Total number of broadcast-directed packets (MAC address FF FF FF FF FF FF) sent by the station.</span></span>

</dd> <dt>

<span data-ttu-id="b5010-123">**TotalMulticastPacketsSent**</span><span class="sxs-lookup"><span data-stu-id="b5010-123">**TotalMulticastPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="b5010-124">Nombre total de paquets de multidiffusion (bit de groupe défini dans l’adresse de destination) envoyés par la station.</span><span class="sxs-lookup"><span data-stu-id="b5010-124">Total number of multicast packets (Group bit set in destination address) sent by the station.</span></span>

</dd> <dt>

<span data-ttu-id="b5010-125">**TotalBytesReceived**</span><span class="sxs-lookup"><span data-stu-id="b5010-125">**TotalBytesReceived**</span></span>
</dt> <dd>

<span data-ttu-id="b5010-126">Nombre total d’octets envoyés à la station.</span><span class="sxs-lookup"><span data-stu-id="b5010-126">Total number of bytes sent to the station.</span></span>

</dd> <dt>

<span data-ttu-id="b5010-127">**TotalBytesSent**</span><span class="sxs-lookup"><span data-stu-id="b5010-127">**TotalBytesSent**</span></span>
</dt> <dd>

<span data-ttu-id="b5010-128">Nombre total d’octets envoyés par la station.</span><span class="sxs-lookup"><span data-stu-id="b5010-128">Total number of bytes sent by the station.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5010-129">Notes</span><span class="sxs-lookup"><span data-stu-id="b5010-129">Remarks</span></span>

<span data-ttu-id="b5010-130">Moniteur réseau stocke les informations de session et de station dans deux tableaux associés.</span><span class="sxs-lookup"><span data-stu-id="b5010-130">Network Monitor stores session and station information in two associated arrays.</span></span> <span data-ttu-id="b5010-131">dont les éléments sont respectivement des structures [SESSIONSTATS](sessionstats.md) et **STATIONSTATS** .</span><span class="sxs-lookup"><span data-stu-id="b5010-131">whose elements are [SESSIONSTATS](sessionstats.md) and **STATIONSTATS** structures respectively.</span></span> <span data-ttu-id="b5010-132">Les membres de ces structures peuvent être utilisés pour naviguer entre eux.</span><span class="sxs-lookup"><span data-stu-id="b5010-132">The members of these structures can be used to navigate between them.</span></span> <span data-ttu-id="b5010-133">Par exemple, pour passer à la station suivante, utilisez **NextStationStats**.</span><span class="sxs-lookup"><span data-stu-id="b5010-133">For example, to move to the next station use **NextStationStats**.</span></span> <span data-ttu-id="b5010-134">Pour accéder à la liste des partenaires de session dans le tableau SESSIONSTATS, utilisez l’index fourni dans **SessionPartnerList**.</span><span class="sxs-lookup"><span data-stu-id="b5010-134">To jump to the session partner list in the SESSIONSTATS array, use the index provided in **SessionPartnerList**.</span></span>

> [!Note]  
> <span data-ttu-id="b5010-135">Le tableau **STATIONSTATS** contient un élément pour chaque station utilisée pendant la capture actuelle.</span><span class="sxs-lookup"><span data-stu-id="b5010-135">The **STATIONSTATS** array contains an element for each station used during the current capture.</span></span> <span data-ttu-id="b5010-136">L’algorithme Moniteur réseau utilise pour ajouter des éléments à ce tableau est basé sur la méthode la plus efficace pour enregistrer des informations lorsque la capture est en cours.</span><span class="sxs-lookup"><span data-stu-id="b5010-136">The algorithm Network Monitor uses to add elements to this array is based on the most efficient way to record information while the capture is in progress.</span></span> <span data-ttu-id="b5010-137">Par conséquent, la station suivante n’est pas toujours l’élément suivant dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="b5010-137">Consequently, the next station is not always the next element in the array.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b5010-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5010-138">Requirements</span></span>



| <span data-ttu-id="b5010-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5010-139">Requirement</span></span> | <span data-ttu-id="b5010-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5010-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b5010-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5010-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b5010-142">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5010-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b5010-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5010-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b5010-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5010-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b5010-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5010-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5010-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5010-146"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5010-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5010-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5010-148">IDelaydC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="b5010-148">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="b5010-149">IRTC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="b5010-149">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="b5010-150">IStats::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="b5010-150">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> </dl>

 

 




