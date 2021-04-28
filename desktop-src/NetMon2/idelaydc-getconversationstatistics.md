---
description: 'IDelaydC :: GetConversationStatistics, méthode : la méthode GetConversationStatistics récupère les informations de session et de station relatives à la capture en cours.'
ms.assetid: 0164fa0e-90f2-4b97-be9d-55d172f8112d
title: 'IDelaydC :: GetConversationStatistics, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d4d4c1bb1ad7ecb45b640c16322e297f9f640ef1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103807"
---
# <a name="idelaydcgetconversationstatistics-method"></a><span data-ttu-id="ba41d-103">IDelaydC :: GetConversationStatistics, méthode</span><span class="sxs-lookup"><span data-stu-id="ba41d-103">IDelaydC::GetConversationStatistics method</span></span>

<span data-ttu-id="ba41d-104">La méthode **GetConversationStatistics** récupère les informations de [*session*](s.md) et de [*station*](s.md) relatives à la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="ba41d-104">The **GetConversationStatistics** method retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba41d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba41d-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="ba41d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba41d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba41d-107">*nSessions* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ba41d-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba41d-108">Pointeur vers une valeur DWORD qui contient le nombre de [*sessions*](s.md) enregistrées pour la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="ba41d-108">Pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="ba41d-109">*lpSessionStats* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ba41d-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba41d-110">Pointeur vers une structure [SESSIONSTATS](sessionstats.md) .</span><span class="sxs-lookup"><span data-stu-id="ba41d-110">Pointer to a [SESSIONSTATS](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ba41d-111">*nStations* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ba41d-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba41d-112">Pointeur vers une valeur DWORD qui contient le nombre de [*stations*](s.md) enregistrées pour la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="ba41d-112">Pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="ba41d-113">*lpStationStats* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ba41d-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba41d-114">Pointeur vers une structure [STATIONSTATS](stationstats.md) .</span><span class="sxs-lookup"><span data-stu-id="ba41d-114">Pointer to a [STATIONSTATS](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ba41d-115">*fClearAfterReading* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba41d-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba41d-116">Indicateur utilisé pour indiquer à Moniteur réseau d’effacer le stockage interne des structures [SESSIONSTATS](sessionstats.md) et [STATIONSTATS](stationstats.md) après avoir récupéré les informations actuelles.</span><span class="sxs-lookup"><span data-stu-id="ba41d-116">Flag used to tell Network Monitor to clear out the internal storage of the [SESSIONSTATS](sessionstats.md) and [STATIONSTATS](stationstats.md) structures after it retrieves the current information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba41d-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ba41d-117">Return value</span></span>

<span data-ttu-id="ba41d-118">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="ba41d-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ba41d-119">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="ba41d-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="ba41d-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ba41d-120">Return code</span></span>                                                                                                   | <span data-ttu-id="ba41d-121">Description</span><span class="sxs-lookup"><span data-stu-id="ba41d-121">Description</span></span>                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ba41d-122"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="ba41d-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="ba41d-123">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="ba41d-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="ba41d-124">Appelez [IDelaydC :: Connect](idelaydc-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="ba41d-124">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="ba41d-125"><dt>**NMERR \_ pas de \_ capture**</dt></span><span class="sxs-lookup"><span data-stu-id="ba41d-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="ba41d-126">Le NPP ne capture pas de données.</span><span class="sxs-lookup"><span data-stu-id="ba41d-126">The NPP is not capturing data.</span></span> <span data-ttu-id="ba41d-127">Appelez [IDelaydC :: Start](idelaydc-start.md) pour démarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="ba41d-127">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="ba41d-128"><dt>**NMERR \_ non \_ retardé**</dt></span><span class="sxs-lookup"><span data-stu-id="ba41d-128"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>            | <span data-ttu-id="ba41d-129">Le NPP est connecté au réseau, mais pas avec la méthode [IDelaydC :: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="ba41d-129">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="ba41d-130"><dt>**NMERR \_ aucune \_ statistique de conversation \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ba41d-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="ba41d-131">La configuration de cette connexion est définie de façon à ne pas enregistrer les statistiques de conversation.</span><span class="sxs-lookup"><span data-stu-id="ba41d-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="ba41d-132">Pour enregistrer les statistiques de conversation, arrêtez la capture, définissez NoConversationStats = YES dans l’objet BLOB de configuration, puis redémarrez la capture.</span><span class="sxs-lookup"><span data-stu-id="ba41d-132">To save conversation statistics, stop the capture, set NoConversationStats = YES in the configuration BLOB, and then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ba41d-133">Notes </span><span class="sxs-lookup"><span data-stu-id="ba41d-133">Remarks</span></span>

<span data-ttu-id="ba41d-134">Cette méthode ne peut être appelée que lorsque la capture de données est en cours ; Lorsque la capture en cours est suspendue, les appels à cette méthode échouent.</span><span class="sxs-lookup"><span data-stu-id="ba41d-134">This method can only be called only while data capture is in progress; when the current capture is paused, calls to this method will not succeed.</span></span> <span data-ttu-id="ba41d-135">Pour démarrer une capture, appelez la méthode [IDelaydC :: Start](idelaydc-start.md) .</span><span class="sxs-lookup"><span data-stu-id="ba41d-135">To start a capture, call the [IDelaydC::Start](idelaydc-start.md) method.</span></span>

<span data-ttu-id="ba41d-136">Pour récupérer d’autres types de statistiques, appelez [IDelaydC :: GetTotalStatistics](idelaydc-gettotalstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="ba41d-136">To retrieve other types of statistics, call [IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba41d-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba41d-137">Requirements</span></span>



| <span data-ttu-id="ba41d-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba41d-138">Requirement</span></span> | <span data-ttu-id="ba41d-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba41d-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba41d-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba41d-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ba41d-141">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba41d-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="ba41d-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba41d-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ba41d-143">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba41d-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="ba41d-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba41d-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba41d-145"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba41d-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="ba41d-146">DLL</span><span class="sxs-lookup"><span data-stu-id="ba41d-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba41d-147"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba41d-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba41d-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba41d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba41d-149">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="ba41d-149">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="ba41d-150">IDelaydC :: Connect</span><span class="sxs-lookup"><span data-stu-id="ba41d-150">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="ba41d-151">IDelaydC::GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="ba41d-151">IDelaydC::GetTotalStatistics</span></span>](idelaydc-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="ba41d-152">IDelaydC :: Start</span><span class="sxs-lookup"><span data-stu-id="ba41d-152">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="ba41d-153">SESSIONSTATS</span><span class="sxs-lookup"><span data-stu-id="ba41d-153">SESSIONSTATS</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="ba41d-154">STATIONSTATS</span><span class="sxs-lookup"><span data-stu-id="ba41d-154">STATIONSTATS</span></span>](stationstats.md)
</dt> </dl>

 

 




