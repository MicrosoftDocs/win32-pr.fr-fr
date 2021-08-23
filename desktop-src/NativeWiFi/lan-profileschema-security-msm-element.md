---
description: Contient les paramètres de sécurité pour les réseaux câblés.
ms.assetid: 08470cf4-3722-4cb9-9877-13eca2f7d04e
title: Élément Security (MSM) (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8f66021f61536e8c8f09663e9ec2513b11d1ec87829f5c100b48cbf15d98cdd2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685059"
---
# <a name="security-msm-element-lan_policy"></a>Élément Security (MSM) (LAN_policy)

L’élément Security (MSM) contient des paramètres de sécurité pour les réseaux câblés. Cet élément est facultatif.

``` syntax
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
```

L’élément de **sécurité** est défini par l’élément [**MSM**](lan-profileschema-msm-lanprofile-element.md) .

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                 | Type    | Description                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md)   | boolean | Spécifie si le service de configuration automatique pour les réseaux câblés tente une authentification de port à l’aide de 802.1 X. <br/>      |
| [**OneXEnforced**](lan-profileschema-onexenforced-security-element.md) | boolean | Spécifie si le service de configuration automatique pour les réseaux câblés requiert l’utilisation de 802.1 X pour l’authentification de port. <br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**MSM**](lan-profileschema-msm-lanprofile-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**MSM (LANProfile)**](lan-profileschema-msm-lanprofile-element.md)
</dt> </dl>

 

 




