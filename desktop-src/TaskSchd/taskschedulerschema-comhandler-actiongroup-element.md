---
title: Comgèrer (actionGroup) (élément)
description: Spécifie une action qui déclenche un gestionnaire.
ms.assetid: 18f16873-3879-4a3b-b8f2-17cc84647e25
keywords:
- Planificateur de tâches d’élément comgérer
topic_type:
- apiref
api_name:
- ComHandler
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2269464efb09e8c513ab2bdebb24744a6b32a671
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942583"
---
# <a name="comhandler-actiongroup-element"></a>Comgèrer (actionGroup) (élément)

Spécifie une action qui déclenche un gestionnaire.

``` syntax
<xs:element name="ComHandler"
    type="comHandlerType"
 />
```

L’élément **comgérer** est défini par [**actionGroup**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                         | Dérivé de                                                       | Description                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Actions**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | Contient les actions effectuées par la tâche.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                               | Type                                                         | Description                                                       |
|-----------------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [**ClassId**](taskschedulerschema-classid-comhandlertype-element.md) | [**guidType**](taskschedulerschema-guidtype-simpletype.md)  | Spécifie l’identificateur de la classe de gestionnaire.<br/>         |
| [**Données**](taskschedulerschema-data-comhandlertype-element.md)       | [**Décimal**](taskschedulerschema-datatype-complextype.md) | Spécifie des données supplémentaires associées au gestionnaire.<br/> |



## <a name="remarks"></a>Notes

Les applications définissent une action de gestionnaire COM à l’aide de l’interface [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .

### <a name="attributes"></a>Attributs

L’attribut suivant est défini par le type complexe [**actionBaseType**](taskschedulerschema-actionbasetype-complextype.md) .

-   ID : identificateur de l’action effectuée par la tâche.

## <a name="examples"></a>Exemples

Le code XML suivant définit une action de gestionnaire COM.


```XML
<Actions>
    <ComHandler>
        <ClassId></ClassId>
        <Data></Data>
    </ComHandler>
</Actions>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





