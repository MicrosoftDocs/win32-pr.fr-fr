---
description: 'Méthode CBasePin. CheckMediaType : la méthode CheckMediaType détermine si le code PIN accepte un type de média spécifique.'
ms.assetid: 6a138679-02b7-4ccc-8881-a0d496f84f93
title: Méthode CBasePin. CheckMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afe39f3a7aac155f3cc87fa6d58f402043861d1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099396"
---
# <a name="cbasepincheckmediatype-method"></a><span data-ttu-id="781bc-103">Méthode CBasePin. CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="781bc-103">CBasePin.CheckMediaType method</span></span>

<span data-ttu-id="781bc-104">La `CheckMediaType` méthode détermine si le code PIN accepte un type de média spécifique.</span><span class="sxs-lookup"><span data-stu-id="781bc-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="781bc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="781bc-105">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="781bc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="781bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="781bc-107">*crédit*</span><span class="sxs-lookup"><span data-stu-id="781bc-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="781bc-108">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui contient le type de média proposé.</span><span class="sxs-lookup"><span data-stu-id="781bc-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="781bc-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="781bc-109">Return value</span></span>

<span data-ttu-id="781bc-110">Retourne S \_ OK si le type de média proposé est acceptable.</span><span class="sxs-lookup"><span data-stu-id="781bc-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="781bc-111">Sinon, retourne S \_ false ou un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="781bc-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="781bc-112">Notes </span><span class="sxs-lookup"><span data-stu-id="781bc-112">Remarks</span></span>

<span data-ttu-id="781bc-113">La classe dérivée doit substituer cette méthode virtuelle pure.</span><span class="sxs-lookup"><span data-stu-id="781bc-113">The derived class must override this pure virtual method.</span></span>

## <a name="requirements"></a><span data-ttu-id="781bc-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="781bc-114">Requirements</span></span>



| <span data-ttu-id="781bc-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="781bc-115">Requirement</span></span> | <span data-ttu-id="781bc-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="781bc-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="781bc-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="781bc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="781bc-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="781bc-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="781bc-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="781bc-119">Library</span></span><br/> | <dl> <span data-ttu-id="781bc-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="781bc-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="781bc-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="781bc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="781bc-122">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="781bc-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




