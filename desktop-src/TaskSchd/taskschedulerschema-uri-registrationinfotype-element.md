---
title: Élément URI (registrationInfoType)
description: Spécifie l’URI de la tâche.
ms.assetid: 5b438e00-ed8a-4ec8-854f-e8eda48d1cfc
keywords:
- Élément URI Planificateur de tâches
topic_type:
- apiref
api_name:
- URI
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be3f5782ba5fc02bc3309abfe337c029d0341667
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743749"
---
# <a name="uri-registrationinfotype-element"></a>Élément URI (registrationInfoType)

Spécifie l’URI de la tâche. Cet élément est utilisé pour spécifier l’emplacement de la tâche inscrite dans l’arborescence des dossiers des tâches.

``` syntax
<xs:element name="URI"
    type="anyURI"
    minOccurs="0"
 />
```

L’élément **URI** est défini par le type complexe [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                           | Dérivé de                                                                         | Description                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.<br/> |



## <a name="remarks"></a>Notes

Pour le développement de script, l’URI de la tâche est spécifié à l’aide de la propriété [**RegistrationInfo. Uri**](registrationinfo-uri.md) .

Pour le développement C++, l’URI de la tâche est spécifié à l’aide de la propriété [**IRegistrationInfo :: URI**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri) .

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

 

 





