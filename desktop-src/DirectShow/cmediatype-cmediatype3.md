---
description: En savoir plus sur la méthode du constructeur CMediaType. CMediaType (mtype. h). Cette méthode utilise les paramètres’mtype’et’PHR'.
ms.assetid: b7d5264a-2a5f-4111-96bb-1ea2b13405be
title: CMediaType. CMediaType, constructeur (mtype. h)-mtype et PHR, paramètres
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 12ef9012e59dfce1f45d21aa720ae13bd660f2d8
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "106523004"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---mtype-and-phr-parameters"></a><span data-ttu-id="c1cf6-104">CMediaType. CMediaType, constructeur (mtype. h)-mtype et PHR, paramètres</span><span class="sxs-lookup"><span data-stu-id="c1cf6-104">CMediaType.CMediaType constructor (Mtype.h) - mtype and phr parameters</span></span>

<span data-ttu-id="c1cf6-105">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="c1cf6-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1cf6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1cf6-106">Syntax</span></span>


```C++
CMediaType(
  [ref] const AM_MEDIA_TYPE &mtype,
              HRESULT       *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="c1cf6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1cf6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1cf6-108">*mtype* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="c1cf6-108">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c1cf6-109">Référence à une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="c1cf6-109">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="c1cf6-110">Le constructeur copie le type de média vers le nouvel objet, y compris le bloc de format, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="c1cf6-110">The constructor copies the media type to the new object, including the format block, if any.</span></span>

</dd> <dt>

<span data-ttu-id="c1cf6-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="c1cf6-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="c1cf6-112">Pointeur vers une variable qui reçoit une valeur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="c1cf6-112">Pointer to a variable that receives an HRESULT value.</span></span> <span data-ttu-id="c1cf6-113">Ce paramètre peut être un pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="c1cf6-113">This parameter can be a **NULL** pointer.</span></span> <span data-ttu-id="c1cf6-114">Dans le cas contraire, l’appelant doit définir la valeur sur S \_ OK avant d’appeler le constructeur.</span><span class="sxs-lookup"><span data-stu-id="c1cf6-114">Otherwise, the caller must set the value to S\_OK before calling the constructor.</span></span> <span data-ttu-id="c1cf6-115">Si le constructeur échoue, il définit la valeur sur un code d’échec.</span><span class="sxs-lookup"><span data-stu-id="c1cf6-115">If the constructor fails, it sets the value to a failure code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1cf6-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c1cf6-116">Remarks</span></span>

<span data-ttu-id="c1cf6-117">Le constructeur appelle la méthode [**CMediaType :: InitMediaType**](cmediatype-initmediatype.md) pour initialiser le type de média.</span><span class="sxs-lookup"><span data-stu-id="c1cf6-117">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1cf6-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1cf6-118">Requirements</span></span>

| <span data-ttu-id="c1cf6-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1cf6-119">Requirement</span></span>                   | <span data-ttu-id="c1cf6-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1cf6-120">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1cf6-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1cf6-121">Header</span></span>  | <span data-ttu-id="c1cf6-122">Mtype. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="c1cf6-122">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="c1cf6-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c1cf6-123">Library</span></span> | <span data-ttu-id="c1cf6-124">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="c1cf6-124">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="c1cf6-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1cf6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1cf6-126">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="c1cf6-126">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




