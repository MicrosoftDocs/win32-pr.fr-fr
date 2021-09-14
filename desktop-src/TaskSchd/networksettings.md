---
title: Objet NetworkSettings
description: Pour les scripts, fournit les paramètres utilisés par le service de Planificateur de tâches pour obtenir un profil réseau.
ms.assetid: 86ac26c3-c868-4886-8f0b-3a6f6efe3e9d
keywords:
- Objet NetworkSettings Planificateur de tâches
- Planificateur de tâches d’objets NetworkSettings, Description
topic_type:
- apiref
api_name:
- NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a1eecfbbdd4e3ea00c8d2412ae912594f2ec297
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123002"
---
# <a name="networksettings-object"></a>Objet NetworkSettings

Pour les scripts, fournit les paramètres utilisés par le service de Planificateur de tâches pour obtenir un profil réseau.

## <a name="members"></a>Membres

L’objet **NetworkSettings** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **NetworkSettings** a ces propriétés.



| Propriété                                        | Type d’accès           | Description                                                                                    |
|:------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [**Identifi**](networksettings-id.md)<br/>     | Lecture/écriture<br/> | Obtient ou définit une valeur GUID qui identifie un profil réseau.<br/>                        |
| [**Nom**](networksettings-name.md)<br/> | Lecture/écriture<br/> | Obtient ou définit le nom d’un profil réseau. Le nom est utilisé à des fins d’affichage. <br/> |



 

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de vos propres données XML pour une tâche, les paramètres réseau sont spécifiés à l’aide de l’élément [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets Planificateur de tâches](task-scheduler-objects.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





