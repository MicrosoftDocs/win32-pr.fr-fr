---
description: 'La \_ méthode obtenir le taux récupère la vitesse de lecture. Cette méthode implémente la méthode IMediaPosition :: obten \_ rate.'
ms.assetid: 216cbcef-4874-4565-abb0-8c8bf67fe23c
title: Méthode CPosPassThru.get_Rate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 46e565f51d7c549f524f9e478b2a8326daf690a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522799"
---
# <a name="cpospassthruget_rate-method"></a><span data-ttu-id="cc8eb-104">CPosPassThru. obtient la \_ méthode rate</span><span class="sxs-lookup"><span data-stu-id="cc8eb-104">CPosPassThru.get\_Rate method</span></span>

<span data-ttu-id="cc8eb-105">La `get_Rate` méthode récupère la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="cc8eb-105">The `get_Rate` method retrieves the playback rate.</span></span> <span data-ttu-id="cc8eb-106">Cette méthode implémente la méthode [**IMediaPosition :: obten \_ rate**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate) .</span><span class="sxs-lookup"><span data-stu-id="cc8eb-106">This method implements the [**IMediaPosition::get\_Rate**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc8eb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc8eb-107">Syntax</span></span>


```C++
HRESULT get_Rate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="cc8eb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc8eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc8eb-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="cc8eb-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="cc8eb-110">Pointeur vers une variable qui reçoit la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="cc8eb-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc8eb-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cc8eb-111">Return value</span></span>

<span data-ttu-id="cc8eb-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="cc8eb-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc8eb-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc8eb-113">Requirements</span></span>



| <span data-ttu-id="cc8eb-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc8eb-114">Requirement</span></span> | <span data-ttu-id="cc8eb-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc8eb-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc8eb-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc8eb-116">Header</span></span><br/>  | <dl> <span data-ttu-id="cc8eb-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc8eb-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cc8eb-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cc8eb-118">Library</span></span><br/> | <dl> <span data-ttu-id="cc8eb-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cc8eb-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc8eb-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc8eb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc8eb-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="cc8eb-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




