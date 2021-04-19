---
description: 'La méthode BeginFlush commence une opération de vidage. Cette méthode implémente la méthode IPin :: BeginFlush.'
ms.assetid: 7c76ca06-dc3c-4f9a-9761-32aea7db4c7e
title: Méthode CTransformInputPin. BeginFlush (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4d028634364ca59ae293d9ebb60a464974ccd74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528535"
---
# <a name="ctransforminputpinbeginflush-method"></a><span data-ttu-id="2a50a-104">Méthode CTransformInputPin. BeginFlush</span><span class="sxs-lookup"><span data-stu-id="2a50a-104">CTransformInputPin.BeginFlush method</span></span>

<span data-ttu-id="2a50a-105">La `BeginFlush` méthode commence une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="2a50a-105">The `BeginFlush` method begins a flush operation.</span></span> <span data-ttu-id="2a50a-106">Cette méthode implémente la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="2a50a-106">This method implements the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a50a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a50a-107">Syntax</span></span>


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="2a50a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a50a-108">Parameters</span></span>

<span data-ttu-id="2a50a-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2a50a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2a50a-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2a50a-110">Return value</span></span>

<span data-ttu-id="2a50a-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2a50a-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2a50a-112">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2a50a-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="2a50a-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2a50a-113">Return code</span></span>                                                                                           | <span data-ttu-id="2a50a-114">Description</span><span class="sxs-lookup"><span data-stu-id="2a50a-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="2a50a-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2a50a-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="2a50a-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="2a50a-116">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="2a50a-117"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="2a50a-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="2a50a-118">La broche de sortie n’est pas connectée.</span><span class="sxs-lookup"><span data-stu-id="2a50a-118">Output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2a50a-119">Notes</span><span class="sxs-lookup"><span data-stu-id="2a50a-119">Remarks</span></span>

<span data-ttu-id="2a50a-120">Cette méthode appelle la méthode [**CBaseInputPin :: BeginFlush**](cbaseinputpin-beginflush.md) du pin.</span><span class="sxs-lookup"><span data-stu-id="2a50a-120">This method calls the pin's [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md) method.</span></span> <span data-ttu-id="2a50a-121">Elle appelle ensuite la méthode [**CTransformFilter :: BeginFlush**](ctransformfilter-beginflush.md) du filtre pour remettre l’appel en aval.</span><span class="sxs-lookup"><span data-stu-id="2a50a-121">Then it calls the filter's [**CTransformFilter::BeginFlush**](ctransformfilter-beginflush.md) method to deliver the call downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a50a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a50a-122">Requirements</span></span>



| <span data-ttu-id="2a50a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a50a-123">Requirement</span></span> | <span data-ttu-id="2a50a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a50a-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a50a-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="2a50a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2a50a-126"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a50a-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2a50a-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2a50a-127">Library</span></span><br/> | <dl> <span data-ttu-id="2a50a-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2a50a-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




