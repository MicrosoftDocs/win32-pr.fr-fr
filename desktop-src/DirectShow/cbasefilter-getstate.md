---
description: 'La méthode GetState récupère l’état du filtre (en cours d’exécution, arrêté ou suspendu). Cette méthode implémente la méthode IMediaFilter :: GetState.'
ms.assetid: e32e3a1d-857f-4db3-b52c-5b6b802ded42
title: Méthode CBaseFilter. GetState (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c9470e5d71bf71f4e37e6eef84015becdf05f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534833"
---
# <a name="cbasefiltergetstate-method"></a><span data-ttu-id="4c8b6-104">Méthode CBaseFilter. GetState</span><span class="sxs-lookup"><span data-stu-id="4c8b6-104">CBaseFilter.GetState method</span></span>

<span data-ttu-id="4c8b6-105">La `GetState` méthode récupère l’état du filtre (en cours d’exécution, arrêté ou suspendu).</span><span class="sxs-lookup"><span data-stu-id="4c8b6-105">The `GetState` method retrieves the filters's state (running, stopped, or paused).</span></span> <span data-ttu-id="4c8b6-106">Cette méthode implémente la méthode [**IMediaFilter :: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) .</span><span class="sxs-lookup"><span data-stu-id="4c8b6-106">This method implements the [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c8b6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c8b6-107">Syntax</span></span>


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a><span data-ttu-id="4c8b6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c8b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c8b6-109">*dwMilliSecsTimeout*</span><span class="sxs-lookup"><span data-stu-id="4c8b6-109">*dwMilliSecsTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="4c8b6-110">Intervalle de délai d’attente, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="4c8b6-110">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="4c8b6-111">*State*</span><span class="sxs-lookup"><span data-stu-id="4c8b6-111">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="4c8b6-112">Pointeur vers une variable qui reçoit un membre du type énuméré d' [**\_ État de filtre**](/windows/win32/api/strmif/ne-strmif-filter_state) , indiquant l’état du filtre.</span><span class="sxs-lookup"><span data-stu-id="4c8b6-112">Pointer to a variable that receives a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the filter's state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c8b6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4c8b6-113">Return value</span></span>

<span data-ttu-id="4c8b6-114">Retourne le \_ pointeur S ou OK \_ .</span><span class="sxs-lookup"><span data-stu-id="4c8b6-114">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c8b6-115">Notes</span><span class="sxs-lookup"><span data-stu-id="4c8b6-115">Remarks</span></span>

<span data-ttu-id="4c8b6-116">Dans la classe de base, toutes les transitions d’État sont synchrones et le paramètre *dwMilliSecsTimeout* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="4c8b6-116">In the base class, all state transitions are synchronous and the *dwMilliSecsTimeout* parameter is ignored.</span></span> <span data-ttu-id="4c8b6-117">Si une classe dérivée exécute des transitions d’État asynchrones, elle doit substituer cette méthode pour attendre pendant les transitions d’État, avec un délai d’attente de *dwMilliSecsTimeout* millisecondes.</span><span class="sxs-lookup"><span data-stu-id="4c8b6-117">If a derived class performs asynchronous state transitions, it should override this method to wait during state transitions, with a time-out of *dwMilliSecsTimeout* milliseconds.</span></span>

<span data-ttu-id="4c8b6-118">Si votre filtre ne remet pas de données pendant la suspension, substituez la `GetState` méthode pour retourner la valeur de VFW \_ S \_ ne pas \_ signaler lorsque le filtre est suspendu (voir [remise d’exemples](delivering-samples.md)).</span><span class="sxs-lookup"><span data-stu-id="4c8b6-118">If your filter does not deliver data while paused, override the `GetState` method to return the value VFW\_S\_CANT\_CUE when the filter is paused (see [Delivering Samples](delivering-samples.md)).</span></span> <span data-ttu-id="4c8b6-119">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4c8b6-119">For example:</span></span>


```C++
CMyFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
        return VFW_S_CANT_CUE;
    else
        return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="4c8b6-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c8b6-120">Requirements</span></span>



| <span data-ttu-id="4c8b6-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c8b6-121">Requirement</span></span> | <span data-ttu-id="4c8b6-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c8b6-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c8b6-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="4c8b6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4c8b6-124"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4c8b6-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4c8b6-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4c8b6-125">Library</span></span><br/> | <dl> <span data-ttu-id="4c8b6-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4c8b6-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c8b6-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c8b6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c8b6-128">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="4c8b6-128">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




