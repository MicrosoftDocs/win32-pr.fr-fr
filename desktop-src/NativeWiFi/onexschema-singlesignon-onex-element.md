---
description: Spécifie les informations de configuration du réseau de l’authentification unique (SSO).
ms.assetid: c0a26f15-77fd-43e9-a6af-54e9b46f03fa
title: Élément singleSignOn (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- singleSignOn
api_type:
- Schema
api_location: ''
ms.openlocfilehash: fd25767ed311e9a6f0e75f8dec090d4b80d3f0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521554"
---
# <a name="singlesignon-onex-element"></a>Élément singleSignOn (OneX)

L’élément singleSignOn (OneX) spécifie les informations de configuration du réseau de l’authentification unique (SSO).

Cet élément est facultatif. N’utilisez pas l’élément singleSignOn dans un profil si le réseau ne l’exige pas.

**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.

``` syntax
<xs:element name="singleSignOn">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="type"
                minOccurs="1"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="preLogon"
                         />
                        <xs:enumeration
                            value="postLogon"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxDelay"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="0"
                         />
                        <xs:enumeration
                            value="120"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="userBasedVirtualLan"
                type="boolean"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L’élément **singleSignOn** est défini par l’élément [**Onex**](onexschema-onex-element.md) .

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                            | Type    | Description                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**maxDelay**](onexschema-maxdelay-singlesignon-element.md)                       |         | Spécifie, en secondes, le délai maximal avant que la tentative de connexion d’authentification unique échoue.<br/>                                                                                                                      |
| [**entrer**](onexschema-type-singlesignon-element.md)                               |         | Spécifie quand l’authentification unique est effectuée. Lorsque la valeur `preLogon` est définie sur, l’authentification unique est effectuée avant que l’utilisateur ouvre une session. Lorsque la valeur `postLogon` est définie sur, l’authentification unique est effectuée immédiatement après la connexion de l’utilisateur.<br/> |
| [**userBasedVirtualLan**](onexschema-userbasedvirtuallan-singlesignon-element.md) | boolean | Spécifie si le réseau local virtuel (VLAN) utilisé par l’appareil change en fonction des informations d’identification de l’utilisateur.<br/>                                                                                                                   |



## <a name="remarks"></a>Notes

Ce paramètre peut être défini sur la ligne de commande à l’aide de la commande **netsh wlan set profileparameter** . Pour plus d’informations, consultez [commandes netsh pour réseau local sans fil (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**802.1x**](onexschema-onex-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**802.1x**](onexschema-onex-element.md)
</dt> </dl>

 

 
