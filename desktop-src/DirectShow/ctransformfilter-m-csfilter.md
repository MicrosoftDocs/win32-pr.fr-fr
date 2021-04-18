---
description: Section critique qui protège l’état du filtre. Pour plus d’informations, consultez Data Flow for filtre Developers.
ms.assetid: 75b9c8b0-e911-41fd-8d07-b854dbe25551
title: 'Membre CTransformFilter :: m_csFilter (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_csFilter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 991b07aa654ce42a651f4fa169e757d8380fdc8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543183"
---
# <a name="ctransformfilterm_csfilter-member"></a><span data-ttu-id="55033-104">CTransformFilter :: m \_ csFilter, membre</span><span class="sxs-lookup"><span data-stu-id="55033-104">CTransformFilter::m\_csFilter member</span></span>

<span data-ttu-id="55033-105">Section critique qui protège l’état du filtre.</span><span class="sxs-lookup"><span data-stu-id="55033-105">Critical section that protects the filter state.</span></span> <span data-ttu-id="55033-106">Pour plus d’informations, consultez [Data Flow for filtre Developers](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="55033-106">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="55033-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55033-107">Syntax</span></span>


```C++
CCritSec m_csFilter;
```



## <a name="requirements"></a><span data-ttu-id="55033-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55033-108">Requirements</span></span>



| <span data-ttu-id="55033-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55033-109">Requirement</span></span> | <span data-ttu-id="55033-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="55033-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55033-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="55033-111">Header</span></span><br/>  | <dl> <span data-ttu-id="55033-112"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55033-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="55033-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="55033-113">Library</span></span><br/> | <dl> <span data-ttu-id="55033-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="55033-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55033-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55033-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55033-116">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="55033-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




