---
description: 'La méthode GetState récupère l’état de l’objet (en cours d’exécution, arrêté ou suspendu). Cette méthode implémente la méthode IMediaFilter :: GetState.'
ms.assetid: d4cc7e2b-5ea5-4165-842f-becc3a81cbce
title: Méthode CBaseMediaFilter. GetState (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eeda91433e0e1474e936902da115e15c37e32e09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525379"
---
# <a name="cbasemediafiltergetstate-method"></a><span data-ttu-id="4f5d4-104">Méthode CBaseMediaFilter. GetState</span><span class="sxs-lookup"><span data-stu-id="4f5d4-104">CBaseMediaFilter.GetState method</span></span>

<span data-ttu-id="4f5d4-105">La `GetState` méthode récupère l’état de l’objet (en cours d’exécution, arrêté ou suspendu).</span><span class="sxs-lookup"><span data-stu-id="4f5d4-105">The `GetState` method retrieves the object's state (running, stopped, or paused).</span></span> <span data-ttu-id="4f5d4-106">Cette méthode implémente la méthode [**IMediaFilter :: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) .</span><span class="sxs-lookup"><span data-stu-id="4f5d4-106">This method implements the [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f5d4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f5d4-107">Syntax</span></span>


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a><span data-ttu-id="4f5d4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f5d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f5d4-109">*dwMilliSecsTimeout*</span><span class="sxs-lookup"><span data-stu-id="4f5d4-109">*dwMilliSecsTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="4f5d4-110">Intervalle de délai d’attente, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="4f5d4-110">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="4f5d4-111">*State*</span><span class="sxs-lookup"><span data-stu-id="4f5d4-111">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="4f5d4-112">Pointeur vers une variable qui reçoit un membre du type énuméré d' [**\_ État de filtre**](/windows/win32/api/strmif/ne-strmif-filter_state) , indiquant l’état de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4f5d4-112">Pointer to a variable that receives a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the object's state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f5d4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4f5d4-113">Return value</span></span>

<span data-ttu-id="4f5d4-114">Retourne le \_ pointeur S ou OK \_ .</span><span class="sxs-lookup"><span data-stu-id="4f5d4-114">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f5d4-115">Notes</span><span class="sxs-lookup"><span data-stu-id="4f5d4-115">Remarks</span></span>

<span data-ttu-id="4f5d4-116">Dans la classe de base, toutes les transitions d’État sont synchrones et le paramètre *dwMilliSecsTimeout* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="4f5d4-116">In the base class, all state transitions are synchronous and the *dwMilliSecsTimeout* parameter is ignored.</span></span> <span data-ttu-id="4f5d4-117">Si une classe dérivée exécute des transitions d’État asynchrones, elle doit substituer cette méthode pour attendre pendant les transitions d’État, avec un délai d’attente de *dwMilliSecsTimeout* millisecondes.</span><span class="sxs-lookup"><span data-stu-id="4f5d4-117">If a derived class performs asynchronous state transitions, it should override this method to wait during state transitions, with a time-out of *dwMilliSecsTimeout* milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f5d4-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f5d4-118">Requirements</span></span>



| <span data-ttu-id="4f5d4-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f5d4-119">Requirement</span></span> | <span data-ttu-id="4f5d4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f5d4-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f5d4-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f5d4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4f5d4-122"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f5d4-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4f5d4-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4f5d4-123">Library</span></span><br/> | <dl> <span data-ttu-id="4f5d4-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4f5d4-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f5d4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f5d4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f5d4-126">**CBaseMediaFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="4f5d4-126">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




