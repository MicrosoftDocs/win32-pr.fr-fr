---
description: La méthode CreateDIB crée une image bitmap indépendante du périphérique (DIB) GDI. Le DIB est alloué dans un bloc mempory partagé, ce qui élimine une opération de copie lorsque le filtre propriétaire BLITS l’image.
ms.assetid: 8a9ab1cf-4104-48e9-ba6c-28d0f1a1d226
title: Méthode CImageAllocator. CreateDIB (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateDIB
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 316b7aeadfa442a8df4e80075380464758f3c6bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526752"
---
# <a name="cimageallocatorcreatedib-method"></a><span data-ttu-id="2f0f5-104">Méthode CImageAllocator. CreateDIB</span><span class="sxs-lookup"><span data-stu-id="2f0f5-104">CImageAllocator.CreateDIB method</span></span>

<span data-ttu-id="2f0f5-105">La `CreateDIB` méthode crée une image bitmap indépendante du périphérique (DIB) GDI.</span><span class="sxs-lookup"><span data-stu-id="2f0f5-105">The `CreateDIB` method creates a GDI device-independent bitmap (DIB).</span></span> <span data-ttu-id="2f0f5-106">Le DIB est alloué dans un bloc mempory partagé, ce qui élimine une opération de copie lorsque le filtre propriétaire BLITS l’image.</span><span class="sxs-lookup"><span data-stu-id="2f0f5-106">The DIB is allocated in a shared mempory block, which eliminates a copy operation when the owning filter blits the image.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f0f5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f0f5-107">Syntax</span></span>


```C++
HRESULT CreateDIB(
        LONG    InSize,
  [ref] DIBDATA &DibData
);
```



## <a name="parameters"></a><span data-ttu-id="2f0f5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f0f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f0f5-109">*InSIZE*</span><span class="sxs-lookup"><span data-stu-id="2f0f5-109">*InSize*</span></span> 
</dt> <dd>

<span data-ttu-id="2f0f5-110">Taille de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="2f0f5-110">Size of the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="2f0f5-111">*DibData* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="2f0f5-111">*DibData* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="2f0f5-112">Référence à une structure [**DIBDATA**](dibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="2f0f5-112">Reference to a [**DIBDATA**](dibdata.md) structure.</span></span> <span data-ttu-id="2f0f5-113">La méthode remplit cette structure avec des informations sur le DIB.</span><span class="sxs-lookup"><span data-stu-id="2f0f5-113">The method fills in this structure with information about the DIB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f0f5-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f0f5-114">Return value</span></span>

<span data-ttu-id="2f0f5-115">Retourne S \_ OK en cas de réussite, ou un code d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2f0f5-115">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f0f5-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f0f5-116">Requirements</span></span>



| <span data-ttu-id="2f0f5-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f0f5-117">Requirement</span></span> | <span data-ttu-id="2f0f5-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f0f5-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f0f5-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f0f5-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2f0f5-120"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f0f5-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2f0f5-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2f0f5-121">Library</span></span><br/> | <dl> <span data-ttu-id="2f0f5-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2f0f5-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f0f5-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f0f5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f0f5-124">**CImageAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="2f0f5-124">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> <dt>

[<span data-ttu-id="2f0f5-125">**CImageAllocator :: Alloc**</span><span class="sxs-lookup"><span data-stu-id="2f0f5-125">**CImageAllocator::Alloc**</span></span>](cimageallocator-alloc.md)
</dt> </dl>

 

 




