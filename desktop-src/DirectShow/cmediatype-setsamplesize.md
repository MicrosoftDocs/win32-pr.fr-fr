---
description: La méthode SetSampleSize spécifie une taille d’échantillon fixe ou spécifie que les échantillons ont une taille variable.
ms.assetid: b0f9dd7b-4ff9-4d11-9c13-b52d7b1549b5
title: Méthode CMediaType. SetSampleSize (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0992afd0576c1039397e6ecaa2119a989283136e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539682"
---
# <a name="cmediatypesetsamplesize-method"></a><span data-ttu-id="809fd-103">Méthode CMediaType. SetSampleSize</span><span class="sxs-lookup"><span data-stu-id="809fd-103">CMediaType.SetSampleSize method</span></span>

<span data-ttu-id="809fd-104">La `SetSampleSize` méthode spécifie une taille d’échantillon fixe ou spécifie que les échantillons ont une taille variable.</span><span class="sxs-lookup"><span data-stu-id="809fd-104">The `SetSampleSize` method specifies a fixed sample size, or specifies that samples have a variable size.</span></span>

## <a name="syntax"></a><span data-ttu-id="809fd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="809fd-105">Syntax</span></span>


```C++
void SetSampleSize(
   ULONG sz
);
```



## <a name="parameters"></a><span data-ttu-id="809fd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="809fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="809fd-107">*SZ*</span><span class="sxs-lookup"><span data-stu-id="809fd-107">*sz*</span></span> 
</dt> <dd>

<span data-ttu-id="809fd-108">Taille de l’échantillon, en octets, ou zéro.</span><span class="sxs-lookup"><span data-stu-id="809fd-108">Sample size, in bytes, or zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="809fd-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="809fd-109">Return value</span></span>

<span data-ttu-id="809fd-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="809fd-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="809fd-111">Notes</span><span class="sxs-lookup"><span data-stu-id="809fd-111">Remarks</span></span>

<span data-ttu-id="809fd-112">Si la valeur de *SZ* est égale à zéro, le type de média utilise des tailles d’échantillons variables.</span><span class="sxs-lookup"><span data-stu-id="809fd-112">If value of *sz* is zero, the media type uses variable sample sizes.</span></span> <span data-ttu-id="809fd-113">Dans le cas contraire, la taille de l’échantillon est fixée à *SZ* octets.</span><span class="sxs-lookup"><span data-stu-id="809fd-113">Otherwise, the sample size is fixed at *sz* bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="809fd-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="809fd-114">Requirements</span></span>



| <span data-ttu-id="809fd-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="809fd-115">Requirement</span></span> | <span data-ttu-id="809fd-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="809fd-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="809fd-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="809fd-117">Header</span></span><br/>  | <dl> <span data-ttu-id="809fd-118"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="809fd-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="809fd-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="809fd-119">Library</span></span><br/> | <dl> <span data-ttu-id="809fd-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="809fd-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="809fd-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="809fd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="809fd-122">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="809fd-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




