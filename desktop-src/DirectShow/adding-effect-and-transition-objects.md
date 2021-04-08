---
description: Ajout d’objets Effect et transition
ms.assetid: fe82392f-33e2-432a-a6e3-710e475547b3
title: Ajout d’objets Effect et transition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6d33ed27faa0c69a755a17c72d9c5b136a4670
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033444"
---
# <a name="adding-effect-and-transition-objects"></a><span data-ttu-id="80ba9-103">Ajout d’objets Effect et transition</span><span class="sxs-lookup"><span data-stu-id="80ba9-103">Adding Effect and Transition Objects</span></span>

<span data-ttu-id="80ba9-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="80ba9-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="80ba9-105">Dans DES, un effet ou une transition est représenté par deux objets :</span><span class="sxs-lookup"><span data-stu-id="80ba9-105">In DES, an effect or transition is represented with two objects:</span></span>

-   <span data-ttu-id="80ba9-106">Un *objet Timeline* représente l’effet ou la transition dans la chronologie.</span><span class="sxs-lookup"><span data-stu-id="80ba9-106">A *timeline object* represents the effect or transition within the timeline.</span></span> <span data-ttu-id="80ba9-107">Pour les effets, l’objet Timeline prend en charge l’interface [**IAMTimelineEffect**](iamtimelineeffect.md) .</span><span class="sxs-lookup"><span data-stu-id="80ba9-107">For effects, the timeline object supports the [**IAMTimelineEffect**](iamtimelineeffect.md) interface.</span></span> <span data-ttu-id="80ba9-108">Pour les transitions, il prend en charge l’interface [**IAMTimelineTrans**](iamtimelinetrans.md) .</span><span class="sxs-lookup"><span data-stu-id="80ba9-108">For transitions, it supports the [**IAMTimelineTrans**](iamtimelinetrans.md) interface.</span></span> <span data-ttu-id="80ba9-109">Les deux types prennent en charge l’interface [**IAMTimelineObj**](iamtimelineobj.md) .</span><span class="sxs-lookup"><span data-stu-id="80ba9-109">Both types support the [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>
-   <span data-ttu-id="80ba9-110">Le sous- *objet* est un objet qui implémente le traitement des données pour l’effet ou la transition.</span><span class="sxs-lookup"><span data-stu-id="80ba9-110">The *subobject* is an object that implements the data processing for the effect or transition.</span></span> <span data-ttu-id="80ba9-111">L’objet Timeline contient un pointeur vers le sous-objet.</span><span class="sxs-lookup"><span data-stu-id="80ba9-111">The timeline object holds a pointer to the subobject.</span></span>

<span data-ttu-id="80ba9-112">Pour ajouter un effet ou une transition, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="80ba9-112">To add an effect or transition, perform the following steps.</span></span>

<span data-ttu-id="80ba9-113">**1. créer l’objet Timeline**</span><span class="sxs-lookup"><span data-stu-id="80ba9-113">**1. Create the Timeline Object**</span></span>

<span data-ttu-id="80ba9-114">Pour créer l’objet Timeline, appelez la méthode [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) .</span><span class="sxs-lookup"><span data-stu-id="80ba9-114">To create the timeline object, call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span> <span data-ttu-id="80ba9-115">Définissez le type sur l' **\_ effet de \_ type \_ principal de chronologie** pour un effet ou une **\_ \_ \_ transition de type principal de chronologie** pour une transition.</span><span class="sxs-lookup"><span data-stu-id="80ba9-115">Set the type equal to **TIMELINE\_MAJOR\_TYPE\_EFFECT** for an effect, or **TIMELINE\_MAJOR\_TYPE\_TRANSITION** for a transition.</span></span>

<span data-ttu-id="80ba9-116">L’exemple suivant crée un objet de transition :</span><span class="sxs-lookup"><span data-stu-id="80ba9-116">The following example creates a transition object:</span></span>


```C++
IAMTimelineObj *pTransObj = NULL;
pTimeline->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);
```



<span data-ttu-id="80ba9-117">**2. spécifiez le sous-objet**</span><span class="sxs-lookup"><span data-stu-id="80ba9-117">**2. Specify the Subobject**</span></span>

<span data-ttu-id="80ba9-118">L’objet Timeline agit comme un wrapper pour un autre objet, appelé le sous- *objet*, qui fait le vrai travail.</span><span class="sxs-lookup"><span data-stu-id="80ba9-118">The timeline object acts as a wrapper for another object, called the *subobject*, which does the real work.</span></span> <span data-ttu-id="80ba9-119">Le sous-objet implémente une transformation de données qui produit l’effet ou la transition souhaité (e).</span><span class="sxs-lookup"><span data-stu-id="80ba9-119">The subobject implements a data transform that produces the desired effect or transition.</span></span> <span data-ttu-id="80ba9-120">Pour obtenir la liste des transitions et des effets fournis avec DES, consultez [transitions et effets](transitions-and-effects.md).</span><span class="sxs-lookup"><span data-stu-id="80ba9-120">For a list of transitions and effects supplied with DES, see [Transitions and Effects](transitions-and-effects.md).</span></span>

<span data-ttu-id="80ba9-121">Pour définir le sous-objet, appelez la méthode [**IAMTimelineObj :: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) sur l’objet Timeline, en lui transmettant l’identificateur de classe (CLSID) du sous-objet.</span><span class="sxs-lookup"><span data-stu-id="80ba9-121">To set the subobject, call the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method on the timeline object, passing it the class identifier (CLSID) of the subobject.</span></span> <span data-ttu-id="80ba9-122">DirectShow fournit un énumérateur pour les effets vidéo et les transitions vidéo, que vous pouvez utiliser pour obtenir le CLSID.</span><span class="sxs-lookup"><span data-stu-id="80ba9-122">DirectShow provides an enumerator for video effects and video transitions, which you can use to obtain the CLSID.</span></span> <span data-ttu-id="80ba9-123">Pour plus d’informations, consultez [énumération des effets et des transitions](enumerating-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="80ba9-123">For more information, see [Enumerating Effects and Transitions](enumerating-effects-and-transitions.md).</span></span>

<span data-ttu-id="80ba9-124">L’exemple suivant définit la [transition de réinitialisation SMPTE](smpte-wipe-transition.md) comme sous-objet :</span><span class="sxs-lookup"><span data-stu-id="80ba9-124">The following example sets the [SMPTE Wipe Transition](smpte-wipe-transition.md) as the subobject :</span></span>


```C++
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe
```



<span data-ttu-id="80ba9-125">**3. définir les heures de début et de fin**</span><span class="sxs-lookup"><span data-stu-id="80ba9-125">**3. Set the Start and Stop Times**</span></span>

<span data-ttu-id="80ba9-126">Pour définir les heures de début et de fin, appelez la méthode [**IAMTimelineObj :: SetStartStop**](iamtimelineobj-setstartstop.md) .</span><span class="sxs-lookup"><span data-stu-id="80ba9-126">To set the start and stop times, call the [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) method.</span></span> <span data-ttu-id="80ba9-127">Ces heures sont relatives à l’heure de début de l’objet parent.</span><span class="sxs-lookup"><span data-stu-id="80ba9-127">These times are relative to the start time of the parent object.</span></span> <span data-ttu-id="80ba9-128">Les effets peuvent se chevaucher dans le même objet, mais les transitions ne le peuvent pas.</span><span class="sxs-lookup"><span data-stu-id="80ba9-128">Effects can overlap within the same object, but transitions cannot.</span></span>

<span data-ttu-id="80ba9-129">L’exemple suivant définit l’heure de début sur 5 secondes et l’heure d’arrêt sur 10 secondes :</span><span class="sxs-lookup"><span data-stu-id="80ba9-129">The following example sets the start time to 5 seconds and the stop time to 10 seconds:</span></span>


```C++
const REFERENCE_TIME ONE_SECOND = 10000000
hr = pTransObj->SetStartStop(5 * ONE_SECOND, 10 * ONE_SECOND);
```



<span data-ttu-id="80ba9-130">Lorsqu’une transition est rendue, la progression de la transition à chaque trame est calculée en fonction d’une propriété **Progress** , qui est normalisée en une plage allant de 0,0 à 1,0.</span><span class="sxs-lookup"><span data-stu-id="80ba9-130">When a transition is rendered, the progress of the transition at each frame is calculated based on a **Progress** property, which is normalized to a range of 0.0 to 1.0.</span></span> <span data-ttu-id="80ba9-131">DES utilise l’heure de début de chaque trame pour calculer la valeur de progression.</span><span class="sxs-lookup"><span data-stu-id="80ba9-131">DES uses the start time of each frame to calculate the progress value.</span></span> <span data-ttu-id="80ba9-132">Cela signifie que si l’heure d’arrêt de la transition est égale à l’heure d’arrêt de la source, la valeur de **progression** n’atteindra jamais exactement 1,0, car l’heure de début de la dernière trame est légèrement supérieure à l’heure d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="80ba9-132">This means if the transition stop time is equal to the source stop time, the **Progress** value will never reach exactly 1.0, because the start time of the last frame is slightly than the stop time.</span></span> <span data-ttu-id="80ba9-133">Pour que la transition atteigne 1,0, définissez l’heure d’arrêt de la transition sur au moins une image antérieure à l’heure d’arrêt source.</span><span class="sxs-lookup"><span data-stu-id="80ba9-133">To make the transition reach 1.0, set the transition stop time to be at least one frame earlier than the source stop time.</span></span>

<span data-ttu-id="80ba9-134">**4. Insérer l’objet dans la chronologie**</span><span class="sxs-lookup"><span data-stu-id="80ba9-134">**4. Insert the Object into the Timeline**</span></span>

<span data-ttu-id="80ba9-135">Pour insérer l’objet dans la chronologie, appelez l’une des méthodes suivantes sur le parent, selon le type d’objet :</span><span class="sxs-lookup"><span data-stu-id="80ba9-135">To insert the object into the timeline, call one of the following methods on the parent, depending on the object type:</span></span>

-   <span data-ttu-id="80ba9-136">Effets : [ **IAMTimelineEffectable :: EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)</span><span class="sxs-lookup"><span data-stu-id="80ba9-136">Effects: [**IAMTimelineEffectable::EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)</span></span>
-   <span data-ttu-id="80ba9-137">Transitions : [ **IAMTimelineTransable :: TransAdd**](iamtimelinetransable-transadd.md)</span><span class="sxs-lookup"><span data-stu-id="80ba9-137">Transitions: [**IAMTimelineTransable::TransAdd**](iamtimelinetransable-transadd.md)</span></span>

<span data-ttu-id="80ba9-138">Dans la méthode [**IAMTimelineEffectable :: EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md) , vous devez spécifier la priorité de l’effet.</span><span class="sxs-lookup"><span data-stu-id="80ba9-138">In the [**IAMTimelineEffectable::EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md) method, you must specify the priority of the effect.</span></span> <span data-ttu-id="80ba9-139">Lorsque les effets se chevauchent sur le même objet, ils sont appliqués par ordre de priorité.</span><span class="sxs-lookup"><span data-stu-id="80ba9-139">When effects overlap on the same object, they are applied in order of priority.</span></span> <span data-ttu-id="80ba9-140">L’effet audio d’enveloppe de volume est une exception. Pour plus d’informations, consultez la référence d' [effet d’enveloppe de volume](volume-envelope-effect.md) .</span><span class="sxs-lookup"><span data-stu-id="80ba9-140">The Volume Envelope audio effect is an exception; see the [Volume Envelope Effect](volume-envelope-effect.md) reference for details.</span></span> <span data-ttu-id="80ba9-141">Au sein d’une composition, toutes les pistes audio sont mélangées avant l’application des effets audio de cette composition.</span><span class="sxs-lookup"><span data-stu-id="80ba9-141">Within a composition, all audio tracks are mixed before the audio effects for that composition are applied.</span></span>

<span data-ttu-id="80ba9-142">Étant donné que les transitions ne peuvent pas se chevaucher sur le même objet, elles n’ont pas de valeur de priorité.</span><span class="sxs-lookup"><span data-stu-id="80ba9-142">Because transitions cannot overlap on the same object, they do not have a priority value.</span></span>

<span data-ttu-id="80ba9-143">L’exemple suivant ajoute l’objet de transition à une piste :</span><span class="sxs-lookup"><span data-stu-id="80ba9-143">The following example adds the transition object to a track:</span></span>


```C++
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
```



<span data-ttu-id="80ba9-144">L’exemple interroge l’objet Track pour l’interface [**IAMTimelineTransable**](iamtimelinetransable.md) avant d’appeler AddTrans.</span><span class="sxs-lookup"><span data-stu-id="80ba9-144">The example queries the track object for the [**IAMTimelineTransable**](iamtimelinetransable.md) interface before calling AddTrans.</span></span>

<span data-ttu-id="80ba9-145">**5. définir les propriétés**</span><span class="sxs-lookup"><span data-stu-id="80ba9-145">**5. Set Properties**</span></span>

<span data-ttu-id="80ba9-146">De nombreux effets et transitions prennent en charge les propriétés personnalisées.</span><span class="sxs-lookup"><span data-stu-id="80ba9-146">Many effects and transitions support custom properties.</span></span> <span data-ttu-id="80ba9-147">Pour plus d’informations, consultez [définition des propriétés des effets et des transitions](setting-properties-on-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="80ba9-147">For information, see [Setting Properties on Effects and Transitions](setting-properties-on-effects-and-transitions.md).</span></span>

<span data-ttu-id="80ba9-148">Exemple</span><span class="sxs-lookup"><span data-stu-id="80ba9-148">Example</span></span>

<span data-ttu-id="80ba9-149">L’exemple de code suivant ajoute une [transition de réinitialisation SMPTE](smpte-wipe-transition.md) à une piste. Elle suppose que l’objet Track existe déjà dans la chronologie.</span><span class="sxs-lookup"><span data-stu-id="80ba9-149">The following code example adds a [SMPTE Wipe Transition](smpte-wipe-transition.md) to a track. It assumes that the track object already exists in the timeline.</span></span>


```C++
IAMTimeline *pTL;
IAMTimelineTrack *pTrack;

// Create timeline with track (not shown).

// Create the transition object. 
IAMTimelineObj *pTransObj = NULL;
hr = pTL->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);

// Set the subobject. 
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe

// Set the start and stop times. 
hr = pTransObj->SetStartStop(50000000, 100000000);

// Insert the transition object into the timeline. 
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
pTransObj->Release();
```



## <a name="related-topics"></a><span data-ttu-id="80ba9-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="80ba9-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80ba9-151">Utilisation des effets et des transitions</span><span class="sxs-lookup"><span data-stu-id="80ba9-151">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



