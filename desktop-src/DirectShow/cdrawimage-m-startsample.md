---
description: La \_ variable de membre m StartSample spécifie l’heure de début de l’exemple le plus récent.
ms.assetid: 2e6d6893-d57b-4009-a6ec-40dc0878d9c4
title: 'Membre CDrawImage :: m_StartSample (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_StartSample
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fd8039b1d37d0e61a150ed6c6944f0052089b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544481"
---
# <a name="cdrawimagem_startsample-member"></a><span data-ttu-id="1cde0-103">CDrawImage :: m \_ StartSample, membre</span><span class="sxs-lookup"><span data-stu-id="1cde0-103">CDrawImage::m\_StartSample member</span></span>

<span data-ttu-id="1cde0-104">La variable de membre **m \_ StartSample** spécifie l’heure de début de l’exemple le plus récent.</span><span class="sxs-lookup"><span data-stu-id="1cde0-104">The **m\_StartSample** member variable specifies the start time of the most recent sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cde0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cde0-105">Syntax</span></span>


```C++
CRefTime m_StartSample;
```



## <a name="remarks"></a><span data-ttu-id="1cde0-106">Notes</span><span class="sxs-lookup"><span data-stu-id="1cde0-106">Remarks</span></span>

<span data-ttu-id="1cde0-107">La valeur est valide uniquement à l’intérieur de la méthode [**CDrawImage ::D isplaysampletimes**](cdrawimage-displaysampletimes.md) .</span><span class="sxs-lookup"><span data-stu-id="1cde0-107">The value is only valid inside the [**CDrawImage::DisplaySampleTimes**](cdrawimage-displaysampletimes.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cde0-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cde0-108">Requirements</span></span>



| <span data-ttu-id="1cde0-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cde0-109">Requirement</span></span> | <span data-ttu-id="1cde0-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cde0-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cde0-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="1cde0-111">Header</span></span><br/>  | <dl> <span data-ttu-id="1cde0-112"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1cde0-112"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1cde0-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1cde0-113">Library</span></span><br/> | <dl> <span data-ttu-id="1cde0-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1cde0-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cde0-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cde0-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cde0-116">**CDrawImage, classe**</span><span class="sxs-lookup"><span data-stu-id="1cde0-116">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




