---
description: 'La méthode EndFlush termine une opération de vidage. Cette méthode implémente la méthode IPin :: EndFlush.'
ms.assetid: 5c27bf76-6886-431d-9958-5064c53909ec
title: Méthode CRenderedInputPin. EndFlush (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d80f6cbc31a8bc5bf797847465a218f32631c1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524063"
---
# <a name="crenderedinputpinendflush-method"></a><span data-ttu-id="e6b8a-104">Méthode CRenderedInputPin. EndFlush</span><span class="sxs-lookup"><span data-stu-id="e6b8a-104">CRenderedInputPin.EndFlush method</span></span>

<span data-ttu-id="e6b8a-105">La `EndFlush` méthode termine une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="e6b8a-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="e6b8a-106">Cette méthode implémente la méthode [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="e6b8a-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6b8a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6b8a-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="e6b8a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6b8a-108">Parameters</span></span>

<span data-ttu-id="e6b8a-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e6b8a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6b8a-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6b8a-110">Return value</span></span>

<span data-ttu-id="e6b8a-111">Retourne S \_ OK en cas de réussite, ou un code d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e6b8a-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6b8a-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e6b8a-112">Remarks</span></span>

<span data-ttu-id="e6b8a-113">Cette méthode efface tous les événements d' [**\_ achèvement EC**](ec-complete.md) en attente.</span><span class="sxs-lookup"><span data-stu-id="e6b8a-113">This method clears any pending [**EC\_COMPLETE**](ec-complete.md) events.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6b8a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6b8a-114">Requirements</span></span>



| <span data-ttu-id="e6b8a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6b8a-115">Requirement</span></span> | <span data-ttu-id="e6b8a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6b8a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6b8a-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6b8a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e6b8a-118"><dt>Amextra. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6b8a-118"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e6b8a-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e6b8a-119">Library</span></span><br/> | <dl> <span data-ttu-id="e6b8a-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e6b8a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6b8a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6b8a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6b8a-122">**CRenderedInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="e6b8a-122">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




