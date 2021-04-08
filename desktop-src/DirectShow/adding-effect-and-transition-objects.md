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
# <a name="adding-effect-and-transition-objects"></a>Ajout d’objets Effect et transition

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Dans DES, un effet ou une transition est représenté par deux objets :

-   Un *objet Timeline* représente l’effet ou la transition dans la chronologie. Pour les effets, l’objet Timeline prend en charge l’interface [**IAMTimelineEffect**](iamtimelineeffect.md) . Pour les transitions, il prend en charge l’interface [**IAMTimelineTrans**](iamtimelinetrans.md) . Les deux types prennent en charge l’interface [**IAMTimelineObj**](iamtimelineobj.md) .
-   Le sous- *objet* est un objet qui implémente le traitement des données pour l’effet ou la transition. L’objet Timeline contient un pointeur vers le sous-objet.

Pour ajouter un effet ou une transition, procédez comme suit.

**1. créer l’objet Timeline**

Pour créer l’objet Timeline, appelez la méthode [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) . Définissez le type sur l' **\_ effet de \_ type \_ principal de chronologie** pour un effet ou une **\_ \_ \_ transition de type principal de chronologie** pour une transition.

L’exemple suivant crée un objet de transition :


```C++
IAMTimelineObj *pTransObj = NULL;
pTimeline->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);
```



**2. spécifiez le sous-objet**

L’objet Timeline agit comme un wrapper pour un autre objet, appelé le sous- *objet*, qui fait le vrai travail. Le sous-objet implémente une transformation de données qui produit l’effet ou la transition souhaité (e). Pour obtenir la liste des transitions et des effets fournis avec DES, consultez [transitions et effets](transitions-and-effects.md).

Pour définir le sous-objet, appelez la méthode [**IAMTimelineObj :: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) sur l’objet Timeline, en lui transmettant l’identificateur de classe (CLSID) du sous-objet. DirectShow fournit un énumérateur pour les effets vidéo et les transitions vidéo, que vous pouvez utiliser pour obtenir le CLSID. Pour plus d’informations, consultez [énumération des effets et des transitions](enumerating-effects-and-transitions.md).

L’exemple suivant définit la [transition de réinitialisation SMPTE](smpte-wipe-transition.md) comme sous-objet :


```C++
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe
```



**3. définir les heures de début et de fin**

Pour définir les heures de début et de fin, appelez la méthode [**IAMTimelineObj :: SetStartStop**](iamtimelineobj-setstartstop.md) . Ces heures sont relatives à l’heure de début de l’objet parent. Les effets peuvent se chevaucher dans le même objet, mais les transitions ne le peuvent pas.

L’exemple suivant définit l’heure de début sur 5 secondes et l’heure d’arrêt sur 10 secondes :


```C++
const REFERENCE_TIME ONE_SECOND = 10000000
hr = pTransObj->SetStartStop(5 * ONE_SECOND, 10 * ONE_SECOND);
```



Lorsqu’une transition est rendue, la progression de la transition à chaque trame est calculée en fonction d’une propriété **Progress** , qui est normalisée en une plage allant de 0,0 à 1,0. DES utilise l’heure de début de chaque trame pour calculer la valeur de progression. Cela signifie que si l’heure d’arrêt de la transition est égale à l’heure d’arrêt de la source, la valeur de **progression** n’atteindra jamais exactement 1,0, car l’heure de début de la dernière trame est légèrement supérieure à l’heure d’arrêt. Pour que la transition atteigne 1,0, définissez l’heure d’arrêt de la transition sur au moins une image antérieure à l’heure d’arrêt source.

**4. Insérer l’objet dans la chronologie**

Pour insérer l’objet dans la chronologie, appelez l’une des méthodes suivantes sur le parent, selon le type d’objet :

-   Effets : [ **IAMTimelineEffectable :: EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)
-   Transitions : [ **IAMTimelineTransable :: TransAdd**](iamtimelinetransable-transadd.md)

Dans la méthode [**IAMTimelineEffectable :: EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md) , vous devez spécifier la priorité de l’effet. Lorsque les effets se chevauchent sur le même objet, ils sont appliqués par ordre de priorité. L’effet audio d’enveloppe de volume est une exception. Pour plus d’informations, consultez la référence d' [effet d’enveloppe de volume](volume-envelope-effect.md) . Au sein d’une composition, toutes les pistes audio sont mélangées avant l’application des effets audio de cette composition.

Étant donné que les transitions ne peuvent pas se chevaucher sur le même objet, elles n’ont pas de valeur de priorité.

L’exemple suivant ajoute l’objet de transition à une piste :


```C++
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
```



L’exemple interroge l’objet Track pour l’interface [**IAMTimelineTransable**](iamtimelinetransable.md) avant d’appeler AddTrans.

**5. définir les propriétés**

De nombreux effets et transitions prennent en charge les propriétés personnalisées. Pour plus d’informations, consultez [définition des propriétés des effets et des transitions](setting-properties-on-effects-and-transitions.md).

Exemple

L’exemple de code suivant ajoute une [transition de réinitialisation SMPTE](smpte-wipe-transition.md) à une piste. Elle suppose que l’objet Track existe déjà dans la chronologie.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des effets et des transitions](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



