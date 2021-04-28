---
description: 'Méthode CBaseOutputPin. EndOfStream : la méthode EndOfStream indique au code confidentiel qu’aucune donnée supplémentaire n’est attendue. Cette méthode implémente la méthode IPin :: EndOfStream.'
ms.assetid: 5c3b5f90-4194-4d65-9f1a-55edf327e3b3
title: Méthode CBaseOutputPin. EndOfStream (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c5f293b8026456618ad1196c491bce58cf481f07
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096147"
---
# <a name="cbaseoutputpinendofstream-method"></a><span data-ttu-id="0d694-104">Méthode CBaseOutputPin. EndOfStream</span><span class="sxs-lookup"><span data-stu-id="0d694-104">CBaseOutputPin.EndOfStream method</span></span>

<span data-ttu-id="0d694-105">La `EndOfStream` méthode indique au code confidentiel qu’aucune donnée supplémentaire n’est attendue.</span><span class="sxs-lookup"><span data-stu-id="0d694-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="0d694-106">Cette méthode implémente la méthode [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="0d694-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d694-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d694-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="0d694-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d694-108">Parameters</span></span>

<span data-ttu-id="0d694-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0d694-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0d694-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0d694-110">Return value</span></span>

<span data-ttu-id="0d694-111">Retourne E \_ inattendu.</span><span class="sxs-lookup"><span data-stu-id="0d694-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d694-112">Notes </span><span class="sxs-lookup"><span data-stu-id="0d694-112">Remarks</span></span>

<span data-ttu-id="0d694-113">Cette méthode doit uniquement être appelée sur les broches d’entrée, de sorte que l’implémentation de **CBaseOutputPin** retourne E \_ inattendue.</span><span class="sxs-lookup"><span data-stu-id="0d694-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d694-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d694-114">Requirements</span></span>



| <span data-ttu-id="0d694-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d694-115">Requirement</span></span> | <span data-ttu-id="0d694-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d694-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d694-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d694-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0d694-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d694-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0d694-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0d694-119">Library</span></span><br/> | <dl> <span data-ttu-id="0d694-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0d694-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d694-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d694-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d694-122">**CBaseOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="0d694-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




