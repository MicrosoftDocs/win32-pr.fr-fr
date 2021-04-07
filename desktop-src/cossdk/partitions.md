---
description: Spécifie les applications contenues dans chaque partition.
ms.assetid: 264a35fd-ba71-4ae9-908a-24a72167c26b
title: Collection partitions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Partitions
api_type:
- COM
api_location: ''
ms.openlocfilehash: b1016ae932d6841a5db590f2d24496113d3cefc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749077"
---
# <a name="partitions-collection"></a>Collection partitions

Spécifie les applications contenues dans chaque partition.

Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **partitions** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**Applications**](applications.md)
-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForPartition**](rolesforpartition.md)

Vous pouvez accéder à cette collection à partir des regroupements suivants :

-   [**Causes**](root.md)

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [Modifiables](#changeable)
-   [Supprimé](#deleteable)
-   [Description](#description)
-   [Identifiant](#partitions-collection)
-   [Nom](#name)

### <a name="changeable"></a>Modifiables



| Entrée | Valeur |
|----------------|--------------------------------------------------|
| Description    | Détermine si cette partition peut être modifiée. |
| Accès         | Lecture/écriture                                        |
| Type           | Bool                                             |
| Default        | Vrai                                             |
| Système minimal | Windows Server 2003                              |



 

### <a name="deleteable"></a>Supprimé



| Entrée | Valeur |
|----------------|---------------------------------------------------|
| Description    | Détermine si cette partition peut être supprimée. |
| Accès         | Lecture/écriture                                         |
| Type           | Bool                                              |
| Default        | Vrai                                              |
| Système minimal | Windows Server 2003                               |



 

### <a name="description"></a>Description



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------|
| Description    | Cette propriété représente la description identifiant la partition. |
| Accès         | Lecture/écriture                                                           |
| Type           | String                                                              |
| Valeur par défaut        | ""                                                                  |
| Système minimal | Windows Server 2003                                                 |



 

### <a name="id"></a>id



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | GUID représentant la partition. Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection. |
| Accès         | WriteOnce                                                                                                                                                          |
| Type           | String                                                                                                                                                             |
| Valeur par défaut        | <Generated>                                                                                                                                                  |
| Système minimal | Windows Server 2003                                                                                                                                                |



 

### <a name="name"></a>Nom



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Représente le nom de la partition. Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Accès         | Lecture/écriture                                                                                                                                                                                                                              |
| Type           | String                                                                                                                                                                                                                                 |
| Valeur par défaut        | « Nouvelle partition »                                                                                                                                                                                                                        |
| Système minimal | Windows Server 2003                                                                                                                                                                                                                    |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
