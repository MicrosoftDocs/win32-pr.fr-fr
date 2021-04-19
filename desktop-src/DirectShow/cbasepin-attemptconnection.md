---
description: La méthode AttemptConnection se connecte à un autre code confidentiel à l’aide d’un type de média spécifié.
ms.assetid: b80cf2c0-7266-4dac-8633-d30a871c57d9
title: Méthode CBasePin. AttemptConnection (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AttemptConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72f80d81b5f105f528292a23f8b58257066b425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534887"
---
# <a name="cbasepinattemptconnection-method"></a><span data-ttu-id="2296a-103">Méthode CBasePin. AttemptConnection</span><span class="sxs-lookup"><span data-stu-id="2296a-103">CBasePin.AttemptConnection method</span></span>

<span data-ttu-id="2296a-104">La `AttemptConnection` méthode se connecte à un autre code confidentiel à l’aide d’un type de média spécifié.</span><span class="sxs-lookup"><span data-stu-id="2296a-104">The `AttemptConnection` method connects to another pin using a specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="2296a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2296a-105">Syntax</span></span>


```C++
virtual HRESULT AttemptConnection(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="2296a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2296a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2296a-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="2296a-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="2296a-108">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du pin de réception.</span><span class="sxs-lookup"><span data-stu-id="2296a-108">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="2296a-109">*crédit*</span><span class="sxs-lookup"><span data-stu-id="2296a-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="2296a-110">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type de média.</span><span class="sxs-lookup"><span data-stu-id="2296a-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2296a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2296a-111">Return value</span></span>

<span data-ttu-id="2296a-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2296a-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2296a-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2296a-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="2296a-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2296a-114">Return code</span></span>                                                                                                | <span data-ttu-id="2296a-115">Description</span><span class="sxs-lookup"><span data-stu-id="2296a-115">Description</span></span>                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="2296a-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2296a-116"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="2296a-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="2296a-117">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="2296a-118"><dt>**TYPE de VFW \_ E \_ \_ non \_ accepté**</dt></span><span class="sxs-lookup"><span data-stu-id="2296a-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="2296a-119">Le type de média n’est pas acceptable.</span><span class="sxs-lookup"><span data-stu-id="2296a-119">The media type is not acceptable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2296a-120">Notes</span><span class="sxs-lookup"><span data-stu-id="2296a-120">Remarks</span></span>

<span data-ttu-id="2296a-121">Cette méthode tente de connecter les deux broches avec un type de média spécifique.</span><span class="sxs-lookup"><span data-stu-id="2296a-121">This method attempts to connect the two pins with a specific media type.</span></span> <span data-ttu-id="2296a-122">Si le type n’est pas acceptable, la méthode échoue sans essayer d’autres types de média.</span><span class="sxs-lookup"><span data-stu-id="2296a-122">If the type is not acceptable, the method fails without trying other media types.</span></span>

<span data-ttu-id="2296a-123">Si le type de média est acceptable, cette méthode appelle la méthode [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) du pin de réception.</span><span class="sxs-lookup"><span data-stu-id="2296a-123">If the media type is acceptable, this method calls the receiving pin's [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span> <span data-ttu-id="2296a-124">Elle appelle ensuite la méthode [**CBasePin :: CompleteConnect**](cbasepin-completeconnect.md) pour terminer la connexion.</span><span class="sxs-lookup"><span data-stu-id="2296a-124">Then it calls the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method to complete the connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="2296a-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2296a-125">Requirements</span></span>



| <span data-ttu-id="2296a-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2296a-126">Requirement</span></span> | <span data-ttu-id="2296a-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="2296a-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2296a-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="2296a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="2296a-129"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2296a-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2296a-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2296a-130">Library</span></span><br/> | <dl> <span data-ttu-id="2296a-131"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2296a-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2296a-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2296a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2296a-133">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="2296a-133">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




