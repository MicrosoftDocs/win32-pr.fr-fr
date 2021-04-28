---
description: 'Méthode CBaseOutputPin. EndFlush : la méthode EndFlush termine une opération de vidage. Cette méthode implémente la méthode IPin :: EndFlush.'
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
ms.openlocfilehash: 53153c6dbd941390c7ef616ee36c56e01214c341
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099507"
---
# <a name="cbaseoutputpinendflush-method"></a><span data-ttu-id="74306-104">Méthode CBaseOutputPin. EndFlush</span><span class="sxs-lookup"><span data-stu-id="74306-104">CBaseOutputPin.EndFlush method</span></span>

<span data-ttu-id="74306-105">La `EndFlush` méthode termine une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="74306-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="74306-106">Cette méthode implémente la méthode [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="74306-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="74306-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74306-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="74306-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74306-108">Parameters</span></span>

<span data-ttu-id="74306-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="74306-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="74306-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="74306-110">Return value</span></span>

<span data-ttu-id="74306-111">Retourne E \_ inattendu.</span><span class="sxs-lookup"><span data-stu-id="74306-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="74306-112">Notes </span><span class="sxs-lookup"><span data-stu-id="74306-112">Remarks</span></span>

<span data-ttu-id="74306-113">Cette méthode doit uniquement être appelée sur les broches d’entrée, de sorte que l’implémentation de **CBaseOutputPin** retourne E \_ inattendue.</span><span class="sxs-lookup"><span data-stu-id="74306-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="74306-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74306-114">Requirements</span></span>



| <span data-ttu-id="74306-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74306-115">Requirement</span></span> | <span data-ttu-id="74306-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="74306-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74306-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="74306-117">Header</span></span><br/>  | <dl> <span data-ttu-id="74306-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74306-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="74306-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="74306-119">Library</span></span><br/> | <dl> <span data-ttu-id="74306-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="74306-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74306-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74306-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74306-122">**CBaseOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="74306-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




