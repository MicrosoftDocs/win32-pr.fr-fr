---
description: Pointeur vers un objet de section critique qui protège l’état de filtre.
ms.assetid: e733360d-ed95-493f-a85b-53d584681f60
title: 'Membre CBasePin :: m_pLock (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0a18755c1ea1c5c29b9839ecaf8803a84f8c8f10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537831"
---
# <a name="cbasepinm_plock-member"></a><span data-ttu-id="b0b2d-103">CBasePin :: m \_ pLock, membre</span><span class="sxs-lookup"><span data-stu-id="b0b2d-103">CBasePin::m\_pLock member</span></span>

<span data-ttu-id="b0b2d-104">Pointeur vers un objet de section critique qui protège l’état de filtre.</span><span class="sxs-lookup"><span data-stu-id="b0b2d-104">Pointer to a critical section object that protects the filter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0b2d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0b2d-105">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a><span data-ttu-id="b0b2d-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0b2d-106">Requirements</span></span>



| <span data-ttu-id="b0b2d-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0b2d-107">Requirement</span></span> | <span data-ttu-id="b0b2d-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0b2d-108">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0b2d-109">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0b2d-109">Header</span></span><br/>  | <dl> <span data-ttu-id="b0b2d-110"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0b2d-110"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b0b2d-111">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b0b2d-111">Library</span></span><br/> | <dl> <span data-ttu-id="b0b2d-112"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b0b2d-112"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0b2d-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0b2d-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0b2d-114">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="b0b2d-114">**CBasePin Class**</span></span>](cbasepin.md)
</dt> <dt>

[<span data-ttu-id="b0b2d-115">Threads et sections critiques</span><span class="sxs-lookup"><span data-stu-id="b0b2d-115">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 




