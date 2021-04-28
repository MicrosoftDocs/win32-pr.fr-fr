---
description: 'Méthode CTransformOutputPin. CheckConnect : la méthode CheckConnect détermine si une connexion de code confidentiel est appropriée.'
ms.assetid: 3dae5c6d-720e-4445-b601-3bdfe32f4c21
title: Méthode CTransformOutputPin. CheckConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 190acd2fbab5206b114b57719d350e3ad5eac0c2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094947"
---
# <a name="ctransformoutputpincheckconnect-method"></a><span data-ttu-id="7a777-103">Méthode CTransformOutputPin. CheckConnect</span><span class="sxs-lookup"><span data-stu-id="7a777-103">CTransformOutputPin.CheckConnect method</span></span>

<span data-ttu-id="7a777-104">La `CheckConnect` méthode détermine si une connexion de code confidentiel est appropriée.</span><span class="sxs-lookup"><span data-stu-id="7a777-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a777-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a777-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="7a777-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a777-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a777-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="7a777-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="7a777-108">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="7a777-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a777-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7a777-109">Return value</span></span>

<span data-ttu-id="7a777-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7a777-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7a777-111">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="7a777-111">Possible values include the following.</span></span>



| <span data-ttu-id="7a777-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7a777-112">Return code</span></span>                                                                                  | <span data-ttu-id="7a777-113">Description</span><span class="sxs-lookup"><span data-stu-id="7a777-113">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="7a777-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7a777-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="7a777-115">Réussite.</span><span class="sxs-lookup"><span data-stu-id="7a777-115">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="7a777-116"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="7a777-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="7a777-117">La broche d’entrée du filtre n’est pas connectée.</span><span class="sxs-lookup"><span data-stu-id="7a777-117">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7a777-118">Notes </span><span class="sxs-lookup"><span data-stu-id="7a777-118">Remarks</span></span>

<span data-ttu-id="7a777-119">Cette méthode remplace la méthode [**CBaseOutputPin :: CheckConnect**](cbaseoutputpin-checkconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="7a777-119">This method overrides the [**CBaseOutputPin::CheckConnect**](cbaseoutputpin-checkconnect.md) method.</span></span> <span data-ttu-id="7a777-120">Elle appelle la méthode [**CTransformFilter :: CheckConnect**](ctransformfilter-checkconnect.md) du filtre, qui retourne la valeur \_ OK dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="7a777-120">It calls the filter's [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="7a777-121">La classe dérivée peut substituer la méthode **CTransformFilter :: CheckConnect** pour effectuer des vérifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="7a777-121">The derived class can override the **CTransformFilter::CheckConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a777-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a777-122">Requirements</span></span>



| <span data-ttu-id="7a777-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a777-123">Requirement</span></span> | <span data-ttu-id="7a777-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a777-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a777-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a777-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7a777-126"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a777-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7a777-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7a777-127">Library</span></span><br/> | <dl> <span data-ttu-id="7a777-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7a777-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




