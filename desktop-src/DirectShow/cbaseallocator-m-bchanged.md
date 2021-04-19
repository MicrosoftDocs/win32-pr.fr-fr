---
description: Indicateur qui spécifie si les exigences de la mémoire tampon ont été modifiées.
ms.assetid: 34d946f9-125c-40fb-b09e-82457add07d6
title: 'Membre CBaseAllocator :: m_bChanged (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86c700f3c0ee820206613bcf3147652b1826b57a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531058"
---
# <a name="cbaseallocatorm_bchanged-member"></a><span data-ttu-id="abefb-103">CBaseAllocator :: m \_ bChanged, membre</span><span class="sxs-lookup"><span data-stu-id="abefb-103">CBaseAllocator::m\_bChanged member</span></span>

<span data-ttu-id="abefb-104">Indicateur qui spécifie si les exigences de la mémoire tampon ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="abefb-104">Flag indicating whether the buffer requirements have changed.</span></span> <span data-ttu-id="abefb-105">La méthode [**CBaseAllocator :: SetProperties**](cbaseallocator-setproperties.md) définit la valeur sur **true**.</span><span class="sxs-lookup"><span data-stu-id="abefb-105">The [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method sets the value to **TRUE**.</span></span> <span data-ttu-id="abefb-106">Dans une classe dérivée, la méthode virtuelle pure [**CBaseAllocator :: Alloc**](cbaseallocator-alloc.md) doit rétablir la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="abefb-106">In a derived class, the pure virtual method [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) should set the value back to **FALSE**.</span></span> <span data-ttu-id="abefb-107">Une fois que les tampons ont été alloués, il n’est pas nécessaire de les réallouer alors que *m \_ bChanged* a la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="abefb-107">Once buffers have been allocated, there is no need to re-allocate them while *m\_bChanged* is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="abefb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abefb-108">Syntax</span></span>


```C++
BOOL m_bChanged;
```



## <a name="requirements"></a><span data-ttu-id="abefb-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="abefb-109">Requirements</span></span>



| <span data-ttu-id="abefb-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="abefb-110">Requirement</span></span> | <span data-ttu-id="abefb-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="abefb-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abefb-112">En-tête</span><span class="sxs-lookup"><span data-stu-id="abefb-112">Header</span></span><br/>  | <dl> <span data-ttu-id="abefb-113"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="abefb-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="abefb-114">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="abefb-114">Library</span></span><br/> | <dl> <span data-ttu-id="abefb-115"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="abefb-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abefb-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abefb-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abefb-117">**CBaseAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="abefb-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




