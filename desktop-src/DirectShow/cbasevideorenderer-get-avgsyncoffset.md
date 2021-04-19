---
description: La \_ méthode obtenir AvgSyncOffset récupère la moyenne du temps, en millisecondes, entre le moment où chaque trame est due et le moment où elle a été réellement restituée pour toutes les trames depuis le début de la diffusion en continu.
ms.assetid: b41741e9-e0b5-4c49-93ef-cb8c0cf2ddeb
title: Méthode CBaseVideoRenderer.get_AvgSyncOffset (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35c682b8f4bb60ec629db5489e879d1ca7968b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545407"
---
# <a name="cbasevideorendererget_avgsyncoffset-method"></a><span data-ttu-id="0d9c4-103">Méthode CBaseVideoRenderer. obten \_ AvgSyncOffset</span><span class="sxs-lookup"><span data-stu-id="0d9c4-103">CBaseVideoRenderer.get\_AvgSyncOffset method</span></span>

<span data-ttu-id="0d9c4-104">La `get_AvgSyncOffset` méthode récupère la moyenne du temps, en millisecondes, entre le moment où chaque trame est due et le moment où elle a été réellement restituée pour toutes les trames depuis le début de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="0d9c4-104">The `get_AvgSyncOffset` method retrieves the average of the time in milliseconds between when each frame was due and when it was actually rendered for all frames since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d9c4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d9c4-105">Syntax</span></span>


```C++
HRESULT get_AvgSyncOffset(
   int *piAvg
);
```



## <a name="parameters"></a><span data-ttu-id="0d9c4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d9c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d9c4-107">*piAvg*</span><span class="sxs-lookup"><span data-stu-id="0d9c4-107">*piAvg*</span></span> 
</dt> <dd>

<span data-ttu-id="0d9c4-108">Pointeur vers la moyenne du temps, comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="0d9c4-108">Pointer to the average of the time as previously described.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d9c4-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d9c4-109">Return value</span></span>

<span data-ttu-id="0d9c4-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0d9c4-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d9c4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0d9c4-111">Remarks</span></span>

<span data-ttu-id="0d9c4-112">Cette fonction membre implémente la méthode [**IQualProp :: obten \_ AvgSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) .</span><span class="sxs-lookup"><span data-stu-id="0d9c4-112">This member function implements the [**IQualProp::get\_AvgSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d9c4-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d9c4-113">Requirements</span></span>



| <span data-ttu-id="0d9c4-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d9c4-114">Requirement</span></span> | <span data-ttu-id="0d9c4-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d9c4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d9c4-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d9c4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0d9c4-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d9c4-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0d9c4-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0d9c4-118">Library</span></span><br/> | <dl> <span data-ttu-id="0d9c4-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0d9c4-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d9c4-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d9c4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d9c4-121">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="0d9c4-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




