---
description: La méthode OnDisplayChange publie un \_ \_ événement de modification d’affichage EC sur le gestionnaire de graphique de filtre.
ms.assetid: e4cdcdf2-7fc2-4893-9897-97bcf2c12610
title: Méthode CBaseRenderer. OnDisplayChange (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnDisplayChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e99a8626d523e8b14b013acc9d2ead462f48df3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537693"
---
# <a name="cbaserendererondisplaychange-method"></a><span data-ttu-id="b1694-103">Méthode CBaseRenderer. OnDisplayChange</span><span class="sxs-lookup"><span data-stu-id="b1694-103">CBaseRenderer.OnDisplayChange method</span></span>

<span data-ttu-id="b1694-104">La `OnDisplayChange` méthode publie un événement de [**\_ \_ modification d’affichage EC**](ec-display-changed.md) sur le gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="b1694-104">The `OnDisplayChange` method posts an [**EC\_DISPLAY\_CHANGED**](ec-display-changed.md) event to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1694-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1694-105">Syntax</span></span>


```C++
BOOL OnDisplayChange();
```



## <a name="parameters"></a><span data-ttu-id="b1694-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1694-106">Parameters</span></span>

<span data-ttu-id="b1694-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b1694-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b1694-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b1694-108">Return value</span></span>

<span data-ttu-id="b1694-109">Retourne la **valeur true** si l’événement a été publié, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b1694-109">Returns **TRUE** if the event was posted, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1694-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b1694-110">Remarks</span></span>

<span data-ttu-id="b1694-111">Les convertisseurs vidéo doivent appeler cette méthode en réponse aux \_ messages WM DISPLAYCHANGE.</span><span class="sxs-lookup"><span data-stu-id="b1694-111">Video renderers should call this method in response to WM\_DISPLAYCHANGE messages.</span></span> <span data-ttu-id="b1694-112">Si la broche d’entrée est connectée, la méthode envoie \_ un \_ événement de modification d’affichage EC au gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="b1694-112">If the input pin is connected, the method sends an EC\_DISPLAY\_CHANGED event to the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1694-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1694-113">Requirements</span></span>



| <span data-ttu-id="b1694-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1694-114">Requirement</span></span> | <span data-ttu-id="b1694-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1694-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1694-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1694-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b1694-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1694-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b1694-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b1694-118">Library</span></span><br/> | <dl> <span data-ttu-id="b1694-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b1694-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1694-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1694-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1694-121">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="b1694-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




