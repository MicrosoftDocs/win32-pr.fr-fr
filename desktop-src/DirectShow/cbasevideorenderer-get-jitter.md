---
description: La \_ méthode obtenir gigue récupère l’écart-type de temps en millisecondes entre chaque frame et le suivant pour toutes les trames depuis le début de la diffusion en continu.
ms.assetid: 629e725e-7dee-4824-8f79-cd3335f4901b
title: Méthode CBaseVideoRenderer.get_Jitter (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_Jitter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef39cdb1b7a77dab22db9728268bf7b23b9fcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542288"
---
# <a name="cbasevideorendererget_jitter-method"></a><span data-ttu-id="b5710-103">CBaseVideoRenderer. obtient la \_ méthode d’instabilité</span><span class="sxs-lookup"><span data-stu-id="b5710-103">CBaseVideoRenderer.get\_Jitter method</span></span>

<span data-ttu-id="b5710-104">La `get_Jitter` méthode récupère l’écart type de temps, en millisecondes, entre chaque frame et le suivant pour tous les frames depuis le début de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="b5710-104">The `get_Jitter` method retrieves the standard deviation of time in milliseconds between each frame and the next for all frames since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5710-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5710-105">Syntax</span></span>


```C++
HRESULT get_Jitter(
   int *piJitter
);
```



## <a name="parameters"></a><span data-ttu-id="b5710-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5710-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5710-107">*piJitter*</span><span class="sxs-lookup"><span data-stu-id="b5710-107">*piJitter*</span></span> 
</dt> <dd>

<span data-ttu-id="b5710-108">Pointeur vers l’écart type du temps d’intertramage, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="b5710-108">Pointer to the standard deviation of the interframe time, in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5710-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b5710-109">Return value</span></span>

<span data-ttu-id="b5710-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b5710-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5710-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b5710-111">Remarks</span></span>

<span data-ttu-id="b5710-112">Cette fonction membre implémente la méthode [**IQualProp :: obtient \_ Gigu**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_jitter) .</span><span class="sxs-lookup"><span data-stu-id="b5710-112">This member function implements the [**IQualProp::get\_Jitter**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_jitter) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5710-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5710-113">Requirements</span></span>



| <span data-ttu-id="b5710-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5710-114">Requirement</span></span> | <span data-ttu-id="b5710-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5710-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5710-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5710-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b5710-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5710-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b5710-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b5710-118">Library</span></span><br/> | <dl> <span data-ttu-id="b5710-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b5710-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5710-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5710-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5710-121">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="b5710-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




