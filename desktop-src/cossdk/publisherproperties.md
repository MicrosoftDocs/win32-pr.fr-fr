---
description: Contient un objet pour chaque propriété de serveur de publication pour la collection SubscriptionsForComponent parente.
ms.assetid: 7699c258-ca11-4652-b2f7-b2f2307c01fc
title: Collection PublisherProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublisherProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4e5876e01a557e9a585423a9e438e773366ca9eaa73e9e67fdaeae8a957b90c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547153"
---
# <a name="publisherproperties-collection"></a>Collection PublisherProperties

Contient un objet pour chaque propriété de serveur de publication pour la collection [**SubscriptionsForComponent**](subscriptionsforcomponent.md) parente.

Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **PublisherProperties** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Vous pouvez accéder à cette collection à partir des regroupements suivants :

-   [**SubscriptionsForComponent**](subscriptionsforcomponent.md)

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

 

 
