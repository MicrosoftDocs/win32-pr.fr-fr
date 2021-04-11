---
description: Contient un objet pour chaque interface exposée par le composant auquel la collection est associée.
ms.assetid: ee755693-e3ff-4bb1-9fde-a2bfee9c3d29
title: Collection InterfacesForComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InterfacesForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9450c898e694e5459dbb126d7f7bf11b853e33d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110910"
---
# <a name="interfacesforcomponent-collection"></a>Collection InterfacesForComponent

Contient un objet pour chaque interface exposée par le composant auquel la collection est associée.

Cette collection ne prend pas en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **InterfacesForComponent** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**ErrorInfo**](errorinfo.md)
-   [**MethodsForInterface**](methodsforinterface.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForInterface**](rolesforinterface.md)

Vous pouvez accéder à cette collection à partir des regroupements suivants :

-   [**Composants**](components.md)

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [IDENTIFICATEUR](#clsid)
-   [Description](#description)
-   [IID](#iid)
-   [Nom](#name)
-   [QueuingEnabled](#queuingenabled)
-   [QueueingSupported](#queueingsupported)

### <a name="clsid"></a>CLSID



| Entrée | Valeur |
|----------------|---------------------------|
| Description    | GUID du composant. |
| Accès         | Lecture seule                  |
| Type           | String                    |
| Valeur par défaut        | N/A                       |
| Système minimal | Windows 2000              |



 

### <a name="description"></a>Description



| Entrée | Valeur |
|----------------|----------------------------------|
| Description    | Description de l’interface. |
| Accès         | Lecture/écriture                        |
| Type           | String                           |
| Valeur par défaut        | ""                               |
| Système minimal | Windows 2000                     |



 

### <a name="iid"></a>IID



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | GUID de l’interface. Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection. |
| Accès         | Lecture seule                                                                                                                                                  |
| Type           | String                                                                                                                                                    |
| Valeur par défaut        | N/A                                                                                                                                                       |
| Système minimal | Windows 2000                                                                                                                                              |



 

### <a name="name"></a>Nom



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom de l’interface. Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Accès         | Lecture seule                                                                                                                                                    |
| Type           | String                                                                                                                                                      |
| Valeur par défaut        | N/A                                                                                                                                                         |
| Système minimal | Windows 2000                                                                                                                                                |



 

### <a name="queuingenabled"></a>QueuingEnabled



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Marque l’interface comme étant en file d’attente et peut être définie à l’aide du kit de développement logiciel (SDK) administrateur ou de l’outil d’administration Services de composants. Toutefois, seule une interface dont l’indicateur de mise **en file d’attente est pris en charge** peut définir l’indicateur de mise en **file d’attente activé** . |
| Accès         | Lecture/écriture                                                                                                                                                                                                                          |
| Type           | Bool                                                                                                                                                                                                                               |
| Default        | False                                                                                                                                                                                                                              |
| Système minimal | Windows 2000                                                                                                                                                                                                                       |



 

### <a name="queueingsupported"></a>QueueingSupported



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | L’interface prend en charge la mise en file d’attente. Pour qu’une interface prenne en charge la mise en file d’attente, toutes les méthodes doivent avoir uniquement des paramètres in. La mise **en file d’attente** est exposée en tant que propriété en lecture seule. |
| Accès         | Lecture seule                                                                                                                                                               |
| Type           | Bool                                                                                                                                                                   |
| Default        | False                                                                                                                                                                  |
| Système minimal | Windows 2000                                                                                                                                                           |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
