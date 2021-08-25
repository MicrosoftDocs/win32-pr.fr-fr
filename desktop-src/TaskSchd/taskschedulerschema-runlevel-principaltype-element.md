---
title: Élément RunLevel (runLevelType)
description: Contient une valeur qui spécifie le niveau de contexte de sécurité pour l’exécution de la tâche.
ms.assetid: dc113ffa-8ac9-4dcd-a106-45295da42f46
keywords:
- Élément RunLevel Planificateur de tâches
topic_type:
- apiref
api_name:
- RunLevel
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 143db96de30e647c67abadc2a9fb4384ae9784604b9c679efd9de5fd2157f923
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991089"
---
# <a name="runlevel-runleveltype-element"></a>Élément RunLevel (runLevelType)

Contient une valeur qui spécifie le niveau de contexte de sécurité pour l’exécution de la tâche. Vous pouvez spécifier l’exécution d’une tâche en utilisant des privilèges minimum ou des privilèges élevés. La valeur 0 spécifie d’exécuter la tâche avec les privilèges les plus faibles, et la valeur 1 spécifie d’exécuter la tâche avec des privilèges élevés.

``` syntax
<xs:element name="RunLevel"
    type="runLevelType"
 />
```

L’élément **runlevel** est défini par le type simple [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                  | Dérivé de                                                           | Description                                                                                                                           |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**Principal (principalType)**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Spécifie les informations d’identification de sécurité pour un principal. Ces informations d’identification définissent le contexte de sécurité sous lequel une tâche s’exécute. <br/> |



## <a name="remarks"></a>Remarques

Pour le développement C++, consultez la [**propriété runlevel de IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel).

Pour le développement de scripts, consultez [**principal. runlevel**](principal-runlevel.md).

Si une tâche est inscrite à l’aide du compte **\\ administrateur builtin** ou des comptes [LocalSystem](/windows/desktop/Services/localsystem-account) ou [LocalService](/windows/desktop/Services/localservice-account) , la propriété [**runlevel**](principal-runlevel.md) est ignorée. La valeur de l’attribut sera également ignorée si le [contrôle de compte d’utilisateur](/windows/desktop/SecAuthZ/user-account-control) (UAC) est désactivé.

Si une tâche est inscrite à l’aide du groupe **administrateurs** pour le contexte de sécurité de la tâche, vous devez également définir la propriété [**runlevel**](principal-runlevel.md) sur « highestAvailable » pour exécuter la tâche. Pour plus d’informations, consultez [contextes de sécurité pour les tâches](security-contexts-for-running-tasks.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

