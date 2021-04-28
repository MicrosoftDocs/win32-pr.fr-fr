---
description: 'CDynamicOutputPin. Disconnect, méthode : la méthode Disconnect interrompt la connexion de code confidentiel actuelle. Cette méthode implémente la méthode IPin ::D éconnecter.'
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
ms.openlocfilehash: 5a775146973b353413fa2e74584a6c763b721e7b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099297"
---
# <a name="cdynamicoutputpindisconnect-method"></a><span data-ttu-id="8a675-104">CDynamicOutputPin. Disconnect, méthode</span><span class="sxs-lookup"><span data-stu-id="8a675-104">CDynamicOutputPin.Disconnect method</span></span>

<span data-ttu-id="8a675-105">La `Disconnect` méthode interrompt la connexion de code confidentiel actuelle.</span><span class="sxs-lookup"><span data-stu-id="8a675-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="8a675-106">Cette méthode implémente la méthode [**IPIN ::D éconnecter**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="8a675-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a675-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a675-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="8a675-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a675-108">Parameters</span></span>

<span data-ttu-id="8a675-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8a675-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8a675-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8a675-110">Return value</span></span>

<span data-ttu-id="8a675-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8a675-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="8a675-112">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8a675-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="8a675-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8a675-113">Return code</span></span>                                                                             | <span data-ttu-id="8a675-114">Description</span><span class="sxs-lookup"><span data-stu-id="8a675-114">Description</span></span>                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="8a675-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="8a675-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="8a675-116">Le pin n’était pas connecté.</span><span class="sxs-lookup"><span data-stu-id="8a675-116">The pin was not connected.</span></span><br/> |
| <dl> <span data-ttu-id="8a675-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8a675-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="8a675-118">Réussite.</span><span class="sxs-lookup"><span data-stu-id="8a675-118">Success.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="8a675-119">Notes </span><span class="sxs-lookup"><span data-stu-id="8a675-119">Remarks</span></span>

<span data-ttu-id="8a675-120">Cette méthode remplace la méthode [**CBasePin ::D éconnecter**](cbasepin-disconnect.md) pour activer la déconnexion pendant que le filtre est actif.</span><span class="sxs-lookup"><span data-stu-id="8a675-120">This method overrides the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method to enable disconnecting while the filter is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a675-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a675-121">Requirements</span></span>



| <span data-ttu-id="8a675-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a675-122">Requirement</span></span> | <span data-ttu-id="8a675-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a675-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a675-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8a675-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8a675-125"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a675-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8a675-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8a675-126">Library</span></span><br/> | <dl> <span data-ttu-id="8a675-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8a675-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a675-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a675-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a675-129">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="8a675-129">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




