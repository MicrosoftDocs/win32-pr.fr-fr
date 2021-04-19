---
description: Détermine si le code confidentiel peut accepter des exemples.
ms.assetid: bc66ab4c-99de-4031-bdac-b1430f736e20
title: Méthode CBaseInputPin. CheckStreaming (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba07d28ac93f7dc511390a851d3c737a833ef3f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540976"
---
# <a name="cbaseinputpincheckstreaming-method"></a><span data-ttu-id="2880a-103">Méthode CBaseInputPin. CheckStreaming</span><span class="sxs-lookup"><span data-stu-id="2880a-103">CBaseInputPin.CheckStreaming method</span></span>

<span data-ttu-id="2880a-104">Détermine si le code confidentiel peut accepter des exemples.</span><span class="sxs-lookup"><span data-stu-id="2880a-104">Determines whether the pin can accept samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="2880a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2880a-105">Syntax</span></span>


```C++
virtual HRESULT CheckStreaming();
```



## <a name="parameters"></a><span data-ttu-id="2880a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2880a-106">Parameters</span></span>

<span data-ttu-id="2880a-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2880a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2880a-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2880a-108">Return value</span></span>

<span data-ttu-id="2880a-109">Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2880a-109">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="2880a-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2880a-110">Return code</span></span>                                                                                           | <span data-ttu-id="2880a-111">Description</span><span class="sxs-lookup"><span data-stu-id="2880a-111">Description</span></span>                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="2880a-112"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2880a-112"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="2880a-113">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="2880a-113">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="2880a-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="2880a-114"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="2880a-115">Le code PIN est en cours de vidage.</span><span class="sxs-lookup"><span data-stu-id="2880a-115">Pin is currently flushing.</span></span><br/> |
| <dl> <span data-ttu-id="2880a-116"><dt>**\_erreur d' \_ exécution VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2880a-116"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="2880a-117">Une erreur d’exécution s’est produite.</span><span class="sxs-lookup"><span data-stu-id="2880a-117">A run-time error occurred.</span></span><br/> |
| <dl> <span data-ttu-id="2880a-118"><dt>**VFW \_ E \_ état incorrect \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2880a-118"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="2880a-119">Le code PIN est arrêté.</span><span class="sxs-lookup"><span data-stu-id="2880a-119">The pin is stopped.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="2880a-120">Notes</span><span class="sxs-lookup"><span data-stu-id="2880a-120">Remarks</span></span>

<span data-ttu-id="2880a-121">La classe dérivée peut substituer cette méthode pour effectuer des vérifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="2880a-121">The derived class can override this method to perform further checks.</span></span> <span data-ttu-id="2880a-122">Dans la méthode de substitution, appelez également l’implémentation de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="2880a-122">In the overriding method, also call the base class implementation.</span></span>

<span data-ttu-id="2880a-123">La méthode [**CBaseInputPin :: Receive**](cbaseinputpin-receive.md) appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="2880a-123">The [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method calls this method.</span></span> <span data-ttu-id="2880a-124">Vous devez substituer la méthode [**CBasePin :: EndOfStream**](cbasepin-endofstream.md) pour appeler également cette méthode.</span><span class="sxs-lookup"><span data-stu-id="2880a-124">You should override the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method to call this method as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="2880a-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2880a-125">Requirements</span></span>



| <span data-ttu-id="2880a-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2880a-126">Requirement</span></span> | <span data-ttu-id="2880a-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="2880a-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2880a-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="2880a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="2880a-129"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2880a-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2880a-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2880a-130">Library</span></span><br/> | <dl> <span data-ttu-id="2880a-131"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2880a-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2880a-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2880a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2880a-133">**CBaseInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="2880a-133">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




