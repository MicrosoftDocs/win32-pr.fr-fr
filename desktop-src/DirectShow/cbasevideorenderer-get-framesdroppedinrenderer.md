---
description: La \_ méthode obtenir FramesDroppedInRenderer récupère le nombre de frames supprimés par le convertisseur.
ms.assetid: d890f285-b3bb-426c-80f6-e273cf0cccbb
title: Méthode CBaseVideoRenderer.get_FramesDroppedInRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDroppedInRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef81678fce8d349c7c047b0453cc480d8673f8f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542289"
---
# <a name="cbasevideorendererget_framesdroppedinrenderer-method"></a><span data-ttu-id="f7026-103">Méthode CBaseVideoRenderer. obten \_ FramesDroppedInRenderer</span><span class="sxs-lookup"><span data-stu-id="f7026-103">CBaseVideoRenderer.get\_FramesDroppedInRenderer method</span></span>

<span data-ttu-id="f7026-104">La `get_FramesDroppedInRenderer` méthode récupère le nombre de frames supprimés par le convertisseur.</span><span class="sxs-lookup"><span data-stu-id="f7026-104">The `get_FramesDroppedInRenderer` method retrieves the number of frames dropped by the renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7026-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7026-105">Syntax</span></span>


```C++
HRESULT get_FramesDroppedInRenderer(
   int *pcFramesDropped
);
```



## <a name="parameters"></a><span data-ttu-id="f7026-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7026-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7026-107">*pcFramesDropped*</span><span class="sxs-lookup"><span data-stu-id="f7026-107">*pcFramesDropped*</span></span> 
</dt> <dd>

<span data-ttu-id="f7026-108">Pointeur vers le nombre de frames supprimés.</span><span class="sxs-lookup"><span data-stu-id="f7026-108">Pointer to the number of frames dropped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7026-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7026-109">Return value</span></span>

<span data-ttu-id="f7026-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f7026-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7026-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f7026-111">Remarks</span></span>

<span data-ttu-id="f7026-112">Cette fonction membre implémente la méthode [**IQualProp :: obten \_ FramesDroppedInRenderer**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) .</span><span class="sxs-lookup"><span data-stu-id="f7026-112">This member function implements the [**IQualProp::get\_FramesDroppedInRenderer**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) method.</span></span> <span data-ttu-id="f7026-113">C’est ainsi que la page de propriétés récupère les données du planificateur.</span><span class="sxs-lookup"><span data-stu-id="f7026-113">This is how the property page retrieves the data from the scheduler.</span></span> <span data-ttu-id="f7026-114">Les frames peuvent également être supprimés en amont sans que le convertisseur ne les visualise même.</span><span class="sxs-lookup"><span data-stu-id="f7026-114">Frames can also be dropped upstream without the renderer even seeing them.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7026-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7026-115">Requirements</span></span>



| <span data-ttu-id="f7026-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7026-116">Requirement</span></span> | <span data-ttu-id="f7026-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7026-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7026-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7026-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f7026-119"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7026-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f7026-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f7026-120">Library</span></span><br/> | <dl> <span data-ttu-id="f7026-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f7026-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7026-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7026-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7026-123">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="f7026-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




