---
description: 'La méthode SetSyncPoint spécifie si le début de cet exemple est un point de synchronisation. Cette méthode implémente la méthode IMediaSample :: SetSyncPoint.'
ms.assetid: 48fc5145-7cce-4e76-860d-45a0d5b43b67
title: Méthode CMediaSample. SetSyncPoint (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 679be6a313329a15c83bee4473e5a944aa3532b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539519"
---
# <a name="cmediasamplesetsyncpoint-method"></a><span data-ttu-id="db758-104">Méthode CMediaSample. SetSyncPoint</span><span class="sxs-lookup"><span data-stu-id="db758-104">CMediaSample.SetSyncPoint method</span></span>

<span data-ttu-id="db758-105">La `SetSyncPoint` méthode spécifie si le début de cet exemple est un point de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="db758-105">The `SetSyncPoint` method specifies whether the beginning of this sample is a synchronization point.</span></span> <span data-ttu-id="db758-106">Cette méthode implémente la méthode [**IMediaSample :: SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) .</span><span class="sxs-lookup"><span data-stu-id="db758-106">This method implements the [**IMediaSample::SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="db758-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db758-107">Syntax</span></span>


```C++
HRESULT SetSyncPoint(
   BOOL bIsSyncPoint
);
```



## <a name="parameters"></a><span data-ttu-id="db758-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db758-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db758-109">*bIsSyncPoint*</span><span class="sxs-lookup"><span data-stu-id="db758-109">*bIsSyncPoint*</span></span> 
</dt> <dd>

<span data-ttu-id="db758-110">Valeur booléenne qui spécifie s’il s’agit d’un point de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="db758-110">Boolean value that specifies whether this is a synchronization point.</span></span> <span data-ttu-id="db758-111">Si la **valeur est true**, il s’agit d’un point de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="db758-111">If **TRUE**, this is a synchronization point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db758-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="db758-112">Return value</span></span>

<span data-ttu-id="db758-113">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="db758-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="db758-114">Notes</span><span class="sxs-lookup"><span data-stu-id="db758-114">Remarks</span></span>

<span data-ttu-id="db758-115">Cette méthode met à jour la variable de membre [**CMediaSample :: m \_ dwFlags**](cmediasample-m-dwflags.md) , qui spécifie la propriété de point de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="db758-115">This method updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies the synchronization-point property.</span></span>

## <a name="requirements"></a><span data-ttu-id="db758-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db758-116">Requirements</span></span>



| <span data-ttu-id="db758-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db758-117">Requirement</span></span> | <span data-ttu-id="db758-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="db758-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db758-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="db758-119">Header</span></span><br/>  | <dl> <span data-ttu-id="db758-120"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db758-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="db758-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="db758-121">Library</span></span><br/> | <dl> <span data-ttu-id="db758-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="db758-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db758-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db758-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db758-124">**CMediaSample, classe**</span><span class="sxs-lookup"><span data-stu-id="db758-124">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




