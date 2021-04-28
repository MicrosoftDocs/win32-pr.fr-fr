---
description: 'Méthode CBaseInputPin. GetAllocator : la méthode GetAllocator récupère l’allocateur de mémoire proposé par ce code confidentiel. Cette méthode implémente la méthode IMemInputPin :: GetAllocator.'
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
ms.openlocfilehash: 72aaf6bb4c1ff8bf108086a8a42a618267c4bc06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099708"
---
# <a name="cbaseinputpingetallocator-method"></a><span data-ttu-id="dce17-104">Méthode CBaseInputPin. GetAllocator</span><span class="sxs-lookup"><span data-stu-id="dce17-104">CBaseInputPin.GetAllocator method</span></span>

<span data-ttu-id="dce17-105">La `GetAllocator` méthode récupère l’allocateur de mémoire proposé par ce code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="dce17-105">The `GetAllocator` method retrieves the memory allocator proposed by this pin.</span></span> <span data-ttu-id="dce17-106">Cette méthode implémente la méthode [**IMemInputPin :: GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) .</span><span class="sxs-lookup"><span data-stu-id="dce17-106">This method implements the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dce17-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dce17-107">Syntax</span></span>


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="dce17-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dce17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dce17-109">*ppAllocator*</span><span class="sxs-lookup"><span data-stu-id="dce17-109">*ppAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="dce17-110">Adresse d’une variable qui reçoit un pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="dce17-110">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dce17-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dce17-111">Return value</span></span>

<span data-ttu-id="dce17-112">Retourne S \_ OK en cas de réussite, ou un code d’erreur de la fonction **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="dce17-112">Returns S\_OK if successful, or an error code from the **CoCreateInstance** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="dce17-113">Notes </span><span class="sxs-lookup"><span data-stu-id="dce17-113">Remarks</span></span>

<span data-ttu-id="dce17-114">Cette méthode crée un objet [**CMemAllocator**](cmemallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="dce17-114">This method creates a [**CMemAllocator**](cmemallocator.md) object.</span></span> <span data-ttu-id="dce17-115">Substituez cette méthode si votre filtre utilise un allocateur à partir d’un code confidentiel en aval ou d’un allocateur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="dce17-115">Override this method if your filter uses an allocator from a downstream pin, or a custom allocator.</span></span>

<span data-ttu-id="dce17-116">Si la méthode est réussie, l’interface **IMemAllocator** a un nombre de références en attente.</span><span class="sxs-lookup"><span data-stu-id="dce17-116">If the method succeeds, the **IMemAllocator** interface has an outstanding reference count.</span></span> <span data-ttu-id="dce17-117">Veillez à le libérer lorsque vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="dce17-117">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="dce17-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dce17-118">Requirements</span></span>



| <span data-ttu-id="dce17-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dce17-119">Requirement</span></span> | <span data-ttu-id="dce17-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="dce17-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce17-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="dce17-121">Header</span></span><br/>  | <dl> <span data-ttu-id="dce17-122"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dce17-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dce17-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dce17-123">Library</span></span><br/> | <dl> <span data-ttu-id="dce17-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dce17-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dce17-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dce17-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dce17-126">**CBaseInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="dce17-126">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




