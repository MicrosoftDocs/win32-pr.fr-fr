---
description: La méthode GetMediaType récupère un type de média par défaut.
ms.assetid: 85605885-adb5-4f13-91af-48bf74684eca
title: Méthode CSourceStream. GetMediaType (source. h)-paramètre pMediaType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8306da8451d4af7da8ce4f4c7d4d3f6fd367e1ec
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106533296"
---
# <a name="csourcestreamgetmediatype-method-sourceh"></a><span data-ttu-id="89958-103">Méthode CSourceStream. GetMediaType (source. h)</span><span class="sxs-lookup"><span data-stu-id="89958-103">CSourceStream.GetMediaType method (Source.h)</span></span>

<span data-ttu-id="89958-104">La `GetMediaType` méthode récupère un type de média par défaut.</span><span class="sxs-lookup"><span data-stu-id="89958-104">The `GetMediaType` method retrieves a preferred media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="89958-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89958-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="89958-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89958-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89958-107">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="89958-107">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="89958-108">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui reçoit le type de média.</span><span class="sxs-lookup"><span data-stu-id="89958-108">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89958-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="89958-109">Return value</span></span>

<span data-ttu-id="89958-110">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="89958-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="89958-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="89958-111">Return code</span></span>                                                                                            | <span data-ttu-id="89958-112">Description</span><span class="sxs-lookup"><span data-stu-id="89958-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="89958-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="89958-113"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="89958-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="89958-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="89958-115"><dt>**VFW \_ S \_ n’a \_ plus d' \_ éléments**</dt></span><span class="sxs-lookup"><span data-stu-id="89958-115"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="89958-116">Index hors limites.</span><span class="sxs-lookup"><span data-stu-id="89958-116">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="89958-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="89958-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="89958-118">Index inférieur à zéro.</span><span class="sxs-lookup"><span data-stu-id="89958-118">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="89958-119"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="89958-119"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="89958-120">Erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="89958-120">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="89958-121">Notes</span><span class="sxs-lookup"><span data-stu-id="89958-121">Remarks</span></span>

<span data-ttu-id="89958-122">Il existe deux versions de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="89958-122">There are two versions of this method.</span></span> <span data-ttu-id="89958-123">Une version remplace la méthode [**CBasePin :: GetMediaType**](cbasepin-getmediatype.md) et prend une valeur d’index en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="89958-123">One version overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method and takes an index value as a parameter.</span></span> <span data-ttu-id="89958-124">L’autre version est conçue pour récupérer un type de média unique, de sorte qu’il n’y ait pas de paramètre d’index.</span><span class="sxs-lookup"><span data-stu-id="89958-124">The other version is designed to retrieve a single media type, so it lacks the index parameter.</span></span>

<span data-ttu-id="89958-125">La méthode à paramètre unique retourne E \_ inattendue.</span><span class="sxs-lookup"><span data-stu-id="89958-125">The single-parameter method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="89958-126">La méthode à deux paramètres vérifie que le paramètre *iPosition* est égal à zéro, puis appelle la version à un seul paramètre.</span><span class="sxs-lookup"><span data-stu-id="89958-126">The two-parameter method verifies that the *iPosition* parameter is zero and then calls the single-parameter version.</span></span> <span data-ttu-id="89958-127">Selon le nombre de types de médias pris en charge par le pin, vous devez remplacer l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="89958-127">Depending on the number of media types the pin supports, you must override one of these methods:</span></span>

-   <span data-ttu-id="89958-128">Si le code PIN ne prend en charge qu’un seul type de média, remplacez la version à paramètre unique.</span><span class="sxs-lookup"><span data-stu-id="89958-128">If the pin supports exactly one media type, override the single-parameter version.</span></span> <span data-ttu-id="89958-129">Renseignez le type de média que le code confidentiel prend en charge.</span><span class="sxs-lookup"><span data-stu-id="89958-129">Fill in the media type that the pin supports.</span></span>
-   <span data-ttu-id="89958-130">Si le code PIN prend en charge plusieurs types de média, remplacez la version à deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="89958-130">If the pin supports more than one media type, override the two-parameter version.</span></span> <span data-ttu-id="89958-131">Substituez également la méthode [**CSourceStream :: CheckMediaType**](csourcestream-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="89958-131">Also override the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="89958-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89958-132">Requirements</span></span>



| <span data-ttu-id="89958-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89958-133">Requirement</span></span> | <span data-ttu-id="89958-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="89958-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89958-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="89958-135">Header</span></span><br/>  | <dl> <span data-ttu-id="89958-136"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89958-136"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="89958-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="89958-137">Library</span></span><br/> | <dl> <span data-ttu-id="89958-138"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="89958-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89958-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89958-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89958-140">**CSourceStream, classe**</span><span class="sxs-lookup"><span data-stu-id="89958-140">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




