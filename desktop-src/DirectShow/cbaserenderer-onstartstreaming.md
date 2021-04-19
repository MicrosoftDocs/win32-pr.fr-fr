---
description: La méthode OnStartStreaming est appelée quand le filtre commence la diffusion en continu.
ms.assetid: 02a5b334-f6c4-4cba-8882-c6b36d97feb3
title: Méthode CBaseRenderer. OnStartStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66433795b0674e1d2d5b7a7de5b1dcd1b50eb424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542576"
---
# <a name="cbaserendereronstartstreaming-method"></a><span data-ttu-id="6b7c6-103">Méthode CBaseRenderer. OnStartStreaming</span><span class="sxs-lookup"><span data-stu-id="6b7c6-103">CBaseRenderer.OnStartStreaming method</span></span>

<span data-ttu-id="6b7c6-104">La `OnStartStreaming` méthode est appelée lorsque le filtre commence la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-104">The `OnStartStreaming` method is called when the filter begins streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b7c6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b7c6-105">Syntax</span></span>


```C++
virtual HRESULT OnStartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="6b7c6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b7c6-106">Parameters</span></span>

<span data-ttu-id="6b7c6-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6b7c6-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6b7c6-108">Return value</span></span>

<span data-ttu-id="6b7c6-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b7c6-110">Notes</span><span class="sxs-lookup"><span data-stu-id="6b7c6-110">Remarks</span></span>

<span data-ttu-id="6b7c6-111">La méthode [**CBaseRenderer :: StartStreaming**](cbaserenderer-startstreaming.md) appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-111">The [**CBaseRenderer::StartStreaming**](cbaserenderer-startstreaming.md) method calls this method.</span></span> <span data-ttu-id="6b7c6-112">Elle ne fait rien dans la classe de base, mais la classe dérivée peut la substituer.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-112">It does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b7c6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b7c6-113">Requirements</span></span>



| <span data-ttu-id="6b7c6-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b7c6-114">Requirement</span></span> | <span data-ttu-id="6b7c6-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b7c6-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b7c6-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="6b7c6-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6b7c6-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b7c6-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6b7c6-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6b7c6-118">Library</span></span><br/> | <dl> <span data-ttu-id="6b7c6-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6b7c6-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b7c6-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b7c6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b7c6-121">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="6b7c6-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




