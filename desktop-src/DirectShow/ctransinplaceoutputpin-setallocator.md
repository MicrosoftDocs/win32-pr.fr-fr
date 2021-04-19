---
description: La méthode SetAllocator spécifie un allocateur pour la connexion.
ms.assetid: 6b8e80f9-3b0d-498f-b1b0-bae491c25e81
title: Méthode CTransInPlaceOutputPin. SetAllocator (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.SetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aacc2680bebcdd7de74f6f357380066a8fd37f1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544078"
---
# <a name="ctransinplaceoutputpinsetallocator-method"></a><span data-ttu-id="65d13-103">Méthode CTransInPlaceOutputPin. SetAllocator</span><span class="sxs-lookup"><span data-stu-id="65d13-103">CTransInPlaceOutputPin.SetAllocator method</span></span>

<span data-ttu-id="65d13-104">La `SetAllocator` méthode spécifie un allocateur pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="65d13-104">The `SetAllocator` method specifies an allocator for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="65d13-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65d13-105">Syntax</span></span>


```C++
void SetAllocator(
   IMemAllocator *pAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="65d13-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65d13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65d13-107">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="65d13-107">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="65d13-108">Pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="65d13-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65d13-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65d13-109">Return value</span></span>

<span data-ttu-id="65d13-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="65d13-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="65d13-111">Notes</span><span class="sxs-lookup"><span data-stu-id="65d13-111">Remarks</span></span>

<span data-ttu-id="65d13-112">La broche de sortie pour ce filtre ne fournit jamais d’allocateur.</span><span class="sxs-lookup"><span data-stu-id="65d13-112">The output pin for this filter never provides an allocator.</span></span> <span data-ttu-id="65d13-113">Cette méthode spécifie l’allocateur pour la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="65d13-113">This method specifies the allocator for the output pin.</span></span> <span data-ttu-id="65d13-114">Elle définit la valeur de la variable membre [**CBaseOutputPin :: m \_ pAllocator**](cbaseoutputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="65d13-114">It sets the value of the [**CBaseOutputPin::m\_pAllocator**](cbaseoutputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="65d13-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65d13-115">Requirements</span></span>



| <span data-ttu-id="65d13-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65d13-116">Requirement</span></span> | <span data-ttu-id="65d13-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="65d13-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65d13-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="65d13-118">Header</span></span><br/>  | <dl> <span data-ttu-id="65d13-119"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65d13-119"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="65d13-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="65d13-120">Library</span></span><br/> | <dl> <span data-ttu-id="65d13-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="65d13-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65d13-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65d13-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65d13-123">**CTransInPlaceOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="65d13-123">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




