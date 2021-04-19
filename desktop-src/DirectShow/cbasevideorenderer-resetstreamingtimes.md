---
description: La méthode ResetStreamingTimes réinitialise toutes les heures qui contrôlent la diffusion en continu.
ms.assetid: 8a596760-a45a-4486-bb91-aab10bbf927f
title: Méthode CBaseVideoRenderer. ResetStreamingTimes (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ResetStreamingTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d887ca9e246d5e3fb746c119b1ed6784201ec702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543588"
---
# <a name="cbasevideorendererresetstreamingtimes-method"></a><span data-ttu-id="13fd5-103">Méthode CBaseVideoRenderer. ResetStreamingTimes</span><span class="sxs-lookup"><span data-stu-id="13fd5-103">CBaseVideoRenderer.ResetStreamingTimes method</span></span>

<span data-ttu-id="13fd5-104">La `ResetStreamingTimes` méthode réinitialise toutes les fois qui contrôlent la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="13fd5-104">The `ResetStreamingTimes` method resets all times that control the streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="13fd5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13fd5-105">Syntax</span></span>


```C++
virtual HRESULT ResetStreamingTimes();
```



## <a name="parameters"></a><span data-ttu-id="13fd5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13fd5-106">Parameters</span></span>

<span data-ttu-id="13fd5-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="13fd5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="13fd5-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="13fd5-108">Return value</span></span>

<span data-ttu-id="13fd5-109">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="13fd5-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13fd5-110">Notes</span><span class="sxs-lookup"><span data-stu-id="13fd5-110">Remarks</span></span>

<span data-ttu-id="13fd5-111">Les heures sont définies de sorte que les frames ne soient pas supprimés initialement et que la première image soit dessinée.</span><span class="sxs-lookup"><span data-stu-id="13fd5-111">The times are set so that frames will not be initially dropped and so that the first frame will be drawn.</span></span>

## <a name="requirements"></a><span data-ttu-id="13fd5-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13fd5-112">Requirements</span></span>



| <span data-ttu-id="13fd5-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13fd5-113">Requirement</span></span> | <span data-ttu-id="13fd5-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="13fd5-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13fd5-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="13fd5-115">Header</span></span><br/>  | <dl> <span data-ttu-id="13fd5-116"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13fd5-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="13fd5-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="13fd5-117">Library</span></span><br/> | <dl> <span data-ttu-id="13fd5-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="13fd5-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13fd5-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13fd5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13fd5-120">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="13fd5-120">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




