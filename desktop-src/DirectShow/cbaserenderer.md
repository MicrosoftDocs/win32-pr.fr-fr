---
description: La classe CBaseRenderer est une classe de base pour l’implémentation de filtres de convertisseur.
ms.assetid: 8d39d3bd-6162-402e-a4b3-0f35d3e29b96
title: CBaseRenderer, classe (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81e529493bfd892607748423bb1bab9016eb232aaeb3ed22287fa2c1c1917687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954802"
---
# <a name="cbaserenderer-class"></a>CBaseRenderer, classe

![hiérarchie de la classe cbaserenderer](images/rbase02.png)

La `CBaseRenderer` classe est une classe de base pour l’implémentation de filtres de convertisseur. Il prend en charge une broche d’entrée, implémentée par la classe [**CRendererInputPin**](crendererinputpin.md) . Pour utiliser cette classe, déclarez une classe dérivée qui hérite de `CBaseRenderer` . Au minimum, la classe dérivée doit implémenter les méthodes suivantes, qui sont déclarées comme virtuelles pures dans la classe de base :

-   [**CBaseRenderer :: CheckMediaType**](cbaserenderer-checkmediatype.md): accepte ou rejette les types de média proposés. Le filtre appelle cette méthode pendant le processus de connexion du code confidentiel.
-   [**CBaseRenderer ::D orendersample**](cbaserenderer-dorendersample.md): restitue un exemple. Le filtre appelle cette méthode pour chaque exemple qu’il reçoit en cours d’exécution.

La classe de base gère les changements d’État et les problèmes de synchronisation. Il planifie également des exemples de rendu, bien qu’il n’implémente aucune mesure de contrôle de qualité. La classe de base déclare également plusieurs méthodes « handler ». Il s’agit des méthodes que le filtre appelle à des points spécifiques dans le processus de diffusion en continu. Elles ne font rien dans la classe de base, mais la classe dérivée peut les substituer. Dans le tableau qui suit, elles sont répertoriées sous l’en-tête méthodes publiques : gestionnaires.

Le gestionnaire [**CBaseRenderer :: OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) mérite une mention spéciale. Le filtre appelle cette méthode s’il reçoit un exemple alors que le filtre est suspendu. Cela peut se produire si le graphique passe de arrêté à suspendu, ou si le graphique est cherché pendant la suspension. Les convertisseurs vidéo utilisent généralement l’exemple pour afficher une image continue. Lorsque le filtre passe de suspendu à en cours d’exécution, il envoie le même échantillon à la méthode [**CBaseRenderer ::D orendersample**](cbaserenderer-dorendersample.md) , comme premier échantillon dans le flux.

La `CBaseRenderer` classe expose les interfaces **IMediaSeeking** et **IMediaPosition** via l’objet [**CRendererPosPassThru**](crendererpospassthru.md) . Elle transmet toutes les demandes de recherche au filtre suivant en amont.

## <a name="scheduling"></a>Planification

Lorsque le filtre amont appelle la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) du code confidentiel d’entrée pour remettre un exemple, le code PIN passe cet appel à la méthode [**CBaseRenderer :: Receive**](cbaserenderer-receive.md) du filtre. Le filtre supprime l’exemple, le restitue immédiatement ou le planifie en vue d’un rendu.

Si l’exemple n’a pas de datage, ou si aucune horloge de référence n’est disponible, le filtre restitue l’exemple immédiatement. Dans le cas contraire, le filtre appelle la méthode [**CBaseRenderer :: ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) pour déterminer la marche à suivre. Par défaut, l’exemple est planifié en fonction de ses horodatages. La classe dérivée peut substituer **ShouldDrawSampleNow** pour prendre en charge le contrôle de qualité.

Pour planifier un exemple, le filtre appelle la méthode [**IReferenceClock :: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) , qui crée une demande de notification. La méthode [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) est ensuite bloquée jusqu’à l’heure planifiée, ou jusqu’à ce que le filtre change d’État. Le blocage empêche le filtre en amont de générer plus d’échantillons jusqu’à ce que l’exemple actuel soit rendu.

Lorsque le filtre en amont appelle la méthode [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) pour signaler la fin du flux, le filtre envoie un événement [**EC \_ complet**](ec-complete.md) au gestionnaire du graphique de filtres. Le filtre attend l’heure d’arrêt de l’exemple actuel avant d’envoyer l’événement.



