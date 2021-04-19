---
description: La méthode GetCurrentSample récupère l’exemple actuel.
ms.assetid: cfdc66e3-7d32-47b7-87f6-99dd9513c93b
title: Méthode CBaseRenderer. GetCurrentSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetCurrentSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48c42ff02b22d30138fcad7d1e8af5e57a391b99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544453"
---
# <a name="cbaserenderergetcurrentsample-method"></a><span data-ttu-id="72d96-103">Méthode CBaseRenderer. GetCurrentSample</span><span class="sxs-lookup"><span data-stu-id="72d96-103">CBaseRenderer.GetCurrentSample method</span></span>

<span data-ttu-id="72d96-104">La `GetCurrentSample` méthode récupère l’exemple actuel.</span><span class="sxs-lookup"><span data-stu-id="72d96-104">The `GetCurrentSample` method retrieves the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="72d96-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72d96-105">Syntax</span></span>


```C++
virtual IMediaSample* GetCurrentSample();
```



## <a name="parameters"></a><span data-ttu-id="72d96-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72d96-106">Parameters</span></span>

<span data-ttu-id="72d96-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="72d96-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72d96-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="72d96-108">Return value</span></span>

<span data-ttu-id="72d96-109">Retourne un pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple, ou **null** si aucun échantillon n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="72d96-109">Returns a pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface, or **NULL** if no sample is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="72d96-110">Notes</span><span class="sxs-lookup"><span data-stu-id="72d96-110">Remarks</span></span>

<span data-ttu-id="72d96-111">À moins que la méthode ne retourne la **valeur null**, la méthode appelle **AddRef** sur le pointeur [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) avant de la retourner.</span><span class="sxs-lookup"><span data-stu-id="72d96-111">Unless the method returns **NULL**, the method calls **AddRef** on the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointer before returning it.</span></span> <span data-ttu-id="72d96-112">L’appelant doit libérer le pointeur.</span><span class="sxs-lookup"><span data-stu-id="72d96-112">The caller must release the pointer.</span></span> <span data-ttu-id="72d96-113">(Par implication, vous devez affecter la valeur de retour à une variable, afin de pouvoir la libérer ultérieurement.)</span><span class="sxs-lookup"><span data-stu-id="72d96-113">(By implication, you must assign the return value to a variable, so that you can release it later.)</span></span>

## <a name="requirements"></a><span data-ttu-id="72d96-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72d96-114">Requirements</span></span>



| <span data-ttu-id="72d96-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72d96-115">Requirement</span></span> | <span data-ttu-id="72d96-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="72d96-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72d96-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="72d96-117">Header</span></span><br/>  | <dl> <span data-ttu-id="72d96-118"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="72d96-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="72d96-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="72d96-119">Library</span></span><br/> | <dl> <span data-ttu-id="72d96-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="72d96-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72d96-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72d96-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72d96-122">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="72d96-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




