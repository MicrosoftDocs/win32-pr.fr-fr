---
description: Demandes de mise en cache du rapport d’analyse hors connexion des frames spécifiés.
MS-HAID: vspixengine.IOfflineAnalysisCacheRequest\_RequestOfflineAnalysisReportAvailabilityAsync\_DWORD\_DWORD\_arr\_IOfflineAnalysisCacheCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IOfflineAnalysisCacheRequest :: RequestOfflineAnalysisReportAvailabilityAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10FA71F8-813D-4788-92C8-00B30A9AE5CC
api_name:
- IOfflineAnalysisCacheRequest.RequestOfflineAnalysisReportAvailabilityAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6e2dfdb1e2a2cc113f9585a818550dd60aa73ae2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522743"
---
# <a name="span-idvspixengineiofflineanalysiscacherequest_requestofflineanalysisreportavailabilityasync_dword_dword_arr_iofflineanalysiscachecallback_ptrspaniofflineanalysiscacherequestrequestofflineanalysisreportavailabilityasync-method"></a><span data-ttu-id="0f489-103"><span id="vspixengine.iofflineanalysiscacherequest_requestofflineanalysisreportavailabilityasync_dword_dword_arr_iofflineanalysiscachecallback_ptr"></span>IOfflineAnalysisCacheRequest :: RequestOfflineAnalysisReportAvailabilityAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="0f489-103"><span id="vspixengine.iofflineanalysiscacherequest_requestofflineanalysisreportavailabilityasync_dword_dword_arr_iofflineanalysiscachecallback_ptr"></span>IOfflineAnalysisCacheRequest::RequestOfflineAnalysisReportAvailabilityAsync method</span></span>

<span data-ttu-id="0f489-104">Demandes de mise en cache du rapport d’analyse hors connexion des frames spécifiés.</span><span class="sxs-lookup"><span data-stu-id="0f489-104">Requests to cache offline analysis report of the specified frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f489-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f489-105">Syntax</span></span>


```C++
HRESULT RequestOfflineAnalysisReportAvailabilityAsync(
   DWORD                           numFrames,
   DWORD []                        count0_frameNumbers,
   IOfflineAnalysisCacheCallback * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="0f489-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f489-106">Parameters</span></span>

<span data-ttu-id="0f489-107">*numFrames* </span><span class="sxs-lookup"><span data-stu-id="0f489-107">*numFrames* </span></span>  
<span data-ttu-id="0f489-108">Nombre d’images pour lesquelles générer des rapports d’analyse.</span><span class="sxs-lookup"><span data-stu-id="0f489-108">The number of frames to generate analysis reports for.</span></span>

<span data-ttu-id="0f489-109">*count0 \_ frameNumbers* </span><span class="sxs-lookup"><span data-stu-id="0f489-109">*count0\_frameNumbers* </span></span>  
<span data-ttu-id="0f489-110">Frames spécifiés.</span><span class="sxs-lookup"><span data-stu-id="0f489-110">The specified frames.</span></span>

<span data-ttu-id="0f489-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="0f489-111">*requestCallback* </span></span>  
<span data-ttu-id="0f489-112">Adresse d’un rappel utilisé pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="0f489-112">The address of a callback used to notify the host of results.</span></span>

## <a name="return-value"></a><span data-ttu-id="0f489-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f489-113">Return value</span></span>

<span data-ttu-id="0f489-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0f489-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0f489-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0f489-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f489-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f489-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0f489-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f489-117">Header</span></span></p></td><td><span data-ttu-id="0f489-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="0f489-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="0f489-119"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f489-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="0f489-120">**IOfflineAnalysisCacheRequest**</span><span class="sxs-lookup"><span data-stu-id="0f489-120">**IOfflineAnalysisCacheRequest**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscacherequest)

 

 
