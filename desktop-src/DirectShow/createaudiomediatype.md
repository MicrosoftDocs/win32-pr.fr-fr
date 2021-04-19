---
description: La fonction CreateAudioMediaType Initialise un type de média à partir d’une structure WAVEFORMATEX.
ms.assetid: 2571b7b4-86e9-443f-a99d-9ba48f469522
title: Fonction CreateAudioMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateAudioMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef4e525762d4b6928e6a9095fad34f3f4f2e96fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543880"
---
# <a name="createaudiomediatype-function"></a><span data-ttu-id="8ae6b-103">CreateAudioMediaType fonction)</span><span class="sxs-lookup"><span data-stu-id="8ae6b-103">CreateAudioMediaType function</span></span>

<span data-ttu-id="8ae6b-104">La fonction **CreateAudioMediaType** Initialise un type de média à partir d’une structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8ae6b-104">The **CreateAudioMediaType** function initializes a media type from a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ae6b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ae6b-105">Syntax</span></span>


```C++
HRESULT STDAPI CreateAudioMediaType(
   const WAVEFORMATEX  *pwfx,
         AM_MEDIA_TYPE *pmt,
         BOOL          bSetFormat
);
```



## <a name="parameters"></a><span data-ttu-id="8ae6b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ae6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ae6b-107">*pwfx*</span><span class="sxs-lookup"><span data-stu-id="8ae6b-107">*pwfx*</span></span> 
</dt> <dd>

<span data-ttu-id="8ae6b-108">Pointeur vers la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) fournie.</span><span class="sxs-lookup"><span data-stu-id="8ae6b-108">Pointer to the supplied [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8ae6b-109">*crédit*</span><span class="sxs-lookup"><span data-stu-id="8ae6b-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="8ae6b-110">Pointeur vers la structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) à initialiser.</span><span class="sxs-lookup"><span data-stu-id="8ae6b-110">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to initialize.</span></span>

</dd> <dt>

<span data-ttu-id="8ae6b-111">*bSetFormat*</span><span class="sxs-lookup"><span data-stu-id="8ae6b-111">*bSetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="8ae6b-112">Indicateur précisant s’il faut initialiser le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="8ae6b-112">Flag indicating whether to initialize the format block.</span></span> <span data-ttu-id="8ae6b-113">Spécifiez **true** pour l’initialiser, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8ae6b-113">Specify **TRUE** to initialize it, or **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ae6b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8ae6b-114">Return value</span></span>

<span data-ttu-id="8ae6b-115">Retourne E \_ OUTOFMEMORY si la mémoire n’a pas pu être allouée pour les données de format ; OK dans le \_ cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8ae6b-115">Returns E\_OUTOFMEMORY if memory could not be allocated for the format data; S\_OK otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ae6b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="8ae6b-116">Remarks</span></span>

<span data-ttu-id="8ae6b-117">Si le paramètre *bSetFormat* a la **valeur true**, la méthode alloue la mémoire pour le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="8ae6b-117">If the *bSetFormat* parameter is **TRUE**, the method allocates the memory for the format block.</span></span> <span data-ttu-id="8ae6b-118">Si le paramètre *VPM* contient déjà un bloc de format alloué, une fuite de mémoire se produit.</span><span class="sxs-lookup"><span data-stu-id="8ae6b-118">If the *pmt* parameter already contains an allocated format block, a memory leak will occur.</span></span> <span data-ttu-id="8ae6b-119">Pour éviter une fuite de mémoire, appelez [**FreeMediaType**](freemediatype.md) avant d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="8ae6b-119">To avoid a memory leak, call [**FreeMediaType**](freemediatype.md) before calling this function.</span></span> <span data-ttu-id="8ae6b-120">Une fois la méthode retournée, appelez à nouveau **FreeMediaType** pour libérer le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="8ae6b-120">After the method returns, call **FreeMediaType** again to free the format block.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ae6b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ae6b-121">Requirements</span></span>



| <span data-ttu-id="8ae6b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ae6b-122">Requirement</span></span> | <span data-ttu-id="8ae6b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ae6b-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ae6b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ae6b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8ae6b-125"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ae6b-125"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="8ae6b-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8ae6b-126">Library</span></span><br/> | <dl> <span data-ttu-id="8ae6b-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8ae6b-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ae6b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ae6b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ae6b-129">**Fonctions de type de média**</span><span class="sxs-lookup"><span data-stu-id="8ae6b-129">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

