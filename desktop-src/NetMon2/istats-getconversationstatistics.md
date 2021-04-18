---
description: Récupère les informations de session et de station relatives à la capture en cours.
ms.assetid: 7fc436fc-b569-402d-a1ea-c1bb65de8a9e
title: 'IStats :: GetConversationStatistics, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 030fafb4ccf041c2804179f8adf0088ca3fba845
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523082"
---
# <a name="istatsgetconversationstatistics-method"></a><span data-ttu-id="28c07-103">IStats :: GetConversationStatistics, méthode</span><span class="sxs-lookup"><span data-stu-id="28c07-103">IStats::GetConversationStatistics method</span></span>

<span data-ttu-id="28c07-104">La méthode **GetConversationStatistics** récupère les informations de session et de station relatives à la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="28c07-104">The **GetConversationStatistics** method retrieves session and station information about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="28c07-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28c07-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="28c07-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28c07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28c07-107">*nSessions* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="28c07-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28c07-108">Pointeur vers une valeur DWORD qui contient le nombre de [*sessions*](s.md) enregistrées pour la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="28c07-108">A pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="28c07-109">*lpSessionStats* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="28c07-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28c07-110">Pointeur vers une structure [**SESSIONSTATS**](sessionstats.md) .</span><span class="sxs-lookup"><span data-stu-id="28c07-110">A pointer to a [**SESSIONSTATS**](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="28c07-111">*nStations* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="28c07-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28c07-112">Pointeur vers une valeur DWORD qui contient le nombre de [*stations*](s.md) enregistrées pour la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="28c07-112">A pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="28c07-113">*lpStationStats* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="28c07-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28c07-114">Pointeur vers une structure [**STATIONSTATS**](stationstats.md) .</span><span class="sxs-lookup"><span data-stu-id="28c07-114">A pointer to a [**STATIONSTATS**](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="28c07-115">*fClearAfterReading* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28c07-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28c07-116">Indicateur utilisé pour indiquer à Moniteur réseau d’effacer le stockage interne des structures [**SESSIONSTATS**](sessionstats.md) et [**STATIONSTATS**](stationstats.md) une fois que les données actuelles ont été récupérées.</span><span class="sxs-lookup"><span data-stu-id="28c07-116">Flag used to instruct Network Monitor to clear the internal storage of the [**SESSIONSTATS**](sessionstats.md) and [**STATIONSTATS**](stationstats.md) structures after the current data is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28c07-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28c07-117">Return value</span></span>

<span data-ttu-id="28c07-118">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="28c07-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="28c07-119">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="28c07-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="28c07-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="28c07-120">Return code</span></span>                                                                                                   | <span data-ttu-id="28c07-121">Description</span><span class="sxs-lookup"><span data-stu-id="28c07-121">Description</span></span>                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="28c07-122"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="28c07-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="28c07-123">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="28c07-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="28c07-124">Appelez [**IStats :: Connect**](istats-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="28c07-124">Call [**IStats::Connect**](istats-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="28c07-125"><dt>**NMERR \_ pas de \_ capture**</dt></span><span class="sxs-lookup"><span data-stu-id="28c07-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="28c07-126">Le NPP ne capture pas de données.</span><span class="sxs-lookup"><span data-stu-id="28c07-126">The NPP is not capturing data.</span></span> <span data-ttu-id="28c07-127">Appelez [**IStats :: Start**](istats-start.md) pour démarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="28c07-127">Call [**IStats::Start**](istats-start.md) to start the capture.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="28c07-128"><dt>**NMERR \_ non \_ stats \_ uniquement**</dt></span><span class="sxs-lookup"><span data-stu-id="28c07-128"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl>        | <span data-ttu-id="28c07-129">Le NPP est connecté au réseau, mais pas avec la méthode [**IStats :: Connect**](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="28c07-129">The NPP is connected to the network, but not with the [**IStats::Connect**](istats-connect.md) method.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="28c07-130"><dt>**NMERR \_ aucune \_ statistique de conversation \_**</dt></span><span class="sxs-lookup"><span data-stu-id="28c07-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="28c07-131">La configuration de cette connexion est définie de façon à ne pas enregistrer les statistiques de conversation.</span><span class="sxs-lookup"><span data-stu-id="28c07-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="28c07-132">Pour enregistrer les statistiques de conversation, arrêtez la capture, définissez **NoConversationStats = Yes** dans l’objet blob de configuration, puis redémarrez la capture.</span><span class="sxs-lookup"><span data-stu-id="28c07-132">To save conversation statistics, stop the capture, set **NoConversationStats = YES** in the configuration BLOB, and then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="28c07-133">Notes</span><span class="sxs-lookup"><span data-stu-id="28c07-133">Remarks</span></span>

<span data-ttu-id="28c07-134">Cette méthode peut être appelée uniquement lorsque la capture de données est en cours ; Lorsque la capture en cours est suspendue, un appel à cette méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="28c07-134">This method can be called only while data capture is in progress; when the current capture is paused, a call to this method will not succeed.</span></span>

<span data-ttu-id="28c07-135">Pour démarrer une capture, appelez la méthode [**IStats :: Start**](istats-start.md) .</span><span class="sxs-lookup"><span data-stu-id="28c07-135">To start a capture, call the [**IStats::Start**](istats-start.md) method.</span></span> <span data-ttu-id="28c07-136">Pour récupérer d’autres types de statistiques, appelez [**IStats :: GetTotalStatistics**](istats-gettotalstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="28c07-136">To retrieve other types of statistics, call [**IStats::GetTotalStatistics**](istats-gettotalstatistics.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="28c07-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28c07-137">Requirements</span></span>



| <span data-ttu-id="28c07-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28c07-138">Requirement</span></span> | <span data-ttu-id="28c07-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="28c07-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28c07-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28c07-140">Minimum supported client</span></span><br/> | <span data-ttu-id="28c07-141">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28c07-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="28c07-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28c07-142">Minimum supported server</span></span><br/> | <span data-ttu-id="28c07-143">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28c07-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="28c07-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="28c07-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="28c07-145"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="28c07-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="28c07-146">DLL</span><span class="sxs-lookup"><span data-stu-id="28c07-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28c07-147"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28c07-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28c07-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28c07-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28c07-149">**IStats**</span><span class="sxs-lookup"><span data-stu-id="28c07-149">**IStats**</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="28c07-150">**IStats::GetTotalStatistics**</span><span class="sxs-lookup"><span data-stu-id="28c07-150">**IStats::GetTotalStatistics**</span></span>](istats-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="28c07-151">**IStats :: Start**</span><span class="sxs-lookup"><span data-stu-id="28c07-151">**IStats::Start**</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="28c07-152">**IStats :: Connect**</span><span class="sxs-lookup"><span data-stu-id="28c07-152">**IStats::Connect**</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="28c07-153">**SESSIONSTATS**</span><span class="sxs-lookup"><span data-stu-id="28c07-153">**SESSIONSTATS**</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="28c07-154">**STATIONSTATS**</span><span class="sxs-lookup"><span data-stu-id="28c07-154">**STATIONSTATS**</span></span>](stationstats.md)
</dt> </dl>

 

 




