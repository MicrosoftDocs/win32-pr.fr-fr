---
description: La méthode CompleteConnect effectue une connexion à une autre broche.
ms.assetid: 568cee55-b9ea-4fc2-ac9d-0080b7de9790
title: Méthode CTransformInputPin. CompleteConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 455517968481b9333fbeba590aca644b34b2f5be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545504"
---
# <a name="ctransforminputpincompleteconnect-method"></a><span data-ttu-id="0a865-103">Méthode CTransformInputPin. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="0a865-103">CTransformInputPin.CompleteConnect method</span></span>

<span data-ttu-id="0a865-104">La `CompleteConnect` méthode termine une connexion à une autre broche.</span><span class="sxs-lookup"><span data-stu-id="0a865-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a865-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a865-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="0a865-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a865-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a865-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="0a865-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="0a865-108">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de l’autre pin.</span><span class="sxs-lookup"><span data-stu-id="0a865-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a865-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0a865-109">Return value</span></span>

<span data-ttu-id="0a865-110">Retourne S \_ OK ou une autre valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0a865-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a865-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0a865-111">Remarks</span></span>

<span data-ttu-id="0a865-112">Cette méthode remplace la méthode [**CBasePin :: CompleteConnect**](cbasepin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="0a865-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="0a865-113">Elle appelle la méthode [**CTransformFilter :: CompleteConnect**](ctransformfilter-completeconnect.md) du filtre, qui retourne la valeur \_ OK dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="0a865-113">It calls the filter's [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="0a865-114">La classe dérivée peut substituer la méthode **CTransformFilter :: CompleteConnect** pour effectuer des vérifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0a865-114">The derived class can override the **CTransformFilter::CompleteConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a865-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a865-115">Requirements</span></span>



| <span data-ttu-id="0a865-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a865-116">Requirement</span></span> | <span data-ttu-id="0a865-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a865-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a865-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a865-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0a865-119"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a865-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0a865-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0a865-120">Library</span></span><br/> | <dl> <span data-ttu-id="0a865-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0a865-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




