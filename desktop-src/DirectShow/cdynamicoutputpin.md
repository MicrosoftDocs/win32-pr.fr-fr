---
description: La classe CDynamicOutputPin implémente une broche de sortie qui prend en charge les reconnexions dynamiques et les modifications de format.
ms.assetid: d2488fba-a653-4b6e-b786-ce95f9e20daa
title: CDynamicOutputPin, classe (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54c6dab41c122456076299df22bf90d886c905cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542636"
---
# <a name="cdynamicoutputpin-class"></a>CDynamicOutputPin, classe

La `CDynamicOutputPin` classe implémente une broche de sortie qui prend en charge les reconnexions dynamiques et les modifications de format.

Cette classe dérive de la classe [**CBaseOutputPin**](cbaseoutputpin.md) et implémente l’interface [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) . Il prend en charge plusieurs opérations importantes pour la génération de graphiques dynamiques :

-   Reconnexion dynamique : le code confidentiel peut se déconnecter et se reconnecter lorsque le filtre est toujours actif (en pause ou en cours d’exécution).
-   Modification du format dynamique : le code confidentiel peut négocier un nouveau type de média alors que le filtre est toujours actif, sans se reconnecter.
-   Contrôle de flow : le filtre propriétaire (ou une application) peut bloquer le workflow de données à partir du code confidentiel sans arrêter le filtre.

Pour plus d’informations, consultez [génération de graphiques dynamiques](dynamic-graph-building.md).

Le code pin a trois États possibles : bloqué, débloqué et en attente. Dans l’état *en attente* , le code PIN attend qu’une opération se termine sur un autre thread, avant que le code confidentiel passe à l’État bloqué. Lorsque le code confidentiel est bloqué, le filtre ne peut pas fournir de données par le biais du code confidentiel ou modifier la connexion du pin.

Pour coordonner plusieurs threads, le filtre propriétaire doit respecter certaines règles. (Pour plus d’informations sur les threads dans le graphique de filtre, consultez [threads et sections critiques](threads-and-critical-sections.md).) Tout d’abord, le thread de streaming doit toujours appeler la méthode [**CDynamicOutputPin :: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) avant d’appeler l’une des méthodes suivantes :

-   [**CDynamicOutputPin::ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)
-   [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md)
-   [**CDynamicOutputPin ::D ynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)
-   [**CBaseOutputPin ::D eliver**](cbaseoutputpin-deliver.md)
-   [**CBaseOutputPin ::D eliverEndOfStream**](cbaseoutputpin-deliverendofstream.md)
-   [**CBaseOutputPin ::D eliverNewSegment**](cbaseoutputpin-delivernewsegment.md)
-   [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

Ensuite, il doit appeler la méthode [**CDynamicOutputPin :: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) .

Deuxièmement, le thread d’application ne doit pas appeler les méthodes de la liste précédente. Troisièmement, le thread de streaming ne doit pas appeler les méthodes de classe qui bloquent ou débloquent le code confidentiel. Ces méthodes sont les suivantes : [**CDynamicOutputPin :: Block**](cdynamicoutputpin-block.md), [**CDynamicOutputPin :: SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md), [**CDynamicOutputPin :: AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)et [**CDynamicOutputPin :: UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md).

Ces règles garantissent que le thread d’application ne peut pas bloquer le code confidentiel pendant que le thread de streaming l’utilise, et vice versa. Une fois que le thread de streaming a appelé **StartUsingOutputPin**, le code pin n’est pas bloqué tant que le thread de streaming n’a pas appelé **StopUsingOutputPin**. À l’inverse, si le code PIN est bloqué, **StartUsingOutputPin** attend que le code confidentiel soit débloqué.

Pour éviter d’oublier d’appeler **StopUsingOutputPin**, vous pouvez utiliser la classe [**CAutoUsingOutputPin**](cautousingoutputpin-cautousingoutputpin.md) . Il appelle **StopUsingOutputPin** automatiquement lorsqu’il est hors de portée.

Quand le filtre propriétaire rejoint ou leaveds le graphique de filtre (dans sa méthode [**IBaseFilter :: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) ), il doit appeler la méthode [**CDynamicOutputPin :: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) du pin.



| Variables membres protégées                                                                      | Description                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md)                                 | Section critique qui protège l’état de blocage.                                                                            |
| [**m \_ hUnblockOutputPinEvent**](cdynamicoutputpin-m-hunblockoutputpinevent.md)                 | Événement signalé lorsque le pin n’est pas bloqué.                                                                           |
| [**m \_ hNotifyCallerPinBlockedEvent**](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)     | Événement signalé lorsque le code confidentiel se bloque correctement ou lorsque l’utilisateur annule un bloc en attente.                                 |
| [**m \_ BlockState**](cdynamicoutputpin-m-blockstate.md)                                         | État de blocage.                                                                                                               |
| [**m \_ dwBlockCallerThreadID**](cdynamicoutputpin-m-dwblockcallerthreadid.md)                   | Identificateur du thread qui a appelé la méthode [**IPinFlowControl :: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) sur ce code confidentiel. |
| [**m \_ dwNumOutstandingOutputPinUsers**](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md) | Nombre de threads de streaming utilisant ce code PIN.                                                                                   |
| [**m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md)                                         | Événement signalé lorsque le filtre s’arrête ou que le code PIN vide les données.                                                         |
| [**m \_ pGraphConfig**](cdynamicoutputpin-m-pgraphconfig.md)                                     | Pointeur vers l’interface [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) pour l’exécution de reconnexions dynamiques.                           |
| [**m \_ bPinUsesReadOnlyAllocator**](cdynamicoutputpin-m-bpinusesreadonlyallocator.md)           | Indicateur qui spécifie si les échantillons de l’allocateur du pin sont en lecture seule.                                                   |
| Méthodes protégées                                                                               | Description                                                                                                                   |
| [**SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)                | Bloque le code confidentiel ; n’est pas retourné tant que le code confidentiel n’est pas bloqué.                                                                     |
| [**AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)              | Bloque le code confidentiel ; peut retourner avant que le code confidentiel soit bloqué.                                                                       |
| [**UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)                                  | Débloque le code confidentiel.                                                                                                             |
| [**BlockOutputPin**](cdynamicoutputpin-blockoutputpin.md)                                      | Bloque le code confidentiel.                                                                                                               |
| [**WaitEvent**](cdynamicoutputpin-waitevent.md)                                                | Attend que l’événement spécifié soit signalé.                                                                                  |
| M&#233;thodes publiques                                                                                  | Description                                                                                                                   |
| [**CDynamicOutputPin**](cdynamicoutputpin-cdynamicoutputpin.md)                                | Méthode de constructeur.                                                                                                           |
| [**~ CDynamicOutputPin**](cdynamicoutputpin--cdynamicoutputpin.md)                              | Méthode de destructeur.                                                                                                            |
| [**SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md)                                        | Spécifie le pointeur [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) et l’événement stop.                                                |
| [**DeliverBeginFlush**](cdynamicoutputpin-deliverbeginflush.md)                                | Demande la broche d’entrée connectée pour commencer une opération de vidage.                                                                  |
| [**DeliverEndFlush**](cdynamicoutputpin-deliverendflush.md)                                    | Demande la broche d’entrée connectée pour terminer une opération de vidage.                                                                    |
| [**Inactif**](cdynamicoutputpin-inactive.md)                                                  | Notifie le code confidentiel que le filtre a arrêté.                                                                                 |
| [**Proactive**](cdynamicoutputpin-active.md)                                                      | Notifie le code confidentiel que le filtre est maintenant actif.                                                                               |
| [**CompleteConnect**](cdynamicoutputpin-completeconnect.md)                                    | Termine une connexion à une broche d’entrée. Virtuels.                                                                              |
| [**StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md)                            | Obtient l’accès au code confidentiel pour une opération de diffusion en continu. Virtuels.                                                                 |
| [**StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md)                              | Libère l’accès au code PIN après une opération de diffusion en continu. Virtuels.                                                              |
| [**StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md)        | Détermine si un thread effectue une opération de diffusion en continu sur le code confidentiel. Virtuels.                                        |
| [**ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)                              | Modifie dynamiquement le type de média pour la connexion et fournit de nouvelles informations de segment.                                  |
| [**ChangeMediaType**](cdynamicoutputpin-changemediatype.md)                                    | Modifie dynamiquement le type de média pour la connexion.                                                                        |
| [**DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)                                  | Effectue une reconnexion dynamique avec un nouveau type de média.                                                                        |
| Méthodes IPin                                                                                    | Description                                                                                                                   |
| [**Déconnecter**](cdynamicoutputpin-disconnect.md)                                              | Interrompt la connexion de code confidentiel actuelle.                                                                                            |
| Méthodes IPinFlowControl                                                                         | Description                                                                                                                   |
| [**Block**](cdynamicoutputpin-block.md)                                                        | Bloque ou débloque le workflow de données à partir du code confidentiel.                                                                             |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




