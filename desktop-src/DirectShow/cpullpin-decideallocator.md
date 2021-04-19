---
description: La méthode DecideAllocator négocie un allocateur avec la broche de sortie.
ms.assetid: 5c04f440-b177-4caa-989f-3aa783c4b348
title: Méthode CPullPin. DecideAllocator (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91ffa139b916b1594e0729a0f8d52f07c62eda12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542696"
---
# <a name="cpullpindecideallocator-method"></a><span data-ttu-id="8c752-103">Méthode CPullPin. DecideAllocator</span><span class="sxs-lookup"><span data-stu-id="8c752-103">CPullPin.DecideAllocator method</span></span>

<span data-ttu-id="8c752-104">La `DecideAllocator` méthode négocie un allocateur avec la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="8c752-104">The `DecideAllocator` method negotiates an allocator with the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c752-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c752-105">Syntax</span></span>


```C++
virtual HRESULT DecideAllocator(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="8c752-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c752-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c752-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="8c752-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="8c752-108">Pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur préféré du code confidentiel d’entrée, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="8c752-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface of the input pin's preferred allocator, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8c752-109">*pProps*</span><span class="sxs-lookup"><span data-stu-id="8c752-109">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="8c752-110">Pointeur vers une structure de [**\_ propriétés d’Allocator**](/windows/win32/api/strmif/ns-strmif-allocator_properties) facultative qui contient les exigences de mémoire tampon du code confidentiel d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8c752-110">Pointer to an optional [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c752-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c752-111">Return value</span></span>

<span data-ttu-id="8c752-112">Retourne S \_ OK en cas de réussite, ou un code d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8c752-112">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c752-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8c752-113">Remarks</span></span>

<span data-ttu-id="8c752-114">Cette méthode appelle la méthode [**IAsyncReader :: RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) pour négocier un allocateur.</span><span class="sxs-lookup"><span data-stu-id="8c752-114">This method calls the [**IAsyncReader::RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) method to negotiate an allocator.</span></span> <span data-ttu-id="8c752-115">Elle transmet le paramètre *pAlloc* directement à la méthode **RequestAllocator** .</span><span class="sxs-lookup"><span data-stu-id="8c752-115">It passes the *pAlloc* parameter directly to the **RequestAllocator** method.</span></span> <span data-ttu-id="8c752-116">Elle transmet le paramètre *pProps* à **RequestAllocator** si *pProps* n’est pas **null**; dans le cas contraire, elle crée une structure de **\_ Propriétés Allocator** avec une requête par défaut de trois tampons de 64 Ko.</span><span class="sxs-lookup"><span data-stu-id="8c752-116">It passes the *pProps* parameter to **RequestAllocator** if *pProps* is non-**NULL**; otherwise, it creates an **ALLOCATOR\_PROPERTIES** structure with a default request of three 64K buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c752-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c752-117">Requirements</span></span>



| <span data-ttu-id="8c752-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c752-118">Requirement</span></span> | <span data-ttu-id="8c752-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c752-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c752-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c752-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8c752-121"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c752-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="8c752-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8c752-122">Library</span></span><br/> | <dl> <span data-ttu-id="8c752-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8c752-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c752-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c752-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c752-125">**CPullPin, classe**</span><span class="sxs-lookup"><span data-stu-id="8c752-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> <dt>

[<span data-ttu-id="8c752-126">**CPullPin :: Connect**</span><span class="sxs-lookup"><span data-stu-id="8c752-126">**CPullPin::Connect**</span></span>](cpullpin-connect.md)
</dt> </dl>

 

 




