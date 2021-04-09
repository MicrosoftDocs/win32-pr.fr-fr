---
description: Demande asynchrone pour obtenir des informations spécifiées sur un frame spécifié unique.
MS-HAID: vspixengine.IFrameEventsRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IFrameEventsCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IFrameEventsRequest :: RequestAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 821E7674-A960-46F6-A7AF-386298902ED6
api_name:
- IFrameEventsRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a001f6a29d17806271ca4f5d29dc80d6e36251bf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108830"
---
# <a name="span-idvspixengineiframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dwordspaniframeeventsrequestrequestasync-method"></a><span data-ttu-id="5c2e8-103"><span id="vspixengine.iframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>IFrameEventsRequest :: RequestAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="5c2e8-103"><span id="vspixengine.iframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>IFrameEventsRequest::RequestAsync method</span></span>

<span data-ttu-id="5c2e8-104">Demande asynchrone pour obtenir des informations spécifiées sur un frame spécifié unique.</span><span class="sxs-lookup"><span data-stu-id="5c2e8-104">An asynchronous request to get specified information about a single specified frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c2e8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c2e8-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  frameNumber,
   DWORD                  numColumns,
   DWORD []               count1_columns,
   IFrameEventsCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="5c2e8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c2e8-106">Parameters</span></span>

<span data-ttu-id="5c2e8-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="5c2e8-107">*frameNumber* </span></span>  
<span data-ttu-id="5c2e8-108">Frame spécifié.</span><span class="sxs-lookup"><span data-stu-id="5c2e8-108">The specified frame.</span></span>

<span data-ttu-id="5c2e8-109">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="5c2e8-109">*numColumns* </span></span>  
<span data-ttu-id="5c2e8-110">Colonnes spécifiées (champs).</span><span class="sxs-lookup"><span data-stu-id="5c2e8-110">The specified columns (fields).</span></span>

<span data-ttu-id="5c2e8-111">*\_colonnes count1* </span><span class="sxs-lookup"><span data-stu-id="5c2e8-111">*count1\_columns* </span></span>  
<span data-ttu-id="5c2e8-112">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="5c2e8-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="5c2e8-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="5c2e8-113">*requestCallback* </span></span>  
<span data-ttu-id="5c2e8-114">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="5c2e8-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="5c2e8-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="5c2e8-115">*requestCookie* </span></span>  
<span data-ttu-id="5c2e8-116">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="5c2e8-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="5c2e8-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="5c2e8-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="5c2e8-118">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="5c2e8-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="5c2e8-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5c2e8-119">Return value</span></span>

<span data-ttu-id="5c2e8-120">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5c2e8-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5c2e8-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5c2e8-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c2e8-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c2e8-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5c2e8-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="5c2e8-123">Header</span></span></p></td><td><span data-ttu-id="5c2e8-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="5c2e8-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5c2e8-125"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c2e8-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5c2e8-126">**IFrameEventsRequest**</span><span class="sxs-lookup"><span data-stu-id="5c2e8-126">**IFrameEventsRequest**</span></span>](/windows/desktop/direct3dtools/iframeeventsrequest)

 

 
