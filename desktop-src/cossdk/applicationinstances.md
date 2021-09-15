---
description: Récupère des informations sur les applications en cours d’exécution.
ms.assetid: 148e42aa-e99e-4fa2-8b74-a7ebf82b99d0
title: Collection ApplicationInstances
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationInstances
api_type:
- COM
api_location: ''
ms.openlocfilehash: 56680a81cc564466dc3586bf0381cf4db97f914b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403564"
---
# <a name="applicationinstances-collection"></a>Collection ApplicationInstances

Récupère des informations sur les applications en cours d’exécution.

Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **ApplicationInstances** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Vous pouvez accéder à cette collection à partir des regroupements suivants :

-   [**Applications**](applications.md)
-   [**Causes**](root.md)

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [Application](#applicationinstances-collection)
-   [HasRecycled](#hasrecycled)
-   [InstanceID](#instanceid)
-   [IsPaused](#ispaused)
-   [PartitionID](#partitionid)
-   [ProcessID](#processid)

### <a name="application"></a>Application



| Entrée | Valeur |
|----------------|-------------------------------------|
| Description    | ID de l’application en cours d’exécution. |
| Access         | Lecture seule                            |
| Type           | String                              |
| Valeur par défaut        | N/A                                 |
| Système minimal | Windows XP                          |



 

### <a name="hasrecycled"></a>HasRecycled



| Entrée | Valeur |
|----------------|---------------------------------------------------------------|
| Description    | Indique si l’instance d’application a été recyclée. |
| Access         | Lecture seule                                                      |
| Type           | Bool                                                          |
| Default        | False                                                         |
| Système minimal | Windows XP                                                    |



 

### <a name="instanceid"></a>InstanceID



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Identificateur global unique de l’instance de l’application. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Access         | Lecture seule                                                                                                                                                                                                                            |
| Type           | String                                                                                                                                                                                                                              |
| Valeur par défaut        | N/A                                                                                                                                                                                                                                 |
| Système minimal | Windows XP                                                                                                                                                                                                                          |



 

### <a name="ispaused"></a>IsPaused



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------|
| Description    | Indique si l’instance d’application est actuellement suspendue. |
| Access         | Lecture seule                                                        |
| Type           | Bool                                                            |
| Default        | False                                                           |
| Système minimal | Windows XP                                                      |



 

### <a name="partitionid"></a>PartitionID



| Entrée | Valeur |
|----------------|-------------------------------------------------|
| Description    | ID de partition que l’application utilise. |
| Access         | Lecture seule                                        |
| Type           | String                                          |
| Valeur par défaut        | N/A                                             |
| Système minimal | Windows XP                                      |



 

### <a name="processid"></a>ProcessID



| Entrée | Valeur |
|----------------|---------------------------------------------|
| Description    | ID de processus de l’instance de l’application. |
| Access         | Lecture seule                                    |
| Type           | String                                      |
| Valeur par défaut        | N/A                                         |
| Système minimal | Windows XP                                  |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
