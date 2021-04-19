---
description: 'La méthode QueryInternalConnections récupère les broches qui sont connectées en interne à ce code confidentiel (dans le filtre). Cette méthode implémente la méthode IPin :: QueryInternalConnections.'
ms.assetid: 08344fc5-38b2-4dbe-8ef9-30d2fcd64187
title: Méthode CBasePin. QueryInternalConnections (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryInternalConnections
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99a636295fc87347a1735ab028b6de342e887d55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530527"
---
# <a name="cbasepinqueryinternalconnections-method"></a><span data-ttu-id="63e1b-104">Méthode CBasePin. QueryInternalConnections</span><span class="sxs-lookup"><span data-stu-id="63e1b-104">CBasePin.QueryInternalConnections method</span></span>

<span data-ttu-id="63e1b-105">La `QueryInternalConnections` méthode récupère les broches qui sont connectées en interne à ce code confidentiel (dans le filtre).</span><span class="sxs-lookup"><span data-stu-id="63e1b-105">The `QueryInternalConnections` method retrieves the pins that are connected internally to this pin (within the filter).</span></span> <span data-ttu-id="63e1b-106">Cette méthode implémente la méthode [**IPIN :: QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) .</span><span class="sxs-lookup"><span data-stu-id="63e1b-106">This method implements the [**IPin::QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="63e1b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63e1b-107">Syntax</span></span>


```C++
HRESULT QueryInternalConnections(
   IPin  *apPin,
   ULONG *nPin
);
```



## <a name="parameters"></a><span data-ttu-id="63e1b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63e1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63e1b-109">*apPin*</span><span class="sxs-lookup"><span data-stu-id="63e1b-109">*apPin*</span></span> 
</dt> <dd>

<span data-ttu-id="63e1b-110">Adresse d’un tableau de pointeurs [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="63e1b-110">Address of an array of [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) pointers.</span></span>

</dd> <dt>

<span data-ttu-id="63e1b-111">*nPin*</span><span class="sxs-lookup"><span data-stu-id="63e1b-111">*nPin*</span></span> 
</dt> <dd>

<span data-ttu-id="63e1b-112">En entrée, spécifie la taille du tableau.</span><span class="sxs-lookup"><span data-stu-id="63e1b-112">On input, specifies the size of the array.</span></span> <span data-ttu-id="63e1b-113">Lorsque la méthode retourne, la valeur est définie sur le nombre de pointeurs retournés dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="63e1b-113">When the method returns, the value is set to the number of pointers returned in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63e1b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="63e1b-114">Return value</span></span>

<span data-ttu-id="63e1b-115">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="63e1b-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="63e1b-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="63e1b-116">Return code</span></span>                                                                               | <span data-ttu-id="63e1b-117">Description</span><span class="sxs-lookup"><span data-stu-id="63e1b-117">Description</span></span>                         |
|-------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="63e1b-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="63e1b-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="63e1b-119">Taille de tableau insuffisante.</span><span class="sxs-lookup"><span data-stu-id="63e1b-119">Insufficient array size.</span></span><br/> |
| <dl> <span data-ttu-id="63e1b-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="63e1b-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="63e1b-121">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="63e1b-121">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="63e1b-122"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="63e1b-122"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="63e1b-123">Échec.</span><span class="sxs-lookup"><span data-stu-id="63e1b-123">Failure.</span></span><br/>                 |
| <dl> <span data-ttu-id="63e1b-124"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="63e1b-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="63e1b-125">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="63e1b-125">Not implemented.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="63e1b-126">Notes</span><span class="sxs-lookup"><span data-stu-id="63e1b-126">Remarks</span></span>

<span data-ttu-id="63e1b-127">Sur certains filtres, les broches d’entrée correspondent à des broches de sortie particulières.</span><span class="sxs-lookup"><span data-stu-id="63e1b-127">On some filters, input pins correspond to particular output pins.</span></span> <span data-ttu-id="63e1b-128">Pour chaque code confidentiel, cette méthode remplit un tableau avec des pointeurs vers les broches correspondantes.</span><span class="sxs-lookup"><span data-stu-id="63e1b-128">For each pin, this method fills an array with pointers to the corresponding pins.</span></span> <span data-ttu-id="63e1b-129">Si chaque broche d’entrée fournit des données pour chaque broche de sortie, retournez E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="63e1b-129">If every input pin provides data for every output pin, return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="63e1b-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63e1b-130">Requirements</span></span>



| <span data-ttu-id="63e1b-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63e1b-131">Requirement</span></span> | <span data-ttu-id="63e1b-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="63e1b-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63e1b-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="63e1b-133">Header</span></span><br/>  | <dl> <span data-ttu-id="63e1b-134"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63e1b-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="63e1b-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="63e1b-135">Library</span></span><br/> | <dl> <span data-ttu-id="63e1b-136"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="63e1b-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63e1b-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63e1b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63e1b-138">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="63e1b-138">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




