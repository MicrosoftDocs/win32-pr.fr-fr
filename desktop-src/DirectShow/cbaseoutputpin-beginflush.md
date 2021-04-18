---
description: 'La méthode BeginFlush commence une opération de vidage. Implémente la méthode IPin :: BeginFlush.'
ms.assetid: f16c8337-5b7f-47e8-810d-00ffb3b5a1b4
title: Méthode CBaseOutputPin. BeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0216f74094d0c024d9b354dc594ff8d65315efbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526546"
---
# <a name="cbaseoutputpinbeginflush-method"></a><span data-ttu-id="e4b77-104">Méthode CBaseOutputPin. BeginFlush</span><span class="sxs-lookup"><span data-stu-id="e4b77-104">CBaseOutputPin.BeginFlush method</span></span>

<span data-ttu-id="e4b77-105">La `BeginFlush` méthode commence une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="e4b77-105">The `BeginFlush` method begins a flush operation.</span></span> <span data-ttu-id="e4b77-106">Implémente la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="e4b77-106">Implements the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4b77-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4b77-107">Syntax</span></span>


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="e4b77-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4b77-108">Parameters</span></span>

<span data-ttu-id="e4b77-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e4b77-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e4b77-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e4b77-110">Return value</span></span>

<span data-ttu-id="e4b77-111">Retourne E \_ inattendu.</span><span class="sxs-lookup"><span data-stu-id="e4b77-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4b77-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e4b77-112">Remarks</span></span>

<span data-ttu-id="e4b77-113">Cette méthode doit uniquement être appelée sur les broches d’entrée, de sorte que l’implémentation de **CBaseOutputPin** retourne E \_ inattendue.</span><span class="sxs-lookup"><span data-stu-id="e4b77-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4b77-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4b77-114">Requirements</span></span>



| <span data-ttu-id="e4b77-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4b77-115">Requirement</span></span> | <span data-ttu-id="e4b77-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4b77-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b77-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4b77-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e4b77-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4b77-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e4b77-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e4b77-119">Library</span></span><br/> | <dl> <span data-ttu-id="e4b77-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e4b77-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4b77-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4b77-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4b77-122">**CBaseOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="e4b77-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




