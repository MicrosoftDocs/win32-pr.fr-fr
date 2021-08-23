---
description: Contient les paramètres globaux de la configuration automatique des réseaux câblés.
ms.assetid: 172cf15c-cd51-43d4-ae5d-f9460c2a40e2
title: Élément globalFlags (LANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- globalFlags
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bfbfecbc1d60e34a913bb523f5af8c2ab25665fd689976c87725d392f6ea26c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801129"
---
# <a name="globalflags-lanpolicy-element"></a>Élément globalFlags (LANPolicy)

L’élément globalFlags (LANPolicy) contient les paramètres globaux de la configuration automatique des réseaux câblés.

``` syntax
<xs:element name="globalFlags">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enableAutoConfig"
                type="boolean"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L’élément **globalFlags** est défini par l’élément [**LANPolicy**](lan-policyschema-lanpolicy-element.md) .

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                           | Type    | Description                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) | boolean | Spécifie si les machines utilisent le service de configuration automatique intégré pour gérer les connexions aux réseaux câblés qui requièrent l’authentification de couche 2 (par exemple, 802.1 X).<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




