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
ms.openlocfilehash: 730701c71a69f05b73524d6f9d1d8ad3d89b5e93620664be33a80c5c41af1479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059655"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TaskSettings**](tasksettings.md)
</dt> <dt>

[**NetworkSettings**](networksettings.md)
</dt> </dl>

 

 





