---
description: 'La méthode ConnectedTo récupère un pointeur désignant le code confidentiel connecté, le cas échéant. Cette méthode implémente la méthode IPin :: ConnectedTo.'
ms.assetid: d8978c9a-e498-4411-a052-f3c2fca570ef
title: Méthode CBasePin. ConnectedTo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectedTo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5003154011f93b2b70ddd49dab00dcc1659eb2f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539662"
---
# <a name="cbasepinconnectedto-method"></a><span data-ttu-id="24ede-104">Méthode CBasePin. ConnectedTo</span><span class="sxs-lookup"><span data-stu-id="24ede-104">CBasePin.ConnectedTo method</span></span>

<span data-ttu-id="24ede-105">La `ConnectedTo` méthode récupère un pointeur vers le code confidentiel connecté, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="24ede-105">The `ConnectedTo` method retrieves a pointer to the connected pin, if any.</span></span> <span data-ttu-id="24ede-106">Cette méthode implémente la méthode [**IPIN :: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) .</span><span class="sxs-lookup"><span data-stu-id="24ede-106">This method implements the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="24ede-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24ede-107">Syntax</span></span>


```C++
HRESULT ConnectedTo(
   IPin **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="24ede-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24ede-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24ede-109">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="24ede-109">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="24ede-110">Adresse d’une variable qui reçoit un pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de l’autre code PIN.</span><span class="sxs-lookup"><span data-stu-id="24ede-110">Address of a variable that receives a pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24ede-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="24ede-111">Return value</span></span>

<span data-ttu-id="24ede-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="24ede-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="24ede-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="24ede-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="24ede-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="24ede-114">Return code</span></span>                                                                                           | <span data-ttu-id="24ede-115">Description</span><span class="sxs-lookup"><span data-stu-id="24ede-115">Description</span></span>                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="24ede-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="24ede-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="24ede-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="24ede-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="24ede-118"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="24ede-118"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="24ede-119">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="24ede-119">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="24ede-120"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="24ede-120"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="24ede-121">Le pin n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="24ede-121">Pin is not connected.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="24ede-122">Notes</span><span class="sxs-lookup"><span data-stu-id="24ede-122">Remarks</span></span>

<span data-ttu-id="24ede-123">Si la méthode est réussie, l’interface **IPIN** qu’elle retourne a un nombre de références en suspens.</span><span class="sxs-lookup"><span data-stu-id="24ede-123">If the method succeeds, the **IPin** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="24ede-124">Veillez à le libérer lorsque vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="24ede-124">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="24ede-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24ede-125">Requirements</span></span>



| <span data-ttu-id="24ede-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24ede-126">Requirement</span></span> | <span data-ttu-id="24ede-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="24ede-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24ede-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="24ede-128">Header</span></span><br/>  | <dl> <span data-ttu-id="24ede-129"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24ede-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="24ede-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="24ede-130">Library</span></span><br/> | <dl> <span data-ttu-id="24ede-131"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="24ede-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24ede-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24ede-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24ede-133">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="24ede-133">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




