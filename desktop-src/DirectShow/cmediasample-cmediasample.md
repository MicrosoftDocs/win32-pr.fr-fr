---
description: Méthode constructeur CMediaSample. CMediaSample.
ms.assetid: 3ee67cfd-a968-4b7c-9c7b-1c28ddb9c343
title: Constructeur CMediaSample. CMediaSample (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.CMediaSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd2601b9f53e8f79d9231dd34054932bec4e671
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095437"
---
# <a name="cmediasamplecmediasample-constructor"></a><span data-ttu-id="f4cac-103">Constructeur CMediaSample. CMediaSample</span><span class="sxs-lookup"><span data-stu-id="f4cac-103">CMediaSample.CMediaSample constructor</span></span>

<span data-ttu-id="f4cac-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="f4cac-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4cac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4cac-105">Syntax</span></span>


```C++
CMediaSample(
   TCHAR          *pName,
   CBaseAllocator *pAllocator,
   HRESULT        *phr,
   LPBYTE         pBuffer = NULL,
   LONG           length = 0
);
```



## <a name="parameters"></a><span data-ttu-id="f4cac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4cac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4cac-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="f4cac-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="f4cac-108">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="f4cac-108">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="f4cac-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="f4cac-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="f4cac-110">Pointeur vers l’objet [**CBaseAllocator**](cbaseallocator.md) qui a créé cet exemple.</span><span class="sxs-lookup"><span data-stu-id="f4cac-110">Pointer to the [**CBaseAllocator**](cbaseallocator.md) object that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="f4cac-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="f4cac-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="f4cac-112">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="f4cac-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="f4cac-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="f4cac-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="f4cac-114">Pointeur vers une mémoire tampon allouée par l’appelant, de la *longueur* de la taille.</span><span class="sxs-lookup"><span data-stu-id="f4cac-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span>

</dd> <dt>

<span data-ttu-id="f4cac-115">*length*</span><span class="sxs-lookup"><span data-stu-id="f4cac-115">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="f4cac-116">Longueur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="f4cac-116">Length of the memory buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4cac-117">Notes </span><span class="sxs-lookup"><span data-stu-id="f4cac-117">Remarks</span></span>

<span data-ttu-id="f4cac-118">La classe de base ne modifie pas la valeur **HRESULT** transmise dans le paramètre *PHR* .</span><span class="sxs-lookup"><span data-stu-id="f4cac-118">The base class does not modify the **HRESULT** value passed in the *phr* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4cac-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4cac-119">Requirements</span></span>



| <span data-ttu-id="f4cac-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4cac-120">Requirement</span></span> | <span data-ttu-id="f4cac-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4cac-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4cac-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="f4cac-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f4cac-123"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4cac-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f4cac-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f4cac-124">Library</span></span><br/> | <dl> <span data-ttu-id="f4cac-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f4cac-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4cac-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4cac-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4cac-127">**CMediaSample, classe**</span><span class="sxs-lookup"><span data-stu-id="f4cac-127">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




