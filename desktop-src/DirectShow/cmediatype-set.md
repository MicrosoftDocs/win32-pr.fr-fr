---
description: La méthode CMediaType. Set (mtype. h) définit le type de média à partir d’un autre type de média. La méthode utilise le paramètre « cmtype ».
ms.assetid: 71c19d0f-93b6-41db-8659-c64411b83e7c
title: CMediaType. Set, méthode (mtype. h)-cmtype [ref], paramètre
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9bf14132660045afbd171173a38d3ea320ba1aa
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "106539931"
---
# <a name="cmediatypeset-method-mtypeh---cmtype-ref-parameter"></a><span data-ttu-id="42122-104">CMediaType. Set, méthode (mtype. h)-cmtype [ref], paramètre</span><span class="sxs-lookup"><span data-stu-id="42122-104">CMediaType.Set method (Mtype.h) - cmtype [ref] parameter</span></span>

<span data-ttu-id="42122-105">La `Set` méthode définit le type de média à partir d’un autre type de média.</span><span class="sxs-lookup"><span data-stu-id="42122-105">The `Set` method sets the media type from another media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="42122-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42122-106">Syntax</span></span>


```C++
HRESULT Set(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a><span data-ttu-id="42122-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42122-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42122-108">*cmtype* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="42122-108">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="42122-109">Référence à un objet [**CMediaType**](cmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="42122-109">Reference to a [**CMediaType**](cmediatype.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42122-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="42122-110">Return value</span></span>

<span data-ttu-id="42122-111">Retourne S \_ OK ou E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="42122-111">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="42122-112">Notes</span><span class="sxs-lookup"><span data-stu-id="42122-112">Remarks</span></span>

<span data-ttu-id="42122-113">Cette méthode copie l’intégralité du type de média à partir de *cmtype*.</span><span class="sxs-lookup"><span data-stu-id="42122-113">This method copies the entire media type from *cmtype*.</span></span>

## <a name="requirements"></a><span data-ttu-id="42122-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42122-114">Requirements</span></span>

| <span data-ttu-id="42122-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42122-115">Requirement</span></span>                   | <span data-ttu-id="42122-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="42122-116">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42122-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="42122-117">Header</span></span>  | <span data-ttu-id="42122-118">Mtype. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="42122-118">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="42122-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="42122-119">Library</span></span> | <span data-ttu-id="42122-120">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="42122-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="42122-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42122-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42122-122">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="42122-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




