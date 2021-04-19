---
description: La méthode NotifyFilterState avertit le pin lorsque l’état du filtre change.
ms.assetid: 0eb3b0e5-9c44-464e-b4ca-bcded731e813
title: Méthode CBaseStreamControl. NotifyFilterState (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.NotifyFilterState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ccb96361c8f4938bd95ffdc29229a035a239cc25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541693"
---
# <a name="cbasestreamcontrolnotifyfilterstate-method"></a><span data-ttu-id="eec4c-103">Méthode CBaseStreamControl. NotifyFilterState</span><span class="sxs-lookup"><span data-stu-id="eec4c-103">CBaseStreamControl.NotifyFilterState method</span></span>

<span data-ttu-id="eec4c-104">La `NotifyFilterState` méthode notifie le code confidentiel lorsque l’état du filtre change.</span><span class="sxs-lookup"><span data-stu-id="eec4c-104">The `NotifyFilterState` method notifies the pin when the filter's state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="eec4c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eec4c-105">Syntax</span></span>


```C++
void NotifyFilterState(
   FILTER_STATE   new_state,
   REFERENCE_TIME tStart = 0
);
```



## <a name="parameters"></a><span data-ttu-id="eec4c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eec4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eec4c-107">*nouvel \_ État*</span><span class="sxs-lookup"><span data-stu-id="eec4c-107">*new\_state*</span></span> 
</dt> <dd>

<span data-ttu-id="eec4c-108">Spécifie le nouvel État, en tant que membre de l’énumération de l' [**\_ État du filtre**](/windows/win32/api/strmif/ne-strmif-filter_state) .</span><span class="sxs-lookup"><span data-stu-id="eec4c-108">Specifies the new state, as a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="eec4c-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="eec4c-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="eec4c-110">Spécifie l’heure de début.</span><span class="sxs-lookup"><span data-stu-id="eec4c-110">Specifies the start time.</span></span> <span data-ttu-id="eec4c-111">Si le nouvel état de filtre est état \_ en cours d’exécution, transmettez la valeur à partir de la méthode [**IMediaFilter :: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .</span><span class="sxs-lookup"><span data-stu-id="eec4c-111">If the new filter state is State\_Running, pass in the value from the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span> <span data-ttu-id="eec4c-112">Sinon, utilisez la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="eec4c-112">Otherwise, use the default value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eec4c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eec4c-113">Return value</span></span>

<span data-ttu-id="eec4c-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="eec4c-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eec4c-115">Notes</span><span class="sxs-lookup"><span data-stu-id="eec4c-115">Remarks</span></span>

<span data-ttu-id="eec4c-116">Cette méthode provoque l’arrêt de l’attente de la méthode [**CBaseStreamControl :: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) .</span><span class="sxs-lookup"><span data-stu-id="eec4c-116">This method causes the [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) method to stop waiting.</span></span> <span data-ttu-id="eec4c-117">Appelez cette méthode chaque fois que le filtre propriétaire change d’État.</span><span class="sxs-lookup"><span data-stu-id="eec4c-117">Call this method whenever the owning filter changes state.</span></span>

## <a name="examples"></a><span data-ttu-id="eec4c-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="eec4c-118">Examples</span></span>


```C++
STDMETHODIMP CMyFilter::Run(REFERENCE_TIME tStart)
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Running, tStart);
   return CBaseFilter::Run(tStart); // Call the filter base class.
}

STDMETHODIMP CMyFilter::Pause()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Paused);
   return CBaseFilter::Pause();
}

STDMETHODIMP CMyFilter::Stop()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Stopped);
   return CBaseFilter::Stop();
}
```



## <a name="requirements"></a><span data-ttu-id="eec4c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eec4c-119">Requirements</span></span>



| <span data-ttu-id="eec4c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eec4c-120">Requirement</span></span> | <span data-ttu-id="eec4c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="eec4c-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eec4c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="eec4c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="eec4c-123"><dt>Strmctl. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eec4c-123"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eec4c-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eec4c-124">Library</span></span><br/> | <dl> <span data-ttu-id="eec4c-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="eec4c-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eec4c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eec4c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec4c-127">**CBaseStreamControl, classe**</span><span class="sxs-lookup"><span data-stu-id="eec4c-127">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




