---
description: 'La méthode EndFlush termine une opération de vidage. Cette méthode implémente la méthode IPin :: EndFlush.'
ms.assetid: c5c76cf8-1ca1-4fef-8776-7f4dcca32939
title: Méthode CBaseOutputPin. EndFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b40bc7db4e8d290ae0cd7e26a9d751e44b0daa4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537639"
---
# <a name="cbaseoutputpinendflush-method"></a><span data-ttu-id="65459-104">Méthode CBaseOutputPin. EndFlush</span><span class="sxs-lookup"><span data-stu-id="65459-104">CBaseOutputPin.EndFlush method</span></span>

<span data-ttu-id="65459-105">La `EndFlush` méthode termine une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="65459-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="65459-106">Cette méthode implémente la méthode [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="65459-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="65459-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65459-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="65459-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65459-108">Parameters</span></span>

<span data-ttu-id="65459-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="65459-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="65459-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65459-110">Return value</span></span>

<span data-ttu-id="65459-111">Retourne E \_ inattendu.</span><span class="sxs-lookup"><span data-stu-id="65459-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="65459-112">Notes</span><span class="sxs-lookup"><span data-stu-id="65459-112">Remarks</span></span>

<span data-ttu-id="65459-113">Cette méthode doit uniquement être appelée sur les broches d’entrée, de sorte que l’implémentation de **CBaseOutputPin** retourne E \_ inattendue.</span><span class="sxs-lookup"><span data-stu-id="65459-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="65459-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65459-114">Requirements</span></span>



| <span data-ttu-id="65459-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65459-115">Requirement</span></span> | <span data-ttu-id="65459-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="65459-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65459-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="65459-117">Header</span></span><br/>  | <dl> <span data-ttu-id="65459-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65459-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="65459-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="65459-119">Library</span></span><br/> | <dl> <span data-ttu-id="65459-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="65459-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65459-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65459-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65459-122">**CBaseOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="65459-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




