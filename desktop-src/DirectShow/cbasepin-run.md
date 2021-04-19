---
description: La méthode Run indique au code confidentiel que le filtre est en cours d’exécution.
ms.assetid: 74aafc89-2d3c-4259-a5b7-d4fb7628f539
title: CBasePin. Run, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35d66f6d504a96c1146bc15285762d83faa6de3b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528525"
---
# <a name="cbasepinrun-method"></a><span data-ttu-id="06a82-103">CBasePin. Run, méthode</span><span class="sxs-lookup"><span data-stu-id="06a82-103">CBasePin.Run method</span></span>

<span data-ttu-id="06a82-104">La `Run` méthode notifie le code confidentiel que le filtre est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="06a82-104">The `Run` method notifies the pin that the filter is now running.</span></span>

## <a name="syntax"></a><span data-ttu-id="06a82-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06a82-105">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="06a82-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06a82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06a82-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="06a82-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="06a82-108">Heure de début passée à la méthode [**IMediaFilter :: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) du filtre.</span><span class="sxs-lookup"><span data-stu-id="06a82-108">Start time as passed to the filter's [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06a82-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06a82-109">Return value</span></span>

<span data-ttu-id="06a82-110">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="06a82-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="06a82-111">Notes</span><span class="sxs-lookup"><span data-stu-id="06a82-111">Remarks</span></span>

<span data-ttu-id="06a82-112">Lorsque le filtre passe de en pause à en cours d’exécution, la classe [**CBaseFilter**](cbasefilter.md) appelle cette méthode sur tous les codes confidentiels du filtre.</span><span class="sxs-lookup"><span data-stu-id="06a82-112">When the filter goes from paused to running, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's pins.</span></span>

<span data-ttu-id="06a82-113">Cette méthode n’a aucun effet dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="06a82-113">This method does nothing in the base class.</span></span> <span data-ttu-id="06a82-114">Les classes dérivées peuvent substituer cette méthode.</span><span class="sxs-lookup"><span data-stu-id="06a82-114">Derived classes can override this method.</span></span> <span data-ttu-id="06a82-115">Par exemple, un code confidentiel peut démarrer un thread de travail qui remet des exemples.</span><span class="sxs-lookup"><span data-stu-id="06a82-115">For example, a pin might start a worker thread that delivers samples.</span></span>

<span data-ttu-id="06a82-116">L’état interne du gestionnaire de graphique de filtre n’est pas mis à jour avant le retour de cette fonction membre, donc ne Testez pas l’État à partir de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="06a82-116">The filter graph manager's internal state is not updated until after this member function returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="06a82-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06a82-117">Requirements</span></span>



| <span data-ttu-id="06a82-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06a82-118">Requirement</span></span> | <span data-ttu-id="06a82-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="06a82-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06a82-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="06a82-120">Header</span></span><br/>  | <dl> <span data-ttu-id="06a82-121"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06a82-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="06a82-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="06a82-122">Library</span></span><br/> | <dl> <span data-ttu-id="06a82-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="06a82-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06a82-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06a82-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06a82-125">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="06a82-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




