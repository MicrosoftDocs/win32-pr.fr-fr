---
description: 'IStats :: GetTotalStatistics, méthode : la méthode GetTotalStatistics récupère les statistiques totales pour la capture actuelle.'
ms.assetid: 494634f6-a9b3-4a50-8920-2387be9ba30f
title: 'IStats :: GetTotalStatistics, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: e6566a58212e8f20d0d999302f41ab97cb9f005e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098407"
---
# <a name="istatsgettotalstatistics-method"></a><span data-ttu-id="9bc12-103">IStats :: GetTotalStatistics, méthode</span><span class="sxs-lookup"><span data-stu-id="9bc12-103">IStats::GetTotalStatistics method</span></span>

<span data-ttu-id="9bc12-104">La méthode **GetTotalStatistics** récupère les [*statistiques totales*](t.md) pour la [*capture*](c.md)en cours.</span><span class="sxs-lookup"><span data-stu-id="9bc12-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9bc12-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9bc12-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="9bc12-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9bc12-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bc12-107">*lpStats* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9bc12-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bc12-108">Pointeur vers une structure de [statistiques](statistics.md)qui fournit le total des statistiques pour la capture.</span><span class="sxs-lookup"><span data-stu-id="9bc12-108">Pointer to a [STATISTICS](statistics.md)structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="9bc12-109">Il incombe à l’appelant d’allouer et de libérer la mémoire utilisée par la structure des **statistiques** .</span><span class="sxs-lookup"><span data-stu-id="9bc12-109">It is the caller's responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="9bc12-110">*fClearAfterReading* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9bc12-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bc12-111">Indicateur utilisé pour indiquer Moniteur réseau comment gérer le stockage interne du total des statistiques.</span><span class="sxs-lookup"><span data-stu-id="9bc12-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="9bc12-112">La valeur TRUE indique Moniteur réseau d’effacer le stockage interne du total des statistiques une fois que les informations actuelles ont été récupérées.</span><span class="sxs-lookup"><span data-stu-id="9bc12-112">A setting of TRUE tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bc12-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9bc12-113">Return value</span></span>

<span data-ttu-id="9bc12-114">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="9bc12-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="9bc12-115">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="9bc12-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="9bc12-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9bc12-116">Return code</span></span>                                                                                            | <span data-ttu-id="9bc12-117">Description</span><span class="sxs-lookup"><span data-stu-id="9bc12-117">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9bc12-118"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="9bc12-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="9bc12-119">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="9bc12-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="9bc12-120">Appelez la méthode [IStats :: Connect](istats-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="9bc12-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="9bc12-121"><dt>**NMERR \_ non \_ stats \_ uniquement**</dt></span><span class="sxs-lookup"><span data-stu-id="9bc12-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="9bc12-122">Le NPP est connecté au réseau, mais pas avec la méthode [IStats :: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="9bc12-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |
| <dl> <span data-ttu-id="9bc12-123"><dt>**NMERR \_ pas de \_ capture**</dt></span><span class="sxs-lookup"><span data-stu-id="9bc12-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="9bc12-124">Le NPP ne capture pas de données.</span><span class="sxs-lookup"><span data-stu-id="9bc12-124">The NPP is not capturing data.</span></span> <span data-ttu-id="9bc12-125">Appelez la méthode [IStats :: Start](istats-start.md) pour commencer à capturer des données.</span><span class="sxs-lookup"><span data-stu-id="9bc12-125">Call the [IStats::Start](istats-start.md) method to start capturing data.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="9bc12-126">Notes </span><span class="sxs-lookup"><span data-stu-id="9bc12-126">Remarks</span></span>

<span data-ttu-id="9bc12-127">Cette méthode retourne les données uniquement lorsqu’une capture est en cours, y compris pendant la suspension de la capture.</span><span class="sxs-lookup"><span data-stu-id="9bc12-127">This method returns data only while a capture is in progress, including while the capture is paused.</span></span>

<span data-ttu-id="9bc12-128">Moniteur réseau stocke également les [*statistiques de conversation*](c.md), qui peuvent être récupérées en appelant la méthode [IStats :: GetConversationStatistics](istats-getconversationstatistics.md) .</span><span class="sxs-lookup"><span data-stu-id="9bc12-128">Network Monitor also stores [*conversation statistics*](c.md), which can be retrieved by calling the [IStats::GetConversationStatistics](istats-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bc12-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9bc12-129">Requirements</span></span>



| <span data-ttu-id="9bc12-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9bc12-130">Requirement</span></span> | <span data-ttu-id="9bc12-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="9bc12-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bc12-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9bc12-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9bc12-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9bc12-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="9bc12-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9bc12-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9bc12-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9bc12-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="9bc12-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="9bc12-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bc12-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bc12-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="9bc12-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9bc12-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bc12-139"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bc12-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bc12-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bc12-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bc12-141">IStats</span><span class="sxs-lookup"><span data-stu-id="9bc12-141">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="9bc12-142">IStats :: Connect</span><span class="sxs-lookup"><span data-stu-id="9bc12-142">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="9bc12-143">IStats::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="9bc12-143">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="9bc12-144">IStats :: Start,</span><span class="sxs-lookup"><span data-stu-id="9bc12-144">IStats::Start,</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="9bc12-145">PORTENT</span><span class="sxs-lookup"><span data-stu-id="9bc12-145">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




