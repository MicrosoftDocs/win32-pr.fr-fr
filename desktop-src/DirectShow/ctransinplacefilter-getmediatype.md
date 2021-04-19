---
description: La méthode GetMediaType récupère un type de média par défaut pour la broche de sortie.
ms.assetid: 1bc6c06d-f399-4b8a-81f2-7fffe4630236
title: Méthode CTransInPlaceFilter. GetMediaType (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2347e0466a7df848e0f0b2bccec325eedfefc8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528056"
---
# <a name="ctransinplacefiltergetmediatype-method"></a><span data-ttu-id="1c548-103">Méthode CTransInPlaceFilter. GetMediaType</span><span class="sxs-lookup"><span data-stu-id="1c548-103">CTransInPlaceFilter.GetMediaType method</span></span>

<span data-ttu-id="1c548-104">La `GetMediaType` méthode récupère un type de média par défaut pour la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="1c548-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c548-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c548-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="1c548-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c548-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c548-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="1c548-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="1c548-108">Valeur d’index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="1c548-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="1c548-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="1c548-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="1c548-110">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui reçoit le type de média.</span><span class="sxs-lookup"><span data-stu-id="1c548-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c548-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1c548-111">Return value</span></span>

<span data-ttu-id="1c548-112">Retourne E \_ inattendu.</span><span class="sxs-lookup"><span data-stu-id="1c548-112">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c548-113">Notes</span><span class="sxs-lookup"><span data-stu-id="1c548-113">Remarks</span></span>

<span data-ttu-id="1c548-114">Cette méthode remplace la méthode [**CTransformFilter :: GetMediaType**](ctransformfilter-getmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="1c548-114">This method overrides the [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method.</span></span> <span data-ttu-id="1c548-115">Dans la classe **CTransInPlaceFilter** , chaque pin appelle le code PIN connecté opposé pour énumérer les types de média préférés.</span><span class="sxs-lookup"><span data-stu-id="1c548-115">In the **CTransInPlaceFilter** class, each pin calls the opposite connected pin to enumerate preferred media types.</span></span> <span data-ttu-id="1c548-116">La broche d’entrée appelle la broche d’entrée du filtre en aval, et la broche de sortie appelle la broche de sortie du filtre en amont.</span><span class="sxs-lookup"><span data-stu-id="1c548-116">The input pin calls the downstream filter's input pin, and the output pin calls the upstream filter's output pin.</span></span> <span data-ttu-id="1c548-117">Par conséquent, la méthode du filtre `GetMediaType` n’est jamais appelée.</span><span class="sxs-lookup"><span data-stu-id="1c548-117">Therefore, the filter's `GetMediaType` method is never called.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c548-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c548-118">Requirements</span></span>



| <span data-ttu-id="1c548-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c548-119">Requirement</span></span> | <span data-ttu-id="1c548-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c548-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c548-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="1c548-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1c548-122"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c548-122"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1c548-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1c548-123">Library</span></span><br/> | <dl> <span data-ttu-id="1c548-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1c548-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c548-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c548-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c548-126">**CTransInPlaceFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="1c548-126">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




