---
description: Contient un profil de réseau câblé.
ms.assetid: f5f9fcdc-febf-4730-8be4-5e1885d9ab08
title: Élément LANProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 58ad88c9f975455bdd2d77a0ef8ee028d9027d9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203764"
---
# <a name="lanprofile-element"></a>Élément LANProfile

L’élément LANProfile contient un profil de réseau câblé. Cet élément est l’élément racine unique d’un profil de réseau câblé.

L’espace de noms cible de l’élément LANProfile est `https://www.microsoft.com/networking/LAN/profile/v1` .

``` syntax
<xs:element name="LANProfile">
    <xs:complexType>
        <xs:sequence>
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

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                 | Type    | Description                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSM**](lan-profileschema-msm-lanprofile-element.md)                 |         | Contient les paramètres de module spécifique au média (MSM). <br/>                                                                               |
| [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md)   | boolean | Spécifie si le service de configuration automatique pour les réseaux câblés tente une authentification de port à l’aide de 802.1 X. <br/>      |
| [**OneXEnforced**](lan-profileschema-onexenforced-security-element.md) | boolean | Spécifie si le service de configuration automatique pour les réseaux câblés requiert l’utilisation de 802.1 X pour l’authentification de port. <br/> |
| [**caution**](lan-profileschema-security-msm-element.md)              |         | Contient les paramètres de sécurité. <br/>                                                                                                  |



## <a name="remarks"></a>Notes

Pour afficher la liste des éléments enfants dans une structure de type arborescence, consultez [ \_ éléments de schéma de profil de réseau local](lan-profileschema-elements.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 




