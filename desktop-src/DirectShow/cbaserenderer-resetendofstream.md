---
description: La méthode ResetEndOfStream réinitialise les indicateurs de fin de flux.
ms.assetid: 80f6d49b-a825-4c3c-b693-7b1d9298f541
title: Méthode CBaseRenderer. ResetEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0269ee2dfafea9265b5eeb82caa4c39f8d91320c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529016"
---
# <a name="cbaserendererresetendofstream-method"></a><span data-ttu-id="28de9-103">Méthode CBaseRenderer. ResetEndOfStream</span><span class="sxs-lookup"><span data-stu-id="28de9-103">CBaseRenderer.ResetEndOfStream method</span></span>

<span data-ttu-id="28de9-104">La `ResetEndOfStream` méthode réinitialise les indicateurs de fin de flux.</span><span class="sxs-lookup"><span data-stu-id="28de9-104">The `ResetEndOfStream` method resets the end-of-stream flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="28de9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28de9-105">Syntax</span></span>


```C++
virtual HRESULT ResetEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="28de9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28de9-106">Parameters</span></span>

<span data-ttu-id="28de9-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="28de9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28de9-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28de9-108">Return value</span></span>

<span data-ttu-id="28de9-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="28de9-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="28de9-110">Notes</span><span class="sxs-lookup"><span data-stu-id="28de9-110">Remarks</span></span>

<span data-ttu-id="28de9-111">Cette méthode efface la condition de fin de flux précédente.</span><span class="sxs-lookup"><span data-stu-id="28de9-111">This method clears the previous end-of-stream condition.</span></span> <span data-ttu-id="28de9-112">À ce stade, le filtre peut recevoir de nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="28de9-112">At that point, the filter can receive new data.</span></span> <span data-ttu-id="28de9-113">Les méthodes [**CBaseRenderer :: Stop**](cbaserenderer-stop.md) et [**CBaseRenderer :: BeginFlush**](cbaserenderer-beginflush.md) appellent cette méthode.</span><span class="sxs-lookup"><span data-stu-id="28de9-113">The [**CBaseRenderer::Stop**](cbaserenderer-stop.md) and [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) methods call this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="28de9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28de9-114">Requirements</span></span>



| <span data-ttu-id="28de9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28de9-115">Requirement</span></span> | <span data-ttu-id="28de9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="28de9-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28de9-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="28de9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="28de9-118"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28de9-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="28de9-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="28de9-119">Library</span></span><br/> | <dl> <span data-ttu-id="28de9-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="28de9-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28de9-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28de9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28de9-122">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="28de9-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




