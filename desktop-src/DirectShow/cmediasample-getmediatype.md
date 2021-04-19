---
description: 'La méthode GetMediaType récupère le type de média si le type de média diffère de l’exemple précédent. Cette méthode implémente la méthode IMediaSample :: GetMediaType.'
ms.assetid: a7850381-d448-4bf6-b059-d734fb3e8e22
title: Méthode CMediaSample. GetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a067494d6236b824ef8fbbcb583ad50503297b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523539"
---
# <a name="cmediasamplegetmediatype-method"></a><span data-ttu-id="954a5-104">Méthode CMediaSample. GetMediaType</span><span class="sxs-lookup"><span data-stu-id="954a5-104">CMediaSample.GetMediaType method</span></span>

<span data-ttu-id="954a5-105">La `GetMediaType` méthode récupère le type de média si le type de média diffère de l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="954a5-105">The `GetMediaType` method retrieves the media type, if the media type differs from the previous sample.</span></span> <span data-ttu-id="954a5-106">Cette méthode implémente la méthode [**IMediaSample :: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) .</span><span class="sxs-lookup"><span data-stu-id="954a5-106">This method implements the [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="954a5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="954a5-107">Syntax</span></span>


```C++
HRESULT GetMediaType(
   AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="954a5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="954a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="954a5-109">*ppMediaType*</span><span class="sxs-lookup"><span data-stu-id="954a5-109">*ppMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="954a5-110">Adresse d’une variable qui reçoit un pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="954a5-110">Address of a variable that receives a pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="954a5-111">Si le type de média n’a pas été modifié par rapport à l’exemple précédent, *\* ppMediaType* a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="954a5-111">If the media type has not changed from the previous sample, *\*ppMediaType* is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="954a5-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="954a5-112">Return value</span></span>

<span data-ttu-id="954a5-113">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="954a5-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="954a5-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="954a5-114">Return code</span></span>                                                                                   | <span data-ttu-id="954a5-115">Description</span><span class="sxs-lookup"><span data-stu-id="954a5-115">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="954a5-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="954a5-116"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="954a5-117">Le type de média n’a pas été modifié par rapport à l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="954a5-117">The media type has not changed from the previous sample.</span></span><br/> |
| <dl> <span data-ttu-id="954a5-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="954a5-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="954a5-119">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="954a5-119">Success.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="954a5-120"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="954a5-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="954a5-121">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="954a5-121">Insufficient memory.</span></span><br/>                                     |



 

## <a name="remarks"></a><span data-ttu-id="954a5-122">Notes</span><span class="sxs-lookup"><span data-stu-id="954a5-122">Remarks</span></span>

<span data-ttu-id="954a5-123">Lorsque vous avez terminé avec le type de média, libérez le bloc de mémoire en appelant la fonction de l’utilitaire [**DeleteMediaType**](deletemediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="954a5-123">When you are done with the media type, free the memory block by calling the [**DeleteMediaType**](deletemediatype.md) utility function.</span></span>

<span data-ttu-id="954a5-124">La variable membre [**CMediaSample :: m \_ pMediaType**](cmediasample-m-pmediatype.md) spécifie le type de média.</span><span class="sxs-lookup"><span data-stu-id="954a5-124">The [**CMediaSample::m\_pMediaType**](cmediasample-m-pmediatype.md) member variable specifies the media type.</span></span> <span data-ttu-id="954a5-125">La variable de membre [**CMediaSample :: m \_ dwFlags**](cmediasample-m-dwflags.md) spécifie si le type de média a changé.</span><span class="sxs-lookup"><span data-stu-id="954a5-125">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies whether the media type has changed.</span></span>

## <a name="requirements"></a><span data-ttu-id="954a5-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="954a5-126">Requirements</span></span>



| <span data-ttu-id="954a5-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="954a5-127">Requirement</span></span> | <span data-ttu-id="954a5-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="954a5-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="954a5-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="954a5-129">Header</span></span><br/>  | <dl> <span data-ttu-id="954a5-130"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="954a5-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="954a5-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="954a5-131">Library</span></span><br/> | <dl> <span data-ttu-id="954a5-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="954a5-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="954a5-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="954a5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="954a5-134">**CMediaSample, classe**</span><span class="sxs-lookup"><span data-stu-id="954a5-134">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




