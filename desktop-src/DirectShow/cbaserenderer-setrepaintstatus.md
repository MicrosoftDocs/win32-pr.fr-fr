---
description: La méthode SetRepaintStatus active ou désactive les événements de redessin.
ms.assetid: 94ae4935-459e-4009-9f64-c7c5b14504ae
title: Méthode CBaseRenderer. SetRepaintStatus (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetRepaintStatus
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39822b535680a699654e969abc316c10c54ba51b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542767"
---
# <a name="cbaserenderersetrepaintstatus-method"></a><span data-ttu-id="7645d-103">Méthode CBaseRenderer. SetRepaintStatus</span><span class="sxs-lookup"><span data-stu-id="7645d-103">CBaseRenderer.SetRepaintStatus method</span></span>

<span data-ttu-id="7645d-104">La `SetRepaintStatus` méthode active ou désactive les événements de redessin.</span><span class="sxs-lookup"><span data-stu-id="7645d-104">The `SetRepaintStatus` method enables or disables repaint events.</span></span>

## <a name="syntax"></a><span data-ttu-id="7645d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7645d-105">Syntax</span></span>


```C++
void SetRepaintStatus(
   BOOL bRepaint
);
```



## <a name="parameters"></a><span data-ttu-id="7645d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7645d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7645d-107">*bRepaint*</span><span class="sxs-lookup"><span data-stu-id="7645d-107">*bRepaint*</span></span> 
</dt> <dd>

<span data-ttu-id="7645d-108">Valeur booléenne indiquant si les événements de redessination sont activés.</span><span class="sxs-lookup"><span data-stu-id="7645d-108">Boolean value indicating whether repaint events are enabled.</span></span> <span data-ttu-id="7645d-109">Si la **valeur est true**, le filtre envoie les événements de [**\_ redessin ce**](ec-repaint.md) au gestionnaire de graphes de filtre.</span><span class="sxs-lookup"><span data-stu-id="7645d-109">If **TRUE**, the filter will sent [**EC\_REPAINT**](ec-repaint.md) events to the filter graph manager.</span></span> <span data-ttu-id="7645d-110">Dans le cas contraire, il n’enverra pas d' \_ événements de REDESSIN ce.</span><span class="sxs-lookup"><span data-stu-id="7645d-110">Otherwise, it will not send EC\_REPAINT events.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7645d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7645d-111">Return value</span></span>

<span data-ttu-id="7645d-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7645d-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7645d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7645d-113">Remarks</span></span>

<span data-ttu-id="7645d-114">Cette méthode garantit que le gestionnaire de graphes de filtre n’est pas submergé d' \_ événements EC REpains redondants.</span><span class="sxs-lookup"><span data-stu-id="7645d-114">This method ensures that the filter graph manager is not flooded with redundant EC\_REPAINT events.</span></span> <span data-ttu-id="7645d-115">Une fois que le filtre a envoyé un événement de [**\_ redessin ce**](ec-repaint.md) , il appelle cette méthode avec la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="7645d-115">After the filter sends an [**EC\_REPAINT**](ec-repaint.md) event, it calls this method with the value **TRUE**.</span></span> <span data-ttu-id="7645d-116">Le filtre n’envoie pas d’événements de redessin EC supplémentaires tant qu’il n’a pas \_ reçu plus de données.</span><span class="sxs-lookup"><span data-stu-id="7645d-116">The filter does not send more EC\_REPAINT events until it receives more data.</span></span>

## <a name="requirements"></a><span data-ttu-id="7645d-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7645d-117">Requirements</span></span>



| <span data-ttu-id="7645d-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7645d-118">Requirement</span></span> | <span data-ttu-id="7645d-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7645d-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7645d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="7645d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="7645d-121"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7645d-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7645d-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7645d-122">Library</span></span><br/> | <dl> <span data-ttu-id="7645d-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7645d-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7645d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7645d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7645d-125">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="7645d-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




