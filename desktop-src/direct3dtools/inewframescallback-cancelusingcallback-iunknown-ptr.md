---
description: Rappel qui avertit l’hôte d’une demande annulée.
MS-HAID: vspixengine.INewFramesCallback\_CancelUsingCallback\_IUnknown\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'INewFramesCallback :: CancelUsingCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 291B2F85-1437-4704-8971-4B7C25B693F8
api_name:
- INewFramesCallback.CancelUsingCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 863219cd37078fbde1e7ef8b2da7677a31e12872
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482656"
---
# <a name="span-idvspixengineinewframescallback_cancelusingcallback_iunknown_ptrspaninewframescallbackcancelusingcallback-method"></a><span data-ttu-id="aaa91-103"><span id="vspixengine.inewframescallback_cancelusingcallback_iunknown_ptr"></span>INewFramesCallback :: CancelUsingCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="aaa91-103"><span id="vspixengine.inewframescallback_cancelusingcallback_iunknown_ptr"></span>INewFramesCallback::CancelUsingCallback method</span></span>

<span data-ttu-id="aaa91-104">Rappel qui avertit l’hôte d’une demande annulée.</span><span class="sxs-lookup"><span data-stu-id="aaa91-104">A callback that notifies the host of a canceled request.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaa91-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aaa91-105">Syntax</span></span>


```C++
HRESULT CancelUsingCallback(
   IUnknown * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="aaa91-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aaa91-106">Parameters</span></span>

<span data-ttu-id="aaa91-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="aaa91-107">*requestCallback* </span></span>  
<span data-ttu-id="aaa91-108">Adresse de la demande annulée.</span><span class="sxs-lookup"><span data-stu-id="aaa91-108">The address of the cancelled request.</span></span>

## <a name="return-value"></a><span data-ttu-id="aaa91-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aaa91-109">Return value</span></span>

<span data-ttu-id="aaa91-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="aaa91-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aaa91-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aaa91-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaa91-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aaa91-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="aaa91-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="aaa91-113">Header</span></span></p></td><td><span data-ttu-id="aaa91-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="aaa91-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="aaa91-115"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aaa91-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="aaa91-116">**INewFramesCallback**</span><span class="sxs-lookup"><span data-stu-id="aaa91-116">**INewFramesCallback**</span></span>](/windows/desktop/direct3dtools/inewframescallback)

 

 
