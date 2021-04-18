---
description: La méthode CreateImageSample crée un exemple de support.
ms.assetid: dae71692-5cbc-4bc7-a363-41766ef17c58
title: Méthode CImageAllocator. CreateImageSample (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57463a7025ea816b6fe6bcaa8b964231458903de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526551"
---
# <a name="cimageallocatorcreateimagesample-method"></a><span data-ttu-id="dc24b-103">Méthode CImageAllocator. CreateImageSample</span><span class="sxs-lookup"><span data-stu-id="dc24b-103">CImageAllocator.CreateImageSample method</span></span>

<span data-ttu-id="dc24b-104">La `CreateImageSample` méthode crée un exemple de support.</span><span class="sxs-lookup"><span data-stu-id="dc24b-104">The `CreateImageSample` method creates a media sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc24b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc24b-105">Syntax</span></span>


```C++
virtual CImageSample* CreateImageSample(
   LPBYTE pData,
   LONG   Length
);
```



## <a name="parameters"></a><span data-ttu-id="dc24b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc24b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc24b-107">*pData*</span><span class="sxs-lookup"><span data-stu-id="dc24b-107">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="dc24b-108">Pointeur vers une mémoire tampon de *longueur* de taille, alloué par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="dc24b-108">Pointer to a buffer of size *Length*, allocated by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="dc24b-109">*Durée*</span><span class="sxs-lookup"><span data-stu-id="dc24b-109">*Length*</span></span> 
</dt> <dd>

<span data-ttu-id="dc24b-110">Longueur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="dc24b-110">Length of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc24b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dc24b-111">Return value</span></span>

<span data-ttu-id="dc24b-112">Retourne un objet [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="dc24b-112">Returns a [**CImageSample**](cimagesample.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc24b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="dc24b-113">Remarks</span></span>

<span data-ttu-id="dc24b-114">Cette méthode crée un nouvel exemple de support, implémenté comme un objet **CImageSample** .</span><span class="sxs-lookup"><span data-stu-id="dc24b-114">This method creates a new media sample, implemented as a **CImageSample** object.</span></span> <span data-ttu-id="dc24b-115">La méthode [**IMediaSample :: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) de l’exemple retourne un pointeur vers la mémoire tampon spécifiée dans le paramètre *pData* .</span><span class="sxs-lookup"><span data-stu-id="dc24b-115">The sample's [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) method returns a pointer to the buffer specified in the *pData* parameter.</span></span>

<span data-ttu-id="dc24b-116">Si vous dérivez une nouvelle classe Allocator de [**CImageAllocator**](cimageallocator.md) et un nouvel exemple de classe de support à partir de [**CImageSample**](cimagesample.md), vous devez substituer cette méthode pour créer une instance de votre classe d’exemple de support.</span><span class="sxs-lookup"><span data-stu-id="dc24b-116">If you derive a new allocator class from [**CImageAllocator**](cimageallocator.md) and a new media sample class from [**CImageSample**](cimagesample.md), you should override this method to create an instance of your media sample class.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc24b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc24b-117">Requirements</span></span>



| <span data-ttu-id="dc24b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc24b-118">Requirement</span></span> | <span data-ttu-id="dc24b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc24b-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc24b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc24b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="dc24b-121"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc24b-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dc24b-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dc24b-122">Library</span></span><br/> | <dl> <span data-ttu-id="dc24b-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dc24b-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc24b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc24b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc24b-125">**CImageAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="dc24b-125">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> <dt>

[<span data-ttu-id="dc24b-126">**CImageAllocator :: Alloc**</span><span class="sxs-lookup"><span data-stu-id="dc24b-126">**CImageAllocator::Alloc**</span></span>](cimageallocator-alloc.md)
</dt> </dl>

 

 




