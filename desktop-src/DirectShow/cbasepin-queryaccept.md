---
description: 'La méthode QueryAccept détermine si le code PIN accepte un type de média spécifié. Cette méthode implémente la méthode IPin :: QueryAccept.'
ms.assetid: 7aa25b45-5116-474b-afee-1eddc8b7fd2a
title: Méthode CBasePin. QueryAccept (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryAccept
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2c4a982f583d1780dbab37d982fd9a54601e141
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533269"
---
# <a name="cbasepinqueryaccept-method"></a><span data-ttu-id="16e05-104">Méthode CBasePin. QueryAccept</span><span class="sxs-lookup"><span data-stu-id="16e05-104">CBasePin.QueryAccept method</span></span>

<span data-ttu-id="16e05-105">La `QueryAccept` méthode détermine si le pin accepte un type de média spécifié.</span><span class="sxs-lookup"><span data-stu-id="16e05-105">The `QueryAccept` method determines whether the pin accepts a specified media type.</span></span> <span data-ttu-id="16e05-106">Cette méthode implémente la méthode [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) .</span><span class="sxs-lookup"><span data-stu-id="16e05-106">This method implements the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="16e05-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16e05-107">Syntax</span></span>


```C++
HRESULT QueryAccept(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="16e05-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16e05-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16e05-109">*crédit*</span><span class="sxs-lookup"><span data-stu-id="16e05-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="16e05-110">Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui spécifie le type de média.</span><span class="sxs-lookup"><span data-stu-id="16e05-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16e05-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16e05-111">Return value</span></span>

<span data-ttu-id="16e05-112">Retourne S \_ OK si le type de média est acceptable.</span><span class="sxs-lookup"><span data-stu-id="16e05-112">Returns S\_OK if the media type is acceptable.</span></span> <span data-ttu-id="16e05-113">Sinon, retourne S \_ false.</span><span class="sxs-lookup"><span data-stu-id="16e05-113">Otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="16e05-114">Notes</span><span class="sxs-lookup"><span data-stu-id="16e05-114">Remarks</span></span>

<span data-ttu-id="16e05-115">Dans la classe de base, cette méthode délègue à la méthode [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="16e05-115">In the base class, this method delegates to the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="16e05-116">Si **CheckMediaType** échoue, `QueryAccept` retourne la \_ valeur false.</span><span class="sxs-lookup"><span data-stu-id="16e05-116">If **CheckMediaType** fails, `QueryAccept` returns S\_FALSE.</span></span>

<span data-ttu-id="16e05-117">Cette méthode ne contient pas la section critique du pin ([**CBasePin :: m \_ pLock**](cbasepin-m-plock.md)).</span><span class="sxs-lookup"><span data-stu-id="16e05-117">This method does not hold the pin's critical section ([**CBasePin::m\_pLock**](cbasepin-m-plock.md)).</span></span> <span data-ttu-id="16e05-118">Si votre classe dérivée modifie dynamiquement l’ensemble des types de médias acceptables, vous devez substituer cette méthode pour contenir la section critique.</span><span class="sxs-lookup"><span data-stu-id="16e05-118">If your derived class dynamically modifies the set of acceptable media types, you should override this method to hold the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="16e05-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16e05-119">Requirements</span></span>



| <span data-ttu-id="16e05-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16e05-120">Requirement</span></span> | <span data-ttu-id="16e05-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="16e05-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16e05-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="16e05-122">Header</span></span><br/>  | <dl> <span data-ttu-id="16e05-123"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16e05-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="16e05-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="16e05-124">Library</span></span><br/> | <dl> <span data-ttu-id="16e05-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="16e05-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16e05-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16e05-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16e05-127">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="16e05-127">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




