---
title: Élément RegistrationInfo (taskType)
description: Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.
ms.assetid: f3961bad-e9a3-4626-87ed-9639d912717d
keywords:
- informations d’inscription Planificateur de tâches, élément XML
- Élément RegistrationInfo Planificateur de tâches
topic_type:
- apiref
api_name:
- RegistrationInfo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45b912bc9f870c39cec9ff37df95df46599c0158dd08bf3ca1d47cee29058979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059767"
---
# <a name="registrationinfo-tasktype-element"></a>Élément RegistrationInfo (taskType)

Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.

``` syntax
<xs:element name="RegistrationInfo"
    type="registrationInfoType"
    minOccurs="0"
 />
```

L’élément **RegistrationInfo** est défini par le type complexe [**TaskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                          | Dérivé de                                                 | Description                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Tâche**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Définit la tâche qui est effectuée par le service Planificateur de tâches.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                                                  | Type     | Description                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------|
| [**Auteur (registrationInfoType)**](taskschedulerschema-author-registrationinfotype-element.md)                         | string   | Spécifie l’auteur de la tâche.<br/>                                                                              |
| [**Date (registrationInfoType)**](taskschedulerschema-date-registrationinfotype-element.md)                             | dateTime | Spécifie la date et l’heure d’enregistrement de la tâche.<br/>                                                       |
| [**Description (registrationInfoType)**](taskschedulerschema-description-registrationinfotype-element.md)               | string   | Spécifie la description de la tâche.<br/>                                                                         |
| [**Documentation (registrationInfoType)**](taskschedulerschema-documentation-registrationinfotype-element.md)           | string   | Spécifie toute documentation supplémentaire pour la tâche.<br/>                                                           |
| [**SecurityDescriptor (registrationInfoType)**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | string   | Spécifie le descripteur de sécurité de la tâche.<br/>                                                                 |
| [**Source (registrationInfoType)**](taskschedulerschema-source-registrationinfotype-element.md)                         | string   | Spécifie l’origine de la tâche. Par exemple, à partir d’un composant, d’un service, d’une application ou d’un utilisateur.<br/> |
| [**URI (registrationInfoType)**](taskschedulerschema-uri-registrationinfotype-element.md)                               | anyURI   | Spécifie l’URI de la tâche.<br/>                                                                                 |
| [**Version (registrationInfoType)**](taskschedulerschema-version-registrationinfotype-element.md)                       | string   | Spécifie le numéro de version de la tâche.<br/>                                                                      |



## <a name="remarks"></a>Remarques

Pour le développement de scripts, les informations d’inscription d’une tâche sont spécifiées à l’aide de la propriété [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) .

Pour le développement C++, les informations d’inscription d’une tâche sont spécifiées à l’aide de la [**propriété RegistrationInfo de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





