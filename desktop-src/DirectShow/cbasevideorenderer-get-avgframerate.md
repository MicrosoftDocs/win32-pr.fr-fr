---
description: La \_ méthode obtenir AvgFrameRate calcule et récupère la fréquence d’images moyenne atteinte.
ms.assetid: f36fc020-8c1a-491f-9f55-18265fde8bf8
title: Méthode CBaseVideoRenderer.get_AvgFrameRate (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgFrameRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56d8fff53f3d56676805eca9029670d51210ef2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543292"
---
# <a name="cbasevideorendererget_avgframerate-method"></a><span data-ttu-id="02edf-103">Méthode CBaseVideoRenderer. obten \_ AvgFrameRate</span><span class="sxs-lookup"><span data-stu-id="02edf-103">CBaseVideoRenderer.get\_AvgFrameRate method</span></span>

<span data-ttu-id="02edf-104">La `get_AvgFrameRate` méthode calcule et récupère la fréquence d’images moyenne atteinte.</span><span class="sxs-lookup"><span data-stu-id="02edf-104">The `get_AvgFrameRate` method calculates and retrieves the average frame rate achieved.</span></span>

## <a name="syntax"></a><span data-ttu-id="02edf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02edf-105">Syntax</span></span>


```C++
HRESULT get_AvgFrameRate(
   int *piAvgFrameRate
);
```



## <a name="parameters"></a><span data-ttu-id="02edf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02edf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02edf-107">*piAvgFrameRate*</span><span class="sxs-lookup"><span data-stu-id="02edf-107">*piAvgFrameRate*</span></span> 
</dt> <dd>

<span data-ttu-id="02edf-108">Pointeur vers le nombre d’images par seconde depuis le début de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="02edf-108">Pointer to the number of frames per second since streaming began.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02edf-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="02edf-109">Return value</span></span>

<span data-ttu-id="02edf-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="02edf-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02edf-111">Notes</span><span class="sxs-lookup"><span data-stu-id="02edf-111">Remarks</span></span>

<span data-ttu-id="02edf-112">Cette fonction membre implémente la méthode [**IQualProp :: obten \_ AvgFrameRate**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate) .</span><span class="sxs-lookup"><span data-stu-id="02edf-112">This member function implements the [**IQualProp::get\_AvgFrameRate**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="02edf-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02edf-113">Requirements</span></span>



| <span data-ttu-id="02edf-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02edf-114">Requirement</span></span> | <span data-ttu-id="02edf-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="02edf-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02edf-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="02edf-116">Header</span></span><br/>  | <dl> <span data-ttu-id="02edf-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02edf-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="02edf-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="02edf-118">Library</span></span><br/> | <dl> <span data-ttu-id="02edf-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="02edf-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02edf-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02edf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02edf-121">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="02edf-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




