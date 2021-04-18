---
description: La méthode CheckConnect détermine si une connexion de code confidentiel est appropriée.
ms.assetid: 511a1594-f3f8-4725-afcd-f14f3a4ebf20
title: Méthode CBasePin. CheckConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24d5c221da417fd1fc2b3f9f140536f825b2f9d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540669"
---
# <a name="cbasepincheckconnect-method"></a><span data-ttu-id="b880b-103">Méthode CBasePin. CheckConnect</span><span class="sxs-lookup"><span data-stu-id="b880b-103">CBasePin.CheckConnect method</span></span>

<span data-ttu-id="b880b-104">La `CheckConnect` méthode détermine si une connexion de code confidentiel est appropriée.</span><span class="sxs-lookup"><span data-stu-id="b880b-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="b880b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b880b-105">Syntax</span></span>


```C++
virtual HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="b880b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b880b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b880b-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="b880b-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="b880b-108">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de l’autre pin.</span><span class="sxs-lookup"><span data-stu-id="b880b-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b880b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b880b-109">Return value</span></span>

<span data-ttu-id="b880b-110">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b880b-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="b880b-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b880b-111">Return code</span></span>                                                                                               | <span data-ttu-id="b880b-112">Description</span><span class="sxs-lookup"><span data-stu-id="b880b-112">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="b880b-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b880b-113"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="b880b-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="b880b-114">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="b880b-115"><dt>**VFW \_ E \_ sens non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b880b-115"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="b880b-116">Les directions de code confidentiel ne sont pas compatibles.</span><span class="sxs-lookup"><span data-stu-id="b880b-116">Pin directions are not compatible.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b880b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b880b-117">Remarks</span></span>

<span data-ttu-id="b880b-118">Cette méthode est appelée sur les deux codes confidentiels au début du processus de connexion.</span><span class="sxs-lookup"><span data-stu-id="b880b-118">This method is called on both pins at the start of the connection process.</span></span> <span data-ttu-id="b880b-119">Le code PIN de connexion l’appelle à partir de la méthode [**CBasePin :: Connect**](cbasepin-connect.md) , et l’épingle de réception l’appelle à partir de la méthode [**CBasePin :: ReceiveConnection**](cbasepin-receiveconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="b880b-119">The connecting pin calls it from within the [**CBasePin::Connect**](cbasepin-connect.md) method, and the receiving pin calls it from within the [**CBasePin::ReceiveConnection**](cbasepin-receiveconnection.md) method.</span></span>

<span data-ttu-id="b880b-120">Utilisez cette méthode pour déterminer si le code confidentiel spécifié par le paramètre *pPin* convient pour une connexion.</span><span class="sxs-lookup"><span data-stu-id="b880b-120">Use this method to determine whether the pin specified by the *pPin* parameter is suitable for a connection.</span></span> <span data-ttu-id="b880b-121">La classe de base retourne une erreur si les deux broches ont la même direction (à la fois l’entrée ou les deux).</span><span class="sxs-lookup"><span data-stu-id="b880b-121">The base class returns an error if both pins have the same direction (both input, or both output).</span></span> <span data-ttu-id="b880b-122">Les classes dérivées peuvent substituer cette méthode pour vérifier d’autres fonctionnalités dans le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="b880b-122">Derived classes can override this method to verify other features in the pin.</span></span> <span data-ttu-id="b880b-123">Par exemple, la classe [**CBaseOutputPin**](cbaseoutputpin.md) interroge la broche d’entrée pour son interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="b880b-123">For example, the [**CBaseOutputPin**](cbaseoutputpin.md) class queries the input pin for its [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

<span data-ttu-id="b880b-124">Si cette méthode échoue, la connexion échoue et le code PIN appelle la méthode [**CBasePin :: BreakConnect**](cbasepin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="b880b-124">If this method fails, the connection fails and the pin calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="b880b-125">Utilisez **BreakConnect** pour libérer toutes les ressources obtenues dans `CheckConnect` .</span><span class="sxs-lookup"><span data-stu-id="b880b-125">Use **BreakConnect** to free any resources obtained in `CheckConnect`.</span></span> <span data-ttu-id="b880b-126">Par exemple, si `CheckConnect` appelle la méthode **QueryInterface** , **BreakConnect** doit libérer l’interface.</span><span class="sxs-lookup"><span data-stu-id="b880b-126">For example, if `CheckConnect` calls the **QueryInterface** method, **BreakConnect** must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="b880b-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b880b-127">Requirements</span></span>



| <span data-ttu-id="b880b-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b880b-128">Requirement</span></span> | <span data-ttu-id="b880b-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="b880b-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b880b-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="b880b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="b880b-131"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b880b-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b880b-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b880b-132">Library</span></span><br/> | <dl> <span data-ttu-id="b880b-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b880b-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b880b-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b880b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b880b-135">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="b880b-135">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




