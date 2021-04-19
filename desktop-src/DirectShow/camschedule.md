---
description: La classe CAMSchedule implémente un planificateur pour les horloges de référence.
ms.assetid: 67aacffb-b781-4323-8973-355a76821401
title: CAMSchedule, classe (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bef8ad07347284c53a3490c21032070788fa3ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533151"
---
# <a name="camschedule-class"></a>CAMSchedule, classe

La `CAMSchedule` classe implémente un planificateur pour les horloges de référence.



| M&#233;thodes publiques                                             | Description                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**CAMSchedule**](camschedule-camschedule.md)             | Méthode de constructeur.                                                                  |
| [**~ CAMSchedule**](camschedule--camschedule.md)           | Méthode de destructeur. Virtuels.                                                          |
| [**GetAdviseCount**](camschedule-getadvisecount.md)       | Récupère le nombre de demandes de notification en attente.                                     |
| [**GetNextAdviseTime**](camschedule-getnextadvisetime.md) | Récupère l’heure de la demande de notification suivante.                                       |
| [**AddAdvisePacket**](camschedule-addadvisepacket.md)     | Ajoute une demande de notification à la liste des demandes en attente.                              |
| [**Arrêter**](camschedule-unadvise.md)                   | Supprime une demande de notification.                                                           |
| [**Lui**](camschedule-advise.md)                       | Distribue toutes les demandes planifiées pour une heure spécifiée ou antérieure.          |
| [**GetEvent**](camschedule-getevent.md)                   | Récupère un handle d’événement, qui est utilisé pour signaler une modification de l’heure suivante de l’avis. |



 

## <a name="remarks"></a>Notes

Cet objet d’assistance gère une liste de demandes de notification pour une horloge de référence. La classe [**CBaseReferenceClock**](cbasereferenceclock.md) l’utilise pour aider à planifier les demandes de notification. Les horloges utilisent cet objet de la manière suivante :

1.  L’horloge crée un thread de travail pour gérer la planification.
2.  Le thread de travail appelle la méthode [**CAMSchedule :: GetEvent**](camschedule-getevent.md) pour récupérer un handle d’événement à partir du planificateur. Il attend cet événement, initialement avec un délai d’attente infini.
3.  Pour planifier une nouvelle demande de notification, l’horloge appelle la méthode [**CAMSchedule :: AddAdvisePacket**](camschedule-addadvisepacket.md) . Une demande de notification peut être à une seule capture ou périodique. Le planificateur conserve la liste des demandes dans l’ordre chronologique.
4.  Si une demande est ajoutée au début de la liste, le planificateur signale l’événement. (La liste est vide au début, donc la première demande est garantie pour signaler l’événement.)
5.  Lorsque l’événement est signalé, le thread de travail appelle la méthode [**CAMSchedule :: Advise**](camschedule-advise.md) , en spécifiant le temps de référence actuel. Si des demandes en attente ont expiré, le planificateur les distribue.
6.  La méthode Advise retourne l’heure de la requête suivante. Le thread de travail utilise cette valeur pour calculer une nouvelle valeur de délai d’attente.
7.  Les étapes 2 6 se répètent indéfiniment.
8.  Pour terminer le thread de travail, l’horloge définit un indicateur interne et signale l’événement.

À l’étape 2, soit l’événement est signalé, soit l’attente expire. Si l’événement est signalé, cela signifie qu’une nouvelle demande a été ajoutée au début de la liste. Le thread de travail doit calculer une nouvelle valeur de délai d’attente. En revanche, si l’attente expire, cela signifie qu’une demande de notification est arrivée à échéance et doit être distribuée. L’appel à Advise à l’étape 5 gère les deux cas.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Dsschedule. h (include streams. h)</dt> </dl>                                                                                |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




