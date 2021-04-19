---
description: 'La méthode EndOfStream indique au code confidentiel qu’aucune donnée supplémentaire n’est attendue. Cette méthode implémente la méthode IPin :: EndOfStream.'
ms.assetid: db9896eb-3db2-4d58-a787-4d80ce8f0d0e
title: Méthode CTransformInputPin. EndOfStream (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc39770f081499be720c433301823cbc60f37d17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528544"
---
# <a name="ctransforminputpinendofstream-method"></a><span data-ttu-id="cab9a-104">Méthode CTransformInputPin. EndOfStream</span><span class="sxs-lookup"><span data-stu-id="cab9a-104">CTransformInputPin.EndOfStream method</span></span>

<span data-ttu-id="cab9a-105">La `EndOfStream` méthode indique au code confidentiel qu’aucune donnée supplémentaire n’est attendue.</span><span class="sxs-lookup"><span data-stu-id="cab9a-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="cab9a-106">Cette méthode implémente la méthode [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="cab9a-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cab9a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cab9a-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="cab9a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cab9a-108">Parameters</span></span>

<span data-ttu-id="cab9a-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="cab9a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cab9a-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cab9a-110">Return value</span></span>

<span data-ttu-id="cab9a-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cab9a-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="cab9a-112">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="cab9a-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="cab9a-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="cab9a-113">Return code</span></span>                                                                                           | <span data-ttu-id="cab9a-114">Description</span><span class="sxs-lookup"><span data-stu-id="cab9a-114">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="cab9a-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cab9a-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="cab9a-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="cab9a-116">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="cab9a-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="cab9a-117"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="cab9a-118">Le code PIN est en cours de vidage.</span><span class="sxs-lookup"><span data-stu-id="cab9a-118">Pin is currently flushing.</span></span><br/>       |
| <dl> <span data-ttu-id="cab9a-119"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="cab9a-119"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="cab9a-120">La broche de sortie n’est pas connectée.</span><span class="sxs-lookup"><span data-stu-id="cab9a-120">The output pin is not connected.</span></span><br/> |
| <dl> <span data-ttu-id="cab9a-121"><dt>**\_erreur d' \_ exécution VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cab9a-121"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="cab9a-122">Une erreur d’exécution s’est produite.</span><span class="sxs-lookup"><span data-stu-id="cab9a-122">A run-time error occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="cab9a-123"><dt>**VFW \_ E \_ état incorrect \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cab9a-123"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="cab9a-124">Le code PIN est arrêté.</span><span class="sxs-lookup"><span data-stu-id="cab9a-124">The pin is stopped.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="cab9a-125">Notes</span><span class="sxs-lookup"><span data-stu-id="cab9a-125">Remarks</span></span>

<span data-ttu-id="cab9a-126">Cette méthode appelle la méthode [**CTransformFilter :: EndOfStream**](ctransformfilter-endofstream.md) du filtre pour remettre la notification de fin de flux en aval.</span><span class="sxs-lookup"><span data-stu-id="cab9a-126">This method calls the filter's [**CTransformFilter::EndOfStream**](ctransformfilter-endofstream.md) method to deliver the end-of-stream notification downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="cab9a-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cab9a-127">Requirements</span></span>



| <span data-ttu-id="cab9a-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cab9a-128">Requirement</span></span> | <span data-ttu-id="cab9a-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="cab9a-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cab9a-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="cab9a-130">Header</span></span><br/>  | <dl> <span data-ttu-id="cab9a-131"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cab9a-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cab9a-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cab9a-132">Library</span></span><br/> | <dl> <span data-ttu-id="cab9a-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cab9a-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




