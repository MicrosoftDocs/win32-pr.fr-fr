---
description: Nombre maximal actuel d’images Delta à supprimer.
ms.assetid: d14c594e-55ab-42c2-bdb0-6829f71d02dd
title: 'Membre CVideoTransformFilter :: m_nWaitForKey (Vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_nWaitForKey
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a168a26816825c33c0e047d93cc8b14ebd0f3536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532499"
---
# <a name="cvideotransformfilterm_nwaitforkey-member"></a><span data-ttu-id="5900d-103">CVideoTransformFilter :: m \_ nWaitForKey, membre</span><span class="sxs-lookup"><span data-stu-id="5900d-103">CVideoTransformFilter::m\_nWaitForKey member</span></span>

<span data-ttu-id="5900d-104">Nombre maximal actuel d’images Delta à supprimer.</span><span class="sxs-lookup"><span data-stu-id="5900d-104">The current maximum number of delta frames to drop.</span></span> <span data-ttu-id="5900d-105">Alors que cette variable est supérieure à zéro, le filtre supprime les frames jusqu’à ce qu’il atteigne une image clé.</span><span class="sxs-lookup"><span data-stu-id="5900d-105">While this variable is greater than zero, the filter will drop frames until it reaches a key frame.</span></span> <span data-ttu-id="5900d-106">Pour chaque frame supprimé, le filtre décrémente cette variable d’une unité, ce qui empêche le filtre de supprimer un nombre excessif de frames.</span><span class="sxs-lookup"><span data-stu-id="5900d-106">For each frame that is dropped, the filter decrements this variable by one, which prevents the filter from dropping an excessive number of frames.</span></span> <span data-ttu-id="5900d-107">Après 30 images Delta dans une ligne sans images clés, le filtre recommence à fournir des frames.</span><span class="sxs-lookup"><span data-stu-id="5900d-107">After 30 delta frames in a row with no key frames, the filter will start delivering frames again.</span></span>

## <a name="syntax"></a><span data-ttu-id="5900d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5900d-108">Syntax</span></span>


```C++
int m_nWaitForKey;
```



## <a name="requirements"></a><span data-ttu-id="5900d-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5900d-109">Requirements</span></span>



| <span data-ttu-id="5900d-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5900d-110">Requirement</span></span> | <span data-ttu-id="5900d-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="5900d-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5900d-112">En-tête</span><span class="sxs-lookup"><span data-stu-id="5900d-112">Header</span></span><br/>  | <dl> <span data-ttu-id="5900d-113"><dt>Vtrans. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5900d-113"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5900d-114">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5900d-114">Library</span></span><br/> | <dl> <span data-ttu-id="5900d-115"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5900d-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5900d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5900d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5900d-117">**CVideoTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="5900d-117">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




