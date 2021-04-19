---
description: Cette classe implémente l’interface IAMStreamControl pour les broches d’entrée et de sortie.
ms.assetid: a0ddc2d5-8385-4209-b1c5-9822c30f8a02
title: CBaseStreamControl, classe (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c20a4f08040bdb2c71bdd8f09aa657719228efa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532218"
---
# <a name="cbasestreamcontrol-class"></a>CBaseStreamControl, classe

![hiérarchie de la classe cbasestreamcontrol](images/strmctl1.png)

Cette classe implémente l’interface [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) pour les broches d’entrée et de sortie. Il permet de contrôler le démarrage et l’arrêt d’un code confidentiel individuel sur le filtre. Un code confidentiel qui prend en charge **IAMStreamControl** doit hériter de cette classe de base. Voici une déclaration classique pour une broche d’entrée :

``` syntax
class CMyInputPin : public CBaseInputPin, public CBaseStreamControl
```

Veillez à remplacer **NonDelegatingQueryInteface** pour exposer **IAMStreamControl**. Pour plus d’informations, consultez [comment implémenter IUnknown](how-to-implement-iunknown.md).



| M&#233;thodes publiques                                                        | Description                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**CBaseStreamControl**](cbasestreamcontrol-cbasestreamcontrol.md)   | Méthode de constructeur.                                                                                  |
| [**~ CBaseStreamControl**](cbasestreamcontrol--cbasestreamcontrol.md) | Méthode de destructeur.                                                                                   |
| [**CheckStreamState**](cbasestreamcontrol-checkstreamstate.md)       | Détermine si un échantillon de média doit être remis ou ignoré.                                  |
| [**Vidage**](cbasestreamcontrol-flushing.md)                       | Notifie la classe de base que le code confidentiel a démarré ou a arrêté le vidage.                                |
| [**NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md)     | Notifie le code confidentiel lorsque l’état du filtre change.                                                    |
| [**SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md)           | Spécifie le récepteur d’événements pour les événements de contrôle de flux.                                                  |
| [**SetSyncSource**](cbasestreamcontrol-setsyncsource.md)             | Notifie la classe de base de l’horloge de référence actuelle.                                              |
| Méthodes IAMStreamControl                                              | Description                                                                                          |
| [**GetInfo**](cbasestreamcontrol-getinfo.md)                         | Récupère des informations sur les paramètres de contrôle de flux actuels, y compris les heures de démarrage et d’arrêt. |
| [**Commencer**](cbasestreamcontrol-startat.md)                         | Informe le code confidentiel quand il faut commencer à transmettre des données.                                                       |
| [**StopAt**](cbasestreamcontrol-stopat.md)                           | Informe le code confidentiel quand il faut arrêter la transmission de données.                                                        |



 

## <a name="remarks"></a>Notes

Cette classe requiert le code confidentiel et le filtre propriétaire pour notifier la classe lorsque divers événements se produisent, tels que le filtre qui rejoint le graphique ou la réception d’une nouvelle horloge de référence. Vous devez appeler les méthodes de classe suivantes :

-   Dans la méthode [**IMediaFilter :: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) du filtre, appelez la méthode [**CBaseStreamControl :: SetSyncSource**](cbasestreamcontrol-setsyncsource.md) . Cette méthode notifie la classe de l’horloge de référence actuelle.
-   Dans la méthode [**CBaseFilter :: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) du filtre, appelez la méthode [**CBaseStreamControl :: SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md) . Cette méthode donne à la classe un pointeur vers le gestionnaire de graphes de filtres, afin que la classe puisse envoyer les événements de contrôle de flux appropriés.
-   Chaque fois que le filtre change d’État (en en cours d’exécution, suspendu ou arrêté), appelez la méthode [**CBaseStreamControl :: NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md) .
-   Dans les méthodes [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) et [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) du pin, appelez la méthode [**CBaseStreamControl :: Flush**](cbasestreamcontrol-flushing.md) .

La `CBaseStreamControl` classe utilise l’horloge de référence du graphique de filtre pour déterminer les échantillons que le filtre doit remettre et celui qu’il doit ignorer. Dans la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) de votre pin, appelez la méthode [**CBaseStreamControl :: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) avec un pointeur vers l’exemple de média entrant. Si la méthode retourne le flux de flux de valeur \_ , fournissez l’exemple en aval. Sinon, ignorez-le.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Strmctl. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




