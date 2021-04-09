---
description: Rappel qui avertit l’hôte des informations d’intersection de l’historique des pixels retournées par la requête dans.
MS-HAID: vspixengine.IPixelHistoryCallback2\_IntersectionsCallback\_DWORD\_PixelHistoryIntersection\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixelHistoryCallback2 :: IntersectionsCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 478B2495-93E4-4BB1-BC86-802D2AFAF97D
api_name:
- IPixelHistoryCallback2.IntersectionsCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 30bde17a2c504b2afdaf9c13a7b6d7014590b1dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109063"
---
# <a name="span-idvspixengineipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arrspanipixelhistorycallback2intersectionscallback-method"></a><span data-ttu-id="b340c-103"><span id="vspixengine.ipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arr"></span>IPixelHistoryCallback2 :: IntersectionsCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="b340c-103"><span id="vspixengine.ipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arr"></span>IPixelHistoryCallback2::IntersectionsCallback method</span></span>

<span data-ttu-id="b340c-104">Rappel qui avertit l’hôte des informations d’intersection de l’historique des pixels retournées par la requête dans.</span><span class="sxs-lookup"><span data-stu-id="b340c-104">A callback that notifies the host of pixel history intersection information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="b340c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b340c-105">Syntax</span></span>


```C++
HRESULT IntersectionsCallback(
   DWORD                       count,
   PixelHistoryIntersection [] count0_intersections
);
```

## <a name="parameters"></a><span data-ttu-id="b340c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b340c-106">Parameters</span></span>

<span data-ttu-id="b340c-107">*saut* </span><span class="sxs-lookup"><span data-stu-id="b340c-107">*count* </span></span>  
<span data-ttu-id="b340c-108">Nombre d’intersections de l’historique des pixels.</span><span class="sxs-lookup"><span data-stu-id="b340c-108">The number of pixel history intersections.</span></span>

<span data-ttu-id="b340c-109">*count0 \_ intersections* </span><span class="sxs-lookup"><span data-stu-id="b340c-109">*count0\_intersections* </span></span>  
<span data-ttu-id="b340c-110">Intersections de l’historique des pixels.</span><span class="sxs-lookup"><span data-stu-id="b340c-110">The pixel history intersections.</span></span>

## <a name="return-value"></a><span data-ttu-id="b340c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b340c-111">Return value</span></span>

<span data-ttu-id="b340c-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b340c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b340c-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b340c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b340c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b340c-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b340c-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="b340c-115">Header</span></span></p></td><td><span data-ttu-id="b340c-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b340c-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b340c-117"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b340c-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b340c-118">**IPixelHistoryCallback2**</span><span class="sxs-lookup"><span data-stu-id="b340c-118">**IPixelHistoryCallback2**</span></span>](/windows/desktop/direct3dtools/ipixelhistorycallback2)

 

 
