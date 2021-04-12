---
description: Demande asynchrone pour obtenir si l’étape du nuanceur de calcul a été utilisée pour le frame et l’événement spécifiés.
MS-HAID: vspixengine.IPipeLineStagesRequest2\_RequestComputeShaderStageAsync\_DWORD\_EventID\_IPipeLineStagesCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesRequest2 :: RequestComputeShaderStageAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: EC5695A6-70B5-4F7D-A235-974A0A59A44F
api_name:
- IPipeLineStagesRequest2.RequestComputeShaderStageAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ec7fe36a35e73ae2d047be11a2d5cf72f65825f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482024"
---
# <a name="span-idvspixengineipipelinestagesrequest2_requestcomputeshaderstageasync_dword_eventid_ipipelinestagescallback_ptr_dword_dwordspanipipelinestagesrequest2requestcomputeshaderstageasync-method"></a><span data-ttu-id="ff1e9-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderstageasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>IPipeLineStagesRequest2 :: RequestComputeShaderStageAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="ff1e9-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderstageasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>IPipeLineStagesRequest2::RequestComputeShaderStageAsync method</span></span>

<span data-ttu-id="ff1e9-104">Demande asynchrone pour obtenir si l’étape du nuanceur de calcul a été utilisée pour le frame et l’événement spécifiés.</span><span class="sxs-lookup"><span data-stu-id="ff1e9-104">An asynchronous request to get whether the compute shader stage was used for the specified frame and event.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff1e9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff1e9-105">Syntax</span></span>


```C++
HRESULT RequestComputeShaderStageAsync(
   DWORD                     frameNumber,
   EventID                   eventID,
   IPipeLineStagesCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="ff1e9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff1e9-106">Parameters</span></span>

<span data-ttu-id="ff1e9-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="ff1e9-107">*frameNumber* </span></span>  
<span data-ttu-id="ff1e9-108">Frame spécifié.</span><span class="sxs-lookup"><span data-stu-id="ff1e9-108">The specified frame.</span></span>

<span data-ttu-id="ff1e9-109">*1001* </span><span class="sxs-lookup"><span data-stu-id="ff1e9-109">*eventID* </span></span>  
<span data-ttu-id="ff1e9-110">Événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="ff1e9-110">The specified event.</span></span>

<span data-ttu-id="ff1e9-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="ff1e9-111">*requestCallback* </span></span>  
<span data-ttu-id="ff1e9-112">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="ff1e9-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="ff1e9-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="ff1e9-113">*requestCookie* </span></span>  
<span data-ttu-id="ff1e9-114">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="ff1e9-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="ff1e9-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="ff1e9-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="ff1e9-116">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="ff1e9-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="ff1e9-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ff1e9-117">Return value</span></span>

<span data-ttu-id="ff1e9-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ff1e9-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ff1e9-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ff1e9-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff1e9-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff1e9-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ff1e9-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff1e9-121">Header</span></span></p></td><td><span data-ttu-id="ff1e9-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ff1e9-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ff1e9-123"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff1e9-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ff1e9-124">**IPipeLineStagesRequest2**</span><span class="sxs-lookup"><span data-stu-id="ff1e9-124">**IPipeLineStagesRequest2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest2)

 

 
