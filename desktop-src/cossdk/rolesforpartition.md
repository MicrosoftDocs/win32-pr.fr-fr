---
description: La collection RolesForPartition est toujours associée à un objet dans la collection partitions. Il contient un objet pour chaque rôle affecté à la partition à laquelle il est associé.
ms.assetid: 56985f55-d6e8-4066-b6d5-21c62d4278ce
title: Collection RolesForPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForPartition
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6c1e64e314478793a5b421d1f0a6a76c2eb028708410a14ea426f52fbd41dfe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637039"
---
# <a name="rolesforpartition-collection"></a>Collection RolesForPartition

La collection **RolesForPartition** est toujours associée à un objet dans la collection [**partitions**](partitions.md) . Il contient un objet pour chaque rôle affecté à la partition à laquelle il est associé.

Cette collection ne prend pas en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **RolesForPartition** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**UsersInPartitionRole**](usersinpartitionrole.md)

Vous pouvez accéder à cette collection à partir des regroupements suivants :

-   [**Partitions**](partitions.md)

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [Description](#description)
-   [Nom](#name)

### <a name="description"></a>Description



| Entrée | Valeur |
|----------------|----------------------------|
| Description    | Description du rôle. |
| Accès         | Lecture seule                   |
| Type           | String                     |
| Valeur par défaut        | ""                         |
| Système minimal | Windows Server 2003        |



 

### <a name="name"></a>Nom



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom du rôle. Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Accès         | Lecture seule                                                                                                                                                                                                                                                    |
| Type           | String                                                                                                                                                                                                                                                      |
| Valeur par défaut        | ""                                                                                                                                                                                                                                                          |
| Système minimal | Windows Server 2003                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
