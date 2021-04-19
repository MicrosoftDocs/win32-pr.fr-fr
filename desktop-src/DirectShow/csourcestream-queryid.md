---
description: La méthode QueryId récupère un identificateur pour le code confidentiel.
ms.assetid: 6050292e-6203-4a79-87bf-47394624cb32
title: Méthode CSourceStream. QueryId (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 267748fe4ce1eeec4650544a2f72069df897a366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543861"
---
# <a name="csourcestreamqueryid-method"></a><span data-ttu-id="db97f-103">CSourceStream. QueryId, méthode</span><span class="sxs-lookup"><span data-stu-id="db97f-103">CSourceStream.QueryId method</span></span>

<span data-ttu-id="db97f-104">La `QueryId` méthode récupère un identificateur pour le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="db97f-104">The `QueryId` method retrieves an identifier for the pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="db97f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db97f-105">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="db97f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db97f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db97f-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="db97f-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="db97f-108">Pointeur vers une variable qui reçoit une chaîne contenant l’identificateur de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="db97f-108">Pointer to a variable that receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db97f-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="db97f-109">Return value</span></span>

<span data-ttu-id="db97f-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="db97f-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="db97f-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="db97f-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="db97f-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="db97f-112">Return code</span></span>                                                                                       | <span data-ttu-id="db97f-113">Description</span><span class="sxs-lookup"><span data-stu-id="db97f-113">Description</span></span>                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="db97f-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="db97f-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="db97f-115">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="db97f-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="db97f-116"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="db97f-116"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="db97f-117">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="db97f-117">Insufficient memory.</span></span><br/>             |
| <dl> <span data-ttu-id="db97f-118"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="db97f-118"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="db97f-119">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="db97f-119">**NULL** pointer argument.</span></span><br/>       |
| <dl> <span data-ttu-id="db97f-120"><dt>**VFW \_ E \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="db97f-120"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="db97f-121">Le code PIN est introuvable dans le filtre.</span><span class="sxs-lookup"><span data-stu-id="db97f-121">Pin was not found on the filter.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="db97f-122">Notes</span><span class="sxs-lookup"><span data-stu-id="db97f-122">Remarks</span></span>

<span data-ttu-id="db97f-123">Cette méthode implémente la méthode [**IPIN :: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .</span><span class="sxs-lookup"><span data-stu-id="db97f-123">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span> <span data-ttu-id="db97f-124">Pour construire une chaîne d’identification, le code PIN appelle la méthode [**CSource :: FindPinNumber**](csource-findpinnumber.md) avec lui-même comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="db97f-124">To construct an identifier string, the pin calls the [**CSource::FindPinNumber**](csource-findpinnumber.md) method with itself as the parameter.</span></span> <span data-ttu-id="db97f-125">La méthode **FindPinNumber** retourne le numéro de code confidentiel, indexé à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="db97f-125">The **FindPinNumber** method returns the pin number, indexed from zero.</span></span> <span data-ttu-id="db97f-126">`QueryId` incrémente la valeur de retour d’une unité et convertit le résultat en une chaîne.</span><span class="sxs-lookup"><span data-stu-id="db97f-126">`QueryId` increments the return value by one and converts the result to a string.</span></span> <span data-ttu-id="db97f-127">Par exemple, la première broche devient « 1 ». la deuxième broche devient « 2 ». et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="db97f-127">For example, the first pin becomes "1"; the second pin becomes "2"; and so forth.</span></span>

<span data-ttu-id="db97f-128">Si cette méthode retourne VFW \_ E \_ \_ introuvable, cela indique que le tableau de codes confidentiels du filtre n’est pas valide, vraisemblablement dû à un bogue dans le filtre.</span><span class="sxs-lookup"><span data-stu-id="db97f-128">If this method returns VFW\_E\_NOT\_FOUND, it indicates that the filter's array of pins is invalid, presumably caused by a bug in the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="db97f-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db97f-129">Requirements</span></span>



| <span data-ttu-id="db97f-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db97f-130">Requirement</span></span> | <span data-ttu-id="db97f-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="db97f-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db97f-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="db97f-132">Header</span></span><br/>  | <dl> <span data-ttu-id="db97f-133"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db97f-133"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="db97f-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="db97f-134">Library</span></span><br/> | <dl> <span data-ttu-id="db97f-135"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="db97f-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db97f-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db97f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db97f-137">**CSourceStream, classe**</span><span class="sxs-lookup"><span data-stu-id="db97f-137">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




