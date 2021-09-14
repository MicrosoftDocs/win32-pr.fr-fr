---
description: Stocke et récupère des informations sur les abonnements aux événements. Cette interface étend l’interface IEventSubscription2.
ms.assetid: fd1c136e-6e4e-42ca-a951-4aa5fcdfaa49
title: Interface IEventSubscription3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3
api_type:
- COM
api_location: ''
ms.openlocfilehash: 94225faf957b2eac3388422d74df3cfdb8bf6d90
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916815"
---
# <a name="ieventsubscription3-interface"></a>Interface IEventSubscription3

Stocke et récupère des informations sur les abonnements aux événements. Cette interface étend l’interface [**IEventSubscription2**](ieventsubscription2.md) .

## <a name="when-to-implement"></a>Quand implémenter

Vous n’avez pas besoin d’implémenter l’interface **IEventSubscription3** . Une classe d’objet d’événement fournie par le système (CLSID \_ CEventSubscription) implémente **IEventSubscription3**.

## <a name="when-to-use"></a>Quand l’utiliser

Le système d' [événements com+](com--events.md) utilise cette interface pour obtenir des informations sur les abonnements individuels.

## <a name="members"></a>Membres

L’interface **IEventSubscription3** hérite de **IEventSubscription2**. **IEventSubscription3** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IEventSubscription3** possède les propriétés suivantes.



| Propriété                                                                                  | Type d’accès           | Description                                                |
|:------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [**EventClassApplicationID**](ieventsubscription3-eventclassapplicationid.md)<br/> | Lecture/écriture<br/> | GUID de l’application de l’objet de classe d’événements.<br/> |
| [**EventClassPartitionID**](ieventsubscription3-eventclasspartitionid.md)<br/>     | Lecture/écriture<br/> | GUID de la partition de l’objet de classe d’événements.<br/>   |
| [**SubscriberApplicationID**](ieventsubscription3-subscriberapplicationid.md)<br/> | Lecture/écriture<br/> | GUID de l’application de l’abonné.<br/>         |
| [**SubscriberPartitionID**](ieventsubscription3-subscriberpartitionid.md)<br/>     | Lecture/écriture<br/> | GUID de la partition de l’abonné.<br/>           |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IEventSubscription2**](ieventsubscription2.md)
</dt> </dl>

 

 




