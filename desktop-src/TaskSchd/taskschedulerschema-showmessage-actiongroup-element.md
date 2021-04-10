---
title: Élément ShowMessage (actionGroup)
description: Représente une action qui affiche une boîte de message.
ms.assetid: 33c6e437-b993-4b5e-b75a-fb3fda9b24df
keywords:
- Élément ShowMessage Planificateur de tâches
topic_type:
- apiref
api_name:
- ShowMessage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1344aadfa5fe67e411048bac2a83330ea704c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317174"
---
# <a name="showmessage-actiongroup-element"></a>Élément ShowMessage (actionGroup)

Représente une action qui affiche une boîte de message.

``` syntax
<xs:element name="ShowMessage"
    type="showMessageType"
 />
```

L’élément **ShowMessage** est défini par [**actionGroup**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                    | Dérivé de                                                       | Description                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Actions (taskType)**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | Contient les actions effectuées par la tâche.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                            | Type           | Description                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [**Corps**](taskschedulerschema-body-showmessagetype-element.md)   | nonEmptyString | Spécifie le texte à afficher dans le corps de la boîte de message. <br/> |
| [**Intitulé**](taskschedulerschema-title-showmessagetype-element.md) | nonEmptyString | Spécifie le titre de la boîte de message. <br/>                       |



## <a name="remarks"></a>Notes

Pour le développement de script, une action de MessageBox est spécifiée à l’aide de l’objet [**ShowMessageAction**](showmessageaction.md) .

Pour le développement C++, une action de MessageBox est spécifiée à l’aide de l’interface [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) .

**Windows 8 et Windows Server 2012 :** Cet élément a été supprimé. Vous pouvez utiliser IExecAction avec la fonction Windows Scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) pour afficher un message dans la session utilisateur.

## <a name="examples"></a>Exemples

Pour obtenir un exemple complet du code XML d’une tâche qui utilise une action de MessageBox, consultez exemple de MessageBox [(XML)](/previous-versions//aa381917(v=vs.85)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                 |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2008 R2<br/>                    |



 

