---
description: 'La méthode StartStreaming est appelée lorsque le filtre passe à l’état suspendu. Cette méthode remplace la méthode CTransformFilter :: StartStreaming.'
ms.assetid: fa05f88f-fed8-479d-b0b4-d9df982d51e7
title: Méthode CVideoTransformFilter. StartStreaming (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5ae8d49401389830f9d5dbf0ec91e7f390c51ca6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540357"
---
# <a name="cvideotransformfilterstartstreaming-method"></a><span data-ttu-id="992d0-104">Méthode CVideoTransformFilter. StartStreaming</span><span class="sxs-lookup"><span data-stu-id="992d0-104">CVideoTransformFilter.StartStreaming method</span></span>

<span data-ttu-id="992d0-105">La `StartStreaming` méthode est appelée lorsque le filtre passe à l’état suspendu.</span><span class="sxs-lookup"><span data-stu-id="992d0-105">The `StartStreaming` method is called when the filter switches to the paused state.</span></span> <span data-ttu-id="992d0-106">Cette méthode remplace la méthode [**CTransformFilter :: StartStreaming**](ctransformfilter-startstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="992d0-106">This method overrides the [**CTransformFilter::StartStreaming**](ctransformfilter-startstreaming.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="992d0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="992d0-107">Syntax</span></span>


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="992d0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="992d0-108">Parameters</span></span>

<span data-ttu-id="992d0-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="992d0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="992d0-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="992d0-110">Return value</span></span>

<span data-ttu-id="992d0-111">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="992d0-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="992d0-112">Notes</span><span class="sxs-lookup"><span data-stu-id="992d0-112">Remarks</span></span>

<span data-ttu-id="992d0-113">Cette méthode réinitialise toutes les statistiques de performances.</span><span class="sxs-lookup"><span data-stu-id="992d0-113">This method resets all of the performance statistics.</span></span>

## <a name="requirements"></a><span data-ttu-id="992d0-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="992d0-114">Requirements</span></span>



| <span data-ttu-id="992d0-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="992d0-115">Requirement</span></span> | <span data-ttu-id="992d0-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="992d0-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="992d0-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="992d0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="992d0-118"><dt>Vtrans. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="992d0-118"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="992d0-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="992d0-119">Library</span></span><br/> | <dl> <span data-ttu-id="992d0-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="992d0-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="992d0-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="992d0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="992d0-122">**CVideoTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="992d0-122">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




