---
description: 'La méthode CheckMediaType détermine si le code PIN accepte un type de média spécifique. Cette méthode implémente la méthode CBasePin :: CheckMediaType virtuelle pure.'
ms.assetid: 3db7c74c-a6aa-4b49-b2a5-9bf8db35fd7e
title: Méthode CSourceStream. CheckMediaType (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62f8b6c18613f5c187fc637febd08b74260a1e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539230"
---
# <a name="csourcestreamcheckmediatype-method"></a><span data-ttu-id="d0fd7-104">Méthode CSourceStream. CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="d0fd7-104">CSourceStream.CheckMediaType method</span></span>

<span data-ttu-id="d0fd7-105">La `CheckMediaType` méthode détermine si le code PIN accepte un type de média spécifique.</span><span class="sxs-lookup"><span data-stu-id="d0fd7-105">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span> <span data-ttu-id="d0fd7-106">Cette méthode implémente la méthode [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) virtuelle pure.</span><span class="sxs-lookup"><span data-stu-id="d0fd7-106">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0fd7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0fd7-107">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="d0fd7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0fd7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0fd7-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="d0fd7-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="d0fd7-110">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui contient le type de média proposé.</span><span class="sxs-lookup"><span data-stu-id="d0fd7-110">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0fd7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d0fd7-111">Return value</span></span>

<span data-ttu-id="d0fd7-112">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d0fd7-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="d0fd7-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d0fd7-113">Return code</span></span>                                                                            | <span data-ttu-id="d0fd7-114">Description</span><span class="sxs-lookup"><span data-stu-id="d0fd7-114">Description</span></span>                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="d0fd7-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d0fd7-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="d0fd7-116">Ce code PIN prend en charge ce type de média.</span><span class="sxs-lookup"><span data-stu-id="d0fd7-116">This pin supports this media type.</span></span><br/>        |
| <dl> <span data-ttu-id="d0fd7-117"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="d0fd7-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="d0fd7-118">Le code PIN ne prend pas en charge ce type de média.</span><span class="sxs-lookup"><span data-stu-id="d0fd7-118">The pin does not support this media type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d0fd7-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d0fd7-119">Remarks</span></span>

<span data-ttu-id="d0fd7-120">Par défaut, le code PIN prend en charge un seul type de média.</span><span class="sxs-lookup"><span data-stu-id="d0fd7-120">By default, the pin supports a single media type.</span></span> <span data-ttu-id="d0fd7-121">Cette méthode récupère le type pris en charge en appelant la version à paramètre unique de la méthode [**CSourceStream :: GetMediaType**](csourcestream-getmediatype.md) et le compare au type proposé.</span><span class="sxs-lookup"><span data-stu-id="d0fd7-121">This method retrieves the supported type by calling the single-parameter version of the [**CSourceStream::GetMediaType**](csourcestream-getmediatype.md) method, and compares it to the proposed type.</span></span> <span data-ttu-id="d0fd7-122">Si votre code PIN prend en charge plusieurs types de média, substituez cette méthode.</span><span class="sxs-lookup"><span data-stu-id="d0fd7-122">If your pin supports more than one media type, override this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0fd7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0fd7-123">Requirements</span></span>



| <span data-ttu-id="d0fd7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0fd7-124">Requirement</span></span> | <span data-ttu-id="d0fd7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0fd7-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0fd7-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0fd7-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d0fd7-127"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0fd7-127"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d0fd7-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d0fd7-128">Library</span></span><br/> | <dl> <span data-ttu-id="d0fd7-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d0fd7-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0fd7-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0fd7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0fd7-131">**CSourceStream, classe**</span><span class="sxs-lookup"><span data-stu-id="d0fd7-131">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




