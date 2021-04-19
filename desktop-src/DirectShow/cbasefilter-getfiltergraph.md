---
description: La méthode GetFilterGraph récupère un pointeur vers le gestionnaire de graphique de filtre.
ms.assetid: 80b41272-2ca1-40db-8624-0d99d66f3c34
title: Méthode CBaseFilter. GetFilterGraph (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0843c7789afc1500565d2737d863cbc8af114d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541153"
---
# <a name="cbasefiltergetfiltergraph-method"></a><span data-ttu-id="f59e7-103">Méthode CBaseFilter. GetFilterGraph</span><span class="sxs-lookup"><span data-stu-id="f59e7-103">CBaseFilter.GetFilterGraph method</span></span>

<span data-ttu-id="f59e7-104">La `GetFilterGraph` méthode récupère un pointeur vers le gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="f59e7-104">The `GetFilterGraph` method retrieves a pointer to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="f59e7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f59e7-105">Syntax</span></span>


```C++
IFilterGraph* GetFilterGraph();
```



## <a name="parameters"></a><span data-ttu-id="f59e7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f59e7-106">Parameters</span></span>

<span data-ttu-id="f59e7-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f59e7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f59e7-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f59e7-108">Return value</span></span>

<span data-ttu-id="f59e7-109">Retourne la valeur de [**CBaseFilter :: m \_ pGraph**](cbasefilter-m-pgraph.md).</span><span class="sxs-lookup"><span data-stu-id="f59e7-109">Returns the value of [**CBaseFilter::m\_pGraph**](cbasefilter-m-pgraph.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f59e7-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f59e7-110">Requirements</span></span>



| <span data-ttu-id="f59e7-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f59e7-111">Requirement</span></span> | <span data-ttu-id="f59e7-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="f59e7-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f59e7-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="f59e7-113">Header</span></span><br/>  | <dl> <span data-ttu-id="f59e7-114"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f59e7-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f59e7-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f59e7-115">Library</span></span><br/> | <dl> <span data-ttu-id="f59e7-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f59e7-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f59e7-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f59e7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f59e7-118">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="f59e7-118">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




