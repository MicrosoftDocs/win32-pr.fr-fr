---
title: Type complexe networkSettingsType
description: Définit les éléments qui fournissent les paramètres utilisés par le service de Planificateur de tâches pour obtenir un profil réseau.
ms.assetid: e5df1dda-b691-47ff-a956-50ff1ce9c7cc
keywords:
- Planificateur de tâches de type complexe networkSettingsType
topic_type:
- apiref
api_name:
- networkSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2a8389b1e1f368bedf03fa38dce9c8e262a401
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942342"
---
# <a name="networksettingstype-complex-type"></a>Type complexe networkSettingsType

Définit les éléments qui fournissent les paramètres utilisés par le service de Planificateur de tâches pour obtenir un profil réseau.

``` syntax
<xs:complexType name="networkSettingsType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="Id"
            type="guidType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                              | Type                                                        | Description                                                                                 |
|----------------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**Identifi**](taskschedulerschema-id-networksettingstype-element.md)     | [**guidType**](taskschedulerschema-guidtype-simpletype.md) | Spécifie une valeur GUID qui identifie un profil réseau. <br/>                       |
| [**Nom**](taskschedulerschema-name-networksettingstype-element.md) | nonEmptyString                                              | Spécifie le nom d’un profil réseau. Le nom est utilisé à des fins d’affichage. <br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





