---
description: La méthode GetRenderEvent récupère l’événement qui planifie le rendu.
ms.assetid: da0272f6-6a1d-4c07-a907-822227b56305
title: Méthode CBaseRenderer. GetRenderEvent (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRenderEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e2fd0b9cd98194129eccd2e24e6ee75577d1eec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522776"
---
# <a name="cbaserenderergetrenderevent-method"></a><span data-ttu-id="72f32-103">Méthode CBaseRenderer. GetRenderEvent</span><span class="sxs-lookup"><span data-stu-id="72f32-103">CBaseRenderer.GetRenderEvent method</span></span>

<span data-ttu-id="72f32-104">La `GetRenderEvent` méthode récupère l’événement qui planifie le rendu.</span><span class="sxs-lookup"><span data-stu-id="72f32-104">The `GetRenderEvent` method retrieves the event that schedules rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="72f32-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72f32-105">Syntax</span></span>


```C++
CAMEvent* GetRenderEvent();
```



## <a name="parameters"></a><span data-ttu-id="72f32-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72f32-106">Parameters</span></span>

<span data-ttu-id="72f32-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="72f32-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72f32-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="72f32-108">Return value</span></span>

<span data-ttu-id="72f32-109">Retourne un pointeur vers l’événement [**CBaseRenderer :: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) .</span><span class="sxs-lookup"><span data-stu-id="72f32-109">Returns a pointer to the [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="72f32-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72f32-110">Requirements</span></span>



| <span data-ttu-id="72f32-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72f32-111">Requirement</span></span> | <span data-ttu-id="72f32-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="72f32-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72f32-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="72f32-113">Header</span></span><br/>  | <dl> <span data-ttu-id="72f32-114"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="72f32-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="72f32-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="72f32-115">Library</span></span><br/> | <dl> <span data-ttu-id="72f32-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="72f32-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72f32-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72f32-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72f32-118">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="72f32-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




