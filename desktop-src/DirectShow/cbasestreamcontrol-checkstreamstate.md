---
description: La méthode CheckStreamState détermine si un exemple de support doit être remis ou ignoré.
ms.assetid: 1533f4b9-e13e-458b-9614-96d733cef4ed
title: Méthode CBaseStreamControl. CheckStreamState (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CheckStreamState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e469e288e853ca88a0cf15c209882a8114e33509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523956"
---
# <a name="cbasestreamcontrolcheckstreamstate-method"></a><span data-ttu-id="adae0-103">Méthode CBaseStreamControl. CheckStreamState</span><span class="sxs-lookup"><span data-stu-id="adae0-103">CBaseStreamControl.CheckStreamState method</span></span>

<span data-ttu-id="adae0-104">La `CheckStreamState` méthode détermine si un échantillon de média doit être remis ou ignoré.</span><span class="sxs-lookup"><span data-stu-id="adae0-104">The `CheckStreamState` method determines whether a media sample should be delivered or discarded.</span></span>

## <a name="syntax"></a><span data-ttu-id="adae0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="adae0-105">Syntax</span></span>


```C++
enum CheckStreamState(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="adae0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="adae0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adae0-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="adae0-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="adae0-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="adae0-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adae0-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="adae0-109">Return value</span></span>

<span data-ttu-id="adae0-110">Retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="adae0-110">Returns one of the following values.</span></span>



| <span data-ttu-id="adae0-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="adae0-111">Return code</span></span>                                                                                       | <span data-ttu-id="adae0-112">Description</span><span class="sxs-lookup"><span data-stu-id="adae0-112">Description</span></span>                     |
|---------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="adae0-113"><dt>**FLUX \_ ignoré**</dt></span><span class="sxs-lookup"><span data-stu-id="adae0-113"><dt>**STREAM\_DISCARDING**</dt></span></span> </dl> | <span data-ttu-id="adae0-114">Ignorez cet exemple.</span><span class="sxs-lookup"><span data-stu-id="adae0-114">Discard this sample.</span></span><br/> |
| <dl> <span data-ttu-id="adae0-115"><dt>**flux \_ de flux**</dt></span><span class="sxs-lookup"><span data-stu-id="adae0-115"><dt>**STREAM\_FLOWING**</dt></span></span> </dl>    | <span data-ttu-id="adae0-116">Fournissez cet exemple.</span><span class="sxs-lookup"><span data-stu-id="adae0-116">Deliver this sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="adae0-117">Notes</span><span class="sxs-lookup"><span data-stu-id="adae0-117">Remarks</span></span>

<span data-ttu-id="adae0-118">Appelez cette méthode lorsque votre code confidentiel reçoit un exemple.</span><span class="sxs-lookup"><span data-stu-id="adae0-118">Call this method when your pin receives a sample.</span></span> <span data-ttu-id="adae0-119">Fournissez l’exemple uniquement si la valeur de retour est flux continu \_ .</span><span class="sxs-lookup"><span data-stu-id="adae0-119">Deliver the sample only if the return value is STREAM\_FLOWING.</span></span> <span data-ttu-id="adae0-120">Si la valeur de retour est une annulation de flux \_ , ignorez l’exemple.</span><span class="sxs-lookup"><span data-stu-id="adae0-120">If the return value is STREAM\_DISCARDING, discard the sample.</span></span>

<span data-ttu-id="adae0-121">Si le code PIN ignore les exemples, il doit marquer l’exemple suivant qu’il remet comme discontinu, en appelant la méthode [**IMediaSample :: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .</span><span class="sxs-lookup"><span data-stu-id="adae0-121">If the pin discards any samples, it should mark the next sample that it delivers as a discontinuity, by calling the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method.</span></span>

<span data-ttu-id="adae0-122">Si votre filtre implémente l’interface [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) pour compter le nombre de frames qu’il supprime, ne comptez pas une trame ignorée en tant que frame supprimé.</span><span class="sxs-lookup"><span data-stu-id="adae0-122">If your filter implements the [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) interface to count how many frames it drops, do not count a discarded frame as a dropped frame.</span></span>

<span data-ttu-id="adae0-123">Lorsque la valeur de retour est une suppression de flux \_ , la méthode se bloque jusqu’à ce que le temps de référence atteigne l’heure de début de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="adae0-123">When the return value is STREAM\_DISCARDING, the method blocks until the reference time reaches the sample's start time.</span></span> <span data-ttu-id="adae0-124">Cela empêche votre pin d’ignorer trop rapidement les exemples.</span><span class="sxs-lookup"><span data-stu-id="adae0-124">This prevents your pin from discarding samples too quickly.</span></span> <span data-ttu-id="adae0-125">Si le filtre est suspendu, le temps d’attente est infini, jusqu’à ce que le filtre exécute, arrête ou vide les données.</span><span class="sxs-lookup"><span data-stu-id="adae0-125">If the filter is paused, the wait time is infinite, until the filter runs, stops, or flushes data.</span></span> <span data-ttu-id="adae0-126">(Les modifications d’état de filtre et la diffusion en continu se produisent sur des threads distincts, donc cela ne provoque aucun blocage).</span><span class="sxs-lookup"><span data-stu-id="adae0-126">(Filter state changes and streaming happen on separate threads, so this does not cause any deadlock.)</span></span>

<span data-ttu-id="adae0-127">L’énumération **CBaseStreamControl :: StreamControlState** est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="adae0-127">The **CBaseStreamControl::StreamControlState** enumeration is defined as follows:</span></span>


```C++
enum StreamControlState{ 
    STREAM_FLOWING = 0x1000,
    STREAM_DISCARDING
};
```



## <a name="examples"></a><span data-ttu-id="adae0-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="adae0-128">Examples</span></span>

<span data-ttu-id="adae0-129">L’exemple suivant suppose que le code confidentiel utilise une variable membre nommée m \_ fLastSampleDiscarded pour effectuer le suivi des discontinuités.</span><span class="sxs-lookup"><span data-stu-id="adae0-129">The following example assumes that the pin uses a member variable named m\_fLastSampleDiscarded to keep track of discontinuities.</span></span>


```C++
CMyPin::Receive(IMediaSample *pSample)
{
    if (!pSample) return E_POINTER;

    int iStreamState = CheckStreamState(pSample);
    if (iStreamState == STREAM_FLOWING) 
    {
        if (m_fLastSampleDiscarded)
            pSample->SetDiscontinuity(TRUE);
        m_fLastSampleDiscarded = FALSE;
        /* Deliver the sample. */
    } 
    else 
    {
        m_fLastSampleDiscarded = TRUE;  
       // Discard this sample. Do not deliver it.
    }
}
```



## <a name="requirements"></a><span data-ttu-id="adae0-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adae0-130">Requirements</span></span>



| <span data-ttu-id="adae0-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="adae0-131">Requirement</span></span> | <span data-ttu-id="adae0-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="adae0-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adae0-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="adae0-133">Header</span></span><br/>  | <dl> <span data-ttu-id="adae0-134"><dt>Strmctl. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="adae0-134"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="adae0-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="adae0-135">Library</span></span><br/> | <dl> <span data-ttu-id="adae0-136"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="adae0-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adae0-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adae0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adae0-138">**CBaseStreamControl, classe**</span><span class="sxs-lookup"><span data-stu-id="adae0-138">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




