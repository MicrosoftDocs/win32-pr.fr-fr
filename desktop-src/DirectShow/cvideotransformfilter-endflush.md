---
description: 'La méthode EndFlush termine une opération de vidage. Cette méthode remplace la méthode CTransformFilter :: EndFlush.'
ms.assetid: e7dfc6f9-1630-426b-95b2-9814331b5e61
title: Méthode CVideoTransformFilter. EndFlush (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca160bd2e3e66df3bcf6f293abe6f828309172c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531000"
---
# <a name="cvideotransformfilterendflush-method"></a><span data-ttu-id="0e98c-104">Méthode CVideoTransformFilter. EndFlush</span><span class="sxs-lookup"><span data-stu-id="0e98c-104">CVideoTransformFilter.EndFlush method</span></span>

<span data-ttu-id="0e98c-105">La `EndFlush` méthode termine une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="0e98c-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="0e98c-106">Cette méthode remplace la méthode [**CTransformFilter :: EndFlush**](ctransformfilter-endflush.md) .</span><span class="sxs-lookup"><span data-stu-id="0e98c-106">This method overrides the [**CTransformFilter::EndFlush**](ctransformfilter-endflush.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e98c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e98c-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="0e98c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e98c-108">Parameters</span></span>

<span data-ttu-id="0e98c-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0e98c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0e98c-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e98c-110">Return value</span></span>

<span data-ttu-id="0e98c-111">Retourne S \_ OK en cas de réussite, ou un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0e98c-111">Returns S\_OK if successful, or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e98c-112">Notes</span><span class="sxs-lookup"><span data-stu-id="0e98c-112">Remarks</span></span>

<span data-ttu-id="0e98c-113">Cette méthode réinitialise toutes les mesures de performances internes du filtre.</span><span class="sxs-lookup"><span data-stu-id="0e98c-113">This method resets all of the filter's internal performance measurements.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e98c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e98c-114">Requirements</span></span>



| <span data-ttu-id="0e98c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e98c-115">Requirement</span></span> | <span data-ttu-id="0e98c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e98c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e98c-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e98c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0e98c-118"><dt>Vtrans. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e98c-118"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0e98c-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0e98c-119">Library</span></span><br/> | <dl> <span data-ttu-id="0e98c-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0e98c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e98c-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e98c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e98c-122">**CVideoTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="0e98c-122">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




