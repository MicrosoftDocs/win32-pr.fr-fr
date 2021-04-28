---
description: 'Méthode CRenderedInputPin. EndFlush : la méthode EndFlush termine une opération de vidage. Cette méthode implémente la méthode IPin :: EndFlush.'
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
ms.openlocfilehash: 7be740df2b3b45d0b681a86b8f70bed8e1395e8f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098917"
---
# <a name="crenderedinputpinendflush-method"></a><span data-ttu-id="ba425-104">Méthode CRenderedInputPin. EndFlush</span><span class="sxs-lookup"><span data-stu-id="ba425-104">CRenderedInputPin.EndFlush method</span></span>

<span data-ttu-id="ba425-105">La `EndFlush` méthode termine une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="ba425-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="ba425-106">Cette méthode implémente la méthode [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="ba425-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba425-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba425-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="ba425-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba425-108">Parameters</span></span>

<span data-ttu-id="ba425-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ba425-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ba425-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ba425-110">Return value</span></span>

<span data-ttu-id="ba425-111">Retourne S \_ OK en cas de réussite, ou un code d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ba425-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba425-112">Notes </span><span class="sxs-lookup"><span data-stu-id="ba425-112">Remarks</span></span>

<span data-ttu-id="ba425-113">Cette méthode efface tous les événements d' [**\_ achèvement EC**](ec-complete.md) en attente.</span><span class="sxs-lookup"><span data-stu-id="ba425-113">This method clears any pending [**EC\_COMPLETE**](ec-complete.md) events.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba425-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba425-114">Requirements</span></span>



| <span data-ttu-id="ba425-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba425-115">Requirement</span></span> | <span data-ttu-id="ba425-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba425-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba425-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba425-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ba425-118"><dt>Amextra. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba425-118"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ba425-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ba425-119">Library</span></span><br/> | <dl> <span data-ttu-id="ba425-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ba425-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba425-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba425-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba425-122">**CRenderedInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="ba425-122">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




