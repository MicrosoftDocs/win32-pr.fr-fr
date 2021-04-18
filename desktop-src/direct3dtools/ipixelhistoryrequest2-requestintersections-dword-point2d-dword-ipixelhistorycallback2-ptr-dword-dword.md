---
description: Demande une liste d’événements qui provoquent une modification dans le pixel spécifié, le rendu cible/UAV et le frame.
MS-HAID: vspixengine.IPixelHistoryRequest2\_RequestIntersections\_DWORD\_Point2D\_DWORD\_IPixelHistoryCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixelHistoryRequest2 :: RequestIntersections, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C8E47935-DFA1-4A76-9D0A-3DF5833A1249
api_name:
- IPixelHistoryRequest2.RequestIntersections
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 56f8da17ca492ca15ca51676ae4f1e1654c6f41f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521556"
---
# <a name="span-idvspixengineipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dwordspanipixelhistoryrequest2requestintersections-method"></a><span data-ttu-id="25dfd-103"><span id="vspixengine.ipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2 :: RequestIntersections, méthode</span><span class="sxs-lookup"><span data-stu-id="25dfd-103"><span id="vspixengine.ipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2::RequestIntersections method</span></span>

<span data-ttu-id="25dfd-104">Demande une liste d’événements qui provoquent une modification dans le pixel spécifié, le rendu cible/UAV et le frame.</span><span class="sxs-lookup"><span data-stu-id="25dfd-104">Requests a list of events that cause a change in the specified pixel, render target / UAV, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="25dfd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25dfd-105">Syntax</span></span>


```C++
HRESULT RequestIntersections(
   DWORD                    frameNumber,
   Point2D                  pixel,
   DWORD                    renderTargetPtr,
   IPixelHistoryCallback2 * requestCallback,
   DWORD                    requestCookie,
   DWORD                    progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="25dfd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25dfd-106">Parameters</span></span>

<span data-ttu-id="25dfd-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="25dfd-107">*frameNumber* </span></span>  
<span data-ttu-id="25dfd-108">Frame spécifié.</span><span class="sxs-lookup"><span data-stu-id="25dfd-108">The specified frame.</span></span>

<span data-ttu-id="25dfd-109">*pixellisé* </span><span class="sxs-lookup"><span data-stu-id="25dfd-109">*pixel* </span></span>  
<span data-ttu-id="25dfd-110">Pixel spécifié.</span><span class="sxs-lookup"><span data-stu-id="25dfd-110">The specified pixel.</span></span>

<span data-ttu-id="25dfd-111">*renderTargetPtr* </span><span class="sxs-lookup"><span data-stu-id="25dfd-111">*renderTargetPtr* </span></span>  
<span data-ttu-id="25dfd-112">Adresse de la cible de rendu spécifiée</span><span class="sxs-lookup"><span data-stu-id="25dfd-112">The address of the specified render target</span></span>

<span data-ttu-id="25dfd-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="25dfd-113">*requestCallback* </span></span>  
<span data-ttu-id="25dfd-114">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="25dfd-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="25dfd-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="25dfd-115">*requestCookie* </span></span>  
<span data-ttu-id="25dfd-116">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="25dfd-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="25dfd-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="25dfd-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="25dfd-118">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="25dfd-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="25dfd-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25dfd-119">Return value</span></span>

<span data-ttu-id="25dfd-120">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="25dfd-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="25dfd-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="25dfd-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="25dfd-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25dfd-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="25dfd-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="25dfd-123">Header</span></span></p></td><td><span data-ttu-id="25dfd-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="25dfd-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="25dfd-125"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25dfd-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="25dfd-126">**IPixelHistoryRequest2**</span><span class="sxs-lookup"><span data-stu-id="25dfd-126">**IPixelHistoryRequest2**</span></span>](/windows/desktop/direct3dtools/ipixelhistoryrequest2)

 

 
