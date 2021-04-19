---
description: La méthode DynamicReconnect effectue une reconnexion dynamique avec un nouveau type de média. La reconnexion peut se produire pendant l’exécution du graphique de filtre.
ms.assetid: 1fe9f1cc-1f5d-407e-8c80-fea6cd1cb16f
title: Méthode CDynamicOutputPin. DynamicReconnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DynamicReconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd595748380a35f74e591283ed3d03273c683e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538751"
---
# <a name="cdynamicoutputpindynamicreconnect-method"></a><span data-ttu-id="e4ecc-104">Méthode CDynamicOutputPin. DynamicReconnect</span><span class="sxs-lookup"><span data-stu-id="e4ecc-104">CDynamicOutputPin.DynamicReconnect method</span></span>

<span data-ttu-id="e4ecc-105">La `DynamicReconnect` méthode effectue une reconnexion dynamique avec un nouveau type de média.</span><span class="sxs-lookup"><span data-stu-id="e4ecc-105">The `DynamicReconnect` method performs a dynamic reconnection with a new media type.</span></span> <span data-ttu-id="e4ecc-106">La reconnexion peut se produire pendant l’exécution du graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="e4ecc-106">The reconnection can occur while the filter graph is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4ecc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4ecc-107">Syntax</span></span>


```C++
HRESULT DynamicReconnect(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="e4ecc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4ecc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4ecc-109">*crédit*</span><span class="sxs-lookup"><span data-stu-id="e4ecc-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="e4ecc-110">Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui spécifie le type de média.</span><span class="sxs-lookup"><span data-stu-id="e4ecc-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4ecc-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e4ecc-111">Return value</span></span>

<span data-ttu-id="e4ecc-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e4ecc-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e4ecc-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e4ecc-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="e4ecc-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e4ecc-114">Return code</span></span>                                                                            | <span data-ttu-id="e4ecc-115">Description</span><span class="sxs-lookup"><span data-stu-id="e4ecc-115">Description</span></span>                                                                                                                                         |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e4ecc-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e4ecc-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="e4ecc-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="e4ecc-117">Success.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="e4ecc-118"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="e4ecc-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="e4ecc-119">Échec.</span><span class="sxs-lookup"><span data-stu-id="e4ecc-119">Failure.</span></span> <span data-ttu-id="e4ecc-120">Le filtre propriétaire n’a peut-être pas appelé la méthode [**CDynamicOutputPin :: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) .</span><span class="sxs-lookup"><span data-stu-id="e4ecc-120">Possibly the owning filter did not call the [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e4ecc-121">Notes</span><span class="sxs-lookup"><span data-stu-id="e4ecc-121">Remarks</span></span>

<span data-ttu-id="e4ecc-122">Cette méthode doit être appelée à partir du thread qui remet les données au code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="e4ecc-122">This method must be called from the same thread that delivers data to the pin.</span></span> <span data-ttu-id="e4ecc-123">Une fois cette méthode appelée, les exemples avec l’ancien type de média ne peuvent pas être remis.</span><span class="sxs-lookup"><span data-stu-id="e4ecc-123">Once this method is called, samples with the old media type cannot be delivered.</span></span> <span data-ttu-id="e4ecc-124">L’appelant doit s’assurer qu’aucun ancien échantillon n’est en attente.</span><span class="sxs-lookup"><span data-stu-id="e4ecc-124">The caller must ensure that no old samples are pending.</span></span>

<span data-ttu-id="e4ecc-125">Appelez [**CDynamicOutputPin :: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="e4ecc-125">Call [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4ecc-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4ecc-126">Requirements</span></span>



| <span data-ttu-id="e4ecc-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4ecc-127">Requirement</span></span> | <span data-ttu-id="e4ecc-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4ecc-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4ecc-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4ecc-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e4ecc-130"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4ecc-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e4ecc-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e4ecc-131">Library</span></span><br/> | <dl> <span data-ttu-id="e4ecc-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e4ecc-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4ecc-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4ecc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4ecc-134">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="e4ecc-134">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




