---
description: 'La méthode SetDiscontinuity spécifie si cet exemple représente une rupture dans le flux de données. Cette méthode implémente la méthode IMediaSample :: SetDiscontinuity.'
ms.assetid: 29072130-1ec7-4b5b-8a43-5308b1365527
title: Méthode CMediaSample. SetDiscontinuity (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35565b2cee0284d0e5b9f85d7335a630b5f54e87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532759"
---
# <a name="cmediasamplesetdiscontinuity-method"></a><span data-ttu-id="46ebc-104">Méthode CMediaSample. SetDiscontinuity</span><span class="sxs-lookup"><span data-stu-id="46ebc-104">CMediaSample.SetDiscontinuity method</span></span>

<span data-ttu-id="46ebc-105">La `SetDiscontinuity` méthode spécifie si cet exemple représente une rupture dans le flux de données.</span><span class="sxs-lookup"><span data-stu-id="46ebc-105">The `SetDiscontinuity` method specifies whether this sample represents a break in the data stream.</span></span> <span data-ttu-id="46ebc-106">Cette méthode implémente la méthode [**IMediaSample :: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .</span><span class="sxs-lookup"><span data-stu-id="46ebc-106">This method implements the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="46ebc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46ebc-107">Syntax</span></span>


```C++
HRESULT SetDiscontinuity(
   BOOL bDiscont
);
```



## <a name="parameters"></a><span data-ttu-id="46ebc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46ebc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46ebc-109">*bDiscont*</span><span class="sxs-lookup"><span data-stu-id="46ebc-109">*bDiscont*</span></span> 
</dt> <dd>

<span data-ttu-id="46ebc-110">Valeur booléenne qui spécifie si cet exemple est une discontinuité.</span><span class="sxs-lookup"><span data-stu-id="46ebc-110">Boolean value that specifies whether this sample is a discontinuity.</span></span> <span data-ttu-id="46ebc-111">Si la **valeur est true**, l’exemple de média est discontinu avec l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="46ebc-111">If **TRUE**, the media sample is discontinuous with the previous sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46ebc-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="46ebc-112">Return value</span></span>

<span data-ttu-id="46ebc-113">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="46ebc-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="46ebc-114">Notes</span><span class="sxs-lookup"><span data-stu-id="46ebc-114">Remarks</span></span>

<span data-ttu-id="46ebc-115">Cette méthode met à jour la variable de membre [**CMediaSample :: m \_ dwFlags**](cmediasample-m-dwflags.md) , qui spécifie la propriété discontinu.</span><span class="sxs-lookup"><span data-stu-id="46ebc-115">This method updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies the discontinuity property.</span></span>

## <a name="requirements"></a><span data-ttu-id="46ebc-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46ebc-116">Requirements</span></span>



| <span data-ttu-id="46ebc-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46ebc-117">Requirement</span></span> | <span data-ttu-id="46ebc-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="46ebc-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46ebc-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="46ebc-119">Header</span></span><br/>  | <dl> <span data-ttu-id="46ebc-120"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46ebc-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="46ebc-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="46ebc-121">Library</span></span><br/> | <dl> <span data-ttu-id="46ebc-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="46ebc-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46ebc-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46ebc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46ebc-124">**CMediaSample, classe**</span><span class="sxs-lookup"><span data-stu-id="46ebc-124">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




