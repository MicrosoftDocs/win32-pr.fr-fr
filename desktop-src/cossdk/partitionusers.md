---
description: Contient un objet pour chaque utilisateur de la partition.
ms.assetid: baec56ae-be8a-42a7-90bc-1db7c5cd7fe2
title: Collection PartitionUsers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PartitionUsers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1521642879037938451decd873a9aa14211ce296
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516581"
---
# <a name="partitionusers-collection"></a>Collection PartitionUsers

Contient un objet pour chaque utilisateur de la partition.

Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **PartitionUsers** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Vous pouvez accéder à cette collection à partir des regroupements suivants :

-   [**Causes**](root.md)

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [AccountName](#accountname)
-   [DefaultPartitionID](#defaultpartitionid)

### <a name="accountname"></a>AccountName



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom du compte de l’utilisateur de la partition. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Accès         | WriteOnce                                                                                                                                                                                                    |
| Type           | String                                                                                                                                                                                                       |
| Valeur par défaut        | « Nouvel utilisateur »                                                                                                                                                                                                   |
| Système minimal | Windows Server 2003                                                                                                                                                                                          |



 

### <a name="defaultpartitionid"></a>DefaultPartitionID



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------|
| Description    | Identificateur global unique de la partition d’application de base. |
| Accès         | Lecture/écriture                                                          |
| Type           | String                                                             |
| Valeur par défaut        | {41E90F3E-56C1-4633-81C3-6E8BAC8BDD70}                             |
| Système minimal | Windows Server 2003                                                |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
