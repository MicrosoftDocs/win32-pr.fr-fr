---
description: La méthode GetState récupère l’état du filtre (en cours d’exécution, arrêté ou suspendu).
ms.assetid: 5d35824c-2509-499a-bbb1-1fb916b51808
title: Méthode CBaseRenderer. GetState (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 451078a6167ff7ca89ad4153c416826af8ac6d05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542268"
---
# <a name="cbaserenderergetstate-method"></a><span data-ttu-id="8ef23-103">Méthode CBaseRenderer. GetState</span><span class="sxs-lookup"><span data-stu-id="8ef23-103">CBaseRenderer.GetState method</span></span>

<span data-ttu-id="8ef23-104">La `GetState` méthode récupère l’état du filtre (en cours d’exécution, arrêté ou suspendu).</span><span class="sxs-lookup"><span data-stu-id="8ef23-104">The `GetState` method retrieves the filters's state (running, stopped, or paused).</span></span>

## <a name="syntax"></a><span data-ttu-id="8ef23-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ef23-105">Syntax</span></span>


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a><span data-ttu-id="8ef23-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ef23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ef23-107">*dwMilliSecsTimeout*</span><span class="sxs-lookup"><span data-stu-id="8ef23-107">*dwMilliSecsTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="8ef23-108">Intervalle de délai d’attente, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="8ef23-108">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="8ef23-109">*State*</span><span class="sxs-lookup"><span data-stu-id="8ef23-109">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="8ef23-110">Pointeur vers une variable qui reçoit un membre du type énuméré d' [**\_ État de filtre**](/windows/win32/api/strmif/ne-strmif-filter_state) , indiquant l’état du filtre.</span><span class="sxs-lookup"><span data-stu-id="8ef23-110">Pointer to a variable that receives a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the filter's state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ef23-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8ef23-111">Return value</span></span>

<span data-ttu-id="8ef23-112">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8ef23-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="8ef23-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8ef23-113">Return code</span></span>                                                                                                | <span data-ttu-id="8ef23-114">Description</span><span class="sxs-lookup"><span data-stu-id="8ef23-114">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="8ef23-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8ef23-115"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="8ef23-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="8ef23-116">Success.</span></span><br/>                                            |
| <dl> <span data-ttu-id="8ef23-117"><dt>**\_ \_ état \_ intermédiaire de VFW S**</dt></span><span class="sxs-lookup"><span data-stu-id="8ef23-117"><dt>**VFW\_S\_STATE\_INTERMEDIATE**</dt></span></span> </dl> | <span data-ttu-id="8ef23-118">Le filtre passe à l’état indiqué.</span><span class="sxs-lookup"><span data-stu-id="8ef23-118">The filter is transitioning to the indicated state.</span></span><br/> |
| <dl> <span data-ttu-id="8ef23-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="8ef23-119"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="8ef23-120">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="8ef23-120">**NULL** pointer argument.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="8ef23-121">Notes</span><span class="sxs-lookup"><span data-stu-id="8ef23-121">Remarks</span></span>

<span data-ttu-id="8ef23-122">Cette méthode remplace la méthode [**CBaseFilter :: GetState**](cbasefilter-getstate.md) .</span><span class="sxs-lookup"><span data-stu-id="8ef23-122">This method overrides the [**CBaseFilter::GetState**](cbasefilter-getstate.md) method.</span></span> <span data-ttu-id="8ef23-123">Quand le convertisseur est suspendu, il ne termine pas la transition d’État tant qu’il n’a pas reçu d’exemple à restituer.</span><span class="sxs-lookup"><span data-stu-id="8ef23-123">When the renderer is paused, it does not complete the state transition until it receives a sample to render.</span></span> <span data-ttu-id="8ef23-124">Si le délai d’attente expire avant la fin de la transition d’État, la méthode retourne le niveau intermédiaire de l' \_ État VFW S \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8ef23-124">If the time-out expires before the state transition is complete, the method returns VFW\_S\_STATE\_INTERMEDIATE.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ef23-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ef23-125">Requirements</span></span>



| <span data-ttu-id="8ef23-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ef23-126">Requirement</span></span> | <span data-ttu-id="8ef23-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ef23-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ef23-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ef23-128">Header</span></span><br/>  | <dl> <span data-ttu-id="8ef23-129"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ef23-129"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8ef23-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8ef23-130">Library</span></span><br/> | <dl> <span data-ttu-id="8ef23-131"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8ef23-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ef23-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ef23-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ef23-133">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="8ef23-133">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




