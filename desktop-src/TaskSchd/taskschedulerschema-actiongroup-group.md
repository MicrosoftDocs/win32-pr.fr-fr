---
title: Groupe actionGroup
description: Définit le groupe d’actions qu’une tâche peut effectuer.
ms.assetid: a43ba021-4a40-4e2c-a57f-bd6ee17706ba
keywords:
- Planificateur de tâches de groupe actionGroup
- actionGroup Planificateur de tâches
topic_type:
- apiref
api_name:
- actionGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af06598c6eca092f474467bea16a7d7b95a9563f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740836"
---
# <a name="actiongroup-group"></a>Groupe actionGroup

Définit le groupe d’actions qu’une tâche peut effectuer.

``` syntax
<xs:group name="actionGroup">
    <xs:choice>
        <xs:element name="Exec"
            type="execType"
         />
        <xs:element name="ComHandler"
            type="comHandlerType"
         />
        <xs:element name="SendEmail"
            type="sendEmailType"
         />
        <xs:element name="ShowMessage"
            type="showMessageType"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                    | Type                                                                       | Description                                                             |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**Comgérer**](taskschedulerschema-comhandler-actiongroup-element.md)   | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md)   | Représente une action qui déclenche un gestionnaire.<br/>                   |
| [**Exécutable**](taskschedulerschema-exec-actiongroup-element.md)               | [**execType**](taskschedulerschema-exectype-complextype.md)               | Représente une action qui exécute une opération de ligne de commande.<br/> |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)     | Représente une action qui envoie un message électronique.<br/>            |
| [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Représente une action qui affiche une boîte de message.<br/>               |



## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de code XML, les éléments définis par ce groupe sont les éléments enfants de l’élément [**actions**](taskschedulerschema-actions-tasktype-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





