---
description: Demande asynchrone d’obtenir des données de nuanceur de calcul pour la distribution spécifiée.
MS-HAID: vspixengine.IPipeLineStagesRequest2\_RequestComputeShaderDataAsync\_EventID\_IPipeLineStagesCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesRequest2 :: RequestComputeShaderDataAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F73EA7B4-9E20-4BFD-8F87-20CE0B6C96D8
api_name:
- IPipeLineStagesRequest2.RequestComputeShaderDataAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cf0d4725d8d2172900a96e58b4c8786ca2a9c851
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106512874"
---
# <a name="span-idvspixengineipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dwordspanipipelinestagesrequest2requestcomputeshaderdataasync-method"></a><span data-ttu-id="7f27c-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dword"></span>IPipeLineStagesRequest2 :: RequestComputeShaderDataAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="7f27c-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dword"></span>IPipeLineStagesRequest2::RequestComputeShaderDataAsync method</span></span>

<span data-ttu-id="7f27c-104">Demande asynchrone d’obtenir des données de nuanceur de calcul pour la distribution spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7f27c-104">An asynchronous request to get compute shader data for the specified dispatch.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f27c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f27c-105">Syntax</span></span>


```C++
HRESULT RequestComputeShaderDataAsync(
   EventID                    eventID,
   IPipeLineStagesCallback2 * requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="7f27c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f27c-106">Parameters</span></span>

<span data-ttu-id="7f27c-107">*1001* </span><span class="sxs-lookup"><span data-stu-id="7f27c-107">*eventID* </span></span>  
<span data-ttu-id="7f27c-108">Événement de dispatch spécifié.</span><span class="sxs-lookup"><span data-stu-id="7f27c-108">The specified dispatch event.</span></span>

<span data-ttu-id="7f27c-109">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="7f27c-109">*requestCallback* </span></span>  
<span data-ttu-id="7f27c-110">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="7f27c-110">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="7f27c-111">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="7f27c-111">*requestCookie* </span></span>  
<span data-ttu-id="7f27c-112">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="7f27c-112">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="7f27c-113">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="7f27c-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="7f27c-114">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="7f27c-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="7f27c-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7f27c-115">Return value</span></span>

<span data-ttu-id="7f27c-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7f27c-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7f27c-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7f27c-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f27c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f27c-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="7f27c-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f27c-119">Header</span></span></p></td><td><span data-ttu-id="7f27c-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="7f27c-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="7f27c-121"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f27c-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="7f27c-122">**IPipeLineStagesRequest2**</span><span class="sxs-lookup"><span data-stu-id="7f27c-122">**IPipeLineStagesRequest2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest2)

 

 
