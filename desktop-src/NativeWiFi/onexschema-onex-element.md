---
description: Spécifie les informations de configuration 802.1 X pour un profil de réseau local câblé ou sans fil.
ms.assetid: 4528fcb5-ee8e-4824-a69e-8d67622c4b4d
title: Élément OneX
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 2a0a58d4f06b30004620f7e222cdbf8a439c9bb57ab4f7ca97e3b86eaacb2e3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684869"
---
# <a name="onex-element"></a>Élément OneX

L’élément OneX spécifie les informations de configuration 802.1 X pour un profil de réseau local câblé ou sans fil. Cet élément est l’élément racine unique pour un profil 802.1 X.

L’espace de noms cible de l’élément OneX est `https://www.microsoft.com/networking/OneX/v1` . La plupart des éléments enfants de l’élément OneX se trouvent dans l' `OneX` espace de noms. Il existe une exception : l’élément [**EAPConfig**](onexschema-eapconfig-onex-element.md) est dans l' `https://www.microsoft.com/provisioning/EapHostConfig` espace de noms.

**Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Seul l’élément [**EAPConfig**](onexschema-eapconfig-onex-element.md) est pris en charge. Les autres éléments, s’ils sont présents dans un profil, seront ignorés.

``` syntax
<xs:element name="OneX">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="cacheUserData"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="heldPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="startPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxStart"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxAuthFailures"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="supplicantMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="inhibitTransmission"
                         />
                        <xs:enumeration
                            value="includeLearning"
                         />
                        <xs:enumeration
                            value="compliant"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="machineOrUser"
                         />
                        <xs:enumeration
                            value="machine"
                         />
                        <xs:enumeration
                            value="user"
                         />
                        <xs:enumeration
                            value="guest"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="singleSignOn"
                minOccurs="0"
            >
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
            <xs:element name="EAPConfig">
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            minOccurs="1"
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



| Élément                                                                            | Type    | Description                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**authMode**](onexschema-authmode-onex-element.md)                               |         | Spécifie le type d’informations d’identification utilisées pour l’authentification.<br/>                                                                                                                                                        |
| [**authPeriod**](onexschema-authperiod-onex-element.md)                           |         | Spécifie la durée maximale, en secondes, pendant laquelle un client attend une réponse de l’authentificateur.<br/>                                                                                                  |
| [**cacheUserData**](onexschema-cacheuserdata-onex-element.md)                     | boolean | Spécifie si les informations d’identification de l’utilisateur sont mises en cache pour les connexions suivantes.<br/>                                                                                                                                     |
| [**EAPConfig**](onexschema-eapconfig-onex-element.md)                             |         | Spécifie la configuration EAPHost.<br/>                                                                                                                                                                              |
| [**heldPeriod**](onexschema-heldperiod-onex-element.md)                           |         | Spécifie la durée, en secondes, pendant laquelle un client ne tentera pas de nouveau l’authentification après l’échec d’une tentative d’authentification.<br/>                                                                             |
| [**maxAuthFailures**](onexschema-maxauthfailures-onex-element.md)                 |         | Spécifie le nombre maximal d’échecs d’authentification autorisé pour un ensemble d’informations d’identification.<br/>                                                                                                                         |
| [**maxDelay**](onexschema-maxdelay-singlesignon-element.md)                       |         | Spécifie, en secondes, le délai maximal avant que la tentative de connexion d’authentification unique échoue.<br/>                                                                                                                      |
| [**maxStart**](onexschema-maxstart-onex-element.md)                               |         | Spécifie le nombre maximal de messages EAPOL-Start envoyés.<br/>                                                                                                                                                        |
| [**singleSignOn**](onexschema-singlesignon-onex-element.md)                       |         | Spécifie les informations de configuration du réseau à authentification unique.<br/>                                                                                                                                                       |
| [**startPeriod**](onexschema-startperiod-onex-element.md)                         |         | Spécifie la durée d’attente, en secondes, avant l’envoi d’un EAPOL-Start.<br/>                                                                                                                                  |
| [**supplicantMode**](onexschema-supplicantmode-onex-element.md)                   |         | Spécifie la méthode de transmission utilisée pour les paquets EAPOL.<br/>                                                                                                                                                      |
| [**entrer**](onexschema-type-singlesignon-element.md)                               |         | Spécifie quand l’authentification unique est effectuée. Lorsque la valeur `preLogon` est définie sur, l’authentification unique est effectuée avant que l’utilisateur ouvre une session. Lorsque la valeur `postLogon` est définie sur, l’authentification unique est effectuée immédiatement après la connexion de l’utilisateur.<br/> |
| [**userBasedVirtualLan**](onexschema-userbasedvirtuallan-singlesignon-element.md) | boolean | Spécifie si le réseau local virtuel (VLAN) utilisé par l’appareil change en fonction des informations d’identification de l’utilisateur.<br/>                                                                                                                   |



## <a name="remarks"></a>Remarques

Pour afficher la liste des éléments enfants dans une structure de type arborescence, consultez [éléments de schéma Onex](onexschema-elements.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                |
| Composant redistribuable<br/>          | API de réseau local sans fil pour Windows XP avec SP2<br/>                 |



 

 