| Variables membres protégées                                                   | Description                                                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ bAbort**](cbaserenderer-m-babort.md)                                  | Indicateur qui spécifie s’il faut arrêter le rendu et rejeter d’autres exemples.                                                               |
| [**m \_ bEOS**](cbaserenderer-m-beos.md)                                      | Indicateur qui spécifie si la fin de flux a été atteinte.                                                                                  |
| [**m \_ bEOSDelivered**](cbaserenderer-m-beosdelivered.md)                    | Indicateur qui spécifie si le filtre a publié l' \_ événement EC Complete.                                                               |
| [**m \_ bInReceive**](cbaserenderer-m-binreceive.md)                          | Indicateur qui spécifie si le filtre traite un appel de **réception** .                                                                |
| [**m \_ bRepaintStatus**](cbaserenderer-m-brepaintstatus.md)                  | Indicateur qui active ou désactive les événements de redessin.                                                                                           |
| [**m \_ bStreaming**](cbaserenderer-m-bstreaming.md)                          | Indicateur qui spécifie si le filtre diffuse des données.                                                                               |
| [**m \_ dwAdvise**](cbaserenderer-m-dwadvise.md)                              | Identificateur de l’événement de minuterie qui planifie le rendu.                                                                                 |
| [**m \_ EndOfStreamTimer**](cbaserenderer-m-endofstreamtimer.md)              | Minuterie-identificateur d’événement, pour la planification \_ des notifications complètes ec.                                                                      |
| [**m \_ evComplete**](cbaserenderer-m-evcomplete.md)                          | Événement signalé lorsqu’une transition d’État est terminée.                                                                             |
| [**m \_ InterfaceLock**](cbaserenderer-m-interfacelock.md)                    | Verrou d’état de filtre.                                                                                                                      |
| [**m \_ ObjectCreationLock**](cbaserenderer-m-objectcreationlock.md)          | Verrou pour protéger la création d’objets à l’intérieur du filtre.                                                                              |
| [**m \_ pInputPin**](cbaserenderer-m-pinputpin.md)                            | Pointeur vers la broche d’entrée du filtre.                                                                                                      |
| [**m \_ pMediaSample**](cbaserenderer-m-pmediasample.md)                      | Pointeur vers l’exemple de média actuel.                                                                                                    |
| [**m \_ pPosition**](cbaserenderer-m-pposition.md)                            | Objet d’assistance pour passer les commandes de recherche en amont.                                                                                           |
| [**m \_ pQSink**](cbaserenderer-m-pqsink.md)                                  | Pointeur vers l’objet qui reçoit les messages de contrôle de qualité.                                                                           |
| [**m \_ RendererLock**](cbaserenderer-m-rendererlock.md)                      | Verrou de streaming.                                                                                                                         |
| [**m \_ RenderEvent**](cbaserenderer-m-renderevent.md)                        | Événement utilisé pour planifier le rendu.                                                                                                       |
| [**m \_ SignalTime**](cbaserenderer-m-signaltime.md)                          | Arrête l’heure sur l’échantillon actuel.                                                                                                        |
| [**m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md)                      | Événement utilisé pour libérer le thread de streaming.                                                                                             |
| M&#233;thodes publiques                                                               | Description                                                                                                                             |
| [**CancelNotification**](cbaserenderer-cancelnotification.md)               | Annule l’événement du minuteur qui planifie le rendu. Virtuels.                                                                              |
| [**CBaseRenderer**](cbaserenderer-cbaserenderer.md)                         | Méthode de constructeur.                                                                                                                     |
| [**~ CBaseRenderer**](cbaserenderer--cbaserenderer.md)                       | Méthode de destructeur.                                                                                                                      |
| [**GetMediaPositionInterface**](cbaserenderer-getmediapositioninterface.md) | Récupère les pointeurs d’interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) et [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) du filtre. Virtuels. |
| [**GetPin**](cbaserenderer-getpin.md)                                       | Récupère un code confidentiel. Virtuels.                                                                                                               |
| [**GetPinCount**](cbaserenderer-getpincount.md)                             | Récupère le nombre de broches. Virtuels.                                                                                                  |
| [**GetSampleTimes**](cbaserenderer-getsampletimes.md)                       | Récupère les horodatages d’un exemple. Virtuels.                                                                                       |
| [**OnDisplayChange**](cbaserenderer-ondisplaychange.md)                     | Publie un événement de [**\_ \_ modification d’affichage EC**](ec-display-changed.md) dans le gestionnaire de graphique de filtre.                                          |
| [**PrepareReceive**](cbaserenderer-preparereceive.md)                       | Prépare le rendu d’un exemple. Virtuels.                                                                                                   |
| [**Çoive**](cbaserenderer-receive.md)                                     | Reçoit l’échantillon de média suivant dans le flux. Virtuels.                                                                                  |
| [**Crée**](cbaserenderer-render.md)                                       | Restitue un exemple. Virtuels.                                                                                                              |
| [**ScheduleSample**](cbaserenderer-schedulesample.md)                       | Planifie un exemple de rendu. Virtuels.                                                                                              |
| [**SendNotifyWindow**](cbaserenderer-sendnotifywindow.md)                   | Notifie le filtre amont du handle de fenêtre vidéo.                                                                                |
| [**SendRepaint**](cbaserenderer-sendrepaint.md)                             | Envoie un événement Repaint au gestionnaire de graphique de filtre.                                                                                      |
| [**SetMediaType**](cbaserenderer-setmediatype.md)                           | Appelée lorsque le type de média du pin est défini. Virtuels.                                                                                       |
| [**SignalTimerFired**](cbaserenderer-signaltimerfired.md)                   | Efface l’identificateur de minuterie utilisé pour planifier le rendu.                                                                                 |
| [**SourceThreadCanWait**](cbaserenderer-sourcethreadcanwait.md)             | Contient ou libère le thread de streaming. Virtuels.                                                                                        |
| [**WaitForReceiveToComplete**](cbaserenderer-waitforreceivetocomplete.md)   | Attend la fin de la méthode [**CBaseRenderer :: Receive**](cbaserenderer-receive.md) .                                               |
| [**WaitForRenderTime**](cbaserenderer-waitforrendertime.md)                 | Attend l’heure de présentation de l’exemple actuel. Virtuels.                                                                              |
| Méthodes publiques : méthodes d’accesseur                                             | Description                                                                                                                             |
| [**ClearPendingSample**](cbaserenderer-clearpendingsample.md)               | Libère l’exemple actuel. Virtuels.                                                                                                   |
| [**GetCurrentSample**](cbaserenderer-getcurrentsample.md)                   | Récupère l’exemple actuel. Virtuels.                                                                                                  |
| [**GetRealState**](cbaserenderer-getrealstate.md)                           | Récupère l’état du filtre.                                                                                                             |
| [**GetRenderEvent**](cbaserenderer-getrenderevent.md)                       | Récupère l’événement qui planifie le rendu.                                                                                           |
| [**HaveCurrentSample**](cbaserenderer-havecurrentsample.md)                 | Détermine si le filtre a un exemple. Virtuels.                                                                                    |
| [**IsEndOfStream**](cbaserenderer-isendofstream.md)                         | Interroge si la notification de fin de flux a été reçue.                                                                            |
| [**IsEndOfStreamDelivered**](cbaserenderer-isendofstreamdelivered.md)       | Interroge si l' \_ événement de la totalité du fait a été remis au gestionnaire du graphique de filtres.                                                  |
| [**IsStreaming**](cbaserenderer-isstreaming.md)                             | Interroge si le filtre diffuse des données.                                                                                           |
| [**SetAbortSignal**](cbaserenderer-setabortsignal.md)                       | Définit un indicateur qui spécifie s’il faut arrêter le rendu et rejeter d’autres exemples.                                                       |
| [**SetRepaintStatus**](cbaserenderer-setrepaintstatus.md)                   | Active ou désactive les événements de redessin.                                                                                                     |
| Méthodes publiques : méthodes State-Change                                         | Description                                                                                                                             |
| [**Actif**](cbaserenderer-active.md)                                       | Appelé lorsque l’état passe à suspendu ou en cours d’exécution. Virtuels.                                                                        |
| [**BeginFlush**](cbaserenderer-beginflush.md)                               | Commence une opération de vidage. Virtuels.                                                                                                      |
| [**BreakConnect**](cbaserenderer-breakconnect.md)                           | Libère la broche d’entrée d’une connexion. Virtuels.                                                                                      |
| [**CheckReady**](cbaserenderer-checkready.md)                               | Interroge si une transition d’État est terminée.                                                                                         |
| [**CompleteConnect**](cbaserenderer-completeconnect.md)                     | Termine la connexion de la broche d’entrée à une autre broche. Virtuels.                                                                           |
| [**CompleteStateChange**](cbaserenderer-completestatechange.md)             | Détermine si une transition vers l’état suspendu est terminée. Virtuels.                                                               |
| [**EndFlush**](cbaserenderer-endflush.md)                                   | Termine une opération de vidage. Virtuels.                                                                                                        |
| [**Inactive**](cbaserenderer-inactive.md)                                   | Appelé lorsque l’état passe à arrêté. Virtuels.                                                                                  |
| [**NotReady**](cbaserenderer-notready.md)                                   | Signale qu’une transition d’État n’est pas encore terminée.                                                                                    |
| [**Ready**](cbaserenderer-ready.md)                                         | Signale qu’une transition d’État est terminée.                                                                                            |
| [**StartStreaming**](cbaserenderer-startstreaming.md)                       | Lance la diffusion en continu lorsque le filtre passe à l’État en cours d’exécution. Virtuels.                                                               |
| [**StopStreaming**](cbaserenderer-stopstreaming.md)                         | Arrête la diffusion en continu lorsque le filtre sort de l’État en cours d’exécution. Virtuels.                                                             |
| Méthodes publiques : méthodes de fin de flux                                        | Description                                                                                                                             |
| [**EndOfStream**](cbaserenderer-endofstream.md)                             | Notifie le filtre que la broche d’entrée a reçu une notification de fin de flux. Virtuels.                                                 |
| [**NotifyEndOfStream**](cbaserenderer-notifyendofstream.md)                 | Publie un événement [**EC \_ complet**](ec-complete.md) dans le gestionnaire du graphique de filtres.                                                         |
| [**ResetEndOfStream**](cbaserenderer-resetendofstream.md)                   | Réinitialise les indicateurs de fin de flux.                                                                                                         |
| [**ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md)         | Annule la minuterie qui planifie les \_ notifications complètes ec. Virtuels.                                                                   |
| [**SendEndOfStream**](cbaserenderer-sendendofstream.md)                     | Si la fin du flux a été atteinte, planifie un \_ événement d’achèvement ce pour le gestionnaire de graphes de filtre. Virtuels.                                    |
| [**TimerCallback**](cbaserenderer-timercallback.md)                         | Méthode de rappel pour l’événement de minuterie de fin de flux.                                                                                      |
| Méthodes publiques : gestionnaires                                                     | Description                                                                                                                             |
| [**OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)           | Appelé lorsque le filtre reçoit un exemple en pause. Virtuels.                                                                         |
| [**OnRenderEnd**](cbaserenderer-onrenderend.md)                             | Appelé après le rendu d’un exemple. Virtuels.                                                                                             |
| [**OnRenderStart**](cbaserenderer-onrenderstart.md)                         | Appelé lorsque le rendu est sur le le début. Virtuels.                                                                                       |
| [**OnStartStreaming**](cbaserenderer-onstartstreaming.md)                   | Appelé lorsque le filtre commence la diffusion en continu. Virtuels.                                                                                       |
| [**OnStopStreaming**](cbaserenderer-onstopstreaming.md)                     | Appelé lorsque le filtre arrête la diffusion en continu. Virtuels.                                                                                        |
| [**OnWaitEnd**](cbaserenderer-onwaitend.md)                                 | Appelé lorsque le filtre est terminé en attendant l’heure de la présentation d’un exemple. Virtuels.                                                       |
| [**OnWaitStart**](cbaserenderer-onwaitstart.md)                             | Appelé lorsque le filtre commence à attendre l’heure de la présentation d’un exemple. Virtuels.                                                        |
| [**PrepareRender**](cbaserenderer-preparerender.md)                         | Appelé avant que le filtre ne restitue un exemple. Virtuels.                                                                                     |
| [**ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md)             | Détermine la façon dont un échantillon est planifié pour le rendu. Virtuels.                                                                            |
| Méthodes virtuelles pures                                                         | Description                                                                                                                             |
| [**CheckMediaType**](cbaserenderer-checkmediatype.md)                       | Détermine si le filtre accepte un type de média spécifique.                                                                                 |
| [**DoRenderSample**](cbaserenderer-dorendersample.md)                       | Restitue un exemple.                                                                                                                       |
| Méthodes IMediaFilter                                                         | Description                                                                                                                             |
| [**GetState**](cbaserenderer-getstate.md)                                   | Récupère l’état du filtre (en cours d’exécution, arrêté ou suspendu).                                                                             |
| [**Suspendre**](cbaserenderer-pause.md)                                         | Suspend le filtre.                                                                                                                      |
| [**Exécuter**](cbaserenderer-run.md)                                             | Permet d'exécuter le filtre.                                                                                                                        |
| [**Erreur**](cbaserenderer-stop.md)                                           | Arrête le filtre.                                                                                                                       |
| Méthodes IBaseFilter                                                          | Description                                                                                                                             |
| [**FindPin**](cbaserenderer-findpin.md)                                     | Récupère le code confidentiel avec l’identificateur spécifié.                                                                                        |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




