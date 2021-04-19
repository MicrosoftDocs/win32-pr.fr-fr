---
description: Méthode de constructeur.
ms.assetid: d7550c38-d728-41b2-80a6-20728abf6012
title: Constructeur CImageSample. CImageSample (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 805be59cfc899b6461fa8c761eebb5821118640f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540179"
---
# <a name="cimagesamplecimagesample-constructor"></a><span data-ttu-id="c0ea8-103">Constructeur CImageSample. CImageSample</span><span class="sxs-lookup"><span data-stu-id="c0ea8-103">CImageSample.CImageSample constructor</span></span>

<span data-ttu-id="c0ea8-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="c0ea8-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0ea8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0ea8-105">Syntax</span></span>


```C++
CImageSample(
   CBaseAllocator *pAllocator,
   TCHAR          *pName,
   HRESULT        *phr,
   LPBYTE         pBuffer,
   LONG           length
);
```



## <a name="parameters"></a><span data-ttu-id="c0ea8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0ea8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0ea8-107">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="c0ea8-107">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="c0ea8-108">Pointeur vers l’allocateur qui a créé cet exemple.</span><span class="sxs-lookup"><span data-stu-id="c0ea8-108">Pointer to the allocator that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="c0ea8-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="c0ea8-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="c0ea8-110">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="c0ea8-110">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="c0ea8-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="c0ea8-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="c0ea8-112">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="c0ea8-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="c0ea8-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="c0ea8-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="c0ea8-114">Pointeur vers une mémoire tampon allouée par l’appelant, de la *longueur* de la taille.</span><span class="sxs-lookup"><span data-stu-id="c0ea8-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span> <span data-ttu-id="c0ea8-115">La mémoire tampon doit contenir une image bitmap indépendante du périphérique (DIB) GDI.</span><span class="sxs-lookup"><span data-stu-id="c0ea8-115">The buffer should contain a GDI device-independent bitmap (DIB).</span></span>

</dd> <dt>

<span data-ttu-id="c0ea8-116">*length*</span><span class="sxs-lookup"><span data-stu-id="c0ea8-116">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="c0ea8-117">Longueur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c0ea8-117">Length of the buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0ea8-118">Notes</span><span class="sxs-lookup"><span data-stu-id="c0ea8-118">Remarks</span></span>

<span data-ttu-id="c0ea8-119">La classe [**CImageAllocator**](cimageallocator.md) crée un DIB à l’aide d’un objet de mappage de fichiers qui est sauvegardé par le fichier de pagination du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="c0ea8-119">The [**CImageAllocator**](cimageallocator.md) class creates a DIB using a file-mapping object that is backed by the operating-system paging file.</span></span> <span data-ttu-id="c0ea8-120">Le descripteur de l’objet de mappage de fichier est stocké dans le membre **hMapping** de la structure **m \_ DibData** .</span><span class="sxs-lookup"><span data-stu-id="c0ea8-120">The handle to the file-mapping object is stored in the **hMapping** member of the **m\_DibData** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0ea8-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0ea8-121">Requirements</span></span>



| <span data-ttu-id="c0ea8-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0ea8-122">Requirement</span></span> | <span data-ttu-id="c0ea8-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0ea8-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0ea8-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0ea8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c0ea8-125"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0ea8-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c0ea8-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c0ea8-126">Library</span></span><br/> | <dl> <span data-ttu-id="c0ea8-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c0ea8-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0ea8-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0ea8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0ea8-129">**CImageSample, classe**</span><span class="sxs-lookup"><span data-stu-id="c0ea8-129">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




