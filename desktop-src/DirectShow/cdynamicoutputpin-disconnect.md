---
description: La méthode Disconnect interrompt la connexion de code confidentiel actuelle. Cette méthode implémente la méthode IPin ::D éconnecter.
ms.assetid: 8d92a504-98ad-4f8f-89a4-f0c80763db44
title: CDynamicOutputPin. Disconnect, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 65c61ecc825d703976aa3163be5922da1ac4471a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531072"
---
# <a name="cdynamicoutputpindisconnect-method"></a><span data-ttu-id="9e2d5-104">CDynamicOutputPin. Disconnect, méthode</span><span class="sxs-lookup"><span data-stu-id="9e2d5-104">CDynamicOutputPin.Disconnect method</span></span>

<span data-ttu-id="9e2d5-105">La `Disconnect` méthode interrompt la connexion de code confidentiel actuelle.</span><span class="sxs-lookup"><span data-stu-id="9e2d5-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="9e2d5-106">Cette méthode implémente la méthode [**IPIN ::D éconnecter**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="9e2d5-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e2d5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e2d5-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="9e2d5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e2d5-108">Parameters</span></span>

<span data-ttu-id="9e2d5-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9e2d5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9e2d5-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e2d5-110">Return value</span></span>

<span data-ttu-id="9e2d5-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9e2d5-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9e2d5-112">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9e2d5-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="9e2d5-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9e2d5-113">Return code</span></span>                                                                             | <span data-ttu-id="9e2d5-114">Description</span><span class="sxs-lookup"><span data-stu-id="9e2d5-114">Description</span></span>                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="9e2d5-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="9e2d5-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="9e2d5-116">Le pin n’était pas connecté.</span><span class="sxs-lookup"><span data-stu-id="9e2d5-116">The pin was not connected.</span></span><br/> |
| <dl> <span data-ttu-id="9e2d5-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9e2d5-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="9e2d5-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="9e2d5-118">Success.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="9e2d5-119">Notes</span><span class="sxs-lookup"><span data-stu-id="9e2d5-119">Remarks</span></span>

<span data-ttu-id="9e2d5-120">Cette méthode remplace la méthode [**CBasePin ::D éconnecter**](cbasepin-disconnect.md) pour activer la déconnexion pendant que le filtre est actif.</span><span class="sxs-lookup"><span data-stu-id="9e2d5-120">This method overrides the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method to enable disconnecting while the filter is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e2d5-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e2d5-121">Requirements</span></span>



| <span data-ttu-id="9e2d5-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e2d5-122">Requirement</span></span> | <span data-ttu-id="9e2d5-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e2d5-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e2d5-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e2d5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9e2d5-125"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e2d5-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9e2d5-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9e2d5-126">Library</span></span><br/> | <dl> <span data-ttu-id="9e2d5-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9e2d5-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e2d5-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e2d5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e2d5-129">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="9e2d5-129">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




