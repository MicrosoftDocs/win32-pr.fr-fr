---
description: La méthode GetMediaType récupère un type de média par défaut. Cette méthode utilise les paramètres *iPosition* et *pMediaType* .
ms.assetid: c5c5f498-a9a3-4ce7-8cf5-941397aa649d
title: Méthode CSourceStream. GetMediaType (source. h)-paramètres iPosition et pMediaType
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
ms.openlocfilehash: 9d8936f08b952af069812859736a6a13ea9c0e4e
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106537735"
---
# <a name="csourcestreamgetmediatype-method-sourceh---iposition-and-pmediatype-parameters"></a><span data-ttu-id="91176-104">Méthode CSourceStream. GetMediaType (source. h)-paramètres iPosition et pMediaType</span><span class="sxs-lookup"><span data-stu-id="91176-104">CSourceStream.GetMediaType method (Source.h) - iPosition and pMediaType parameters</span></span>

<span data-ttu-id="91176-105">La méthode **GetMediaType** récupère un type de média par défaut.</span><span class="sxs-lookup"><span data-stu-id="91176-105">The **GetMediaType** method retrieves a preferred media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="91176-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91176-106">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="91176-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91176-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91176-108">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="91176-108">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="91176-109">Valeur d’index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="91176-109">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="91176-110">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="91176-110">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="91176-111">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui reçoit le type de média.</span><span class="sxs-lookup"><span data-stu-id="91176-111">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91176-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91176-112">Return value</span></span>

<span data-ttu-id="91176-113">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="91176-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="91176-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="91176-114">Return code</span></span>                                                                                            | <span data-ttu-id="91176-115">Description</span><span class="sxs-lookup"><span data-stu-id="91176-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="91176-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="91176-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="91176-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="91176-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="91176-118"><dt>**VFW \_ S \_ n’a \_ plus d' \_ éléments**</dt></span><span class="sxs-lookup"><span data-stu-id="91176-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="91176-119">Index hors limites.</span><span class="sxs-lookup"><span data-stu-id="91176-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="91176-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="91176-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="91176-121">Index inférieur à zéro.</span><span class="sxs-lookup"><span data-stu-id="91176-121">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="91176-122"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="91176-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="91176-123">Erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="91176-123">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="91176-124">Notes</span><span class="sxs-lookup"><span data-stu-id="91176-124">Remarks</span></span>

<span data-ttu-id="91176-125">Il existe deux versions de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="91176-125">There are two versions of this method.</span></span> <span data-ttu-id="91176-126">Une version remplace la méthode [**CBasePin :: GetMediaType**](cbasepin-getmediatype.md) et prend une valeur d’index en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="91176-126">One version overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method and takes an index value as a parameter.</span></span> <span data-ttu-id="91176-127">L’autre version est conçue pour récupérer un type de média unique, de sorte qu’il n’y ait pas de paramètre d’index.</span><span class="sxs-lookup"><span data-stu-id="91176-127">The other version is designed to retrieve a single media type, so it lacks the index parameter.</span></span>

<span data-ttu-id="91176-128">La méthode à paramètre unique retourne E \_ inattendue.</span><span class="sxs-lookup"><span data-stu-id="91176-128">The single-parameter method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="91176-129">La méthode à deux paramètres vérifie que le paramètre *iPosition* est égal à zéro, puis appelle la version à un seul paramètre.</span><span class="sxs-lookup"><span data-stu-id="91176-129">The two-parameter method verifies that the *iPosition* parameter is zero and then calls the single-parameter version.</span></span> <span data-ttu-id="91176-130">Selon le nombre de types de médias pris en charge par le pin, vous devez remplacer l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="91176-130">Depending on the number of media types the pin supports, you must override one of these methods:</span></span>

-   <span data-ttu-id="91176-131">Si le code PIN ne prend en charge qu’un seul type de média, remplacez la version à paramètre unique.</span><span class="sxs-lookup"><span data-stu-id="91176-131">If the pin supports exactly one media type, override the single-parameter version.</span></span> <span data-ttu-id="91176-132">Renseignez le type de média que le code confidentiel prend en charge.</span><span class="sxs-lookup"><span data-stu-id="91176-132">Fill in the media type that the pin supports.</span></span>
-   <span data-ttu-id="91176-133">Si le code PIN prend en charge plusieurs types de média, remplacez la version à deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="91176-133">If the pin supports more than one media type, override the two-parameter version.</span></span> <span data-ttu-id="91176-134">Substituez également la méthode [**CSourceStream :: CheckMediaType**](csourcestream-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="91176-134">Also override the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="91176-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91176-135">Requirements</span></span>



| <span data-ttu-id="91176-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91176-136">Requirement</span></span> | <span data-ttu-id="91176-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="91176-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91176-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="91176-138">Header</span></span>  | <span data-ttu-id="91176-139">Source. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="91176-139">Source.h (include Streams.h)</span></span>                                                                                    |
| <span data-ttu-id="91176-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="91176-140">Library</span></span> | <span data-ttu-id="91176-141">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="91176-141">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="91176-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91176-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91176-143">**CSourceStream, classe**</span><span class="sxs-lookup"><span data-stu-id="91176-143">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




