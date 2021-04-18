---
description: La classe CBaseReferenceClock implémente une horloge de référence.
ms.assetid: 898e1968-a9ab-4bb9-abf0-943bfae502e2
title: CBaseReferenceClock, classe (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1da55a57faac201a2dbf0ef4d8a9774157d9215d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526737"
---
# <a name="cbasereferenceclock-class"></a>CBaseReferenceClock, classe

![hiérarchie de la classe cbasereferenceclock](images/rclock01.png)

La `CBaseReferenceClock` classe implémente une horloge de référence.



| Variables membres protégées                                                         | Description                                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m \_ pSchedule**](cbasereferenceclock-m-pschedule.md)                            | Objet [**CAMSchedule**](camschedule.md) qui gère les tâches de planification pour l’horloge. |
| Méthodes protégées                                                                  | Description                                                                            |
| [**~ CBaseReferenceClock**](cbasereferenceclock--cbasereferenceclock.md)           | Méthode de destructeur.                                                                     |
| M&#233;thodes publiques                                                                     | Description                                                                            |
| [**CBaseReferenceClock**](cbasereferenceclock-cbasereferenceclock.md)             | Méthode de constructeur.                                                                    |
| [**GetPrivateTime**](cbasereferenceclock-getprivatetime.md)                       | Récupère le temps réel à partir de l’horloge.                                                |
| [**SetTimeDelta**](cbasereferenceclock-settimedelta.md)                           | Ajuste l’heure de l’horloge interne.                                                       |
| [**GetSchedule**](cbasereferenceclock-getschedule.md)                             | Récupère un pointeur vers l’objet de planification de l’horloge.                                  |
| [**TriggerThread**](cbasereferenceclock-triggerthread.md)                         | Sort le thread de travail qui gère la planification.                                    |
| Méthodes IReferenceClock                                                            | Description                                                                            |
| [**GetTime**](cbasereferenceclock-gettime.md)                                     | Récupère le temps de référence actuel.                                                  |
| [**AdviseTime**](cbasereferenceclock-advisetime.md)                               | Crée une demande de notification à une seule capture.                                                     |
| [**AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md)                       | Crée une demande de notification périodique.                                                     |
| [**Arrêter**](cbasereferenceclock-unadvise.md)                                   | Supprime une demande de notification en attente.                                                      |
| Méthodes IReferenceClockTimerControl                                                | Description                                                                            |
| [**GetDefaultTimerResolution**](cbasereferenceclock-getdefaulttimerresolution.md) | Retourne la résolution actuelle de la minuterie de l’horloge de référence.                         |
| [**SetDefaultTimerResolution**](cbasereferenceclock-setdefaulttimerresolution.md) | Définit la résolution de la minuterie de l’horloge de référence.                                    |
| Fonctions d’assistance                                                                   | Description                                                                            |
| [**ConvertToMilliseconds**](converttomilliseconds.md)                             | Convertit une durée de référence en millisecondes.                                             |



 

## <a name="remarks"></a>Notes

Cette classe implémente une horloge de référence qui prend en charge les interfaces [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) et [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) . Si un filtre peut fournir une horloge de référence pour le graphique de filtre, par exemple, en accédant à un périphérique matériel, il peut utiliser cette classe pour implémenter l’horloge.

L' `CBaseReferenceClock` objet gère deux valeurs d’heure distinctes :

-   En interne, la méthode [**CBaseReferenceClock :: GetPrivateTime**](cbasereferenceclock-getprivatetime.md) retourne l’heure réelle conservée par l’horloge.
-   En externe, la méthode [**CBaseReferenceClock :: getTime**](cbasereferenceclock-gettime.md) retourne le temps de référence pour le graphique de filtre.

Il est valide que l’horloge interne s’exécute sur de courtes périodes. Par exemple, si l’horloge dérive vers l’avant, le filtre peut l’ajuster en arrière. (Voir [**CBaseReferenceClock :: SetTimeDelta**](cbasereferenceclock-settimedelta.md).) La méthode **getTime** utilise les valeurs d’heure indiquées par **GetPrivateTime**. Toutefois, le temps de référence croît de façon monotone ; en d’autres termes, il ne s’exécute jamais en arrière. Par conséquent, si l’horloge interne s’exécute en arrière, **getTime** continue à signaler l’ancienne fois jusqu’à ce que l’horloge interne rattrape.

Par exemple, les deux méthodes peuvent retourner les séquences suivantes :

``` syntax
GetPrivateTime: 105, 106, 103, 104, 105, 106, 107, 108
GetTime:        105, 106, 106, 106, 106, 106, 107, 108
```

Le troisième cycle d’horloge, l’horloge interne passe à 103. La méthode **getTime** continue à signaler 106 jusqu’à ce que l’horloge interne rattrape.

Par défaut, **GetPrivateTime** retourne l’heure système, via un appel à la fonction **timeGetTime** . Un filtre qui fournit une horloge de référence à partir d’un périphérique externe peut effectuer l’une des opérations suivantes :

-   Remplacez **GetPrivateTime** pour retourner l’heure à partir de l’appareil.
-   Surveillez l’écart entre l’heure de l’appareil et l’heure système, puis appelez **SetTimeDelta** pour effectuer des corrections.

Cette classe utilise un objet [**CAMSchedule**](camschedule.md) pour gérer la planification des demandes de notification. Pour plus d’informations, consultez la documentation de la classe **CAMSchedule** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Refclock. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




