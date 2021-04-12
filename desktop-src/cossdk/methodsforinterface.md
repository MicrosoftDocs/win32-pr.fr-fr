---
description: Contient un objet pour chaque méthode sur l’interface à laquelle la collection est associée.
ms.assetid: e64b007f-e44d-4b6b-97b2-1e017c5a7dbe
title: Collection MethodsForInterface
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MethodsForInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6057d06d4a67222095d5bb0b5ae6da0d603fb4ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393227"
---
# <a name="methodsforinterface-collection"></a>Collection MethodsForInterface

Contient un objet pour chaque méthode sur l’interface à laquelle la collection est associée.

Cette collection ne prend pas en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **MethodsForInterface** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForMethod**](rolesformethod.md)

Vous pouvez accéder à cette collection à partir des regroupements suivants :

-   [**InterfacesForComponent**](interfacesforcomponent.md)

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [AutoComplete](#autocomplete)
-   [IDENTIFICATEUR](#clsid)
-   [Description](#description)
-   [IID](#iid)
-   [Index](#index)
-   [Nom](#name)

### <a name="autocomplete"></a>AutoComplete



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Détermine si l’objet est désactivé automatiquement à la fin de la méthode, sans qu’il soit nécessaire d’appeler SetComplete ou SetAbort. Cela affecte uniquement le paramètre par défaut du bit « Done » de l’activation JIT au démarrage de la méthode. ce bit peut être réinitialisé (comme avec SetComplete ou SetAbort) dans la méthode pour remplacer la valeur par défaut. |
| Accès         | Lecture/écriture                                                                                                                                                                                                                                                                                                                                  |
| Type           | Bool                                                                                                                                                                                                                                                                                                                                       |
| Default        | False                                                                                                                                                                                                                                                                                                                                      |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                                                                                               |



 

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
|----------------|------------------------------|
| Description    | Description de la méthode. |
| Accès         | Lecture/écriture                    |
| Type           | String                       |
| Valeur par défaut        | ""                           |
| Système minimal | Windows 2000                 |



 

### <a name="iid"></a>IID



| Entrée | Valeur |
|----------------|---------------------------|
| Description    | GUID de l’interface. |
| Accès         | Lecture seule                  |
| Type           | String                    |
| Valeur par défaut        | N/A                       |
| Système minimal | Windows 2000              |



 

### <a name="index"></a>Index



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Identificateur de dispatch de la méthode. Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection. |
| Accès         | Lecture seule                                                                                                                                                        |
| Type           | **GRANDE**                                                                                                                                                       |
| Default        | N/A                                                                                                                                                             |
| Système minimal | Windows 2000                                                                                                                                                    |



 

### <a name="name"></a>Nom



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom de la méthode. Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Accès         | Lecture seule                                                                                                                                           |
| Type           | String                                                                                                                                             |
| Valeur par défaut        | N/A                                                                                                                                                |
| Système minimal | Windows 2000                                                                                                                                       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
