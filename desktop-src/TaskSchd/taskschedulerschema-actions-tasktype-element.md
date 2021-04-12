---
title: Élément actions (taskType)
description: Contient les actions effectuées par la tâche.
ms.assetid: 0a48fbd6-8a6f-4bad-9b28-0631dce15748
keywords:
- Élément actions (taskType) Planificateur de tâches
- actions Planificateur de tâches, XML
- Actions, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Actions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 21af0f8a06faa9cdc61917dcb3b3b0672c47e0e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384224"
---
# <a name="actions-tasktype-element"></a>Élément actions (taskType)

Contient les actions effectuées par la tâche.

``` syntax
<xs:element name="Actions"
    type="actionsType"
 />
```

L’élément **actions** est défini par le type complexe [**TaskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                          | Dérivé de                                                 | Description                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Tâche**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Décrit la tâche effectuée par le service Planificateur de tâches.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                    | Type                                                                       | Description                                                            |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Comgérer**](taskschedulerschema-comhandler-actiongroup-element.md)   | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md)   | Spécifie une action qui déclenche un gestionnaire.<br/>                   |
| [**Exécutable**](taskschedulerschema-exec-actiongroup-element.md)               | [**execType**](taskschedulerschema-exectype-complextype.md)               | Spécifie une action qui exécute une opération de ligne de commande.<br/> |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)     | Spécifie une action qui envoie un message électronique.<br/>            |
| [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Spécifie une action qui affiche une boîte de message.<br/>               |



## <a name="attributes"></a>Attributs



| Nom    | Type | Description                                                                                          |
|---------|------|------------------------------------------------------------------------------------------------------|
| Context |      | Identificateur principal de l’utilisateur qui est le contexte de sécurité pour les actions de la tâche.<br/> |



## <a name="remarks"></a>Notes

Les éléments enfants répertoriés précédemment (32 maximum) sont définis par le groupe [**actionGroup**](taskschedulerschema-actiongroup-group.md) . Ces éléments peuvent être ajoutés dans n’importe quel ordre.

Pour le développement C++, les actions d’une tâche sont définies dans l’interface [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) .

Pour le développement de scripts, les actions d’une tâche sont définies dans l’objet [**ActionCollection**](actioncollection.md) .

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple complet de code XML pour une tâche qui contient une seule action d’exécution, consultez [exemple de déclencheur d’heure (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**taskType**](taskschedulerschema-tasktype-complextype.md)
</dt> <dt>

[**actionGroup**](taskschedulerschema-actiongroup-group.md)
</dt> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





