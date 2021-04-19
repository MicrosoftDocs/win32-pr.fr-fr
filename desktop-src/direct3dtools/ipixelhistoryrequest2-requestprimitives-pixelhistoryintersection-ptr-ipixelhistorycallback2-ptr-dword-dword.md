---
description: Demande une liste de primitives à partir d’une intersection particulière. Pour plus d’informations, consultez la fonction membre RequestIntersections.
MS-HAID: vspixengine.IPixelHistoryRequest2\_RequestPrimitives\_PixelHistoryIntersection\_ptr\_IPixelHistoryCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixelHistoryRequest2 :: RequestPrimitives, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CFEB833C-1747-4153-A691-7529AA3F4095
api_name:
- IPixelHistoryRequest2.RequestPrimitives
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 71b248f86e20e560238a1c59b1a0199f285493a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514717"
---
# <a name="span-idvspixengineipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dwordspanipixelhistoryrequest2requestprimitives-method"></a><span data-ttu-id="860fd-104"><span id="vspixengine.ipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2 :: RequestPrimitives, méthode</span><span class="sxs-lookup"><span data-stu-id="860fd-104"><span id="vspixengine.ipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2::RequestPrimitives method</span></span>

<span data-ttu-id="860fd-105">Demande une liste de primitives à partir d’une intersection particulière.</span><span class="sxs-lookup"><span data-stu-id="860fd-105">Requests a list of primitives from a particular intersection.</span></span> <span data-ttu-id="860fd-106">Pour plus d’informations, consultez la fonction membre RequestIntersections.</span><span class="sxs-lookup"><span data-stu-id="860fd-106">For more information, see the RequestIntersections member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="860fd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="860fd-107">Syntax</span></span>


```C++
HRESULT RequestPrimitives(
   PixelHistoryIntersection * intersection,
   IPixelHistoryCallback2 *   requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="860fd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="860fd-108">Parameters</span></span>

<span data-ttu-id="860fd-109">*ensembles* </span><span class="sxs-lookup"><span data-stu-id="860fd-109">*intersection* </span></span>  
<span data-ttu-id="860fd-110">Adresse de l’intersection spécifiée.</span><span class="sxs-lookup"><span data-stu-id="860fd-110">The address of the specified intersection.</span></span>

<span data-ttu-id="860fd-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="860fd-111">*requestCallback* </span></span>  
<span data-ttu-id="860fd-112">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="860fd-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="860fd-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="860fd-113">*requestCookie* </span></span>  
<span data-ttu-id="860fd-114">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="860fd-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="860fd-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="860fd-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="860fd-116">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="860fd-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="860fd-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="860fd-117">Return value</span></span>

<span data-ttu-id="860fd-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="860fd-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="860fd-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="860fd-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="860fd-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="860fd-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="860fd-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="860fd-121">Header</span></span></p></td><td><span data-ttu-id="860fd-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="860fd-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="860fd-123"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="860fd-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="860fd-124">**IPixelHistoryRequest2**</span><span class="sxs-lookup"><span data-stu-id="860fd-124">**IPixelHistoryRequest2**</span></span>](/windows/desktop/direct3dtools/ipixelhistoryrequest2)

 

 
