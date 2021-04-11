---
title: Élément SecurityDescriptor (registrationInfoType)
description: Spécifie le descripteur de sécurité de la tâche.
ms.assetid: 79821b20-226a-4e7e-8ca1-6c9cf9f1b56e
keywords:
- Élément SecurityDescriptor Planificateur de tâches
topic_type:
- apiref
api_name:
- SecurityDescriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 20f352e20f1017029558a0de0a99186a978edbf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032532"
---
# <a name="securitydescriptor-registrationinfotype-element"></a>Élément SecurityDescriptor (registrationInfoType)

Spécifie le descripteur de sécurité de la tâche.

``` syntax
<xs:element name="SecurityDescriptor"
    type="string"
 />
```

L’élément **SecurityDescriptor** est défini par le type complexe [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                           | Dérivé de                                                                         | Description                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.<br/> |



## <a name="remarks"></a>Notes

Pour le développement de scripts, le descripteur de sécurité d’une tâche est spécifié à l’aide de la propriété [**RegistrationInfo. SecurityDescriptor**](registrationinfo-securitydescriptor.md) .

Pour le développement C++, le descripteur de sécurité d’une tâche est spécifié à l’aide de la propriété [**IRegistrationInfo :: SecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_securitydescriptor) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





