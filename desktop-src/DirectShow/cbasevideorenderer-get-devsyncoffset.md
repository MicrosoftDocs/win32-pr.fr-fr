---
description: La \_ méthode obtenir DevSyncOffset récupère l’écart type du temps, en millisecondes, entre le moment où chaque image est due et le moment où elle a été réellement rendue, pour toutes les images depuis le début de la diffusion en continu.
ms.assetid: 86f60064-f913-4377-bad0-148a213171fc
title: Méthode CBaseVideoRenderer.get_DevSyncOffset (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_DevSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9926e809901f7290738e2e2cf3d094e54e068580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523949"
---
# <a name="cbasevideorendererget_devsyncoffset-method"></a><span data-ttu-id="a6830-103">Méthode CBaseVideoRenderer. obten \_ DevSyncOffset</span><span class="sxs-lookup"><span data-stu-id="a6830-103">CBaseVideoRenderer.get\_DevSyncOffset method</span></span>

<span data-ttu-id="a6830-104">La `get_DevSyncOffset` méthode récupère l’écart type du temps, en millisecondes, entre le moment où chaque image est due et le moment où elle a été réellement rendue, pour toutes les images depuis le début de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="a6830-104">The `get_DevSyncOffset` method retrieves the standard deviation of the time in milliseconds between when each frame was due and when it was actually rendered, for all frames since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6830-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6830-105">Syntax</span></span>


```C++
HRESULT get_DevSyncOffset(
   int *piDev
);
```



## <a name="parameters"></a><span data-ttu-id="a6830-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6830-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6830-107">*piDev*</span><span class="sxs-lookup"><span data-stu-id="a6830-107">*piDev*</span></span> 
</dt> <dd>

<span data-ttu-id="a6830-108">Pointeur vers l’écart type de l’heure comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="a6830-108">Pointer to the standard deviation of the time as previously described.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6830-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a6830-109">Return value</span></span>

<span data-ttu-id="a6830-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a6830-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6830-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a6830-111">Remarks</span></span>

<span data-ttu-id="a6830-112">Cette fonction membre implémente la méthode [**IQualProp :: obten \_ DevSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset) .</span><span class="sxs-lookup"><span data-stu-id="a6830-112">This member function implements the [**IQualProp::get\_DevSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6830-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6830-113">Requirements</span></span>



| <span data-ttu-id="a6830-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6830-114">Requirement</span></span> | <span data-ttu-id="a6830-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6830-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6830-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6830-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a6830-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6830-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a6830-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a6830-118">Library</span></span><br/> | <dl> <span data-ttu-id="a6830-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a6830-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6830-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6830-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6830-121">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="a6830-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




