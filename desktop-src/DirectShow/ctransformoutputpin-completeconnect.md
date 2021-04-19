---
description: La méthode CompleteConnect effectue une connexion à une autre broche.
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
ms.openlocfilehash: 8d0c9c9fc7096191d7cdedffa21e2639fa0750ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538014"
---
# <a name="ctransformoutputpincompleteconnect-method"></a><span data-ttu-id="0fdc3-103">Méthode CTransformOutputPin. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="0fdc3-103">CTransformOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="0fdc3-104">La `CompleteConnect` méthode termine une connexion à une autre broche.</span><span class="sxs-lookup"><span data-stu-id="0fdc3-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fdc3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0fdc3-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="0fdc3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0fdc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fdc3-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="0fdc3-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="0fdc3-108">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de l’autre pin.</span><span class="sxs-lookup"><span data-stu-id="0fdc3-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fdc3-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0fdc3-109">Return value</span></span>

<span data-ttu-id="0fdc3-110">Retourne S \_ OK ou une autre valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0fdc3-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fdc3-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0fdc3-111">Remarks</span></span>

<span data-ttu-id="0fdc3-112">Cette méthode remplace la méthode [**CBaseOutputPin :: CompleteConnect**](cbaseoutputpin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="0fdc3-112">This method overrides the [**CBaseOutputPin::CompleteConnect**](cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="0fdc3-113">Elle appelle la méthode [**CTransformFilter :: CompleteConnect**](ctransformfilter-completeconnect.md) du filtre, qui retourne la valeur \_ OK dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="0fdc3-113">It calls the filter's [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="0fdc3-114">La classe dérivée peut substituer la méthode **CTransformFilter :: CompleteConnect** pour effectuer des vérifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0fdc3-114">The derived class can override the **CTransformFilter::CompleteConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fdc3-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0fdc3-115">Requirements</span></span>



| <span data-ttu-id="0fdc3-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0fdc3-116">Requirement</span></span> | <span data-ttu-id="0fdc3-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="0fdc3-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fdc3-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="0fdc3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0fdc3-119"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0fdc3-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0fdc3-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0fdc3-120">Library</span></span><br/> | <dl> <span data-ttu-id="0fdc3-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0fdc3-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




