---
title: Élément NetworkProfileName (settingsType)
description: Contient le nom d’un profil réseau. Le service de Planificateur de tâches vérifie la disponibilité de ce réseau lorsque l’élément RunOnlyIfNetworkAvailable est défini sur true. Le nom est utilisé à des fins d’affichage.
ms.assetid: f02dc75c-6c48-4a42-8263-13d9704b993c
keywords:
- Élément NetworkProfileName Planificateur de tâches
topic_type:
- apiref
api_name:
- NetworkProfileName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 464c8b8f23dfeed6ea7c3412c3eeec07f20e5a8a7fcea662b4a16dfac7cb3fb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758489"
---
# <a name="networkprofilename-settingstype-element"></a>Élément NetworkProfileName (settingsType)

Contient le nom d’un profil réseau. Le service de Planificateur de tâches vérifie la disponibilité de ce réseau lorsque l’élément [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) est défini sur **true**. Le nom est utilisé à des fins d’affichage.

``` syntax
<xs:element name="NetworkProfileName"
    type="string"
    minOccurs="0"
 />
```

L’élément **NetworkProfileName** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                      | Dérivé de                                                         | Description                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Paramètres (taskType)**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Spécifie les paramètres utilisés par le Planificateur de tâches pour effectuer la tâche.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





