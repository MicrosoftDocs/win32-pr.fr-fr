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
ms.openlocfilehash: d9969e4e3827d926d8c295d4e1a3ce7b77550804eb4995a267a920a16871837f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758469"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





