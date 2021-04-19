---
description: 'La méthode IsPreroll détermine si cet exemple est un exemple de préroll. Un exemple de préroll ne doit pas être affiché. Cette méthode implémente la méthode IMediaSample :: IsPreroll.'
ms.assetid: fbcf7aab-473c-49c1-9a8f-4a619f4e28f4
title: Méthode CMediaSample. IsPreroll (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b40cf8fd6a1adb5186309f47da0f0ae3dc30412a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520803"
---
# <a name="cmediasampleispreroll-method"></a><span data-ttu-id="ba112-105">Méthode CMediaSample. IsPreroll</span><span class="sxs-lookup"><span data-stu-id="ba112-105">CMediaSample.IsPreroll method</span></span>

<span data-ttu-id="ba112-106">La `IsPreroll` méthode détermine si cet exemple est un exemple de préroll.</span><span class="sxs-lookup"><span data-stu-id="ba112-106">The `IsPreroll` method determines if this sample is a preroll sample.</span></span> <span data-ttu-id="ba112-107">Un exemple de préroll ne doit pas être affiché.</span><span class="sxs-lookup"><span data-stu-id="ba112-107">A preroll sample should not be displayed.</span></span> <span data-ttu-id="ba112-108">Cette méthode implémente la méthode [**IMediaSample :: IsPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll) .</span><span class="sxs-lookup"><span data-stu-id="ba112-108">This method implements the [**IMediaSample::IsPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba112-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba112-109">Syntax</span></span>


```C++
HRESULT IsPreroll();
```



## <a name="parameters"></a><span data-ttu-id="ba112-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba112-110">Parameters</span></span>

<span data-ttu-id="ba112-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ba112-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ba112-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ba112-112">Return value</span></span>

<span data-ttu-id="ba112-113">Retourne S \_ OK si l’exemple est un exemple de préroll et s \_ false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ba112-113">Returns S\_OK if the sample is a preroll sample, and S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba112-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ba112-114">Remarks</span></span>

<span data-ttu-id="ba112-115">La variable de membre [**CMediaSample :: m \_ dwFlags**](cmediasample-m-dwflags.md) spécifie cette propriété.</span><span class="sxs-lookup"><span data-stu-id="ba112-115">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba112-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba112-116">Requirements</span></span>



| <span data-ttu-id="ba112-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba112-117">Requirement</span></span> | <span data-ttu-id="ba112-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba112-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba112-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba112-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ba112-120"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba112-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ba112-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ba112-121">Library</span></span><br/> | <dl> <span data-ttu-id="ba112-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ba112-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba112-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba112-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba112-124">**CMediaSample, classe**</span><span class="sxs-lookup"><span data-stu-id="ba112-124">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




