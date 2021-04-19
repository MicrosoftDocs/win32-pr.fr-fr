---
description: La méthode ScheduleSample remplace la classe de base qui effectue le travail principal pour conserver un nombre d’échantillons dessinés et supprimés (qui sont utilisés par l’implémentation de IQualProp).
ms.assetid: 66e4e318-a7ff-4ba0-9ac5-24ba39ac86f1
title: Méthode CBaseVideoRenderer. ScheduleSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62827f1cda9423f9a5128c35289803027bfa78a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539178"
---
# <a name="cbasevideorendererschedulesample-method"></a><span data-ttu-id="9766b-103">Méthode CBaseVideoRenderer. ScheduleSample</span><span class="sxs-lookup"><span data-stu-id="9766b-103">CBaseVideoRenderer.ScheduleSample method</span></span>

<span data-ttu-id="9766b-104">La `ScheduleSample` méthode remplace la classe de base qui effectue le travail principal pour conserver un nombre d’échantillons dessinés et supprimés (qui sont utilisés par l’implémentation de [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) ).</span><span class="sxs-lookup"><span data-stu-id="9766b-104">The `ScheduleSample` method overrides the base class that does the main work to keep a count of samples drawn and dropped (which are used by the [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) implementation).</span></span>

## <a name="syntax"></a><span data-ttu-id="9766b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9766b-105">Syntax</span></span>


```C++
BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="9766b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9766b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9766b-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="9766b-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="9766b-108">Pointeur vers l’exemple de média.</span><span class="sxs-lookup"><span data-stu-id="9766b-108">Pointer to the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9766b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9766b-109">Return value</span></span>

<span data-ttu-id="9766b-110">Retourne la **valeur true** si l’exemple est planifié ; Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="9766b-110">Returns **TRUE** if the sample is scheduled; otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9766b-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9766b-111">Requirements</span></span>



| <span data-ttu-id="9766b-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9766b-112">Requirement</span></span> | <span data-ttu-id="9766b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="9766b-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9766b-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="9766b-114">Header</span></span><br/>  | <dl> <span data-ttu-id="9766b-115"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9766b-115"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9766b-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9766b-116">Library</span></span><br/> | <dl> <span data-ttu-id="9766b-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9766b-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9766b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9766b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9766b-119">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="9766b-119">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




