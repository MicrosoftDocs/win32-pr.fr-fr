---
description: La méthode CheckConnect détermine si une connexion de code confidentiel est appropriée.
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
ms.openlocfilehash: b9a20eb8d3e20679cb8805d3a1cd8e167ef0bfd5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526396"
---
# <a name="ctransformoutputpincheckconnect-method"></a><span data-ttu-id="06742-103">Méthode CTransformOutputPin. CheckConnect</span><span class="sxs-lookup"><span data-stu-id="06742-103">CTransformOutputPin.CheckConnect method</span></span>

<span data-ttu-id="06742-104">La `CheckConnect` méthode détermine si une connexion de code confidentiel est appropriée.</span><span class="sxs-lookup"><span data-stu-id="06742-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="06742-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06742-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="06742-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06742-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06742-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="06742-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="06742-108">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="06742-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06742-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06742-109">Return value</span></span>

<span data-ttu-id="06742-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="06742-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="06742-111">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="06742-111">Possible values include the following.</span></span>



| <span data-ttu-id="06742-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="06742-112">Return code</span></span>                                                                                  | <span data-ttu-id="06742-113">Description</span><span class="sxs-lookup"><span data-stu-id="06742-113">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="06742-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="06742-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="06742-115">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="06742-115">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="06742-116"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="06742-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="06742-117">La broche d’entrée du filtre n’est pas connectée.</span><span class="sxs-lookup"><span data-stu-id="06742-117">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="06742-118">Notes</span><span class="sxs-lookup"><span data-stu-id="06742-118">Remarks</span></span>

<span data-ttu-id="06742-119">Cette méthode remplace la méthode [**CBaseOutputPin :: CheckConnect**](cbaseoutputpin-checkconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="06742-119">This method overrides the [**CBaseOutputPin::CheckConnect**](cbaseoutputpin-checkconnect.md) method.</span></span> <span data-ttu-id="06742-120">Elle appelle la méthode [**CTransformFilter :: CheckConnect**](ctransformfilter-checkconnect.md) du filtre, qui retourne la valeur \_ OK dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="06742-120">It calls the filter's [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="06742-121">La classe dérivée peut substituer la méthode **CTransformFilter :: CheckConnect** pour effectuer des vérifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="06742-121">The derived class can override the **CTransformFilter::CheckConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="06742-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06742-122">Requirements</span></span>



| <span data-ttu-id="06742-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06742-123">Requirement</span></span> | <span data-ttu-id="06742-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="06742-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06742-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="06742-125">Header</span></span><br/>  | <dl> <span data-ttu-id="06742-126"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06742-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="06742-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="06742-127">Library</span></span><br/> | <dl> <span data-ttu-id="06742-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="06742-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




