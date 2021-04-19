---
description: 'La méthode EndFlush termine une opération de vidage. Cette méthode implémente la méthode IPin :: EndFlush.'
ms.assetid: ebc70df3-e99d-4292-990b-99b79ff06461
title: Méthode CTransformInputPin. EndFlush (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0fe6afeaa0ca3d47b278987af494221e8f50340
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530542"
---
# <a name="ctransforminputpinendflush-method"></a><span data-ttu-id="a5540-104">Méthode CTransformInputPin. EndFlush</span><span class="sxs-lookup"><span data-stu-id="a5540-104">CTransformInputPin.EndFlush method</span></span>

<span data-ttu-id="a5540-105">La `EndFlush` méthode termine une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="a5540-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="a5540-106">Cette méthode implémente la méthode [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="a5540-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5540-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5540-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="a5540-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5540-108">Parameters</span></span>

<span data-ttu-id="a5540-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a5540-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a5540-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a5540-110">Return value</span></span>

<span data-ttu-id="a5540-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a5540-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a5540-112">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a5540-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="a5540-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a5540-113">Return code</span></span>                                                                                           | <span data-ttu-id="a5540-114">Description</span><span class="sxs-lookup"><span data-stu-id="a5540-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="a5540-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a5540-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="a5540-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="a5540-116">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="a5540-117"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="a5540-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="a5540-118">La broche de sortie n’est pas connectée.</span><span class="sxs-lookup"><span data-stu-id="a5540-118">Output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a5540-119">Notes</span><span class="sxs-lookup"><span data-stu-id="a5540-119">Remarks</span></span>

<span data-ttu-id="a5540-120">Cette méthode appelle la méthode [**CTransformFilter :: EndFlush**](ctransformfilter-endflush.md) du filtre pour remettre l’appel en aval.</span><span class="sxs-lookup"><span data-stu-id="a5540-120">This method calls the filter's [**CTransformFilter::EndFlush**](ctransformfilter-endflush.md) method to deliver the call downstream.</span></span> <span data-ttu-id="a5540-121">Elle appelle ensuite la méthode [**CBaseInputPin :: EndFlush**](cbaseinputpin-endflush.md) du pin.</span><span class="sxs-lookup"><span data-stu-id="a5540-121">Then it calls the pin's [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5540-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5540-122">Requirements</span></span>



| <span data-ttu-id="a5540-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5540-123">Requirement</span></span> | <span data-ttu-id="a5540-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5540-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5540-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5540-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a5540-126"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a5540-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a5540-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a5540-127">Library</span></span><br/> | <dl> <span data-ttu-id="a5540-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a5540-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




