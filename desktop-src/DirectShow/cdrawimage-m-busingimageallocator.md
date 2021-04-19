---
description: La \_ variable de membre m bUsingImageAllocator indique si l’allocateur de la connexion de code confidentiel est un objet CImageAllocator. Si la valeur est TRUE, l’allocateur est un objet CImageAllocator (ou est dérivé de cette classe).
ms.assetid: 8eddcab6-77b9-4c8f-be74-33e91661430d
title: 'Membre CDrawImage :: m_bUsingImageAllocator (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bUsingImageAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e08d1e8217f42c6855759cefeef40e56949156fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544030"
---
# <a name="cdrawimagem_busingimageallocator-member"></a><span data-ttu-id="11c60-104">CDrawImage :: m \_ bUsingImageAllocator, membre</span><span class="sxs-lookup"><span data-stu-id="11c60-104">CDrawImage::m\_bUsingImageAllocator member</span></span>

<span data-ttu-id="11c60-105">La `m_bUsingImageAllocator` variable membre indique si l’allocateur pour la connexion de code confidentiel est un objet **CImageAllocator** .</span><span class="sxs-lookup"><span data-stu-id="11c60-105">The `m_bUsingImageAllocator` member variable indicates whether the allocator for the pin connection is a **CImageAllocator** object.</span></span> <span data-ttu-id="11c60-106">Si la valeur est **true**, l’allocateur est un objet **CImageAllocator** (ou est dérivé de cette classe).</span><span class="sxs-lookup"><span data-stu-id="11c60-106">If the value is **TRUE**, the allocator is a **CImageAllocator** object (or is derived from that class).</span></span>

## <a name="syntax"></a><span data-ttu-id="11c60-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11c60-107">Syntax</span></span>


```C++
BOOL m_bUsingImageAllocator;
```



## <a name="remarks"></a><span data-ttu-id="11c60-108">Notes</span><span class="sxs-lookup"><span data-stu-id="11c60-108">Remarks</span></span>

<span data-ttu-id="11c60-109">Lorsque la valeur est **true**, l’objet **CDrawImage** peut utiliser les fonctions **GDI BitBlt** et **StretchBlt** pour restituer l’image, plutôt que les fonctions **SetDIBitsToDevice** et **StretchDIBits** plus lentes.</span><span class="sxs-lookup"><span data-stu-id="11c60-109">When the value is **TRUE**, the **CDrawImage** object can use the GDI **BitBlt** and **StretchBlt** functions to render the image, rather than the slower **SetDIBitsToDevice** and **StretchDIBits** functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="11c60-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11c60-110">Requirements</span></span>



| <span data-ttu-id="11c60-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11c60-111">Requirement</span></span> | <span data-ttu-id="11c60-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="11c60-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11c60-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="11c60-113">Header</span></span><br/>  | <dl> <span data-ttu-id="11c60-114"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11c60-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="11c60-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="11c60-115">Library</span></span><br/> | <dl> <span data-ttu-id="11c60-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="11c60-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11c60-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11c60-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11c60-118">**CDrawImage, classe**</span><span class="sxs-lookup"><span data-stu-id="11c60-118">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="11c60-119">**CDrawImage::NotifyAllocator**</span><span class="sxs-lookup"><span data-stu-id="11c60-119">**CDrawImage::NotifyAllocator**</span></span>](cdrawimage-notifyallocator.md)
</dt> <dt>

[<span data-ttu-id="11c60-120">**CDrawImage::UsingImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="11c60-120">**CDrawImage::UsingImageAllocator**</span></span>](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




