---
description: 'La méthode IsSyncPoint détermine si le début de l’exemple est un point de synchronisation. Cette méthode implémente la méthode IMediaSample :: IsSyncPoint.'
ms.assetid: e57f78f4-7bb9-4e23-bcb4-55ad7ab5482c
title: Méthode CMediaSample. IsSyncPoint (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8cc93c03ce3b864e1c1b0a5794d711b1b0c3d68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545903"
---
# <a name="cmediasampleissyncpoint-method"></a><span data-ttu-id="6c421-104">Méthode CMediaSample. IsSyncPoint</span><span class="sxs-lookup"><span data-stu-id="6c421-104">CMediaSample.IsSyncPoint method</span></span>

<span data-ttu-id="6c421-105">La `IsSyncPoint` méthode détermine si le début de l’exemple est un point de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="6c421-105">The `IsSyncPoint` method determines if the beginning of the sample is a synchronization point.</span></span> <span data-ttu-id="6c421-106">Cette méthode implémente la méthode [**IMediaSample :: IsSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint) .</span><span class="sxs-lookup"><span data-stu-id="6c421-106">This method implements the [**IMediaSample::IsSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c421-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c421-107">Syntax</span></span>


```C++
HRESULT IsSyncPoint();
```



## <a name="parameters"></a><span data-ttu-id="6c421-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c421-108">Parameters</span></span>

<span data-ttu-id="6c421-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6c421-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6c421-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6c421-110">Return value</span></span>

<span data-ttu-id="6c421-111">Retourne S \_ OK si l’échantillon est un point de synchronisation, ou a la \_ valeur false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6c421-111">Returns S\_OK if the sample is a synchronization point, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c421-112">Notes</span><span class="sxs-lookup"><span data-stu-id="6c421-112">Remarks</span></span>

<span data-ttu-id="6c421-113">La variable de membre [**CMediaSample :: m \_ dwFlags**](cmediasample-m-dwflags.md) spécifie cette propriété.</span><span class="sxs-lookup"><span data-stu-id="6c421-113">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c421-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c421-114">Requirements</span></span>



| <span data-ttu-id="6c421-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c421-115">Requirement</span></span> | <span data-ttu-id="6c421-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c421-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c421-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c421-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6c421-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c421-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6c421-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6c421-119">Library</span></span><br/> | <dl> <span data-ttu-id="6c421-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6c421-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c421-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c421-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c421-122">**CMediaSample, classe**</span><span class="sxs-lookup"><span data-stu-id="6c421-122">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




