---
description: 'La méthode active indique au code confidentiel que le filtre est maintenant actif. Cette méthode remplace la méthode CBasePin :: active. Si le code PIN est connecté, cette méthode démarre le thread de streaming.'
ms.assetid: ea32b602-2583-4de6-96ec-6ea875c49d14
title: Méthode CSourceStream. active (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a161c82621f29b916e03fbc2e59ec762871940b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542619"
---
# <a name="csourcestreamactive-method"></a><span data-ttu-id="24b05-105">CSourceStream. active, méthode</span><span class="sxs-lookup"><span data-stu-id="24b05-105">CSourceStream.Active method</span></span>

<span data-ttu-id="24b05-106">La `Active` méthode notifie le code confidentiel que le filtre est maintenant actif.</span><span class="sxs-lookup"><span data-stu-id="24b05-106">The `Active` method notifies the pin that the filter is now active.</span></span> <span data-ttu-id="24b05-107">Cette méthode remplace la méthode [**CBasePin :: active**](cbasepin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="24b05-107">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span> <span data-ttu-id="24b05-108">Si le code PIN est connecté, cette méthode démarre le thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="24b05-108">If the pin is connected, this method starts the streaming thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="24b05-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24b05-109">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="24b05-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24b05-110">Parameters</span></span>

<span data-ttu-id="24b05-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="24b05-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="24b05-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="24b05-112">Return value</span></span>

<span data-ttu-id="24b05-113">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="24b05-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="24b05-114">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="24b05-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="24b05-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="24b05-115">Return code</span></span>                                                                             | <span data-ttu-id="24b05-116">Description</span><span class="sxs-lookup"><span data-stu-id="24b05-116">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="24b05-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="24b05-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="24b05-118">Le code PIN est déjà actif.</span><span class="sxs-lookup"><span data-stu-id="24b05-118">The pin is already active.</span></span><br/>  |
| <dl> <span data-ttu-id="24b05-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="24b05-119"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="24b05-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="24b05-120">Success.</span></span><br/>                    |
| <dl> <span data-ttu-id="24b05-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="24b05-121"><dt>**E\_FAIL**</dt></span></span> </dl>  | <span data-ttu-id="24b05-122">Impossible de démarrer le thread.</span><span class="sxs-lookup"><span data-stu-id="24b05-122">Could not start the thread.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="24b05-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24b05-123">Requirements</span></span>



| <span data-ttu-id="24b05-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24b05-124">Requirement</span></span> | <span data-ttu-id="24b05-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="24b05-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24b05-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="24b05-126">Header</span></span><br/>  | <dl> <span data-ttu-id="24b05-127"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24b05-127"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="24b05-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="24b05-128">Library</span></span><br/> | <dl> <span data-ttu-id="24b05-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="24b05-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24b05-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24b05-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24b05-131">**CSourceStream, classe**</span><span class="sxs-lookup"><span data-stu-id="24b05-131">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




