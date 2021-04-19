---
description: La méthode JoinFilterGraph envoie la \_ \_ notification d’événement détruite de la fenêtre EC lorsqu’un filtre est supprimé du graphique de filtre.
ms.assetid: b54d2deb-d36f-43a9-aa00-d607f487d8b7
title: Méthode CBaseVideoRenderer. JoinFilterGraph (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acabb6deeb6577fa04479fc4014e210d4a5654d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541634"
---
# <a name="cbasevideorendererjoinfiltergraph-method"></a><span data-ttu-id="5069d-103">Méthode CBaseVideoRenderer. JoinFilterGraph</span><span class="sxs-lookup"><span data-stu-id="5069d-103">CBaseVideoRenderer.JoinFilterGraph method</span></span>

<span data-ttu-id="5069d-104">La `JoinFilterGraph` méthode envoie la notification d’événement de la [**\_ fenêtre EC \_ détruite**](ec-window-destroyed.md) lorsqu’un filtre est supprimé du graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="5069d-104">The `JoinFilterGraph` method sends [**EC\_WINDOW\_DESTROYED**](ec-window-destroyed.md) event notification when a filter is removed from the filter graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="5069d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5069d-105">Syntax</span></span>


```C++
HRESULT JoinFilterGraph(
       IBaseFilterGraph *pGraph,
  [in] LPCWSTR          pName
);
```



## <a name="parameters"></a><span data-ttu-id="5069d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5069d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5069d-107">*pGraph*</span><span class="sxs-lookup"><span data-stu-id="5069d-107">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="5069d-108">Pointeur vers le graphique de filtre à joindre.</span><span class="sxs-lookup"><span data-stu-id="5069d-108">Pointer to the filter graph to join.</span></span>

</dd> <dt>

<span data-ttu-id="5069d-109">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5069d-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5069d-110">Pointeur vers le nom du filtre ajouté.</span><span class="sxs-lookup"><span data-stu-id="5069d-110">Pointer to the name of the filter being added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5069d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5069d-111">Return value</span></span>

<span data-ttu-id="5069d-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="5069d-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5069d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5069d-113">Remarks</span></span>

<span data-ttu-id="5069d-114">Cette fonction membre remplace la fonction membre [**CBaseFilter :: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) .</span><span class="sxs-lookup"><span data-stu-id="5069d-114">This member function overrides the [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) member function.</span></span> <span data-ttu-id="5069d-115">Si le filtre quitte le graphique de filtre (*pGraph* a la **valeur null**), il envoie une notification d’événement de la [**\_ fenêtre EC \_ détruite**](ec-window-destroyed.md) afin que le gestionnaire de ressources ne conserve pas le convertisseur comme un objet de focus.</span><span class="sxs-lookup"><span data-stu-id="5069d-115">If the filter is leaving the filter graph (*pGraph* is **NULL**), it sends an [**EC\_WINDOW\_DESTROYED**](ec-window-destroyed.md) event notification so that the resource manager does not hold on to the renderer as a focus object.</span></span>

## <a name="requirements"></a><span data-ttu-id="5069d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5069d-116">Requirements</span></span>



| <span data-ttu-id="5069d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5069d-117">Requirement</span></span> | <span data-ttu-id="5069d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5069d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5069d-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="5069d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5069d-120"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5069d-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5069d-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5069d-121">Library</span></span><br/> | <dl> <span data-ttu-id="5069d-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5069d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5069d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5069d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5069d-124">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="5069d-124">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




