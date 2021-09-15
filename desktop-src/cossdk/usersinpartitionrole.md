---
description: UsersInPartitionRole collection-contient un objet pour chaque utilisateur du rôle auquel la collection est associée.
ms.assetid: c6aebf7a-04d1-4c7c-a015-bc6fb4841c4a
title: Collection UsersInPartitionRole
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInPartitionRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2a4c134ebead08ef576337528a8ef75d8b8be21a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127310829"
---
# <a name="usersinpartitionrole-collection"></a>Collection UsersInPartitionRole

Contient un objet pour chaque utilisateur du rôle auquel la collection est associée.

Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **UsersInPartitionRole** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Vous pouvez accéder à cette collection à partir des regroupements suivants :

-   [**RolesForPartition**](rolesforpartition.md)

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [Utilisateur](#usersinpartitionrole-collection)

### <a name="user"></a>Utilisateur



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom d'utilisateur. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Access         | WriteOnce                                                                                                                                                                             |
| Type           | String                                                                                                                                                                                |
| Valeur par défaut        | « Nouvel utilisateur »                                                                                                                                                                            |
| Système minimal | Windows Server 2003                                                                                                                                                                   |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
