---
description: Section critique qui protège l’état de diffusion en continu. Pour plus d’informations, consultez Data Flow for filtre Developers.
ms.assetid: f77c3129-ca25-47b8-8a6e-3a07169701af
title: 'Membre CTransformFilter :: m_csReceive (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_csReceive
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 542f108cee8dbe761040ef8474ae7cec565e0b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533170"
---
# <a name="ctransformfilterm_csreceive-member"></a><span data-ttu-id="6ed5f-104">CTransformFilter :: m \_ csReceive, membre</span><span class="sxs-lookup"><span data-stu-id="6ed5f-104">CTransformFilter::m\_csReceive member</span></span>

<span data-ttu-id="6ed5f-105">Section critique qui protège l’état de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="6ed5f-105">Critical section that protects the streaming state.</span></span> <span data-ttu-id="6ed5f-106">Pour plus d’informations, consultez [Data Flow for filtre Developers](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="6ed5f-106">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6ed5f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ed5f-107">Syntax</span></span>


```C++
CCritSec m_csReceive;
```



## <a name="requirements"></a><span data-ttu-id="6ed5f-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ed5f-108">Requirements</span></span>



| <span data-ttu-id="6ed5f-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ed5f-109">Requirement</span></span> | <span data-ttu-id="6ed5f-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ed5f-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ed5f-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="6ed5f-111">Header</span></span><br/>  | <dl> <span data-ttu-id="6ed5f-112"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ed5f-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6ed5f-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6ed5f-113">Library</span></span><br/> | <dl> <span data-ttu-id="6ed5f-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6ed5f-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ed5f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ed5f-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ed5f-116">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="6ed5f-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




