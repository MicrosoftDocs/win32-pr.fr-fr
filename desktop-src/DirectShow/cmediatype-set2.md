---
description: La méthode Set définit le type de média à partir d’un autre type de média.
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: CMediaType. Set, méthode (mtype. h)-mtype [ref], paramètre
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
ms.openlocfilehash: e8fd9145ee33dbe4b589b34833836466efa62ada
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106540131"
---
# <a name="cmediatypeset-method-mtypeh"></a><span data-ttu-id="8ce3b-103">CMediaType. Set, méthode (mtype. h)</span><span class="sxs-lookup"><span data-stu-id="8ce3b-103">CMediaType.Set method (Mtype.h)</span></span>

<span data-ttu-id="8ce3b-104">La `Set` méthode définit le type de média à partir d’un autre type de média.</span><span class="sxs-lookup"><span data-stu-id="8ce3b-104">The `Set` method sets the media type from another media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ce3b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ce3b-105">Syntax</span></span>


```C++
HRESULT Set(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a><span data-ttu-id="8ce3b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ce3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ce3b-107">*mtype* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="8ce3b-107">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8ce3b-108">Référence à une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="8ce3b-108">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ce3b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8ce3b-109">Return value</span></span>

<span data-ttu-id="8ce3b-110">Retourne S \_ OK ou E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8ce3b-110">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ce3b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8ce3b-111">Remarks</span></span>

<span data-ttu-id="8ce3b-112">Cette méthode copie l’intégralité du type de média à partir de *mtype*.</span><span class="sxs-lookup"><span data-stu-id="8ce3b-112">This method copies the entire media type from *mtype*.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ce3b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ce3b-113">Requirements</span></span>



| <span data-ttu-id="8ce3b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ce3b-114">Requirement</span></span> | <span data-ttu-id="8ce3b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ce3b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ce3b-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ce3b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8ce3b-117"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ce3b-117"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="8ce3b-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8ce3b-118">Library</span></span><br/> | <dl> <span data-ttu-id="8ce3b-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8ce3b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ce3b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ce3b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ce3b-121">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="8ce3b-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




