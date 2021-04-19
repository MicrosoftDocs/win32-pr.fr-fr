---
description: 'La méthode ReceiveConnection accepte une connexion à partir d’un autre code PIN. Cette méthode implémente la méthode IPin :: ReceiveConnection.'
ms.assetid: f17e7d93-ac45-4b8a-98c6-0c76ec7117c9
title: Méthode CBasePin. ReceiveConnection (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ReceiveConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d0a8134201af1d3c931121f59a20360020a53a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537992"
---
# <a name="cbasepinreceiveconnection-method"></a><span data-ttu-id="e6757-104">Méthode CBasePin. ReceiveConnection</span><span class="sxs-lookup"><span data-stu-id="e6757-104">CBasePin.ReceiveConnection method</span></span>

<span data-ttu-id="e6757-105">La `ReceiveConnection` méthode accepte une connexion à partir d’un autre code PIN.</span><span class="sxs-lookup"><span data-stu-id="e6757-105">The `ReceiveConnection` method accepts a connection from another pin.</span></span> <span data-ttu-id="e6757-106">Cette méthode implémente la méthode [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) .</span><span class="sxs-lookup"><span data-stu-id="e6757-106">This method implements the [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6757-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6757-107">Syntax</span></span>


```C++
HRESULT ReceiveConnection(
   IPin          *pConnector,
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="e6757-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6757-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6757-109">*pConnector*</span><span class="sxs-lookup"><span data-stu-id="e6757-109">*pConnector*</span></span> 
</dt> <dd>

<span data-ttu-id="e6757-110">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du code PIN de connexion.</span><span class="sxs-lookup"><span data-stu-id="e6757-110">Pointer to the connecting pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e6757-111">*crédit*</span><span class="sxs-lookup"><span data-stu-id="e6757-111">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="e6757-112">Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui spécifie le type de média.</span><span class="sxs-lookup"><span data-stu-id="e6757-112">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6757-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6757-113">Return value</span></span>

<span data-ttu-id="e6757-114">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6757-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e6757-115">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e6757-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="e6757-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e6757-116">Return code</span></span>                                                                                                | <span data-ttu-id="e6757-117">Description</span><span class="sxs-lookup"><span data-stu-id="e6757-117">Description</span></span>                                                                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e6757-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e6757-118"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="e6757-119">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="e6757-119">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="e6757-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="e6757-120"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="e6757-121">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="e6757-121">**NULL** pointer argument.</span></span><br/>                                              |
| <dl> <span data-ttu-id="e6757-122"><dt>**VFW \_ E \_ déjà \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="e6757-122"><dt>**VFW\_E\_ALREADY\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="e6757-123">Le pin est déjà connecté.</span><span class="sxs-lookup"><span data-stu-id="e6757-123">The pin is already connected.</span></span><br/>                                           |
| <dl> <span data-ttu-id="e6757-124"><dt>**VFW \_ E \_ non \_ arrêté**</dt></span><span class="sxs-lookup"><span data-stu-id="e6757-124"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl>        | <span data-ttu-id="e6757-125">Le filtre est actif et le code confidentiel ne prend pas en charge la reconnexion dynamique.</span><span class="sxs-lookup"><span data-stu-id="e6757-125">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |
| <dl> <span data-ttu-id="e6757-126"><dt>**TYPE de VFW \_ E \_ \_ non \_ accepté**</dt></span><span class="sxs-lookup"><span data-stu-id="e6757-126"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="e6757-127">Le type de média spécifié n’est pas acceptable.</span><span class="sxs-lookup"><span data-stu-id="e6757-127">The specified media type is not acceptable.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="e6757-128">Notes</span><span class="sxs-lookup"><span data-stu-id="e6757-128">Remarks</span></span>

<span data-ttu-id="e6757-129">La broche de sortie appelle cette méthode sur la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e6757-129">The output pin calls this method on the input pin.</span></span> <span data-ttu-id="e6757-130">Si la broche d’entrée retourne un code d’erreur, la connexion échoue.</span><span class="sxs-lookup"><span data-stu-id="e6757-130">If the input pin returns an error code, the connection fails.</span></span>

<span data-ttu-id="e6757-131">Dans la classe de base, cette méthode effectue les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e6757-131">In the base class, this method performs the following steps:</span></span>

-   <span data-ttu-id="e6757-132">Vérifie si le code PIN est déjà connecté.</span><span class="sxs-lookup"><span data-stu-id="e6757-132">Checks whether the pin is already connected.</span></span>
-   <span data-ttu-id="e6757-133">Vérifie si le filtre est arrêté.</span><span class="sxs-lookup"><span data-stu-id="e6757-133">Checks whether the filter is stopped.</span></span>
-   <span data-ttu-id="e6757-134">Appelle la méthode [**CBasePin :: CheckConnect**](cbasepin-checkconnect.md) pour tester si le code confidentiel de connexion est approprié.</span><span class="sxs-lookup"><span data-stu-id="e6757-134">Calls the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method to test whether the connecting pin is suitable.</span></span>
-   <span data-ttu-id="e6757-135">Appelle la méthode [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) pour tester si le type de média est acceptable.</span><span class="sxs-lookup"><span data-stu-id="e6757-135">Calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to test whether the media type is acceptable.</span></span>

<span data-ttu-id="e6757-136">Si toutes ces étapes réussissent, la méthode appelle les méthodes [**CBasePin :: CompleteConnect**](cbasepin-completeconnect.md) et [**SetMediaType**](cbasepin-setmediatype.md) pour terminer la connexion.</span><span class="sxs-lookup"><span data-stu-id="e6757-136">If all of these steps succeed, the method calls the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) and [**SetMediaType**](cbasepin-setmediatype.md) methods to complete the connection.</span></span> <span data-ttu-id="e6757-137">Ces méthodes stockent le type de média et un pointeur vers la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="e6757-137">These methods store the media type and a pointer to the output pin.</span></span>

<span data-ttu-id="e6757-138">Si **CheckConnect** ou **CheckMediaType** échouent, la classe de base appelle la méthode [**CBasePin :: BreakConnect**](cbasepin-breakconnect.md) pour rompre la connexion, puis retourne un code d’erreur à partir de `ReceiveConnection` .</span><span class="sxs-lookup"><span data-stu-id="e6757-138">If **CheckConnect** or **CheckMediaType** fail, the base class calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method to break the connection and then returns an error code from `ReceiveConnection`.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6757-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6757-139">Requirements</span></span>



| <span data-ttu-id="e6757-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6757-140">Requirement</span></span> | <span data-ttu-id="e6757-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6757-141">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6757-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6757-142">Header</span></span><br/>  | <dl> <span data-ttu-id="e6757-143"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6757-143"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e6757-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e6757-144">Library</span></span><br/> | <dl> <span data-ttu-id="e6757-145"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e6757-145"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6757-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6757-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6757-147">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="e6757-147">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




