---
description: La classe CBaseInputPin est une classe de base abstraite pour l’implémentation des codes confidentiels d’entrée. Cette classe ajoute la prise en charge de l’interface IMemInputPin, en plus de la prise en charge de l’interface IPin fournie par CBasePin.
ms.assetid: 5a2b7f09-8c8b-45da-a4b7-afeb8d5548c1
title: CBaseInputPin, classe (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba55006438a8484b0bf10b95ac8b9d8bbdb56e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544095"
---
# <a name="cbaseinputpin-class"></a>CBaseInputPin, classe

![hiérarchie de la classe cbaseinputpin](images/filter07.png)

La `CBaseInputPin` classe est une classe de base abstraite pour l’implémentation des codes confidentiels d’entrée. Cette classe ajoute la prise en charge de l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , en plus de la prise en charge de l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) fournie par [**CBasePin**](cbasepin.md).

Pour utiliser cette classe, dérivez une nouvelle classe et substituez au moins les méthodes suivantes :

-   [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md)
-   [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md)
-   [**CBaseInputPin :: Receive**](cbaseinputpin-receive.md)
-   [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md)
-   [**CBasePin::GetMediaType**](cbasepin-getmediatype.md)

Selon la fonction du code PIN, vous devrez peut-être remplacer des méthodes supplémentaires dans `CBaseInputPin` ou **CBasePin**.



| Variables membres protégées                                                 | Description                                                                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**m \_ pAllocator**](cbaseinputpin-m-pallocator.md)                        | Pointeur vers l’allocateur de mémoire.                                                                            |
| [**m \_ bReadOnly**](cbaseinputpin-m-breadonly.md)                          | Indicateur qui spécifie si l’allocateur produit des exemples de supports en lecture seule.                                 |
| [**m \_ bFlushing**](cbaseinputpin-m-bflushing.md)                          | Indicateur qui spécifie si le pin est actuellement en cours de vidage.                                                  |
| [**m \_ SampleProps**](cbaseinputpin-m-sampleprops.md)                      | Propriétés de l’exemple le plus récent.                                                                       |
| M&#233;thodes publiques                                                             | Description                                                                                                 |
| [**CBaseInputPin**](cbaseinputpin-cbaseinputpin.md)                       | Méthode de constructeur.                                                                                         |
| [**~ CBaseInputPin**](cbaseinputpin--cbaseinputpin.md)                     | Méthode de destructeur.                                                                                          |
| [**BreakConnect**](cbaseinputpin-breakconnect.md)                         | Libère le code confidentiel d’une connexion.                                                                         |
| [**IsReadOnly**](cbaseinputpin-isreadonly.md)                             | Interroge si l’allocateur utilise des exemples de supports en lecture seule.                                                 |
| [**IsFlushing**](cbaseinputpin-isflushing.md)                             | Interroge si le filtre est en cours de vidage.                                                           |
| [**CheckStreaming**](cbaseinputpin-checkstreaming.md)                     | Détermine si le code confidentiel peut accepter des exemples. Virtuels.                                                     |
| [**PassNotify**](cbaseinputpin-passnotify.md)                             | Transmet un message de contrôle qualité à l’objet approprié.                                                 |
| [**Inactif**](cbaseinputpin-inactive.md)                                 | Notifie le code confidentiel que le filtre n’est plus actif. Virtuels.                                              |
| [**SampleProps**](cbaseinputpin-sampleprops.md)                           | Récupère les propriétés de l’exemple le plus récent.                                                         |
| Méthodes IPin                                                               | Description                                                                                                 |
| [**BeginFlush**](cbaseinputpin-beginflush.md)                             | Commence une opération de vidage.                                                                                   |
| [**EndFlush**](cbaseinputpin-endflush.md)                                 | Termine une opération de vidage.                                                                                     |
| Méthodes IMemInputPin                                                       | Description                                                                                                 |
| [**GetAllocator**](cbaseinputpin-getallocator.md)                         | Récupère l’allocateur de mémoire proposé par ce code confidentiel.                                                        |
| [**NotifyAllocator**](cbaseinputpin-notifyallocator.md)                   | Spécifie un allocateur pour la connexion.                                                                  |
| [**GetAllocatorRequirements**](cbaseinputpin-getallocatorrequirements.md) | Récupère les propriétés d’allocateur demandées par la broche d’entrée.                                              |
| [**Çoive**](cbaseinputpin-receive.md)                                   | Reçoit l’échantillon de média suivant dans le flux.                                                               |
| [**ReceiveMultiple**](cbaseinputpin-receivemultiple.md)                   | Reçoit plusieurs exemples dans le flux.                                                                    |
| [**ReceiveCanBlock**](cbaseinputpin-receivecanblock.md)                   | Détermine si les appels à la méthode [**CBaseInputPin :: Receive**](cbaseinputpin-receive.md) peuvent se bloquer. |
| Méthodes IQualityControl                                                    | Description                                                                                                 |
| [**Notifier**](cbaseinputpin-notify.md)                                     | Reçoit un message de contrôle qualité.                                                                         |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




