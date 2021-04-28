---
description: 'IRTC :: GetTotalStatistics, méthode : la méthode GetTotalStatistics récupère les statistiques totales pour la capture actuelle.'
ms.assetid: e5098984-c69e-4cd5-9143-d85dfcbd7b92
title: 'IRTC :: GetTotalStatistics, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 8ed659efe388f4eb9c9ac8afd6aa2c74fd0af7d3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110687"
---
# <a name="irtcgettotalstatistics-method"></a><span data-ttu-id="119ce-103">IRTC :: GetTotalStatistics, méthode</span><span class="sxs-lookup"><span data-stu-id="119ce-103">IRTC::GetTotalStatistics method</span></span>

<span data-ttu-id="119ce-104">La méthode **GetTotalStatistics** récupère les [*statistiques totales*](t.md) pour la [*capture*](c.md)en cours.</span><span class="sxs-lookup"><span data-stu-id="119ce-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="119ce-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="119ce-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="119ce-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="119ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="119ce-107">*lpStats* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="119ce-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="119ce-108">Pointeur vers une structure de [statistiques](statistics.md) qui fournit le total des statistiques pour la capture.</span><span class="sxs-lookup"><span data-stu-id="119ce-108">Pointer to a [STATISTICS](statistics.md) structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="119ce-109">Il incombe aux appelants d’allouer et de libérer la mémoire utilisée par la structure des **statistiques** .</span><span class="sxs-lookup"><span data-stu-id="119ce-109">It is the callers responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="119ce-110">*fClearAfterReading* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="119ce-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="119ce-111">Indicateur utilisé pour indiquer Moniteur réseau comment gérer le stockage interne du total des statistiques.</span><span class="sxs-lookup"><span data-stu-id="119ce-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="119ce-112">La **valeur true** indique Moniteur réseau d’effacer le stockage interne du total des statistiques une fois que les informations actuelles ont été récupérées.</span><span class="sxs-lookup"><span data-stu-id="119ce-112">A setting of **TRUE** tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="119ce-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="119ce-113">Return value</span></span>

<span data-ttu-id="119ce-114">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="119ce-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="119ce-115">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="119ce-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="119ce-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="119ce-116">Return code</span></span>                                                                                          | <span data-ttu-id="119ce-117">Description</span><span class="sxs-lookup"><span data-stu-id="119ce-117">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="119ce-118"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="119ce-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="119ce-119">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="119ce-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="119ce-120">Appelez [IRTC :: Connect](irtc-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="119ce-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="119ce-121"><dt>**NMERR \_ pas de \_ temps réel**</dt></span><span class="sxs-lookup"><span data-stu-id="119ce-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="119ce-122">Le NPP est connecté au réseau, mais pas avec la méthode [IRTC :: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="119ce-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |
| <dl> <span data-ttu-id="119ce-123"><dt>**NMERR \_ pas de \_ capture**</dt></span><span class="sxs-lookup"><span data-stu-id="119ce-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="119ce-124">Le NPP ne capture pas de données.</span><span class="sxs-lookup"><span data-stu-id="119ce-124">The NPP is not capturing data.</span></span> <span data-ttu-id="119ce-125">Appelez [IRTC :: Start](irtc-start.md) pour commencer à capturer des données.</span><span class="sxs-lookup"><span data-stu-id="119ce-125">Call [IRTC::Start](irtc-start.md) to start capturing data.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="119ce-126">Notes </span><span class="sxs-lookup"><span data-stu-id="119ce-126">Remarks</span></span>

<span data-ttu-id="119ce-127">Cette méthode retourne les données uniquement lorsqu’une capture est en cours, y compris pendant la suspension de la capture.</span><span class="sxs-lookup"><span data-stu-id="119ce-127">This method returns data only while a capture is in progress, including while the capture is paused.</span></span>

<span data-ttu-id="119ce-128">Moniteur réseau stocke également les [*statistiques de conversation*](c.md).</span><span class="sxs-lookup"><span data-stu-id="119ce-128">Network Monitor also stores [*conversation statistics*](c.md).</span></span> <span data-ttu-id="119ce-129">Pour récupérer des statistiques de conversation, appelez la méthode [IRTC :: GetConversationStatistics](irtc-getconversationstatistics.md) .</span><span class="sxs-lookup"><span data-stu-id="119ce-129">To retrieve conversation statistics, call the [IRTC::GetConversationStatistics](irtc-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="119ce-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="119ce-130">Requirements</span></span>



| <span data-ttu-id="119ce-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="119ce-131">Requirement</span></span> | <span data-ttu-id="119ce-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="119ce-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="119ce-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="119ce-133">Minimum supported client</span></span><br/> | <span data-ttu-id="119ce-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="119ce-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="119ce-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="119ce-135">Minimum supported server</span></span><br/> | <span data-ttu-id="119ce-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="119ce-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="119ce-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="119ce-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="119ce-138"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="119ce-138"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="119ce-139">DLL</span><span class="sxs-lookup"><span data-stu-id="119ce-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="119ce-140"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="119ce-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="119ce-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="119ce-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="119ce-142">IRTC</span><span class="sxs-lookup"><span data-stu-id="119ce-142">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="119ce-143">IRTC :: Connect</span><span class="sxs-lookup"><span data-stu-id="119ce-143">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="119ce-144">IRTC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="119ce-144">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="119ce-145">IRTC :: Start</span><span class="sxs-lookup"><span data-stu-id="119ce-145">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="119ce-146">PORTENT</span><span class="sxs-lookup"><span data-stu-id="119ce-146">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




