---
description: 'La méthode QueryId récupère l’identificateur de code confidentiel. Cette méthode remplace la méthode CBasePin :: QueryId.'
ms.assetid: 9543234c-5349-49d0-b410-1c461ee4eabe
title: CRendererInputPin. QueryId, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b56ae2a846b4d89da4c6a9d4c8f88bd3094c5cff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533473"
---
# <a name="crendererinputpinqueryid-method"></a><span data-ttu-id="646ab-104">CRendererInputPin. QueryId, méthode</span><span class="sxs-lookup"><span data-stu-id="646ab-104">CRendererInputPin.QueryId method</span></span>

<span data-ttu-id="646ab-105">La `QueryId` méthode récupère l’identificateur de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="646ab-105">The `QueryId` method retrieves the pin identifier.</span></span> <span data-ttu-id="646ab-106">Cette méthode remplace la méthode [**CBasePin :: QueryId**](cbasepin-queryid.md) .</span><span class="sxs-lookup"><span data-stu-id="646ab-106">This method overrides the [**CBasePin::QueryId**](cbasepin-queryid.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="646ab-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="646ab-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="646ab-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="646ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="646ab-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="646ab-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="646ab-110">Reçoit une chaîne contenant l’identificateur de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="646ab-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="646ab-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="646ab-111">Return value</span></span>

<span data-ttu-id="646ab-112">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="646ab-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="646ab-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="646ab-113">Return code</span></span>                                                                                   | <span data-ttu-id="646ab-114">Description</span><span class="sxs-lookup"><span data-stu-id="646ab-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="646ab-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="646ab-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="646ab-116">Succès</span><span class="sxs-lookup"><span data-stu-id="646ab-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="646ab-117"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="646ab-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="646ab-118">Mémoire insuffisante</span><span class="sxs-lookup"><span data-stu-id="646ab-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="646ab-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="646ab-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="646ab-120">Argument de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="646ab-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="646ab-121">Notes</span><span class="sxs-lookup"><span data-stu-id="646ab-121">Remarks</span></span>

<span data-ttu-id="646ab-122">Cette méthode alloue la chaîne de caractères larges « in » et l’assigne au paramètre *ID* .</span><span class="sxs-lookup"><span data-stu-id="646ab-122">This method allocates the wide-character string "In" and assigns it to the *Id* parameter.</span></span> <span data-ttu-id="646ab-123">L’appelant doit libérer la mémoire allouée à l’aide de la fonction **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="646ab-123">The caller must free the allocated memory, using the **CoTaskMemFree** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="646ab-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="646ab-124">Requirements</span></span>



| <span data-ttu-id="646ab-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="646ab-125">Requirement</span></span> | <span data-ttu-id="646ab-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="646ab-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="646ab-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="646ab-127">Header</span></span><br/>  | <dl> <span data-ttu-id="646ab-128"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="646ab-128"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="646ab-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="646ab-129">Library</span></span><br/> | <dl> <span data-ttu-id="646ab-130"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="646ab-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="646ab-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="646ab-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="646ab-132">**CRendererInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="646ab-132">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




