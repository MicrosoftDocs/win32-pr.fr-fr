---
description: Méthode de constructeur. Le constructeur obtient l’accès au code confidentiel spécifié.
ms.assetid: 518d41aa-8361-4769-aa9b-14676b676d6f
title: Constructeur CAutoUsingOutputPin. CAutoUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin.CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94bafcdcb6e44a07afdccea382d783c20a9ad2ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533314"
---
# <a name="cautousingoutputpincautousingoutputpin-constructor"></a><span data-ttu-id="73a68-104">Constructeur CAutoUsingOutputPin. CAutoUsingOutputPin</span><span class="sxs-lookup"><span data-stu-id="73a68-104">CAutoUsingOutputPin.CAutoUsingOutputPin constructor</span></span>

<span data-ttu-id="73a68-105">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="73a68-105">Constructor method.</span></span> <span data-ttu-id="73a68-106">Le constructeur obtient l’accès au code confidentiel spécifié.</span><span class="sxs-lookup"><span data-stu-id="73a68-106">The constructor obtains access to the specified pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="73a68-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73a68-107">Syntax</span></span>


```C++
CAutoUsingOutputPin(
   CDynamicOutputPin *pOutputPin,
   HRESULT           *phr
);
```



## <a name="parameters"></a><span data-ttu-id="73a68-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73a68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73a68-109">*pOutputPin*</span><span class="sxs-lookup"><span data-stu-id="73a68-109">*pOutputPin*</span></span> 
</dt> <dd>

<span data-ttu-id="73a68-110">Pointeur vers un objet [**CDynamicOutputPin**](cdynamicoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="73a68-110">Pointer to a [**CDynamicOutputPin**](cdynamicoutputpin.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="73a68-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="73a68-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="73a68-112">Pointeur vers une variable qui contient une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="73a68-112">Pointer to a variable that contains an **HRESULT** value.</span></span> <span data-ttu-id="73a68-113">La valeur doit être \_ OK.</span><span class="sxs-lookup"><span data-stu-id="73a68-113">The value must be S\_OK.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73a68-114">Notes</span><span class="sxs-lookup"><span data-stu-id="73a68-114">Remarks</span></span>

<span data-ttu-id="73a68-115">Lorsque la méthode retourne, la valeur de *\* PHR* indique la réussite ou l’échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="73a68-115">When the method returns, the value of *\*phr* indicates the success or failure of the method.</span></span>

## <a name="requirements"></a><span data-ttu-id="73a68-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73a68-116">Requirements</span></span>



| <span data-ttu-id="73a68-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73a68-117">Requirement</span></span> | <span data-ttu-id="73a68-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="73a68-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73a68-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="73a68-119">Header</span></span><br/>  | <dl> <span data-ttu-id="73a68-120"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="73a68-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="73a68-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="73a68-121">Library</span></span><br/> | <dl> <span data-ttu-id="73a68-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="73a68-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73a68-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73a68-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73a68-124">**CAutoUsingOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="73a68-124">**CAutoUsingOutputPin Class**</span></span>](cautousingoutputpin-cautousingoutputpin.md)
</dt> </dl>

 

 




