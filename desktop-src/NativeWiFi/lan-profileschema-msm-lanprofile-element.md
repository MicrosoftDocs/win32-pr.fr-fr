---
description: Contient les paramètres de module spécifique au média (MSM).
ms.assetid: fe858701-e0eb-4817-b3c2-ae61e96a4cbe
title: Élément MSM (LANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSM
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e9e58895ae36a304e713ecdb21b4008a2027e8c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203762"
---
# <a name="msm-lanprofile-element"></a>Élément MSM (LANProfile)

L’élément MSM (LANProfile) contient des paramètres de module spécifique au média (MSM).

``` syntax
<xs:element name="MSM">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="security">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OneXEnforced"
                            type="boolean"
                         />
                        <xs:element name="OneXEnabled"
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

L’élément **MSM** est défini par l’élément [**LANProfile**](lan-profileschema-lanprofile-element.md) .

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                 | Type    | Description                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md)   | boolean | Spécifie si le service de configuration automatique pour les réseaux câblés tente une authentification de port à l’aide de 802.1 X.<br/>       |
| [**OneXEnforced**](lan-profileschema-onexenforced-security-element.md) | boolean | Spécifie si le service de configuration automatique pour les réseaux câblés requiert l’utilisation de 802.1 X pour l’authentification de port. <br/> |
| [**caution**](lan-profileschema-security-msm-element.md)              |         | Contient les paramètres de sécurité. <br/>                                                                                                  |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**LANProfile**](lan-profileschema-lanprofile-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**LANProfile**](lan-profileschema-lanprofile-element.md)
</dt> </dl>

 

 




