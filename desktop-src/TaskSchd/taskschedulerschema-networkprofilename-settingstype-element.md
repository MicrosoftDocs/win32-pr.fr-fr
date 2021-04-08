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
ms.openlocfilehash: 76a1e89b1d40a422f10512583563e9b1ac56c06f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742157"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





