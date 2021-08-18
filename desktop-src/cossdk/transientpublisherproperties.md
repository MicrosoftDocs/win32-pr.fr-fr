---
description: Contient un objet pour chaque propriété de serveur de publication temporaire pour la collection TransientSubscriptions parente. Les abonnements temporaires peuvent être créés à la volée pour les instances d’objets en cours d’exécution, et ils disparaissent quand l’objet est détruit.
ms.assetid: 63921caa-5c22-4203-b1a3-f143928f4742
title: Collection TransientPublisherProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientPublisherProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 63799e7c39a87b94dace1fc0a85ca67d18fc7c9a1b0bd407fae52df62344cdeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119372689"
---
# <a name="transientpublisherproperties-collection"></a>Collection TransientPublisherProperties

Contient un objet pour chaque propriété de serveur de publication temporaire pour la collection [**TransientSubscriptions**](transientsubscriptions.md) parente. Les abonnements temporaires peuvent être créés à la volée pour les instances d’objets en cours d’exécution, et ils disparaissent quand l’objet est détruit.

Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **TransientPublisherProperties** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

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
| Accès         | WriteOnce                                                                                                                                                                                                                                                              |
| Type           | String                                                                                                                                                                                                                                                                 |
| Valeur par défaut        | « Nouvelle propriété »                                                                                                                                                                                                                                                         |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                           |



 

### <a name="value"></a>Valeur



| Entrée | Valeur |
|----------------|---------------------------|
| Description    | Valeur de la propriété. |
| Accès         | Lecture/écriture                 |
| Type           | Variante                   |
| Default        | N/A                       |
| Système minimal | Windows 2000              |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
