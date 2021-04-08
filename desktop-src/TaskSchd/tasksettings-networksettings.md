---
title: TaskSettings. NetworkSettings, propriété
description: Pour les scripts, obtient ou définit l’objet paramètres réseau qui contient un identificateur et un nom de profil réseau.
ms.assetid: 3d368f6c-4534-4e71-8fbd-84361730a3e2
keywords:
- Planificateur de tâches de la propriété NetworkSettings
- Planificateur de tâches de la propriété NetworkSettings, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété NetworkSettings
topic_type:
- apiref
api_name:
- TaskSettings.NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68c81350c8516a47eb7eb160541b86945c86e29b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740428"
---
# <a name="tasksettingsnetworksettings-property"></a>TaskSettings. NetworkSettings, propriété

Pour les scripts, obtient ou définit l’objet paramètres réseau qui contient un identificateur et un nom de profil réseau. Si la propriété [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) de [**TaskSettings**](tasksettings.md) a la **valeur true** et qu’un propfile réseau est spécifié dans la propriété **NetworkSettings** , la tâche s’exécute uniquement si le profil réseau spécifié est disponible.

## <a name="syntax"></a>Syntaxe


```VB
TaskSettings.NetworkSettings As NetworkSettings
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**NetworkSettings**](networksettings.md) qui contient un identificateur et un nom de profil réseau.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TaskSettings**](tasksettings.md)
</dt> <dt>

[**NetworkSettings**](networksettings.md)
</dt> </dl>

 

 





