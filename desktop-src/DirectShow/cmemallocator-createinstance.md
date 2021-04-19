---
description: La méthode CreateInstance crée une nouvelle instance de la classe CMemAllocator.
ms.assetid: 87a831a4-2414-4240-8448-c5d90f130470
title: Méthode CMemAllocator. CreateInstance (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ef85de95db74e8a9d7aa6a7b1ba977620a29826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537976"
---
# <a name="cmemallocatorcreateinstance-method"></a><span data-ttu-id="0fc23-103">CMemAllocator. CreateInstance, méthode</span><span class="sxs-lookup"><span data-stu-id="0fc23-103">CMemAllocator.CreateInstance method</span></span>

<span data-ttu-id="0fc23-104">La `CreateInstance` méthode crée une nouvelle instance de la classe **CMemAllocator** .</span><span class="sxs-lookup"><span data-stu-id="0fc23-104">The `CreateInstance` method creates a new instance of the **CMemAllocator** class.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fc23-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0fc23-105">Syntax</span></span>


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="0fc23-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0fc23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fc23-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="0fc23-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="0fc23-108">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="0fc23-108">Pointer to the owner of this object.</span></span> <span data-ttu-id="0fc23-109">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="0fc23-109">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="0fc23-110">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="0fc23-110">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0fc23-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="0fc23-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="0fc23-112">Pointeur vers une variable qui reçoit une valeur **HRESULT** indiquant la réussite ou l’échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="0fc23-112">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fc23-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0fc23-113">Return value</span></span>

<span data-ttu-id="0fc23-114">Retourne un pointeur vers un nouvel objet **CMemAllocator** , typé en tant qu’objet **CUnknown** .</span><span class="sxs-lookup"><span data-stu-id="0fc23-114">Returns a pointer to a new **CMemAllocator** object, typed as a **CUnknown** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fc23-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0fc23-115">Requirements</span></span>



| <span data-ttu-id="0fc23-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0fc23-116">Requirement</span></span> | <span data-ttu-id="0fc23-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="0fc23-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fc23-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="0fc23-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0fc23-119"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0fc23-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0fc23-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0fc23-120">Library</span></span><br/> | <dl> <span data-ttu-id="0fc23-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0fc23-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fc23-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fc23-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fc23-123">**CMemAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="0fc23-123">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




