---
title: Élément NetworkSettings (settingsType)
description: Contient les paramètres utilisés par le service de Planificateur de tâches pour obtenir un profil réseau. Le service de Planificateur de tâches vérifie la disponibilité de ce réseau lorsque l’élément RunOnlyIfNetworkAvailable est défini sur true.
ms.assetid: 7452b788-a170-4afe-abc5-ebcd3722da0d
keywords:
- Élément NetworkSettings Planificateur de tâches
topic_type:
- apiref
api_name:
- NetworkSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c7861d91cbc2647d241bc41753efbebcc346759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465806"
---
# <a name="networksettings-settingstype-element"></a>Élément NetworkSettings (settingsType)

Contient les paramètres utilisés par le service de Planificateur de tâches pour obtenir un profil réseau. Le service de Planificateur de tâches vérifie la disponibilité de ce réseau lorsque l’élément [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) est défini sur **true**.

``` syntax
<xs:element name="NetworkSettings"
    type="networkSettingsType"
    minOccurs="0"
 />
```

L’élément **NetworkSettings** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                      | Dérivé de                                                         | Description                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Paramètres (taskType)**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Spécifie les paramètres utilisés par le Planificateur de tâches pour effectuer la tâche.<br/> |



## <a name="remarks"></a>Notes

Pour le développement C++, consultez la [**propriété NetworkSettings de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings).

Pour le développement de scripts, consultez [**TaskSettings. NetworkSettings**](tasksettings-networksettings.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





