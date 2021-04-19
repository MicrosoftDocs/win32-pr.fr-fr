---
description: La méthode BreakConnect libère le code confidentiel d’une connexion.
ms.assetid: bf68aca3-93e5-4f9d-9980-1a5eed1513f5
title: Méthode CTransformOutputPin. BreakConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 316806b89adf6493f32125da488990151f0916b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532860"
---
# <a name="ctransformoutputpinbreakconnect-method"></a><span data-ttu-id="7619f-103">Méthode CTransformOutputPin. BreakConnect</span><span class="sxs-lookup"><span data-stu-id="7619f-103">CTransformOutputPin.BreakConnect method</span></span>

<span data-ttu-id="7619f-104">La `BreakConnect` méthode libère le code confidentiel d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="7619f-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7619f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7619f-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="7619f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7619f-106">Parameters</span></span>

<span data-ttu-id="7619f-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7619f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7619f-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7619f-108">Return value</span></span>

<span data-ttu-id="7619f-109">Retourne S \_ OK ou une autre valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7619f-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7619f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7619f-110">Remarks</span></span>

<span data-ttu-id="7619f-111">Cette méthode remplace la méthode [**CBaseOutputPin :: BreakConnect**](cbaseoutputpin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="7619f-111">This method overrides the [**CBaseOutputPin::BreakConnect**](cbaseoutputpin-breakconnect.md) method.</span></span> <span data-ttu-id="7619f-112">Elle appelle la méthode [**CTransformFilter :: BreakConnect**](ctransformfilter-breakconnect.md) du filtre, qui retourne la valeur \_ OK dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="7619f-112">It calls the filter's [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="7619f-113">La classe dérivée peut substituer la méthode **CTransformFilter :: BreakConnect** .</span><span class="sxs-lookup"><span data-stu-id="7619f-113">The derived class can override the **CTransformFilter::BreakConnect** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7619f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7619f-114">Requirements</span></span>



| <span data-ttu-id="7619f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7619f-115">Requirement</span></span> | <span data-ttu-id="7619f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7619f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7619f-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="7619f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7619f-118"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7619f-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7619f-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7619f-119">Library</span></span><br/> | <dl> <span data-ttu-id="7619f-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7619f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




