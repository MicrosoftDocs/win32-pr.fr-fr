---
description: La classe CBasePin est une classe abstraite qui implémente un code confidentiel générique.
ms.assetid: 23b9a0e2-24fe-4ff9-b2bb-97630c237de9
title: CBasePin, classe (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3ba7b3a85b512b2ad8d6e85aa38627a2abc68c21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094822"
---
# <a name="cbasepin-class"></a>CBasePin, classe

![hiérarchie de la classe cbasepin](images/filter02.png)

La `CBasePin` classe est une classe abstraite qui implémente un code confidentiel générique.

Les rubriques suivantes décrivent comment utiliser cette classe :

-   [Processus de connexion CBasePin](cbasepin-connection-process.md)
-   [Notification de la CBasePin des modifications d’état de filtre](notifying-cbasepin-of-filter-state-changes.md)
-   [Dérivation à partir de CBasePin](deriving-from-cbasepin.md)



| Variables membres protégées                                               | Description                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**m \_ pname**](cbasepin-m-pname.md)                                     | Nom du code confidentiel.                                                                                                  |
| [**connecté à m \_**](cbasepin-m-connected.md)                             | Pointeur vers le code confidentiel qui est connecté à ce code confidentiel.                                                          |
| [**Rép. m \_**](cbasepin-m-dir.md)                                         | Direction du code PIN.                                                                                      |
| [**m \_ pLock**](cbasepin-m-plock.md)                                     | Pointeur vers un objet de section critique.                                                                      |
| [**m \_ bRunTimeError**](cbasepin-m-bruntimeerror.md)                     | Indicateur qui signale si une erreur d’exécution s’est produite.                                                 |
| [**m \_ bCanReconnectWhenActive**](cbasepin-m-bcanreconnectwhenactive.md) | Indicateur qui spécifie si le code PIN prend en charge la reconnexion dynamique.                                         |
| [**m \_ bTryMyTypesFirst**](cbasepin-m-btrymytypesfirst.md)               | Indicateur qui spécifie si le code PIN tente ses propres types de média préférés avant ceux du code confidentiel de réception. |
| [**m \_ pFilter**](cbasepin-m-pfilter.md)                                 | Pointeur vers le filtre qui a créé le code confidentiel.                                                                |
| [**m \_ pQSink**](cbasepin-m-pqsink.md)                                   | Pointeur vers l’objet qui gère les messages de qualité.                                                       |
| [**m \_ TypeVersion**](cbasepin-m-typeversion.md)                         | Version actuelle du jeu de types de médias préférés.                                                       |
| [**m \_ MT**](cbasepin-m-mt.md)                                           | Type de média pour la connexion de code confidentiel actuelle.                                                                 |
| [**m \_ tStart**](cbasepin-m-tstart.md)                                   | Heure de début du segment.                                                                                        |
| [**m \_ tStop**](cbasepin-m-tstop.md)                                     | Heure d’arrêt du segment.                                                                                         |
| [**m \_ dRate**](cbasepin-m-drate.md)                                     | Taux de segment.                                                                                              |
| Méthodes protégées                                                        | Description                                                                                                |
| [**DisplayPinInfo**](cbasepin-displaypininfo.md)                        | Effectue le suivi d’une connexion de code confidentiel pendant le débogage.                                                                  |
| [**DisplayTypeInfo**](cbasepin-displaytypeinfo.md)                      | Affiche des informations sur le type de média pendant le débogage.                                                          |
| [**AttemptConnection**](cbasepin-attemptconnection.md)                  | Établit une connexion à un autre code confidentiel à l’aide d’un type de média spécifié.                                                      |
| [**TryMediaTypes**](cbasepin-trymediatypes.md)                          | À partir d’une liste de types de médias, tente d’effectuer une connexion à l’aide de l’un de ces types.                      |
| [**AgreeMediaType**](cbasepin-agreemediatype.md)                        | Recherche un type de média pour établir une connexion de code confidentiel.                                                        |
| [**DisconnectInternal**](cbasepin-disconnectinternal.md)                | Interrompt la connexion de code confidentiel actuelle.                                                                         |
| M&#233;thodes publiques                                                           | Description                                                                                                |
| [**CBasePin**](cbasepin-cbasepin.md)                                    | Méthode de constructeur.                                                                                        |
| [**~ CBasePin**](cbasepin--cbasepin.md)                                 | Méthode de destructeur. Virtuels.                                                                                |
| [**IsConnected**](cbasepin-isconnected.md)                              | Détermine si le code PIN est connecté à un autre code confidentiel.                                                    |
| [**GetConnected**](cbasepin-getconnected.md)                            | Récupère le code confidentiel qui est connecté à ce code confidentiel.                                                           |
| [**IsStopped**](cbasepin-isstopped.md)                                  | Détermine si le filtre contenant ce code confidentiel est arrêté.                                              |
| [**GetMediaTypeVersion**](cbasepin-getmediatypeversion.md)              | Récupère un numéro de version pour l’ensemble de types de médias préférés. Virtuels.                                  |
| [**IncrementTypeVersion**](cbasepin-incrementtypeversion.md)            | Incrémente le numéro de version sur le jeu de types de médias préférés.                                         |
| [**Actif**](cbasepin-active.md)                                        | Notifie le code confidentiel que le filtre est maintenant actif. Virtuels.                                                   |
| [**Inactif**](cbasepin-inactive.md)                                    | Notifie le code confidentiel que le filtre n’est plus actif. Virtuels.                                             |
| [**Exécuter**](cbasepin-run.md)                                              | Notifie le code confidentiel que le filtre est en cours d’exécution. Virtuels.                                                  |
| [**SetMediaType**](cbasepin-setmediatype.md)                            | Définit le type de média pour la connexion. Virtuels.                                                           |
| [**CheckConnect**](cbasepin-checkconnect.md)                            | Détermine si une connexion de code confidentiel est appropriée. Virtuels.                                                  |
| [**BreakConnect**](cbasepin-breakconnect.md)                            | Libère le code confidentiel d’une connexion. Virtuels.                                                               |
| [**CompleteConnect**](cbasepin-completeconnect.md)                      | Termine une connexion à un autre code confidentiel. Virtuels.                                                            |
| [**GetMediaType**](cbasepin-getmediatype.md)                            | Récupère un type de média par défaut, par valeur d’index. Virtuels.                                                 |
| [**CurrentStopTime**](cbasepin-currentstoptime.md)                      | Récupère l’heure d’arrêt du segment.                                                                           |
| [**CurrentStartTime**](cbasepin-currentstarttime.md)                    | Récupère l’heure de début du segment.                                                                          |
| [**CurrentRate**](cbasepin-currentrate.md)                              | Récupère le taux de segment.                                                                                |
| [**Nomme**](cbasepin-name.md)                                            | Récupère l’identificateur de code confidentiel.                                                                              |
| [**SetReconnectWhenActive**](cbasepin-setreconnectwhenactive.md)        | Spécifie si le code PIN prend en charge les reconnexions dynamiques.                                                  |
| [**CanReconnectWhenActive**](cbasepin-canreconnectwhenactive.md)        | Interroge si le code PIN prend en charge les reconnexions dynamiques.                                                    |
| Méthodes virtuelles pures                                                     | Description                                                                                                |
| [**CheckMediaType**](cbasepin-checkmediatype.md)                        | Détermine si le code PIN accepte un type de média spécifique.                                                       |
| Méthodes IPin                                                             | Description                                                                                                |
| [**Connecter**](cbasepin-connect.md)                                      | Connecte le pin à un autre code PIN.                                                                           |
| [**ReceiveConnection**](cbasepin-receiveconnection.md)                  | Accepte une connexion à partir d’un autre code PIN.                                                                     |
| [**Déconnecter**](cbasepin-disconnect.md)                                | Interrompt la connexion de code confidentiel actuelle.                                                                         |
| [**ConnectedTo**](cbasepin-connectedto.md)                              | Récupère le pin connecté à ce code confidentiel.                                                                   |
| [**ConnectionMediaType**](cbasepin-connectionmediatype.md)              | Récupère le type de média pour la connexion de code confidentiel actuelle, le cas échéant.                                           |
| [**QueryPinInfo**](cbasepin-querypininfo.md)                            | Récupère des informations sur le code confidentiel.                                                                       |
| [**QueryDirection**](cbasepin-querydirection.md)                        | Récupère la direction du code confidentiel (entrée ou sortie).                                                      |
| [**QueryId**](cbasepin-queryid.md)                                      | Récupère l’identificateur de code confidentiel.                                                                              |
| [**QueryAccept**](cbasepin-queryaccept.md)                              | Détermine si le code confidentiel accepte un type de média spécifié.                                                 |
| [**EnumMediaTypes**](cbasepin-enummediatypes.md)                        | Énumère les types de médias préférés du pin.                                                                |
| [**QueryInternalConnections**](cbasepin-queryinternalconnections.md)    | Récupère les broches qui sont connectées en interne à ce code confidentiel (dans le filtre).                          |
| [**EndOfStream**](cbasepin-endofstream.md)                              | Notifie le code confidentiel qu’aucune donnée supplémentaire n’est attendue.                                                      |
| [**NewSegment**](cbasepin-newsegment.md)                                | Avertit le code confidentiel que les exemples de supports reçus après cet appel sont regroupés en tant que segment.                     |
| Méthodes IQualityControl                                                  | Description                                                                                                |
| [**Notifier**](cbasepin-notify.md)                                        | Notifie le code confidentiel qu’une modification de qualité est demandée.                                                       |
| [**SetSink**](cbasepin-setsink.md)                                      | Définit un gestionnaire de qualité externe.                                                                          |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




