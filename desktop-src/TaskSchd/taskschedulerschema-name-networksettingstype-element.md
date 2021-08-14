---
title: Élément Name (networkSettingsType)
description: Contient le nom d’un profil réseau. Le nom est utilisé à des fins d’affichage.
ms.assetid: 86e4e68d-3c36-41eb-8563-d7d5125a5957
keywords:
- Élément Name Planificateur de tâches
topic_type:
- apiref
api_name:
- Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c41b92c7e63a820c2a2a34378b041bec3a49f432b52887a732c3f3bfd360b10f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758499"
---
# <a name="name-networksettingstype-element"></a>Élément Name (networkSettingsType)

Contient le nom d’un profil réseau. Le nom est utilisé à des fins d’affichage.

``` syntax
<xs:element name="Name"
    type="nonEmptyString"
    minOccurs="0"
 />
```

L’élément **Name** est défini par le type complexe [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                            | Dérivé de                                                                       | Description                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetworkSettings (settingsType)**](taskschedulerschema-networksettings-settingstype-element.md) | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) | Contient les paramètres utilisés par le service de Planificateur de tâches pour obtenir un profil réseau. Le service de Planificateur de tâches vérifie la disponibilité de ce réseau lorsque l’élément [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) est défini sur **true**.<br/> |



## <a name="remarks"></a>Remarques

Pour le développement C++, consultez la [**propriété Name de INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).

Pour le développement de scripts, consultez [**NetworkSettings.Name**](networksettings-name.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





