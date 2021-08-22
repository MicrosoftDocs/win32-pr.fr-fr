---
description: Stocke et récupère des informations sur les abonnements aux événements. Cette interface étend l’interface IEventSubscription.
ms.assetid: f153afb7-c897-40f8-81ed-50308844cac5
title: Interface IEventSubscription2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2
api_type:
- COM
api_location: ''
ms.openlocfilehash: 332f123756d1340352524852aa5bcb38fce09612f52554facaf6e5c8c2398e73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047479"
---
# <a name="ieventsubscription2-interface"></a>Interface IEventSubscription2

Stocke et récupère des informations sur les abonnements aux événements. Cette interface étend l’interface [**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription) .

## <a name="when-to-implement"></a>Quand implémenter

Vous n’avez pas besoin d’implémenter l’interface **IEventSubscription2** . Une classe d’objet d’événement fournie par le système (CLSID \_ CEventSubscription) implémente **IEventSubscription2**.

## <a name="when-to-use"></a>Quand l’utiliser

Le système d' [événements com+](com--events.md) utilise cette interface pour obtenir des informations sur les abonnements individuels.

## <a name="members"></a>Membres

L’interface **IEventSubscription2** hérite de **IEventSubscription**. **IEventSubscription2** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IEventSubscription2** possède les propriétés suivantes.



| Propriété                                                                      | Type d’accès           | Description                                                |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [**FilterCriteria**](ieventsubscription2-filtercriteria.md)<br/>       | Lecture/écriture<br/> | Critères de filtre régissant l’abonnement.<br/> |
| [**SubscriberMoniker**](ieventsubscription2-subscribermoniker.md)<br/> | Lecture/écriture<br/> | Moniker de l’abonné.<br/>                       |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 




