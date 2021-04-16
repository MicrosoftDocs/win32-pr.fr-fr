---
description: Rappel qui avertit l’hôte d’une demande annulée à l’aide d’un cookie qui identifie de façon unique la demande.
MS-HAID: vspixengine.INewFramesCallback\_CancelUsingCookie\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'INewFramesCallback :: CancelUsingCookie, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36176554-BB4F-40CB-AB7B-4957DA84BAA8
api_name:
- INewFramesCallback.CancelUsingCookie
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dfbbbda1a11244088dccad640be348da1e4d8313
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481281"
---
# <a name="span-idvspixengineinewframescallback_cancelusingcookie_dwordspaninewframescallbackcancelusingcookie-method"></a><span data-ttu-id="993b2-103"><span id="vspixengine.inewframescallback_cancelusingcookie_dword"></span>INewFramesCallback :: CancelUsingCookie, méthode</span><span class="sxs-lookup"><span data-stu-id="993b2-103"><span id="vspixengine.inewframescallback_cancelusingcookie_dword"></span>INewFramesCallback::CancelUsingCookie method</span></span>

<span data-ttu-id="993b2-104">Rappel qui avertit l’hôte d’une demande annulée à l’aide d’un cookie qui identifie de façon unique la demande.</span><span class="sxs-lookup"><span data-stu-id="993b2-104">A callback that notifies the host of a canceled request by using a cookie that uniquely identifies the request.</span></span>

## <a name="syntax"></a><span data-ttu-id="993b2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="993b2-105">Syntax</span></span>


```C++
HRESULT CancelUsingCallback(
   IUnknown * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="993b2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="993b2-106">Parameters</span></span>

<span data-ttu-id="993b2-107">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="993b2-107">*requestCookie* </span></span>  
<span data-ttu-id="993b2-108">Cookie qui idenfies de façon unique la demande annulée.</span><span class="sxs-lookup"><span data-stu-id="993b2-108">The cookie which uniquely idenfies the cancelled request.</span></span>

## <a name="return-value"></a><span data-ttu-id="993b2-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="993b2-109">Return value</span></span>

<span data-ttu-id="993b2-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="993b2-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="993b2-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="993b2-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="993b2-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="993b2-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="993b2-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="993b2-113">Header</span></span></p></td><td><span data-ttu-id="993b2-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="993b2-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="993b2-115"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="993b2-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="993b2-116">**INewFramesCallback**</span><span class="sxs-lookup"><span data-stu-id="993b2-116">**INewFramesCallback**</span></span>](/windows/desktop/direct3dtools/inewframescallback)

 

 
