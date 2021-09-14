---
description: Contient un objet pour chaque propriété d’abonné de la collection TransientSubscriptions parente. Les abonnements temporaires peuvent être créés à la volée pour les instances d’objets en cours d’exécution, et ils disparaissent quand l’objet est détruit.
ms.assetid: b4f003b0-db9d-45f1-a57d-3e4d321289ca
title: Collection TransientSubscriberProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientSubscriberProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 17f89638efe232f2cdf06e1206f74a0df44601b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127310854"
---
# <a name="transientsubscriberproperties-collection"></a>Collection TransientSubscriberProperties

Contient un objet pour chaque propriété d’abonné de la collection [**TransientSubscriptions**](transientsubscriptions.md) parente. Les abonnements temporaires peuvent être créés à la volée pour les instances d’objets en cours d’exécution, et ils disparaissent quand l’objet est détruit.

Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **TransientSubscriberProperties** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Vous pouvez accéder à cette collection à partir des regroupements suivants :

-   [**TransientSubscriptions**](transientsubscriptions.md)

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [Nom](#name)
-   [Valeur](#value)

### <a name="name"></a>Nom



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom de la propriété. Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Access         | WriteOnce                                                                                                                                                                                                                                                              |
| Type           | String                                                                                                                                                                                                                                                                 |
| Valeur par défaut        | « Nouvelle propriété »                                                                                                                                                                                                                                                         |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                           |



 

### <a name="value"></a>Valeur



| Entrée | Valeur |
|----------------|---------------------------|
| Description    | Valeur de la propriété. |
| Access         | Lecture/écriture                 |
| Type           | Variante                   |
| Default        | N/A                       |
| Système minimal | Windows 2000              |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
