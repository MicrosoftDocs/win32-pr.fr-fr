---
description: 'La méthode GetActualDataLength récupère la longueur des données valides dans la mémoire tampon. Cette méthode implémente la méthode IMediaSample :: GetActualDataLength.'
ms.assetid: bdb8c2b9-7be4-494b-bb96-34a9936d4a2f
title: Méthode CMediaSample. GetActualDataLength (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e65b72c1e0b6db85a271c10f76e5630b0799b78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535368"
---
# <a name="cmediasamplegetactualdatalength-method"></a><span data-ttu-id="bb23c-104">Méthode CMediaSample. GetActualDataLength</span><span class="sxs-lookup"><span data-stu-id="bb23c-104">CMediaSample.GetActualDataLength method</span></span>

<span data-ttu-id="bb23c-105">La `GetActualDataLength` méthode récupère la longueur des données valides dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="bb23c-105">The `GetActualDataLength` method retrieves the length of the valid data in the buffer.</span></span> <span data-ttu-id="bb23c-106">Cette méthode implémente la méthode [**IMediaSample :: GetActualDataLength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength) .</span><span class="sxs-lookup"><span data-stu-id="bb23c-106">This method implements the [**IMediaSample::GetActualDataLength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb23c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb23c-107">Syntax</span></span>


```C++
LONG GetActualDataLength();
```



## <a name="parameters"></a><span data-ttu-id="bb23c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb23c-108">Parameters</span></span>

<span data-ttu-id="bb23c-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="bb23c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bb23c-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bb23c-110">Return value</span></span>

<span data-ttu-id="bb23c-111">Retourne la longueur des données valides, en octets.</span><span class="sxs-lookup"><span data-stu-id="bb23c-111">Returns the length of the valid data, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb23c-112">Notes</span><span class="sxs-lookup"><span data-stu-id="bb23c-112">Remarks</span></span>

<span data-ttu-id="bb23c-113">La variable membre [**CMediaSample :: m \_ lActual**](cmediasample-m-lactual.md) spécifie cette propriété.</span><span class="sxs-lookup"><span data-stu-id="bb23c-113">The [**CMediaSample::m\_lActual**](cmediasample-m-lactual.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb23c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb23c-114">Requirements</span></span>



| <span data-ttu-id="bb23c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb23c-115">Requirement</span></span> | <span data-ttu-id="bb23c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb23c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb23c-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb23c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="bb23c-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb23c-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bb23c-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bb23c-119">Library</span></span><br/> | <dl> <span data-ttu-id="bb23c-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bb23c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb23c-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb23c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb23c-122">**CMediaSample, classe**</span><span class="sxs-lookup"><span data-stu-id="bb23c-122">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

