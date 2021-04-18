---
description: 'La méthode IsDiscontinuity détermine si cet exemple représente une rupture dans le flux de données. Cette méthode implémente la méthode IMediaSample :: IsDiscontinuity.'
ms.assetid: 125b4a86-bd26-4539-a9ab-281f1aed1836
title: Méthode CMediaSample. IsDiscontinuity (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e222ea813793dd537c8623f74403baed9a320a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532930"
---
# <a name="cmediasampleisdiscontinuity-method"></a><span data-ttu-id="66425-104">Méthode CMediaSample. IsDiscontinuity</span><span class="sxs-lookup"><span data-stu-id="66425-104">CMediaSample.IsDiscontinuity method</span></span>

<span data-ttu-id="66425-105">La `IsDiscontinuity` méthode détermine si cet exemple représente une rupture dans le flux de données.</span><span class="sxs-lookup"><span data-stu-id="66425-105">The `IsDiscontinuity` method determines if this sample represents a break in the data stream.</span></span> <span data-ttu-id="66425-106">Cette méthode implémente la méthode [**IMediaSample :: IsDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-isdiscontinuity) .</span><span class="sxs-lookup"><span data-stu-id="66425-106">This method implements the [**IMediaSample::IsDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-isdiscontinuity) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="66425-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66425-107">Syntax</span></span>


```C++
HRESULT IsDiscontinuity();
```



## <a name="parameters"></a><span data-ttu-id="66425-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66425-108">Parameters</span></span>

<span data-ttu-id="66425-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="66425-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="66425-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="66425-110">Return value</span></span>

<span data-ttu-id="66425-111">Retourne S \_ OK si l’exemple est une interruption dans le flux de données, et \_ s false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="66425-111">Returns S\_OK if the sample is a break in the data stream, and S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="66425-112">Notes</span><span class="sxs-lookup"><span data-stu-id="66425-112">Remarks</span></span>

<span data-ttu-id="66425-113">La variable de membre [**CMediaSample :: m \_ dwFlags**](cmediasample-m-dwflags.md) spécifie cette propriété.</span><span class="sxs-lookup"><span data-stu-id="66425-113">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="66425-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66425-114">Requirements</span></span>



| <span data-ttu-id="66425-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66425-115">Requirement</span></span> | <span data-ttu-id="66425-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="66425-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66425-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="66425-117">Header</span></span><br/>  | <dl> <span data-ttu-id="66425-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66425-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="66425-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="66425-119">Library</span></span><br/> | <dl> <span data-ttu-id="66425-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="66425-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66425-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66425-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66425-122">**CMediaSample, classe**</span><span class="sxs-lookup"><span data-stu-id="66425-122">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




