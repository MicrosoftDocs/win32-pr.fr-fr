---
title: ClassId (comHandlerType) (élément)
description: Spécifie l’identificateur de la classe de gestionnaire.
ms.assetid: 38ebcc39-85f2-4f61-8cb6-556c242a63d9
keywords:
- ClassId, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- ClassId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d2729226320758f93140e1d4073286fba02f446d34f9eb9c36caf931b7190e4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119402119"
---
# <a name="classid-comhandlertype-element"></a>ClassId (comHandlerType) (élément)

Spécifie l’identificateur de la classe de gestionnaire.

``` syntax
<xs:element name="ClassId"
    type="guidType"
 />
```

L’élément **ClassID** est défini par le type complexe [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                  | Dérivé de                                                             | Description                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [**Comgérer**](taskschedulerschema-comhandler-actiongroup-element.md) | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) | Spécifie une action qui déclenche un gestionnaire.<br/> |



## <a name="remarks"></a>Remarques

Les applications définissent l’identificateur de classe à l’aide de la propriété [**ClassID**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid) de l’interface [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





