---
description: Demande la sortie trame de la cible, de l’événement et du frame de rendu spécifiés.
MS-HAID: vspixengine.IFrameBufferRequest\_RequestAsync\_DWORD\_EventID\_DWORD\_IFrameBufferCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IFrameBufferRequest :: RequestAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 93E9BDFE-3913-4242-A973-7C113B6663FB
api_name:
- IFrameBufferRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 35c50b78486f25051e14ce2811382875e1fab240
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106530822"
---
# <a name="span-idvspixengineiframebufferrequest_requestasync_dword_eventid_dword_iframebuffercallback_ptr_dword_dwordspaniframebufferrequestrequestasync-method"></a><span data-ttu-id="56e64-103"><span id="vspixengine.iframebufferrequest_requestasync_dword_eventid_dword_iframebuffercallback_ptr_dword_dword"></span>IFrameBufferRequest :: RequestAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="56e64-103"><span id="vspixengine.iframebufferrequest_requestasync_dword_eventid_dword_iframebuffercallback_ptr_dword_dword"></span>IFrameBufferRequest::RequestAsync method</span></span>

<span data-ttu-id="56e64-104">Demande la sortie trame de la cible, de l’événement et du frame de rendu spécifiés.</span><span class="sxs-lookup"><span data-stu-id="56e64-104">Requests framebuffer output of the specified render target, event, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="56e64-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56e64-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  frameNumber,
   EventID                eventID,
   DWORD                  renderTargetIndex,
   IFrameBufferCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="56e64-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56e64-106">Parameters</span></span>

<span data-ttu-id="56e64-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="56e64-107">*frameNumber* </span></span>  
<span data-ttu-id="56e64-108">Frame spécifié.</span><span class="sxs-lookup"><span data-stu-id="56e64-108">The specified frame.</span></span>

<span data-ttu-id="56e64-109">*1001* </span><span class="sxs-lookup"><span data-stu-id="56e64-109">*eventID* </span></span>  
<span data-ttu-id="56e64-110">Événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="56e64-110">The specified event.</span></span>

<span data-ttu-id="56e64-111">*renderTargetIndex* </span><span class="sxs-lookup"><span data-stu-id="56e64-111">*renderTargetIndex* </span></span>  
<span data-ttu-id="56e64-112">Index de la cible de rendu spécifiée.</span><span class="sxs-lookup"><span data-stu-id="56e64-112">The index of the specified render target.</span></span>

<span data-ttu-id="56e64-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="56e64-113">*requestCallback* </span></span>  
<span data-ttu-id="56e64-114">Adresse d’un rappel utilisé pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="56e64-114">The address of a callback used to notify the host of results.</span></span>

<span data-ttu-id="56e64-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="56e64-115">*requestCookie* </span></span>  
<span data-ttu-id="56e64-116">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="56e64-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="56e64-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="56e64-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="56e64-118">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="56e64-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="56e64-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56e64-119">Return value</span></span>

<span data-ttu-id="56e64-120">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="56e64-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="56e64-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="56e64-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="56e64-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56e64-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="56e64-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="56e64-123">Header</span></span></p></td><td><span data-ttu-id="56e64-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="56e64-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="56e64-125"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56e64-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="56e64-126">**IFrameBufferRequest**</span><span class="sxs-lookup"><span data-stu-id="56e64-126">**IFrameBufferRequest**</span></span>](/windows/desktop/direct3dtools/iframebufferrequest)

 

 
