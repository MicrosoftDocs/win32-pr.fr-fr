---
description: La méthode GetConversationStatistics récupère les informations de session et de station relatives à la capture en cours.
ms.assetid: 27f364cd-fee9-4262-b181-c5f15fb12e51
title: 'IRTC :: GetConversationStatistics, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 758488cb3c3f65922bbf6aac4f39774a5430fc92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864070"
---
# <a name="irtcgetconversationstatistics-method"></a><span data-ttu-id="59847-103">IRTC :: GetConversationStatistics, méthode</span><span class="sxs-lookup"><span data-stu-id="59847-103">IRTC::GetConversationStatistics method</span></span>

<span data-ttu-id="59847-104">La méthode **GetConversationStatistics** récupère les informations de [*session*](s.md) et de [*station*](s.md) relatives à la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="59847-104">The **GetConversationStatistics** method retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="59847-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59847-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="59847-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59847-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59847-107">*nSessions* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="59847-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59847-108">Pointeur vers une valeur DWORD qui contient le nombre de [*sessions*](s.md) enregistrées pour la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="59847-108">Pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="59847-109">*lpSessionStats* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="59847-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59847-110">Pointeur vers une structure [SESSIONSTATS](sessionstats.md) .</span><span class="sxs-lookup"><span data-stu-id="59847-110">Pointer to a [SESSIONSTATS](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="59847-111">*nStations* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="59847-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59847-112">Pointeur vers une valeur DWORD qui contient le nombre de [*stations*](s.md) enregistrées pour la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="59847-112">Pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="59847-113">*lpStationStats* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="59847-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59847-114">Pointeur vers une structure [STATIONSTATS](stationstats.md) .</span><span class="sxs-lookup"><span data-stu-id="59847-114">Pointer to a [STATIONSTATS](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="59847-115">*fClearAfterReading* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59847-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59847-116">Indicateur utilisé pour indiquer à Moniteur réseau d’effacer le stockage interne des structures [SESSIONSTATS](sessionstats.md) et [STATIONSTATS](stationstats.md) après avoir récupéré les informations actuelles.</span><span class="sxs-lookup"><span data-stu-id="59847-116">Flag used to tell Network Monitor to clear out the internal storage of the [SESSIONSTATS](sessionstats.md) and [STATIONSTATS](stationstats.md) structures after it retrieves the current information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59847-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59847-117">Return value</span></span>

<span data-ttu-id="59847-118">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="59847-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="59847-119">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="59847-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="59847-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="59847-120">Return code</span></span>                                                                                                   | <span data-ttu-id="59847-121">Description</span><span class="sxs-lookup"><span data-stu-id="59847-121">Description</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="59847-122"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="59847-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="59847-123">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="59847-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="59847-124">Appelez [IRTC :: Connect](irtc-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="59847-124">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="59847-125"><dt>**NMERR \_ pas de \_ capture**</dt></span><span class="sxs-lookup"><span data-stu-id="59847-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="59847-126">Le NPP ne capture pas de données.</span><span class="sxs-lookup"><span data-stu-id="59847-126">The NPP is not capturing data.</span></span> <span data-ttu-id="59847-127">Appelez [IRTC :: Start](irtc-start.md) pour démarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="59847-127">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="59847-128"><dt>**NMERR \_ pas de \_ temps réel**</dt></span><span class="sxs-lookup"><span data-stu-id="59847-128"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>           | <span data-ttu-id="59847-129">Le NPP est connecté au réseau, mais pas avec la méthode [IRTC :: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="59847-129">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                                                                                                                          |
| <dl> <span data-ttu-id="59847-130"><dt>**NMERR \_ aucune \_ statistique de conversation \_**</dt></span><span class="sxs-lookup"><span data-stu-id="59847-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="59847-131">La configuration de cette connexion est définie de façon à ne pas enregistrer les statistiques de conversation.</span><span class="sxs-lookup"><span data-stu-id="59847-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="59847-132">Pour enregistrer les statistiques de conversation, arrêtez la capture, définissez NoConversationStats = YES dans l’objet BLOB de configuration, puis redémarrez la capture.</span><span class="sxs-lookup"><span data-stu-id="59847-132">To save conversation statistics, stop the capture, set NoConversationStats = YES in the configuration BLOB, then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="59847-133">Notes</span><span class="sxs-lookup"><span data-stu-id="59847-133">Remarks</span></span>

<span data-ttu-id="59847-134">Cette méthode peut uniquement être appelée pendant que vous capturez des données ; Si vous appelez cette méthode alors que la capture en cours est suspendue, la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="59847-134">This method can only be called while you are capturing data; if you call this method while the current capture is paused, the method will not succeed.</span></span> <span data-ttu-id="59847-135">Pour démarrer une capture, appelez la méthode [IRTC :: Start](irtc-start.md) .</span><span class="sxs-lookup"><span data-stu-id="59847-135">To start a capture, call the [IRTC::Start](irtc-start.md) method.</span></span>

<span data-ttu-id="59847-136">Pour récupérer d’autres types de statistiques, appelez la méthode [IRTC :: GetTotalStatistics](irtc-gettotalstatistics.md) .</span><span class="sxs-lookup"><span data-stu-id="59847-136">To retrieve other types of statistics, call the [IRTC::GetTotalStatistics](irtc-gettotalstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="59847-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59847-137">Requirements</span></span>



| <span data-ttu-id="59847-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59847-138">Requirement</span></span> | <span data-ttu-id="59847-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="59847-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59847-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59847-140">Minimum supported client</span></span><br/> | <span data-ttu-id="59847-141">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59847-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="59847-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59847-142">Minimum supported server</span></span><br/> | <span data-ttu-id="59847-143">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59847-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="59847-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="59847-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="59847-145"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="59847-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="59847-146">DLL</span><span class="sxs-lookup"><span data-stu-id="59847-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59847-147"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59847-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59847-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59847-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59847-149">IRTC</span><span class="sxs-lookup"><span data-stu-id="59847-149">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="59847-150">IRTC :: Connect</span><span class="sxs-lookup"><span data-stu-id="59847-150">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="59847-151">IRTC::GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="59847-151">IRTC::GetTotalStatistics</span></span>](irtc-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="59847-152">IRTC :: Start</span><span class="sxs-lookup"><span data-stu-id="59847-152">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="59847-153">SESSIONSTATS</span><span class="sxs-lookup"><span data-stu-id="59847-153">SESSIONSTATS</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="59847-154">STATIONSTATS</span><span class="sxs-lookup"><span data-stu-id="59847-154">STATIONSTATS</span></span>](stationstats.md)
</dt> </dl>

 

 




