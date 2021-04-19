---
description: 'La méthode Connect connecte le pin à un autre code PIN. Cette méthode implémente la méthode IPin :: Connect.'
ms.assetid: 8ea99d2f-09da-4b15-a3b0-04ceb7888bc1
title: CBasePin. Connect, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed8bcdab7e0909e59e7d9ec00645786f8ce48c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528562"
---
# <a name="cbasepinconnect-method"></a><span data-ttu-id="b475c-104">CBasePin. Connect, méthode</span><span class="sxs-lookup"><span data-stu-id="b475c-104">CBasePin.Connect method</span></span>

<span data-ttu-id="b475c-105">La `Connect` méthode connecte le pin à un autre code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="b475c-105">The `Connect` method connects the pin to another pin.</span></span> <span data-ttu-id="b475c-106">Cette méthode implémente la méthode [**IPIN :: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) .</span><span class="sxs-lookup"><span data-stu-id="b475c-106">This method implements the [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b475c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b475c-107">Syntax</span></span>


```C++
HRESULT Connect(
         IPin          *pReceivePin,
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="b475c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b475c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b475c-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="b475c-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="b475c-110">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du pin de réception.</span><span class="sxs-lookup"><span data-stu-id="b475c-110">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="b475c-111">*crédit*</span><span class="sxs-lookup"><span data-stu-id="b475c-111">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="b475c-112">Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui spécifie le type de média pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="b475c-112">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type for the connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b475c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b475c-113">Return value</span></span>

<span data-ttu-id="b475c-114">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b475c-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b475c-115">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b475c-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="b475c-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b475c-116">Return code</span></span>                                                                                                  | <span data-ttu-id="b475c-117">Description</span><span class="sxs-lookup"><span data-stu-id="b475c-117">Description</span></span>                                                                        |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b475c-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b475c-118"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="b475c-119">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="b475c-119">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="b475c-120"><dt>**VFW \_ E \_ déjà \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="b475c-120"><dt>**VFW\_E\_ALREADY\_CONNECTED**</dt></span></span> </dl>    | <span data-ttu-id="b475c-121">Le pin est déjà connecté.</span><span class="sxs-lookup"><span data-stu-id="b475c-121">The pin is already connected.</span></span><br/>                                           |
| <dl> <span data-ttu-id="b475c-122"><dt>**VFW \_ E \_ aucun \_ \_ type acceptable**</dt></span><span class="sxs-lookup"><span data-stu-id="b475c-122"><dt>**VFW\_E\_NO\_ACCEPTABLE\_TYPES**</dt></span></span> </dl> | <span data-ttu-id="b475c-123">Impossible de trouver un type de média acceptable.</span><span class="sxs-lookup"><span data-stu-id="b475c-123">Could not find an acceptable media type.</span></span><br/>                                |
| <dl> <span data-ttu-id="b475c-124"><dt>**VFW \_ E \_ non \_ arrêté**</dt></span><span class="sxs-lookup"><span data-stu-id="b475c-124"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl>          | <span data-ttu-id="b475c-125">Le filtre est actif et le code confidentiel ne prend pas en charge la reconnexion dynamique.</span><span class="sxs-lookup"><span data-stu-id="b475c-125">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |
| <dl> <span data-ttu-id="b475c-126"><dt>**TYPE de VFW \_ E \_ \_ non \_ accepté**</dt></span><span class="sxs-lookup"><span data-stu-id="b475c-126"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl>   | <span data-ttu-id="b475c-127">Le type de média spécifié n’est pas acceptable.</span><span class="sxs-lookup"><span data-stu-id="b475c-127">The specified media type is not acceptable.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="b475c-128">Notes</span><span class="sxs-lookup"><span data-stu-id="b475c-128">Remarks</span></span>

<span data-ttu-id="b475c-129">Le paramètre *VPM* peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b475c-129">The *pmt* parameter can be **NULL**.</span></span> <span data-ttu-id="b475c-130">Il peut également spécifier un type de média partiel, avec la valeur GUID \_ null pour le type, le sous-type ou le format principal.</span><span class="sxs-lookup"><span data-stu-id="b475c-130">It can also specify a partial media type, with a value of GUID\_NULL for the major type, subtype, or format.</span></span>

<span data-ttu-id="b475c-131">Dans la classe de base, cette méthode teste si le pin est déjà connecté et si le filtre est arrêté.</span><span class="sxs-lookup"><span data-stu-id="b475c-131">In the base class, this method tests whether the pin is already connected and whether the filter is stopped.</span></span> <span data-ttu-id="b475c-132">Elle délègue le reste du processus de connexion à la méthode [**CBasePin :: AgreeMediaType**](cbasepin-agreemediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="b475c-132">It delegates the rest of the connection process to the [**CBasePin::AgreeMediaType**](cbasepin-agreemediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b475c-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b475c-133">Requirements</span></span>



| <span data-ttu-id="b475c-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b475c-134">Requirement</span></span> | <span data-ttu-id="b475c-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="b475c-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b475c-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="b475c-136">Header</span></span><br/>  | <dl> <span data-ttu-id="b475c-137"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b475c-137"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b475c-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b475c-138">Library</span></span><br/> | <dl> <span data-ttu-id="b475c-139"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b475c-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b475c-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b475c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b475c-141">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="b475c-141">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




