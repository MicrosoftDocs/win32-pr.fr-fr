---
description: Une demande asynchrone pour obtenir les frames de liste capturés dans le journal de graphisme.
MS-HAID: vspixengine.IFrameListRequest\_RequestAsync\_IFrameListCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IFrameListRequest :: RequestAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 309C28F2-CE01-49E7-9A21-5053E3ED7721
api_name:
- IFrameListRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3627fc5ef3a425ae7607009b4ad382080ea99192
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033413"
---
# <a name="span-idvspixengineiframelistrequest_requestasync_iframelistcallback_ptr_dword_dwordspaniframelistrequestrequestasync-method"></a><span data-ttu-id="83fa9-103"><span id="vspixengine.iframelistrequest_requestasync_iframelistcallback_ptr_dword_dword"></span>IFrameListRequest :: RequestAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="83fa9-103"><span id="vspixengine.iframelistrequest_requestasync_iframelistcallback_ptr_dword_dword"></span>IFrameListRequest::RequestAsync method</span></span>

<span data-ttu-id="83fa9-104">Une demande asynchrone pour obtenir les frames de liste capturés dans le journal de graphisme.</span><span class="sxs-lookup"><span data-stu-id="83fa9-104">An asynchronous request to get the list frames captured in the graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="83fa9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83fa9-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   IFrameListCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="83fa9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83fa9-106">Parameters</span></span>

<span data-ttu-id="83fa9-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="83fa9-107">*requestCallback* </span></span>  
<span data-ttu-id="83fa9-108">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="83fa9-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="83fa9-109">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="83fa9-109">*requestCookie* </span></span>  
<span data-ttu-id="83fa9-110">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="83fa9-110">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="83fa9-111">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="83fa9-111">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="83fa9-112">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="83fa9-112">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="83fa9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="83fa9-113">Return value</span></span>

<span data-ttu-id="83fa9-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="83fa9-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="83fa9-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="83fa9-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="83fa9-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83fa9-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="83fa9-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="83fa9-117">Header</span></span></p></td><td><span data-ttu-id="83fa9-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="83fa9-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="83fa9-119"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83fa9-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="83fa9-120">**IFrameListRequest**</span><span class="sxs-lookup"><span data-stu-id="83fa9-120">**IFrameListRequest**</span></span>](/windows/desktop/direct3dtools/iframelistrequest)

 

 
