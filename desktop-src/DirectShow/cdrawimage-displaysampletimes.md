---
description: La méthode DisplaySampleTimes dessine les horodatages d’un échantillon de support en haut de l’image vidéo.
ms.assetid: 3741dc74-5311-4cb1-9e6b-4a8bf6113477
title: Méthode CDrawImage. DisplaySampleTimes (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DisplaySampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9988aaedf9a1c01c83412cdbe9e00533556c9b15
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543369"
---
# <a name="cdrawimagedisplaysampletimes-method"></a><span data-ttu-id="888ed-103">Méthode CDrawImage. DisplaySampleTimes</span><span class="sxs-lookup"><span data-stu-id="888ed-103">CDrawImage.DisplaySampleTimes method</span></span>

<span data-ttu-id="888ed-104">La `DisplaySampleTimes` méthode dessine les horodatages d’un échantillon de support en haut de l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="888ed-104">The `DisplaySampleTimes` method draws the time stamps of a media sample on top of the video image.</span></span>

## <a name="syntax"></a><span data-ttu-id="888ed-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="888ed-105">Syntax</span></span>


```C++
void DisplaySampleTimes(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="888ed-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="888ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="888ed-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="888ed-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="888ed-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="888ed-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="888ed-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="888ed-109">Return value</span></span>

<span data-ttu-id="888ed-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="888ed-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="888ed-111">Notes</span><span class="sxs-lookup"><span data-stu-id="888ed-111">Remarks</span></span>

<span data-ttu-id="888ed-112">Cette méthode est appelée uniquement dans les versions Debug.</span><span class="sxs-lookup"><span data-stu-id="888ed-112">This method is called only in debug builds.</span></span>

## <a name="requirements"></a><span data-ttu-id="888ed-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="888ed-113">Requirements</span></span>



| <span data-ttu-id="888ed-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="888ed-114">Requirement</span></span> | <span data-ttu-id="888ed-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="888ed-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="888ed-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="888ed-116">Header</span></span><br/>  | <dl> <span data-ttu-id="888ed-117"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="888ed-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="888ed-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="888ed-118">Library</span></span><br/> | <dl> <span data-ttu-id="888ed-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="888ed-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="888ed-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="888ed-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="888ed-121">**CDrawImage, classe**</span><span class="sxs-lookup"><span data-stu-id="888ed-121">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




