---
description: 'La méthode SetMediaType définit le type de média pour l’exemple. Cette méthode implémente la méthode IMediaSample :: SetMediaType.'
ms.assetid: 4423cc1e-d6e1-49e7-9cc1-1a1d71a3497b
title: Méthode CMediaSample. SetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f46fc4e8c348b1d03d19e815f658e0f637b8f880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532950"
---
# <a name="cmediasamplesetmediatype-method"></a><span data-ttu-id="86e3c-104">Méthode CMediaSample. SetMediaType</span><span class="sxs-lookup"><span data-stu-id="86e3c-104">CMediaSample.SetMediaType method</span></span>

<span data-ttu-id="86e3c-105">La `SetMediaType` méthode définit le type de média pour l’exemple.</span><span class="sxs-lookup"><span data-stu-id="86e3c-105">The `SetMediaType` method sets the media type for the sample.</span></span> <span data-ttu-id="86e3c-106">Cette méthode implémente la méthode [**IMediaSample :: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) .</span><span class="sxs-lookup"><span data-stu-id="86e3c-106">This method implements the [**IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="86e3c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86e3c-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
   AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="86e3c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86e3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86e3c-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="86e3c-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="86e3c-110">Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="86e3c-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86e3c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="86e3c-111">Return value</span></span>

<span data-ttu-id="86e3c-112">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="86e3c-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="86e3c-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="86e3c-113">Return code</span></span>                                                                                   | <span data-ttu-id="86e3c-114">Description</span><span class="sxs-lookup"><span data-stu-id="86e3c-114">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="86e3c-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="86e3c-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="86e3c-116">Succès</span><span class="sxs-lookup"><span data-stu-id="86e3c-116">Success</span></span><br/>             |
| <dl> <span data-ttu-id="86e3c-117"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="86e3c-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="86e3c-118">Mémoire insuffisante</span><span class="sxs-lookup"><span data-stu-id="86e3c-118">Insufficient memory</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="86e3c-119">Notes</span><span class="sxs-lookup"><span data-stu-id="86e3c-119">Remarks</span></span>

<span data-ttu-id="86e3c-120">Cette méthode définit la variable de membre [**CMediaSample :: m \_ pMediaType**](cmediasample-m-pmediatype.md) , qui spécifie le type de média et la variable de membre [**CMediaSample :: m \_ dwFlags**](cmediasample-m-dwflags.md) , qui spécifie si le type de média a changé.</span><span class="sxs-lookup"><span data-stu-id="86e3c-120">This method sets the [**CMediaSample::m\_pMediaType**](cmediasample-m-pmediatype.md) member variable, which specifies the media type, and the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies whether the media type has changed.</span></span>

<span data-ttu-id="86e3c-121">Cette méthode effectue une copie de la \_ structure du type de média am \_ .</span><span class="sxs-lookup"><span data-stu-id="86e3c-121">This method makes a copy of the AM\_MEDIA\_TYPE structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="86e3c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86e3c-122">Requirements</span></span>



| <span data-ttu-id="86e3c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86e3c-123">Requirement</span></span> | <span data-ttu-id="86e3c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="86e3c-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86e3c-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="86e3c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="86e3c-126"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86e3c-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="86e3c-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="86e3c-127">Library</span></span><br/> | <dl> <span data-ttu-id="86e3c-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="86e3c-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86e3c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86e3c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e3c-130">**CMediaSample, classe**</span><span class="sxs-lookup"><span data-stu-id="86e3c-130">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




