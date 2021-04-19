---
description: La méthode IsEndOfStreamDelivered demande si l' \_ événement EC Complete a été remis au gestionnaire du graphique de filtres.
ms.assetid: 13138626-35b0-4da1-9c7e-5d22d86ad2e3
title: Méthode CBaseRenderer. IsEndOfStreamDelivered (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.IsEndOfStreamDelivered
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f60216afc6481411010fb2f2b0618c36a7d7acf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525530"
---
# <a name="cbaserendererisendofstreamdelivered-method"></a><span data-ttu-id="b2d17-103">Méthode CBaseRenderer. IsEndOfStreamDelivered</span><span class="sxs-lookup"><span data-stu-id="b2d17-103">CBaseRenderer.IsEndOfStreamDelivered method</span></span>

<span data-ttu-id="b2d17-104">La `IsEndOfStreamDelivered` méthode détermine si l' \_ événement EC Complete a été remis au gestionnaire du graphique de filtres.</span><span class="sxs-lookup"><span data-stu-id="b2d17-104">The `IsEndOfStreamDelivered` method queries whether the EC\_COMPLETE event has been delivered to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2d17-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2d17-105">Syntax</span></span>


```C++
BOOL IsEndOfStreamDelivered();
```



## <a name="parameters"></a><span data-ttu-id="b2d17-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2d17-106">Parameters</span></span>

<span data-ttu-id="b2d17-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b2d17-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b2d17-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b2d17-108">Return value</span></span>

<span data-ttu-id="b2d17-109">Retourne l’indicateur [**CBaseRenderer :: m \_ bEOSDelivered**](cbaserenderer-m-beosdelivered.md) .</span><span class="sxs-lookup"><span data-stu-id="b2d17-109">Returns the [**CBaseRenderer::m\_bEOSDelivered**](cbaserenderer-m-beosdelivered.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2d17-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2d17-110">Requirements</span></span>



| <span data-ttu-id="b2d17-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2d17-111">Requirement</span></span> | <span data-ttu-id="b2d17-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2d17-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2d17-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="b2d17-113">Header</span></span><br/>  | <dl> <span data-ttu-id="b2d17-114"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2d17-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b2d17-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b2d17-115">Library</span></span><br/> | <dl> <span data-ttu-id="b2d17-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b2d17-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2d17-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2d17-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2d17-118">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="b2d17-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




