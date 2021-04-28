---
description: 'Méthode CTransformOutputPin. CompleteConnect : la méthode CompleteConnect effectue une connexion à une autre broche.'
ms.assetid: 14bc48bc-ddfb-4491-8d5b-9e5ac601ba04
title: Méthode CTransformOutputPin. CompleteConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ab3d7e56473094b31c0d97d0e15c083ff61a21d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094917"
---
# <a name="ctransformoutputpincompleteconnect-method"></a><span data-ttu-id="68d7e-103">Méthode CTransformOutputPin. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="68d7e-103">CTransformOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="68d7e-104">La `CompleteConnect` méthode termine une connexion à une autre broche.</span><span class="sxs-lookup"><span data-stu-id="68d7e-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="68d7e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68d7e-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="68d7e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68d7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68d7e-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="68d7e-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="68d7e-108">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de l’autre pin.</span><span class="sxs-lookup"><span data-stu-id="68d7e-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68d7e-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="68d7e-109">Return value</span></span>

<span data-ttu-id="68d7e-110">Retourne S \_ OK ou une autre valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="68d7e-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68d7e-111">Notes </span><span class="sxs-lookup"><span data-stu-id="68d7e-111">Remarks</span></span>

<span data-ttu-id="68d7e-112">Cette méthode remplace la méthode [**CBaseOutputPin :: CompleteConnect**](cbaseoutputpin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="68d7e-112">This method overrides the [**CBaseOutputPin::CompleteConnect**](cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="68d7e-113">Elle appelle la méthode [**CTransformFilter :: CompleteConnect**](ctransformfilter-completeconnect.md) du filtre, qui retourne la valeur \_ OK dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="68d7e-113">It calls the filter's [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="68d7e-114">La classe dérivée peut substituer la méthode **CTransformFilter :: CompleteConnect** pour effectuer des vérifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="68d7e-114">The derived class can override the **CTransformFilter::CompleteConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="68d7e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68d7e-115">Requirements</span></span>



| <span data-ttu-id="68d7e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68d7e-116">Requirement</span></span> | <span data-ttu-id="68d7e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="68d7e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68d7e-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="68d7e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="68d7e-119"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="68d7e-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="68d7e-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="68d7e-120">Library</span></span><br/> | <dl> <span data-ttu-id="68d7e-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="68d7e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




