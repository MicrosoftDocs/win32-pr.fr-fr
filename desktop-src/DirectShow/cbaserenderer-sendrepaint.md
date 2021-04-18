---
description: La méthode SendRepaint envoie un événement Repaint au gestionnaire de graphique de filtre.
ms.assetid: 78e5c46c-ca5d-4c5d-9dfc-992ce6b150ad
title: Méthode CBaseRenderer. SendRepaint (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendRepaint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b3a88f0c1dae54cb5d9be1e4e9ad3e9677bdd958
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533118"
---
# <a name="cbaserenderersendrepaint-method"></a><span data-ttu-id="9a449-103">Méthode CBaseRenderer. SendRepaint</span><span class="sxs-lookup"><span data-stu-id="9a449-103">CBaseRenderer.SendRepaint method</span></span>

<span data-ttu-id="9a449-104">La `SendRepaint` méthode envoie un événement Repaint au gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="9a449-104">The `SendRepaint` method sends a repaint event to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a449-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a449-105">Syntax</span></span>


```C++
void SendRepaint();
```



## <a name="parameters"></a><span data-ttu-id="9a449-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a449-106">Parameters</span></span>

<span data-ttu-id="9a449-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9a449-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a449-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9a449-108">Return value</span></span>

<span data-ttu-id="9a449-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9a449-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a449-110">Notes</span><span class="sxs-lookup"><span data-stu-id="9a449-110">Remarks</span></span>

<span data-ttu-id="9a449-111">Cette méthode envoie un événement de [**\_ redessin ce**](ec-repaint.md) au gestionnaire de graphes de filtre si les conditions suivantes sont vraies :</span><span class="sxs-lookup"><span data-stu-id="9a449-111">This method sends an [**EC\_REPAINT**](ec-repaint.md) event to the filter graph manager if the following conditions are true:</span></span>

-   <span data-ttu-id="9a449-112">La broche d’entrée est connectée.</span><span class="sxs-lookup"><span data-stu-id="9a449-112">The input pin is connected.</span></span>
-   <span data-ttu-id="9a449-113">Le filtre n’efface pas les données.</span><span class="sxs-lookup"><span data-stu-id="9a449-113">The filter is not flushing data.</span></span>
-   <span data-ttu-id="9a449-114">La fin de flux n’a pas été atteinte.</span><span class="sxs-lookup"><span data-stu-id="9a449-114">The end-of-stream was not reached.</span></span>
-   <span data-ttu-id="9a449-115">L’indicateur [**CBaseRenderer :: m \_ bAbort**](cbaserenderer-m-babort.md) a la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="9a449-115">The [**CBaseRenderer::m\_bAbort**](cbaserenderer-m-babort.md) flag is **FALSE**.</span></span>
-   <span data-ttu-id="9a449-116">L’indicateur [**CBaseRenderer :: m \_ bRepaintStatus**](cbaserenderer-m-brepaintstatus.md) a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="9a449-116">The [**CBaseRenderer::m\_bRepaintStatus**](cbaserenderer-m-brepaintstatus.md) flag is **TRUE**.</span></span>

<span data-ttu-id="9a449-117">En fonction de l’état du graphique, l’événement EC \_ REpaint peut entraîner le renvoi d’un échantillon par le filtre en amont, le graphique de filtre pour la recherche de son emplacement actuel, ou le gestionnaire de graphes de filtre à suspendre momentanément.</span><span class="sxs-lookup"><span data-stu-id="9a449-117">Depending on the state of the graph, the EC\_REPAINT event can cause the upstream filter to re-send a sample; the filter graph to seek to its current location; or the filter graph manager to pause momentarily.</span></span> <span data-ttu-id="9a449-118">(Voir [**ce \_ redessin**](ec-repaint.md).) Cet événement est potentiellement inefficace. il doit donc être utilisé avec modération.</span><span class="sxs-lookup"><span data-stu-id="9a449-118">(See [**EC\_REPAINT**](ec-repaint.md).) This event is potentially inefficient, so it should be used sparingly.</span></span> <span data-ttu-id="9a449-119">Toutefois, les convertisseurs vidéo doivent parfois actualiser l’affichage.</span><span class="sxs-lookup"><span data-stu-id="9a449-119">However, video renderers sometimes need to refresh the display.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a449-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a449-120">Requirements</span></span>



| <span data-ttu-id="9a449-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a449-121">Requirement</span></span> | <span data-ttu-id="9a449-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a449-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a449-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="9a449-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9a449-124"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a449-124"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9a449-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9a449-125">Library</span></span><br/> | <dl> <span data-ttu-id="9a449-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9a449-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a449-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a449-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a449-128">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="9a449-128">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




