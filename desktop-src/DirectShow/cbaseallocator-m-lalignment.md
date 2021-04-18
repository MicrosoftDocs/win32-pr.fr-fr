---
description: 'Alignement de chaque mémoire tampon. L’adresse de chaque mémoire tampon doit être un multiple pair de cette valeur. Le préfixe doit être calculé dans l’alignement ; consultez CBaseAllocator :: m \_ lPrefix.'
ms.assetid: 2b71b60a-feeb-4f09-bd56-e126eac8e150
title: 'Membre CBaseAllocator :: m_lAlignment (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lAlignment
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bfdfe7a83a244d5c8cd40a0a4ec747f286c5099
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540548"
---
# <a name="cbaseallocatorm_lalignment-member"></a><span data-ttu-id="ce955-105">CBaseAllocator :: m \_ lAlignment, membre</span><span class="sxs-lookup"><span data-stu-id="ce955-105">CBaseAllocator::m\_lAlignment member</span></span>

<span data-ttu-id="ce955-106">Alignement de chaque mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ce955-106">Alignment of each buffer.</span></span> <span data-ttu-id="ce955-107">L’adresse de chaque mémoire tampon doit être un multiple pair de cette valeur.</span><span class="sxs-lookup"><span data-stu-id="ce955-107">The address of each buffer must be an even multiple of this value.</span></span> <span data-ttu-id="ce955-108">Le préfixe doit être calculé dans l’alignement ; consultez [**CBaseAllocator :: m \_ lPrefix**](cbaseallocator-m-lprefix.md).</span><span class="sxs-lookup"><span data-stu-id="ce955-108">The prefix must be calculated into the alignment; see [**CBaseAllocator::m\_lPrefix**](cbaseallocator-m-lprefix.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ce955-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce955-109">Syntax</span></span>


```C++
long m_lAlignment;
```



## <a name="requirements"></a><span data-ttu-id="ce955-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce955-110">Requirements</span></span>



| <span data-ttu-id="ce955-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce955-111">Requirement</span></span> | <span data-ttu-id="ce955-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce955-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce955-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce955-113">Header</span></span><br/>  | <dl> <span data-ttu-id="ce955-114"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce955-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ce955-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ce955-115">Library</span></span><br/> | <dl> <span data-ttu-id="ce955-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ce955-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce955-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce955-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce955-118">**CBaseAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="ce955-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




