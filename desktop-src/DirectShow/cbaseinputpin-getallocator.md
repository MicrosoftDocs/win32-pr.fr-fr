---
description: 'La méthode GetAllocator récupère l’allocateur de mémoire proposé par ce code confidentiel. Cette méthode implémente la méthode IMemInputPin :: GetAllocator.'
ms.assetid: 07bc77f8-a877-4403-b424-20bda715a818
title: Méthode CBaseInputPin. GetAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 098738fc63ba1834b1eefb4b2518e3309db35c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541046"
---
# <a name="cbaseinputpingetallocator-method"></a><span data-ttu-id="99e4c-104">Méthode CBaseInputPin. GetAllocator</span><span class="sxs-lookup"><span data-stu-id="99e4c-104">CBaseInputPin.GetAllocator method</span></span>

<span data-ttu-id="99e4c-105">La `GetAllocator` méthode récupère l’allocateur de mémoire proposé par ce code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="99e4c-105">The `GetAllocator` method retrieves the memory allocator proposed by this pin.</span></span> <span data-ttu-id="99e4c-106">Cette méthode implémente la méthode [**IMemInputPin :: GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) .</span><span class="sxs-lookup"><span data-stu-id="99e4c-106">This method implements the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="99e4c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99e4c-107">Syntax</span></span>


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="99e4c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99e4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99e4c-109">*ppAllocator*</span><span class="sxs-lookup"><span data-stu-id="99e4c-109">*ppAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="99e4c-110">Adresse d’une variable qui reçoit un pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="99e4c-110">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99e4c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="99e4c-111">Return value</span></span>

<span data-ttu-id="99e4c-112">Retourne S \_ OK en cas de réussite, ou un code d’erreur de la fonction **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="99e4c-112">Returns S\_OK if successful, or an error code from the **CoCreateInstance** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="99e4c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="99e4c-113">Remarks</span></span>

<span data-ttu-id="99e4c-114">Cette méthode crée un objet [**CMemAllocator**](cmemallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="99e4c-114">This method creates a [**CMemAllocator**](cmemallocator.md) object.</span></span> <span data-ttu-id="99e4c-115">Substituez cette méthode si votre filtre utilise un allocateur à partir d’un code confidentiel en aval ou d’un allocateur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="99e4c-115">Override this method if your filter uses an allocator from a downstream pin, or a custom allocator.</span></span>

<span data-ttu-id="99e4c-116">Si la méthode est réussie, l’interface **IMemAllocator** a un nombre de références en attente.</span><span class="sxs-lookup"><span data-stu-id="99e4c-116">If the method succeeds, the **IMemAllocator** interface has an outstanding reference count.</span></span> <span data-ttu-id="99e4c-117">Veillez à le libérer lorsque vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="99e4c-117">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="99e4c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99e4c-118">Requirements</span></span>



| <span data-ttu-id="99e4c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99e4c-119">Requirement</span></span> | <span data-ttu-id="99e4c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="99e4c-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99e4c-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="99e4c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="99e4c-122"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99e4c-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="99e4c-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="99e4c-123">Library</span></span><br/> | <dl> <span data-ttu-id="99e4c-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="99e4c-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99e4c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99e4c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99e4c-126">**CBaseInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="99e4c-126">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




