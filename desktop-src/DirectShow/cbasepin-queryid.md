---
description: 'La méthode QueryId récupère l’identificateur de code confidentiel. Cette méthode implémente la méthode IPin :: QueryId.'
ms.assetid: b365a574-61b4-454c-b062-8826cbe10f03
title: CBasePin. QueryId, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa14fb933c89da0b0b6d2eebfab480b5508a3666
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545479"
---
# <a name="cbasepinqueryid-method"></a><span data-ttu-id="f304a-104">CBasePin. QueryId, méthode</span><span class="sxs-lookup"><span data-stu-id="f304a-104">CBasePin.QueryId method</span></span>

<span data-ttu-id="f304a-105">La `QueryId` méthode récupère l’identificateur de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="f304a-105">The `QueryId` method retrieves the pin identifier.</span></span> <span data-ttu-id="f304a-106">Cette méthode implémente la méthode [**IPIN :: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .</span><span class="sxs-lookup"><span data-stu-id="f304a-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f304a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f304a-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="f304a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f304a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f304a-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="f304a-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="f304a-110">Pointeur vers l’identificateur de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="f304a-110">Pointer to the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f304a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f304a-111">Return value</span></span>

<span data-ttu-id="f304a-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f304a-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f304a-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f304a-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="f304a-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f304a-114">Return code</span></span>                                                                                   | <span data-ttu-id="f304a-115">Description</span><span class="sxs-lookup"><span data-stu-id="f304a-115">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="f304a-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f304a-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f304a-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="f304a-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="f304a-118"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="f304a-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f304a-119">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="f304a-119">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="f304a-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="f304a-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f304a-121">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="f304a-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f304a-122">Notes</span><span class="sxs-lookup"><span data-stu-id="f304a-122">Remarks</span></span>

<span data-ttu-id="f304a-123">Cette méthode retourne une copie de la variable membre [**CBasePin :: m \_ pname**](cbasepin-m-pname.md) .</span><span class="sxs-lookup"><span data-stu-id="f304a-123">This method returns a copy of the [**CBasePin::m\_pName**](cbasepin-m-pname.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="f304a-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f304a-124">Requirements</span></span>



| <span data-ttu-id="f304a-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f304a-125">Requirement</span></span> | <span data-ttu-id="f304a-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f304a-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f304a-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="f304a-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f304a-128"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f304a-128"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f304a-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f304a-129">Library</span></span><br/> | <dl> <span data-ttu-id="f304a-130"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f304a-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f304a-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f304a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f304a-132">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="f304a-132">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




