---
description: La méthode SetPoint définit le pointeur sur la mémoire tampon.
ms.assetid: 60627600-c982-462e-b540-327a58e57615
title: Méthode CMediaSample. SetPoint (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67d9fc5d260cc627919a458593328c36f0de9a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544072"
---
# <a name="cmediasamplesetpointer-method"></a><span data-ttu-id="243cf-103">CMediaSample. SetPoint, méthode</span><span class="sxs-lookup"><span data-stu-id="243cf-103">CMediaSample.SetPointer method</span></span>

<span data-ttu-id="243cf-104">La `SetPointer` méthode définit le pointeur sur la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="243cf-104">The `SetPointer` method sets the pointer to the memory buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="243cf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="243cf-105">Syntax</span></span>


```C++
HRESULT SetPointer(
   BYTE *ptr,
   LONG cBytes
);
```



## <a name="parameters"></a><span data-ttu-id="243cf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="243cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="243cf-107">*ptr*</span><span class="sxs-lookup"><span data-stu-id="243cf-107">*ptr*</span></span> 
</dt> <dd>

<span data-ttu-id="243cf-108">Pointeur vers une mémoire tampon allouée par l’appelant, de taille *cBytes*.</span><span class="sxs-lookup"><span data-stu-id="243cf-108">Pointer to a memory buffer allocated by the caller, of size *cBytes*.</span></span>

</dd> <dt>

<span data-ttu-id="243cf-109">*cBytes*</span><span class="sxs-lookup"><span data-stu-id="243cf-109">*cBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="243cf-110">Longueur de la mémoire tampon, en octets.</span><span class="sxs-lookup"><span data-stu-id="243cf-110">Length of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="243cf-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="243cf-111">Return value</span></span>

<span data-ttu-id="243cf-112">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="243cf-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="243cf-113">Notes</span><span class="sxs-lookup"><span data-stu-id="243cf-113">Remarks</span></span>

<span data-ttu-id="243cf-114">Cette méthode permet à l’allocateur de définir un nouveau pointeur pour l’exemple.</span><span class="sxs-lookup"><span data-stu-id="243cf-114">This method enables the allocator to set a new pointer for the sample.</span></span>

<span data-ttu-id="243cf-115">Cette méthode n’est pas disponible par le biais de l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .</span><span class="sxs-lookup"><span data-stu-id="243cf-115">This method is not available through the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="243cf-116">L’objet qui crée l’exemple peut accéder à cette méthode (via **CMediaSample**), mais les autres objets ne le peuvent pas.</span><span class="sxs-lookup"><span data-stu-id="243cf-116">The object that creates the sample can access this method (through **CMediaSample**), but other objects cannot.</span></span>

## <a name="requirements"></a><span data-ttu-id="243cf-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="243cf-117">Requirements</span></span>



| <span data-ttu-id="243cf-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="243cf-118">Requirement</span></span> | <span data-ttu-id="243cf-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="243cf-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="243cf-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="243cf-120">Header</span></span><br/>  | <dl> <span data-ttu-id="243cf-121"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="243cf-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="243cf-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="243cf-122">Library</span></span><br/> | <dl> <span data-ttu-id="243cf-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="243cf-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="243cf-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="243cf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="243cf-125">**CMediaSample, classe**</span><span class="sxs-lookup"><span data-stu-id="243cf-125">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




