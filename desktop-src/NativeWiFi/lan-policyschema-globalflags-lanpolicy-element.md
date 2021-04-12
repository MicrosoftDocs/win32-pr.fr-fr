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
ms.openlocfilehash: c9a244fbbc616e3092e2293fe187da1d7be0fa53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203765"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



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

 

 




