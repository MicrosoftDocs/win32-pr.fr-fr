---
description: La classe CBaseFilter est une classe abstraite pour l’implémentation de filtres.
ms.assetid: 4610c8d6-9d7d-47ca-b1d5-0a867153a5f6
title: CBaseFilter, classe (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe032d0614b1067c9351b643d457a718b4917a8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528911"
---
# <a name="cbasefilter-class"></a>CBaseFilter, classe

![hiérarchie de la classe cbasefilter](images/filter01.png)

La `CBaseFilter` classe est une classe abstraite pour l’implémentation de filtres. Pour implémenter un filtre à l’aide de cette classe, vous devez effectuer au moins les étapes suivantes :

-   Dérivez une nouvelle classe de `CBaseFilter` .
-   Incluez les variables membres qui définissent les broches sur le filtre. Les codes confidentiels doivent hériter de la classe [**CBasePin**](cbasepin.md) .
-   Substituez la méthode virtuelle pure [**CBaseFilter :: GetPin**](cbasefilter-getpin.md), qui récupère les broches sur le filtre.
-   Substituez la méthode virtuelle pure [**CBaseFilter :: GetPinCount**](cbasefilter-getpincount.md), qui récupère le nombre de broches.
-   Fournit des méthodes pour la génération, le traitement ou le rendu des exemples multimédias.

Plusieurs classes de base dérivent de `CBaseFilter` , y compris [**CSource**](csource.md), [**CBaseRenderer**](cbaserenderer.md)et [**CTransformFilter**](ctransformfilter.md). Il est généralement plus facile d’implémenter un filtre avec l’une de ces classes spécialisées, plutôt que d’utiliser `CBaseFilter` directement.



| Variables membres protégées                                     | Description                                                                                        |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**\_État m**](cbasefilter-m-state.md)                        | État actuel du filtre.                                                                       |
| [**m \_ pClock**](cbasefilter-m-pclock.md)                      | Pointeur vers l’horloge de référence du filtre.                                                           |
| [**m \_ tStart**](cbasefilter-m-tstart.md)                      | Temps de référence qui correspond au temps de flux 0.                                                  |
| [**m \_ CLSID**](cbasefilter-m-clsid.md)                        | Identificateur de classe (CLSID) du filtre.                                                            |
| [**m \_ pLock**](cbasefilter-m-plock.md)                        | Pointeur vers une section critique utilisée pour sérialiser les modifications d’État.                             |
| [**m \_ pname**](cbasefilter-m-pname.md)                        | Nom du filtre.                                                                                       |
| [**m \_ pGraph**](cbasefilter-m-pgraph.md)                      | Pointeur vers le gestionnaire de graphique de filtre.                                                               |
| [**m \_ pSink**](cbasefilter-m-psink.md)                        | Pointeur vers l’interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) sur le gestionnaire de graphique de filtre.   |
| [**m \_ PinVersion**](cbasefilter-m-pinversion.md)              | Version actuelle du jeu de codes PIN sur ce filtre.                                                 |
| M&#233;thodes publiques                                                 | Description                                                                                        |
| [**CBaseFilter**](cbasefilter-cbasefilter.md)                 | Méthode de constructeur.                                                                                |
| [**~ CBaseFilter**](cbasefilter--cbasefilter.md)              | Méthode de destructeur.                                                                                 |
| [**StreamTime**](cbasefilter-streamtime.md)                   | Récupère le temps de flux actuel. Virtuels.                                                        |
| [**IsActive**](cbasefilter-isactive.md)                       | Détermine si le filtre est actuellement actif (en cours d’exécution ou en pause).                             |
| [**IsStopped**](cbasefilter-isstopped.md)                     | Détermine si le filtre est actuellement arrêté.                                                |
| [**NotifyEvent**](cbasefilter-notifyevent.md)                 | Envoie une notification d’événement au gestionnaire de graphique de filtre.                                           |
| [**GetFilterGraph**](cbasefilter-getfiltergraph.md)           | Récupère un pointeur vers le gestionnaire de graphique de filtre.                                                   |
| [**ReconnectPin**](cbasefilter-reconnectpin.md)               | Rompt une connexion de code confidentiel existante et la reconnecte au même code PIN, à l’aide d’un type de média spécifié. |
| [**GetPinVersion**](cbasefilter-getpinversion.md)             | Récupère un numéro de version pour l’ensemble de broches sur ce filtre. Virtuels.                            |
| [**IncrementPinVersion**](cbasefilter-incrementpinversion.md) | Incrémente le numéro de version sur le jeu de broches.                                                  |
| [**GetSetupData**](cbasefilter-getsetupdata.md)               | Récupère les données d’inscription pour le filtre. Virtuels.                                           |
| Méthodes virtuelles pures                                           | Description                                                                                        |
| [**GetPinCount**](cbasefilter-getpincount.md)                 | Récupère le nombre de broches.                                                                      |
| [**GetPin**](cbasefilter-getpin.md)                           | Récupère un code confidentiel.                                                                                   |
| IPersist, méthodes                                               | Description                                                                                        |
| [**GetClassID**](cbasefilter-getclassid.md)                   | Récupère l’identificateur de classe.                                                                    |
| Méthodes IMediaFilter                                           | Description                                                                                        |
| [**GetState**](cbasefilter-getstate.md)                       | Récupère l’état du filtre (en cours d’exécution, arrêté ou suspendu).                                        |
| [**SetSyncSource**](cbasefilter-setsyncsource.md)             | Définit une horloge de référence pour le filtre.                                                             |
| [**GetSyncSource**](cbasefilter-getsyncsource.md)             | Récupère l’horloge de référence utilisée par le filtre.                                            |
| [**Erreur**](cbasefilter-stop.md)                               | Arrête le filtre.                                                                                  |
| [**Suspendre**](cbasefilter-pause.md)                             | Suspend le filtre.                                                                                 |
| [**Utilisez**](cbasefilter-run.md)                                 | Permet d'exécuter le filtre.                                                                                   |
| Méthodes IBaseFilter                                            | Description                                                                                        |
| [**EnumPins**](cbasefilter-enumpins.md)                       | Énumère les broches sur ce filtre.                                                                |
| [**FindPin**](cbasefilter-findpin.md)                         | Récupère le code confidentiel avec l’identificateur spécifié.                                                   |
| [**QueryFilterInfo**](cbasefilter-queryfilterinfo.md)         | Récupère des informations sur le filtre.                                                            |
| [**JoinFilterGraph**](cbasefilter-joinfiltergraph.md)         | Notifie le filtre qu’il a rejoint ou a laissé un graphique de filtre.                                     |
| [**QueryVendorInfo**](cbasefilter-queryvendorinfo.md)         | Récupère une chaîne contenant des informations sur le fournisseur.                                                  |
| Méthodes IAMovieSetup                                           | Description                                                                                        |
| [**S’inscrire**](cbasefilter-register.md)                       | Ajoute le filtre au registre.                                                                   |
| [**Unregister**](cbasefilter-unregister.md)                   | Supprime le filtre du Registre.                                                              |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




