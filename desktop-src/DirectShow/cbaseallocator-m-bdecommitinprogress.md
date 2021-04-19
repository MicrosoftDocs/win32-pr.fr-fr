---
description: Indicateur spécifiant si une opération de dévalidation est en cours.
ms.assetid: aa008be1-8faa-4dc1-9641-37dcc59ce6c7
title: 'Membre CBaseAllocator :: m_bDecommitInProgress (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDecommitInProgress
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27aaf2766f67ebb77250522346cfe5c76acdf6d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523943"
---
# <a name="cbaseallocatorm_bdecommitinprogress-member"></a><span data-ttu-id="f8cd4-103">CBaseAllocator :: m \_ bDecommitInProgress, membre</span><span class="sxs-lookup"><span data-stu-id="f8cd4-103">CBaseAllocator::m\_bDecommitInProgress member</span></span>

<span data-ttu-id="f8cd4-104">Indicateur spécifiant si une opération de dévalidation est en cours.</span><span class="sxs-lookup"><span data-stu-id="f8cd4-104">Flag indicating whether a decommit operation is in progress.</span></span> <span data-ttu-id="f8cd4-105">La valeur est **true** après l’appel de la méthode [**CBaseAllocator ::D ecommit**](cbaseallocator-decommit.md) , mais avant la libération de toutes les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="f8cd4-105">The value is **TRUE** after the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method is called, but before all the buffers have been released.</span></span> <span data-ttu-id="f8cd4-106">Si la valeur est **true**, la méthode [**CBaseAllocator :: GetBuffer**](cbaseallocator-getbuffer.md) échoue.</span><span class="sxs-lookup"><span data-stu-id="f8cd4-106">If the value is **TRUE**, the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method fails.</span></span> <span data-ttu-id="f8cd4-107">En outre, l’allocateur ne doit pas être supprimé tant que la valeur est **true**.</span><span class="sxs-lookup"><span data-stu-id="f8cd4-107">Also, the allocator should not deleted itself while the value is **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8cd4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8cd4-108">Syntax</span></span>


```C++
BOOL m_bDecommitInProgress;
```



## <a name="requirements"></a><span data-ttu-id="f8cd4-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8cd4-109">Requirements</span></span>



| <span data-ttu-id="f8cd4-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8cd4-110">Requirement</span></span> | <span data-ttu-id="f8cd4-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8cd4-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8cd4-112">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8cd4-112">Header</span></span><br/>  | <dl> <span data-ttu-id="f8cd4-113"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8cd4-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f8cd4-114">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f8cd4-114">Library</span></span><br/> | <dl> <span data-ttu-id="f8cd4-115"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f8cd4-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8cd4-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8cd4-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8cd4-117">**CBaseAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="f8cd4-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




