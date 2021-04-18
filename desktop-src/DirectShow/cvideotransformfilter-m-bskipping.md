---
description: Valeur booléenne qui indique si le filtre supprime actuellement des frames. Si cette valeur est TRUE, le filtre continue à supprimer des frames jusqu’à ce qu’il atteigne l’image clé suivante, ou jusqu’à ce qu’il reçoive 30 images Delta dans une ligne sans image clé.
ms.assetid: 1af22879-bf9b-4835-b3b5-06fb52b3140f
title: 'Membre CVideoTransformFilter :: m_bSkipping (Vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSkipping
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7beb4073052149e246a55ffbb1ff057e836704c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528894"
---
# <a name="cvideotransformfilterm_bskipping-member"></a><span data-ttu-id="3d96a-104">CVideoTransformFilter :: m \_ bSkipping, membre</span><span class="sxs-lookup"><span data-stu-id="3d96a-104">CVideoTransformFilter::m\_bSkipping member</span></span>

<span data-ttu-id="3d96a-105">Valeur booléenne qui indique si le filtre supprime actuellement des frames.</span><span class="sxs-lookup"><span data-stu-id="3d96a-105">Boolean value that indicates whether the filter is currently dropping frames.</span></span> <span data-ttu-id="3d96a-106">Si cette valeur est **true**, le filtre continue à supprimer des frames jusqu’à ce qu’il atteigne l’image clé suivante, ou jusqu’à ce qu’il reçoive 30 images Delta dans une ligne sans image clé.</span><span class="sxs-lookup"><span data-stu-id="3d96a-106">If this value is **TRUE**, the filter continues to drop frames until it reaches the next key frame, or until it receives 30 delta frames in a row without a key frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d96a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d96a-107">Syntax</span></span>


```C++
BOOL m_bSkipping;
```



## <a name="requirements"></a><span data-ttu-id="3d96a-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d96a-108">Requirements</span></span>



| <span data-ttu-id="3d96a-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d96a-109">Requirement</span></span> | <span data-ttu-id="3d96a-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d96a-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d96a-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="3d96a-111">Header</span></span><br/>  | <dl> <span data-ttu-id="3d96a-112"><dt>Vtrans. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d96a-112"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3d96a-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3d96a-113">Library</span></span><br/> | <dl> <span data-ttu-id="3d96a-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3d96a-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d96a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d96a-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d96a-116">**CVideoTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="3d96a-116">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




