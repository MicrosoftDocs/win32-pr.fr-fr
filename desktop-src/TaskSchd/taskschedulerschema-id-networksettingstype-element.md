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
ms.openlocfilehash: 3d14865d50e9c3418e3ef65cdbeaea747a98a4ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106369"
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



## <a name="remarks"></a>Notes

Pour le développement C++, consultez [**propriété ID de INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).

Pour le développement de scripts, consultez [**NetworkSettings.ID**](networksettings-id.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





