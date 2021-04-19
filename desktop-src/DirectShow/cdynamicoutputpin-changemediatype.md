---
description: La méthode ChangeMediaType modifie dynamiquement le type de média pour la connexion.
ms.assetid: 38efdfdc-f636-4cad-b8d3-8c63a277644e
title: Méthode CDynamicOutputPin. ChangeMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89c15e3076a95f8fee3f2f2970fc59da5cf3bf4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537697"
---
# <a name="cdynamicoutputpinchangemediatype-method"></a><span data-ttu-id="8809b-103">Méthode CDynamicOutputPin. ChangeMediaType</span><span class="sxs-lookup"><span data-stu-id="8809b-103">CDynamicOutputPin.ChangeMediaType method</span></span>

<span data-ttu-id="8809b-104">La `ChangeMediaType` méthode modifie dynamiquement le type de média pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="8809b-104">The `ChangeMediaType` method dynamically changes the media type for the connection.</span></span> <span data-ttu-id="8809b-105">La modification peut se produire pendant l’exécution du graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="8809b-105">The change can occur while the filter graph is running.</span></span> <span data-ttu-id="8809b-106">Une fois cette méthode appelée, les exemples avec l’ancien type de média ne peuvent pas être remis.</span><span class="sxs-lookup"><span data-stu-id="8809b-106">Once this method is called, samples with the old media type cannot be delivered.</span></span> <span data-ttu-id="8809b-107">L’appelant doit s’assurer qu’aucun ancien échantillon n’est en attente.</span><span class="sxs-lookup"><span data-stu-id="8809b-107">The caller must ensure that no old samples are pending.</span></span>

## <a name="syntax"></a><span data-ttu-id="8809b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8809b-108">Syntax</span></span>


```C++
HRESULT ChangeMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="8809b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8809b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8809b-110">*crédit*</span><span class="sxs-lookup"><span data-stu-id="8809b-110">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="8809b-111">Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui spécifie le type de média.</span><span class="sxs-lookup"><span data-stu-id="8809b-111">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8809b-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8809b-112">Return value</span></span>

<span data-ttu-id="8809b-113">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8809b-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="8809b-114">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8809b-114">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="8809b-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8809b-115">Return code</span></span>                                                                                           | <span data-ttu-id="8809b-116">Description</span><span class="sxs-lookup"><span data-stu-id="8809b-116">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8809b-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8809b-117"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="8809b-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="8809b-118">Success.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="8809b-119"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="8809b-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="8809b-120">Échec.</span><span class="sxs-lookup"><span data-stu-id="8809b-120">Failure.</span></span> <span data-ttu-id="8809b-121">Le filtre propriétaire n’a peut-être pas appelé [**CDynamicOutputPin :: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span><span class="sxs-lookup"><span data-stu-id="8809b-121">Possibly the owning filter did not call [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span></span><br/> |
| <dl> <span data-ttu-id="8809b-122"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="8809b-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="8809b-123">Le pin n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="8809b-123">The pin is not connected.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="8809b-124">Notes</span><span class="sxs-lookup"><span data-stu-id="8809b-124">Remarks</span></span>

<span data-ttu-id="8809b-125">Appelez la méthode [**CDynamicOutputPin :: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="8809b-125">Call the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method before calling this method.</span></span>

<span data-ttu-id="8809b-126">Cette méthode vérifie d’abord si la broche d’entrée en aval peut accepter le nouveau format sans se reconnecter.</span><span class="sxs-lookup"><span data-stu-id="8809b-126">This method first checks whether the downstream input pin can accept the new format without reconnecting.</span></span> <span data-ttu-id="8809b-127">Il interroge la broche d’entrée de l’interface [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) .</span><span class="sxs-lookup"><span data-stu-id="8809b-127">It queries the input pin for the [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) interface.</span></span> <span data-ttu-id="8809b-128">Si la broche d’entrée prend en charge **IPinConnection**, la méthode appelle la méthode [**IPinConnection ::D ynamicqueryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) avec le type de média proposé.</span><span class="sxs-lookup"><span data-stu-id="8809b-128">If the input pin supports **IPinConnection**, the method calls the [**IPinConnection::DynamicQueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) method with the proposed media type.</span></span> <span data-ttu-id="8809b-129">Si la broche d’entrée accepte le nouveau type de média, la méthode appelle la méthode [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) et renégocie les spécifications de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="8809b-129">If the input pin accepts the new media type, the method calls the [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method and renegotiates the allocator requirements.</span></span>

<span data-ttu-id="8809b-130">En revanche, si le code pin en aval ne prend pas en charge **IPinConnection**, ou s’il rejette le nouveau type de média, la méthode appelle la méthode [**CDynamicOutputPin ::D ynamicreconnect**](cdynamicoutputpin-dynamicreconnect.md) pour effectuer une reconnexion dynamique.</span><span class="sxs-lookup"><span data-stu-id="8809b-130">On the other hand, if the downstream pin does not support **IPinConnection**, or if it rejects the new media type, the method calls the [**CDynamicOutputPin::DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md) method to perform a dynamic reconnection.</span></span>

## <a name="requirements"></a><span data-ttu-id="8809b-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8809b-131">Requirements</span></span>



| <span data-ttu-id="8809b-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8809b-132">Requirement</span></span> | <span data-ttu-id="8809b-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="8809b-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8809b-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="8809b-134">Header</span></span><br/>  | <dl> <span data-ttu-id="8809b-135"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8809b-135"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8809b-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8809b-136">Library</span></span><br/> | <dl> <span data-ttu-id="8809b-137"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8809b-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8809b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8809b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8809b-139">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="8809b-139">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




