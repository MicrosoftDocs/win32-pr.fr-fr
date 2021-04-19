---
description: La fonction CopyMediaType copie une \_ \_ structure de type de média AM dans une autre structure, y compris le bloc de format
ms.assetid: 5b47e197-abb5-4b2c-ad65-a506c5e239be
title: Fonction CopyMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CopyMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e37f277244ae9b82c395d7901917e1fc1e78b35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544468"
---
# <a name="copymediatype-function"></a><span data-ttu-id="d1a29-103">CopyMediaType fonction)</span><span class="sxs-lookup"><span data-stu-id="d1a29-103">CopyMediaType function</span></span>

<span data-ttu-id="d1a29-104">La fonction **CopyMediaType** copie une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) dans une autre structure, y compris le bloc de format</span><span class="sxs-lookup"><span data-stu-id="d1a29-104">The **CopyMediaType** function copies an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure into another structure, including the format block</span></span>

## <a name="syntax"></a><span data-ttu-id="d1a29-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1a29-105">Syntax</span></span>


```C++
HRESULT WINAPI CopyMediaType(
         AM_MEDIA_TYPE *pmtTarget,
   const AM_MEDIA_TYPE *pmtSource
);
```



## <a name="parameters"></a><span data-ttu-id="d1a29-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1a29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1a29-107">*pmtTarget*</span><span class="sxs-lookup"><span data-stu-id="d1a29-107">*pmtTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="d1a29-108">Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="d1a29-108">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="d1a29-109">La méthode copie le type de média dans cette structure.</span><span class="sxs-lookup"><span data-stu-id="d1a29-109">The method copies the media type into this structure.</span></span>

</dd> <dt>

<span data-ttu-id="d1a29-110">*pmtSource*</span><span class="sxs-lookup"><span data-stu-id="d1a29-110">*pmtSource*</span></span> 
</dt> <dd>

<span data-ttu-id="d1a29-111">Pointeur vers une structure [**de \_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) source à copier.</span><span class="sxs-lookup"><span data-stu-id="d1a29-111">Pointer to a source [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to copy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1a29-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1a29-112">Return value</span></span>

<span data-ttu-id="d1a29-113">Retourne S \_ OK ou E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d1a29-113">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1a29-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d1a29-114">Remarks</span></span>

<span data-ttu-id="d1a29-115">Cette fonction alloue la mémoire pour le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="d1a29-115">This function allocates the memory for the format block.</span></span> <span data-ttu-id="d1a29-116">Si le paramètre *pmtTarget* contient déjà un bloc de format alloué, une fuite de mémoire se produit.</span><span class="sxs-lookup"><span data-stu-id="d1a29-116">If the *pmtTarget* parameter already contains an allocated format block, a memory leak will occur.</span></span> <span data-ttu-id="d1a29-117">Pour éviter une fuite de mémoire, appelez [**FreeMediaType**](freemediatype.md) avant d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="d1a29-117">To avoid a memory leak, call [**FreeMediaType**](freemediatype.md) before calling this function.</span></span>

<span data-ttu-id="d1a29-118">Une fois la méthode retournée, appelez [**FreeMediaType**](freemediatype.md) sur *pmtTarget* pour libérer le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="d1a29-118">After the method returns, call [**FreeMediaType**](freemediatype.md) on *pmtTarget* to free the format block.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1a29-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1a29-119">Requirements</span></span>



| <span data-ttu-id="d1a29-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1a29-120">Requirement</span></span> | <span data-ttu-id="d1a29-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1a29-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1a29-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1a29-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d1a29-123"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1a29-123"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="d1a29-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d1a29-124">Library</span></span><br/> | <dl> <span data-ttu-id="d1a29-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d1a29-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1a29-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1a29-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1a29-127">**Fonctions de type de média**</span><span class="sxs-lookup"><span data-stu-id="d1a29-127">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

 




