---
description: Indique la date à laquelle les échantillons arrivent au convertisseur, en unités de temps de référence. Stockéesyntaxe.
ms.assetid: 7b30fbe1-5e57-4aa4-8e87-ddd584f186e4
title: 'Membre CVideoTransformFilter :: m_itrLate (Vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_itrLate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ed93a4612d8fa5d4fe79239c6a7f4f5e479717
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537570"
---
# <a name="cvideotransformfilterm_itrlate-member"></a><span data-ttu-id="ce00f-104">CVideoTransformFilter :: m \_ itrLate, membre</span><span class="sxs-lookup"><span data-stu-id="ce00f-104">CVideoTransformFilter::m\_itrLate member</span></span>

<span data-ttu-id="ce00f-105">Indique la date à laquelle les échantillons arrivent au convertisseur, en unités de temps de référence.</span><span class="sxs-lookup"><span data-stu-id="ce00f-105">Indicates how late the samples are arriving at the renderer, in reference time units.</span></span> <span data-ttu-id="ce00f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce00f-106">Syntax</span></span>

## <a name="syntax"></a><span data-ttu-id="ce00f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce00f-107">Syntax</span></span>


```C++
int m_itrLate;
```



## <a name="remarks"></a><span data-ttu-id="ce00f-108">Notes</span><span class="sxs-lookup"><span data-stu-id="ce00f-108">Remarks</span></span>

<span data-ttu-id="ce00f-109">Lorsque le filtre reçoit un message de qualité en aval, il stocke la valeur de fin dans cette variable.</span><span class="sxs-lookup"><span data-stu-id="ce00f-109">When the filter receives a quality message from downstream, it stores the lateness value in this variable.</span></span> <span data-ttu-id="ce00f-110">Quand le filtre supprime des frames, il met à jour cette valeur en soustrayant la durée de chaque image.</span><span class="sxs-lookup"><span data-stu-id="ce00f-110">As the filter drops frames, it updates this value by subtracting the duration of each frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce00f-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce00f-111">Requirements</span></span>



| <span data-ttu-id="ce00f-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce00f-112">Requirement</span></span> | <span data-ttu-id="ce00f-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce00f-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce00f-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce00f-114">Header</span></span><br/>  | <dl> <span data-ttu-id="ce00f-115"><dt>Vtrans. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce00f-115"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ce00f-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ce00f-116">Library</span></span><br/> | <dl> <span data-ttu-id="ce00f-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ce00f-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce00f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce00f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce00f-119">**CVideoTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="ce00f-119">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




