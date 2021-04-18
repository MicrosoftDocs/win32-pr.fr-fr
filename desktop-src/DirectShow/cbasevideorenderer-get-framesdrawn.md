---
description: La \_ méthode obtenir FramesDrawn récupère la \_ variable membre cFramesDrawn, en donnant le nombre de frames dessinés depuis le début de la diffusion en continu.
ms.assetid: 486b5541-2952-47ce-944e-4efb8e5af9dd
title: Méthode CBaseVideoRenderer.get_FramesDrawn (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDrawn
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec8254e06429022bf657322e98ab317475c82f90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540388"
---
# <a name="cbasevideorendererget_framesdrawn-method"></a><span data-ttu-id="b3259-103">Méthode CBaseVideoRenderer. obten \_ FramesDrawn</span><span class="sxs-lookup"><span data-stu-id="b3259-103">CBaseVideoRenderer.get\_FramesDrawn method</span></span>

<span data-ttu-id="b3259-104">La `get_FramesDrawn` méthode récupère la variable de membre **m \_ cFramesDrawn** , en donnant le nombre d’images dessinées depuis le début de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="b3259-104">The `get_FramesDrawn` method retrieves the **m\_cFramesDrawn** member variable, giving the number of frames drawn since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3259-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3259-105">Syntax</span></span>


```C++
HRESULT get_FramesDrawn(
   int *pcFramesDrawn
);
```



## <a name="parameters"></a><span data-ttu-id="b3259-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3259-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3259-107">*pcFramesDrawn*</span><span class="sxs-lookup"><span data-stu-id="b3259-107">*pcFramesDrawn*</span></span> 
</dt> <dd>

<span data-ttu-id="b3259-108">Pointeur vers le nombre de frames dessinés.</span><span class="sxs-lookup"><span data-stu-id="b3259-108">Pointer to the number of frames drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3259-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3259-109">Return value</span></span>

<span data-ttu-id="b3259-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b3259-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3259-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b3259-111">Remarks</span></span>

<span data-ttu-id="b3259-112">Cette fonction membre implémente la méthode [**IQualProp :: obten \_ FramesDrawn**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdrawn) .</span><span class="sxs-lookup"><span data-stu-id="b3259-112">This member function implements the [**IQualProp::get\_FramesDrawn**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdrawn) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3259-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3259-113">Requirements</span></span>



| <span data-ttu-id="b3259-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3259-114">Requirement</span></span> | <span data-ttu-id="b3259-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3259-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3259-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3259-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b3259-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3259-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b3259-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b3259-118">Library</span></span><br/> | <dl> <span data-ttu-id="b3259-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b3259-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3259-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3259-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3259-121">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="b3259-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




