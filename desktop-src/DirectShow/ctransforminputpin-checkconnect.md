---
description: 'Méthode CTransformInputPin. CheckConnect : la méthode CheckConnect détermine si une connexion de code confidentiel est appropriée.'
ms.assetid: b8ace40d-31f5-49b0-a4cd-6ece0f883d96
title: Méthode CTransformInputPin. CheckConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e981254677c2e0a361a0a21f125f734ff1403db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095087"
---
# <a name="ctransforminputpincheckconnect-method"></a><span data-ttu-id="0d4be-103">Méthode CTransformInputPin. CheckConnect</span><span class="sxs-lookup"><span data-stu-id="0d4be-103">CTransformInputPin.CheckConnect method</span></span>

<span data-ttu-id="0d4be-104">La `CheckConnect` méthode détermine si une connexion de code confidentiel est appropriée.</span><span class="sxs-lookup"><span data-stu-id="0d4be-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d4be-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d4be-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="0d4be-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d4be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d4be-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="0d4be-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="0d4be-108">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="0d4be-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d4be-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0d4be-109">Return value</span></span>

<span data-ttu-id="0d4be-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0d4be-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0d4be-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0d4be-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="0d4be-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0d4be-112">Return code</span></span>                                                                                               | <span data-ttu-id="0d4be-113">Description</span><span class="sxs-lookup"><span data-stu-id="0d4be-113">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="0d4be-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0d4be-114"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="0d4be-115">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="0d4be-115">Success</span></span><br/>             |
| <dl> <span data-ttu-id="0d4be-116"><dt>**VFW \_ E \_ sens non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0d4be-116"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="0d4be-117">Sens du code confidentiel incorrect</span><span class="sxs-lookup"><span data-stu-id="0d4be-117">Wrong pin direction</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0d4be-118">Notes </span><span class="sxs-lookup"><span data-stu-id="0d4be-118">Remarks</span></span>

<span data-ttu-id="0d4be-119">Cette méthode remplace la méthode [**CBasePin :: CheckConnect**](cbasepin-checkconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="0d4be-119">This method overrides the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method.</span></span> <span data-ttu-id="0d4be-120">Elle appelle la méthode [**CTransformFilter :: CheckConnect**](ctransformfilter-checkconnect.md) du filtre, qui retourne la valeur \_ OK dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="0d4be-120">It calls the filter's [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="0d4be-121">La classe dérivée peut substituer la méthode **CTransformFilter :: CheckConnect** pour effectuer des vérifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0d4be-121">The derived class can override the **CTransformFilter::CheckConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d4be-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d4be-122">Requirements</span></span>



| <span data-ttu-id="0d4be-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d4be-123">Requirement</span></span> | <span data-ttu-id="0d4be-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d4be-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d4be-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d4be-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0d4be-126"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d4be-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0d4be-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0d4be-127">Library</span></span><br/> | <dl> <span data-ttu-id="0d4be-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0d4be-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




