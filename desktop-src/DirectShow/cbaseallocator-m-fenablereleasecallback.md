---
description: 'Indicateur qui spécifie si le rappel de mise en version est activé. Cet indicateur est défini dans la méthode du constructeur. Si la valeur est FALSe, l’appel de la méthode CBaseAllocator :: SetNotify provoque l’activation d’une assertion (dans les versions Debug).'
ms.assetid: cc9adc7c-ec44-41e7-875a-b3e553120804
title: 'Membre CBaseAllocator :: m_fEnableReleaseCallback (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fEnableReleaseCallback
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 626f1e8f4101eb48e79bc1cf679d1b91be9b2b31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541763"
---
# <a name="cbaseallocatorm_fenablereleasecallback-member"></a><span data-ttu-id="a3cf3-105">CBaseAllocator :: m \_ fEnableReleaseCallback, membre</span><span class="sxs-lookup"><span data-stu-id="a3cf3-105">CBaseAllocator::m\_fEnableReleaseCallback member</span></span>

<span data-ttu-id="a3cf3-106">Indicateur qui spécifie si le rappel de mise en version est activé.</span><span class="sxs-lookup"><span data-stu-id="a3cf3-106">Flag indicating whether the release callback is enabled.</span></span> <span data-ttu-id="a3cf3-107">Cet indicateur est défini dans la méthode du constructeur.</span><span class="sxs-lookup"><span data-stu-id="a3cf3-107">This flag is set in the constructor method.</span></span> <span data-ttu-id="a3cf3-108">Si la valeur est **false**, l’appel de la méthode [**CBaseAllocator :: SetNotify**](cbaseallocator-setnotify.md) provoque l’activation d’une assertion (dans les versions Debug).</span><span class="sxs-lookup"><span data-stu-id="a3cf3-108">If the value is **FALSE**, calling the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method causes an assertion to fire (in debug builds).</span></span>

## <a name="syntax"></a><span data-ttu-id="a3cf3-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3cf3-109">Syntax</span></span>


```C++
BOOL m_fEnableReleaseCallback;
```



## <a name="requirements"></a><span data-ttu-id="a3cf3-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3cf3-110">Requirements</span></span>



| <span data-ttu-id="a3cf3-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3cf3-111">Requirement</span></span> | <span data-ttu-id="a3cf3-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3cf3-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3cf3-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3cf3-113">Header</span></span><br/>  | <dl> <span data-ttu-id="a3cf3-114"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3cf3-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a3cf3-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a3cf3-115">Library</span></span><br/> | <dl> <span data-ttu-id="a3cf3-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a3cf3-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3cf3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3cf3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3cf3-118">**CBaseAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="a3cf3-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




