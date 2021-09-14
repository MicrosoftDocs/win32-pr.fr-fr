---
description: La classe CSourceStream fournit une broche de sortie pour la classe de filtre CSource.
ms.assetid: 5ccfb129-93e2-4773-9398-5f59f2914ba7
title: Classe CSourceStream (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36b9085df8c15e765c751be8b5fcdfd4f4a02140
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010017"
---
# <a name="csourcestream-class"></a>CSourceStream, classe

![hiérarchie de la classe csourcestream](images/source02.png)

La classe **CSourceStream** fournit une broche de sortie pour la classe de filtre [**CSource**](csource.md) .

Pour plus d’informations sur l’utilisation de cette classe, consultez [**CSource**](csource.md). Cette classe hérite de la classe [**CAMThread**](camthread.md) , qui fournit un thread de travail pour la diffusion en continu des données à partir du code confidentiel. La classe **CSourceStream** implémente les méthodes d’assistance suivantes pour envoyer des demandes au thread :

-   [**CSourceStream :: Exit**](csourcestream-exit.md)
-   [**CSourceStream :: init**](csourcestream-init.md)
-   [**CSourceStream ::P ause**](csourcestream-pause.md)
-   [**CSourceStream :: Run**](csourcestream-run.md)
-   [**CSourceStream :: Stop**](csourcestream-stop.md)

La première requête au thread doit être [**init**](csourcestream-init.md). La demande de [**sortie**](csourcestream-exit.md) met fin au thread. Dans la pratique, il n’est pas nécessaire d’appeler directement l’une de ces méthodes, car les méthodes [**CSourceStream :: active**](csourcestream-active.md) et [**CSourceStream :: inactive**](csourcestream-inactive.md) du pin les appellent en fonction des besoins.

La classe fournit également plusieurs méthodes de « gestionnaire » :

-   [**CSourceStream::OnThreadCreate**](csourcestream-onthreadcreate.md)
-   [**CSourceStream::OnThreadDestroy**](csourcestream-onthreaddestroy.md)
-   [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md)

Celles-ci ne font rien dans la classe de base, mais la classe dérivée peut les substituer.



| Variables membres protégées                                             | Description                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ pFilter**](csourcestream-m-pfilter.md)                          | Pointeur vers le filtre qui contient ce pin.                                                                                     |
| Méthodes protégées                                                      | Description                                                                                                                       |
| [**OnThreadCreate**](csourcestream-onthreadcreate.md)                 | Appelé lorsque le thread de streaming est initialisé. Virtuels.                                                                         |
| [**OnThreadDestroy**](csourcestream-onthreaddestroy.md)               | Appelé lorsque le thread de streaming est sur le point de se fermer. Virtuels.                                                                       |
| [**OnThreadStartPlay**](csourcestream-onthreadstartplay.md)           | Appelée au début de la méthode [**CSourceStream ::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) . Virtuels. |
| [**Actif**](csourcestream-active.md)                                 | Notifie le code confidentiel que le filtre est maintenant actif.                                                                                   |
| [**Inactif**](csourcestream-inactive.md)                             | Notifie le code confidentiel que le filtre n’est plus actif.                                                                             |
| [**GetRequest**](csourcestream-getrequest.md)                         | Attend la demande de thread suivante.                                                                                                |
| [**CheckRequest**](csourcestream-checkrequest.md)                     | Vérifie s’il existe une demande de thread, sans blocage.                                                                            |
| [**ThreadProc**](csourcestream-threadproc.md)                         | Procédure de thread. Virtuels.                                                                                                        |
| [**DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) | Génère des données multimédias et les remet à la broche d’entrée en aval. Virtuels.                                                        |
| [**CheckMediaType**](csourcestream-checkmediatype.md)                 | Détermine si le code PIN accepte un type de média spécifique. Virtuels.                                                                     |
| [**GetMediaType**](csourcestream-getmediatype.md)                     | Récupère un type de média par défaut. Virtuels.                                                                                        |
| M&#233;thodes publiques                                                         | Description                                                                                                                       |
| [**CSourceStream**](csourcestream-csourcestream.md)                   | Méthode de constructeur.                                                                                                               |
| [**~ CSourceStream**](csourcestream--csourcestream.md)                | Méthode de destructeur. Virtuels.                                                                                                       |
| [**Init**](csourcestream-init.md)                                     | Initialise le thread de diffusion en continu.                                                                                                 |
| [**Quitter**](csourcestream-exit.md)                                     | Signale le thread de diffusion en continu à quitter.                                                                                             |
| [**Exécuter**](csourcestream-run.md)                                       | Signale l’exécution du thread de streaming.                                                                                              |
| [**Suspendre**](csourcestream-pause.md)                                   | Signale que le thread de streaming devient actif.                                                                                    |
| [**Arrêter**](csourcestream-stop.md)                                     | Signale l’arrêt du thread de streaming.                                                                                             |
| Méthodes virtuelles pures                                                   | Description                                                                                                                       |
| [**FillBuffer**](csourcestream-fillbuffer.md)                         | Remplit un échantillon de média avec des données.                                                                                                   |
| Méthodes IPin                                                           | Description                                                                                                                       |
| [**QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)                                        | Récupère un identificateur pour le code confidentiel.                                                                                              |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Écriture de filtres source](writing-source-filters.md)
</dt> </dl>

 

 




