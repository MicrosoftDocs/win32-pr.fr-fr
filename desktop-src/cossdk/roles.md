---
description: La collection de rôles est toujours liée à un objet dans la collection d’applications. Elle contient un objet pour chaque rôle affecté à l’application à laquelle elle est associée.
ms.assetid: 87f39c2a-ad66-4390-9220-06751dcebd95
title: Collection de rôles
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Roles
api_type:
- COM
api_location: ''
ms.openlocfilehash: f676a53f5fe54e42ca2a489ad834b9c91e4e0ef5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201100"
---
# <a name="roles-collection"></a>Collection de rôles

La collection de **rôles** est toujours liée à un objet dans la collection d' [**applications**](applications.md) . Elle contient un objet pour chaque rôle affecté à l’application à laquelle elle est associée.

Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **roles** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**UsersInRole**](usersinrole.md)

Vous pouvez accéder à cette collection à partir des regroupements suivants :

-   [**Applications**](applications.md)

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [Description](#description)
-   [Nom](#name)

### <a name="description"></a>Description



| Entrée | Valeur |
|----------------|----------------------------|
| Description    | Description du rôle. |
| Accès         | Lecture/écriture                  |
| Type           | String                     |
| Valeur par défaut        | ""                         |
| Système minimal | Windows 2000               |



 

### <a name="name"></a>Nom



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom du rôle. Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Accès         | WriteOnce                                                                                                                                                                                                                                                   |
| Type           | String                                                                                                                                                                                                                                                      |
| Valeur par défaut        | « Nouveau rôle »                                                                                                                                                                                                                                                  |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
