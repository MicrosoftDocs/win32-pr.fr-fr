---
title: Élément ID (networkSettingsType)
description: Contient une valeur GUID qui identifie un profil réseau.
ms.assetid: 527912ab-9a81-4570-91c5-8f5943e79a28
keywords:
- ID, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 06196710b9db9d39d45a24b78bccabf479ef210a97f3cea1fd19286b76f2fc42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125839"
---
# <a name="id-networksettingstype-element"></a>Élément ID (networkSettingsType)

Contient une valeur GUID qui identifie un profil réseau.

``` syntax
<xs:element name="Id"
    type="guidType"
    minOccurs="0"
 />
```

L’élément **ID** est défini par le type complexe [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                            | Dérivé de                                                                       | Description                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetworkSettings (settingsType)**](taskschedulerschema-networksettings-settingstype-element.md) | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) | Contient les paramètres utilisés par le service de Planificateur de tâches pour obtenir un profil réseau. Le service de Planificateur de tâches vérifie la disponibilité de ce réseau lorsque l’élément [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) est défini sur **true**.<br/> |



## <a name="remarks"></a>Remarques

Pour le développement C++, consultez [**propriété ID de INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).

Pour le développement de scripts, consultez [**NetworkSettings.ID**](networksettings-id.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





