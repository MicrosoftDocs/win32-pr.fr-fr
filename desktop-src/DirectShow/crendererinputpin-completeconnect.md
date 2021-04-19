---
description: 'La méthode CompleteConnect effectue une connexion à une broche de sortie. Cette méthode remplace la méthode CBasePin :: CompleteConnect.'
ms.assetid: 32d95815-e018-4724-8cf3-8cd093ede517
title: Méthode CRendererInputPin. CompleteConnect (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e868693308d40fb786f201a9d7f056dd88326ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543951"
---
# <a name="crendererinputpincompleteconnect-method"></a><span data-ttu-id="85124-104">Méthode CRendererInputPin. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="85124-104">CRendererInputPin.CompleteConnect method</span></span>

<span data-ttu-id="85124-105">La `CompleteConnect` méthode termine une connexion à une broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="85124-105">The `CompleteConnect` method completes a connection to an output pin.</span></span> <span data-ttu-id="85124-106">Cette méthode remplace la méthode [**CBasePin :: CompleteConnect**](cbasepin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="85124-106">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="85124-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85124-107">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="85124-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85124-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85124-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="85124-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="85124-110">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de la broche de sortie</span><span class="sxs-lookup"><span data-stu-id="85124-110">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85124-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="85124-111">Return value</span></span>

<span data-ttu-id="85124-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="85124-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="85124-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85124-113">Requirements</span></span>



| <span data-ttu-id="85124-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85124-114">Requirement</span></span> | <span data-ttu-id="85124-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="85124-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85124-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="85124-116">Header</span></span><br/>  | <dl> <span data-ttu-id="85124-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85124-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="85124-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="85124-118">Library</span></span><br/> | <dl> <span data-ttu-id="85124-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="85124-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85124-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85124-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85124-121">**CRendererInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="85124-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




