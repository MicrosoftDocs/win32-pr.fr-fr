---
description: La méthode StreamingThreadUsingOutputPin détermine si un thread effectue une opération de diffusion en continu sur le code confidentiel.
ms.assetid: b6432a11-4e8b-4eb4-ad8e-aaff9398641b
title: Méthode CDynamicOutputPin. StreamingThreadUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StreamingThreadUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 797dcb94e227861642de2a05e6edf24f675bb4e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526406"
---
# <a name="cdynamicoutputpinstreamingthreadusingoutputpin-method"></a><span data-ttu-id="89ebf-103">Méthode CDynamicOutputPin. StreamingThreadUsingOutputPin</span><span class="sxs-lookup"><span data-stu-id="89ebf-103">CDynamicOutputPin.StreamingThreadUsingOutputPin method</span></span>

<span data-ttu-id="89ebf-104">La méthode StreamingThreadUsingOutputPin détermine si un thread effectue une opération de diffusion en continu sur le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="89ebf-104">The StreamingThreadUsingOutputPin method determines whether any thread is performing a streaming operation on the pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="89ebf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89ebf-105">Syntax</span></span>


```C++
virtual bool StreamingThreadUsingOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="89ebf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89ebf-106">Parameters</span></span>

<span data-ttu-id="89ebf-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="89ebf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="89ebf-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="89ebf-108">Return value</span></span>

<span data-ttu-id="89ebf-109">Retourne la **valeur true** si un thread effectue une opération de diffusion en continu sur le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="89ebf-109">Returns **TRUE** if a thread is performing a streaming operation on the pin.</span></span> <span data-ttu-id="89ebf-110">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="89ebf-110">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="89ebf-111">Notes</span><span class="sxs-lookup"><span data-stu-id="89ebf-111">Remarks</span></span>

<span data-ttu-id="89ebf-112">Si des threads ont été retournés avec succès à partir de la méthode [**CDynamicOutputPin :: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) et n’ont pas effectué d’appel correspondant à la méthode [**CDynamicOutputPin :: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) , cette méthode retourne **true**.</span><span class="sxs-lookup"><span data-stu-id="89ebf-112">If any threads have successfully returned from the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method and have not made a corresponding call to the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method, this method returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="89ebf-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89ebf-113">Requirements</span></span>



| <span data-ttu-id="89ebf-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89ebf-114">Requirement</span></span> | <span data-ttu-id="89ebf-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="89ebf-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89ebf-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="89ebf-116">Header</span></span><br/>  | <dl> <span data-ttu-id="89ebf-117"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89ebf-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="89ebf-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="89ebf-118">Library</span></span><br/> | <dl> <span data-ttu-id="89ebf-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="89ebf-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89ebf-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89ebf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89ebf-121">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="89ebf-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




