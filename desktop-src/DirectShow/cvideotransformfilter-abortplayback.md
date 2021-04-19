---
description: La méthode AbortPlayback est utilisée pour signaler une erreur de diffusion en continu. Elle envoie un \_ événement EC ERRORABORT au gestionnaire de graphique de filtre et envoie une notification de fin de flux en aval.
ms.assetid: b48ec72f-d220-4b27-98fc-88eaa4f663eb
title: Méthode CVideoTransformFilter. AbortPlayback (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AbortPlayback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 952987dec315408920e92d79003480a01640d14e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525928"
---
# <a name="cvideotransformfilterabortplayback-method"></a><span data-ttu-id="66ab1-104">Méthode CVideoTransformFilter. AbortPlayback</span><span class="sxs-lookup"><span data-stu-id="66ab1-104">CVideoTransformFilter.AbortPlayback method</span></span>

<span data-ttu-id="66ab1-105">La `AbortPlayback` méthode est utilisée pour signaler une erreur de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="66ab1-105">The `AbortPlayback` method is used to signal a streaming error.</span></span> <span data-ttu-id="66ab1-106">Elle envoie un événement [**EC \_ ERRORABORT**](ec-errorabort.md) au gestionnaire de graphique de filtre et envoie une notification de fin de flux en aval.</span><span class="sxs-lookup"><span data-stu-id="66ab1-106">It sends an [**EC\_ERRORABORT**](ec-errorabort.md) event to the Filter Graph Manager, and sends an end-of-stream notification downstream.</span></span>

## <a name="syntax"></a><span data-ttu-id="66ab1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66ab1-107">Syntax</span></span>


```C++
HRESULT AbortPlayback(
   HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="66ab1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66ab1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66ab1-109">*heure(s)*</span><span class="sxs-lookup"><span data-stu-id="66ab1-109">*hr*</span></span> 
</dt> <dd>

<span data-ttu-id="66ab1-110">Valeur **HRESULT** de l’opération qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="66ab1-110">**HRESULT** value of the operation that failed.</span></span> <span data-ttu-id="66ab1-111">Cette valeur est utilisée comme premier paramètre d’événement pour l' \_ événement EC ERRORABORT.</span><span class="sxs-lookup"><span data-stu-id="66ab1-111">This value is used as the first event parameter for the EC\_ERRORABORT event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66ab1-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="66ab1-112">Return value</span></span>

<span data-ttu-id="66ab1-113">Retourne la valeur du paramètre *HR* .</span><span class="sxs-lookup"><span data-stu-id="66ab1-113">Returns the value of the *hr* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="66ab1-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66ab1-114">Requirements</span></span>



| <span data-ttu-id="66ab1-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66ab1-115">Requirement</span></span> | <span data-ttu-id="66ab1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="66ab1-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66ab1-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="66ab1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="66ab1-118"><dt>Vtrans. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66ab1-118"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="66ab1-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="66ab1-119">Library</span></span><br/> | <dl> <span data-ttu-id="66ab1-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="66ab1-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66ab1-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66ab1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66ab1-122">**CVideoTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="66ab1-122">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




