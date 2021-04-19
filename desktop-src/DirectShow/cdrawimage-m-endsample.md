---
description: La \_ variable de membre m EndSample spécifie l’heure d’arrêt de l’exemple le plus récent.
ms.assetid: 694815b6-8da5-4174-b2c7-7d686a557c6c
title: 'Membre CDrawImage :: m_EndSample (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_EndSample
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 78268e8335d6dd8c24497a9e4d74b0caab205a99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540317"
---
# <a name="cdrawimagem_endsample-member"></a><span data-ttu-id="e1c55-103">CDrawImage :: m \_ EndSample, membre</span><span class="sxs-lookup"><span data-stu-id="e1c55-103">CDrawImage::m\_EndSample member</span></span>

<span data-ttu-id="e1c55-104">La `m_EndSample` variable membre spécifie l’heure d’arrêt de l’exemple le plus récent.</span><span class="sxs-lookup"><span data-stu-id="e1c55-104">The `m_EndSample` member variable specifies the stop time of the most recent sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1c55-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1c55-105">Syntax</span></span>


```C++
CRefTime m_EndSample;
```



## <a name="remarks"></a><span data-ttu-id="e1c55-106">Notes</span><span class="sxs-lookup"><span data-stu-id="e1c55-106">Remarks</span></span>

<span data-ttu-id="e1c55-107">La valeur est valide uniquement à l’intérieur de la méthode [**CDrawImage ::D isplaysampletimes**](cdrawimage-displaysampletimes.md) .</span><span class="sxs-lookup"><span data-stu-id="e1c55-107">The value is only valid inside the [**CDrawImage::DisplaySampleTimes**](cdrawimage-displaysampletimes.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1c55-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1c55-108">Requirements</span></span>



| <span data-ttu-id="e1c55-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1c55-109">Requirement</span></span> | <span data-ttu-id="e1c55-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1c55-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1c55-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1c55-111">Header</span></span><br/>  | <dl> <span data-ttu-id="e1c55-112"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1c55-112"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e1c55-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e1c55-113">Library</span></span><br/> | <dl> <span data-ttu-id="e1c55-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e1c55-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1c55-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1c55-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1c55-116">**CDrawImage, classe**</span><span class="sxs-lookup"><span data-stu-id="e1c55-116">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




