---
title: Élément Data (comHandlerType)
description: Spécifie des données supplémentaires associées au gestionnaire.
ms.assetid: 352cb92b-54bb-4bb0-8a43-123c88c80962
keywords:
- Planificateur de tâches d’élément de données
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d009005dc2bb889c8bd9e34e84d853665310330a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011041"
---
# <a name="data-comhandlertype-element"></a>Élément Data (comHandlerType)

Spécifie des données supplémentaires associées au gestionnaire.

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

L’élément de **données** est défini par le type complexe [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                  | Dérivé de                                                             | Description                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [**Comgérer**](taskschedulerschema-comhandler-actiongroup-element.md) | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) | Spécifie une action qui déclenche un gestionnaire.<br/> |



## <a name="remarks"></a>Notes

Les applications définissent les données du gestionnaire à l’aide de la propriété [**Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) de l’interface [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





