---
description: Contient un profil de réseau local sans fil.
ms.assetid: bc97cb49-3891-4a4a-aab4-895cd9ce6908
title: Élément WLANProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 227d912128bf3f656fca7aecbaf0fe0640659465
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119377"
---
# <a name="wlanprofile-element"></a>Élément WLANProfile

L’élément **WLANProfile** contient un profil de réseau local sans fil. Cet élément est l’élément racine unique pour un profil sans fil.

L’espace de noms cible de l’élément WLANProfile est `https://www.microsoft.com/networking/WLAN/profile/v1` .

``` syntax
<xs:element name="WLANProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="SSIDConfig"
                maxOccurs="256"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="SSID"
                            maxOccurs="256"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="hex"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="hexBinary"
                                            >
                                                <xs:minLength
                                                    value="1"
                                                 />
                                                <xs:maxLength
                                                    value="32"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="name"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:minLength
                                                    value="1"
                                                 />
                                                <xs:maxLength
                                                    value="32"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
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
                        <xs:element name="nonBroadcast"
                            type="boolean"
                            minOccurs="0"
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
            <xs:element name="connectionType">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="IBSS"
                         />
                        <xs:enumeration
                            value="ESS"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="connectionMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="auto"
                         />
                        <xs:enumeration
                            value="manual"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="autoSwitch"
                type="boolean"
                minOccurs="0"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
            <xs:element name="MSM"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="connectivity"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="phyType"
                                        minOccurs="0"
                                        maxOccurs="4"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:enumeration
                                                    value="a"
                                                 />
                                                <xs:enumeration
                                                    value="b"
                                                 />
                                                <xs:enumeration
                                                    value="g"
                                                 />
                                                <xs:enumeration
                                                    value="n"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
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
                        <xs:element name="security"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="authEncryption">
                                        <xs:complexType>
                                            <xs:sequence>
                                                <xs:element name="authentication">
                                                    <xs:simpleType>
                                                        <xs:restriction
                                                            base="string"
                                                        >
                                                            <xs:enumeration
                                                                value="open"
                                                             />
                                                            <xs:enumeration
                                                                value="shared"
                                                             />
                                                            <xs:enumeration
                                                                value="WPA"
                                                             />
                                                            <xs:enumeration
                                                                value="WPAPSK"
                                                             />
                                                            <xs:enumeration
                                                                value="WPA2"
                                                             />
                                                            <xs:enumeration
                                                                value="WPA2PSK"
                                                             />
                                                        </xs:restriction>
                                                    </xs:simpleType>
                                                </xs:element>
                                                <xs:element name="encryption">
                                                    <xs:simpleType>
                                                        <xs:restriction
                                                            base="string"
                                                        >
                                                            <xs:enumeration
                                                                value="none"
                                                             />
                                                            <xs:enumeration
                                                                value="WEP"
                                                             />
                                                            <xs:enumeration
                                                                value="TKIP"
                                                             />
                                                            <xs:enumeration
                                                                value="AES"
                                                             />
                                                        </xs:restriction>
                                                    </xs:simpleType>
                                                </xs:element>
                                                <xs:element name="useOneX"
                                                    type="boolean"
                                                    minOccurs="0"
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
                                    <xs:element name="sharedKey"
                                        minOccurs="0"
                                    >
                                        <xs:complexType>
                                            <xs:sequence>
                                                <xs:element name="keyType">
                                                    <xs:simpleType>
                                                        <xs:restriction
                                                            base="string"
                                                        >
                                                            <xs:enumeration
                                                                value="networkKey"
                                                             />
                                                            <xs:enumeration
                                                                value="passPhrase"
                                                             />
                                                        </xs:restriction>
                                                    </xs:simpleType>
                                                </xs:element>
                                                <xs:element name="protected"
                                                    type="boolean"
                                                 />
                                                <xs:element name="keyMaterial"
                                                    type="string"
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
                                    <xs:element name="keyIndex"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="integer"
                                            >
                                                <xs:minInclusive
                                                    value="0"
                                                 />
                                                <xs:maxInclusive
                                                    value="3"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="PMKCacheMode"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:enumeration
                                                    value="disabled"
                                                 />
                                                <xs:enumeration
                                                    value="enabled"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="PMKCacheTTL"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="integer"
                                            >
                                                <xs:minInclusive
                                                    value="5"
                                                 />
                                                <xs:maxInclusive
                                                    value="1400"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="PMKCacheSize"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="integer"
                                            >
                                                <xs:minInclusive
                                                    value="1"
                                                 />
                                                <xs:maxInclusive
                                                    value="255"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="preAuthMode"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:enumeration
                                                    value="disabled"
                                                 />
                                                <xs:enumeration
                                                    value="enabled"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="preAuthThrottle"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="integer"
                                            >
                                                <xs:minInclusive
                                                    value="1"
                                                 />
                                                <xs:maxInclusive
                                                    value="16"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
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
            <xs:element name="IHV"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OUIHeader">
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="OUI">
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="hexBinary"
                                            >
                                                <xs:length
                                                    value="3"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="type">
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="hexBinary"
                                            >
                                                <xs:length
                                                    value="1"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
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
                        <xs:element name="connectivity"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:any
                                        processContents="lax"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="security"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:any
                                        processContents="lax"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="useMSOneX"
                            type="boolean"
                            minOccurs="0"
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

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                            | Type                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**authEncryption**](wlan-profileschema-authencryption-security-element.md)       |                                                                   | Spécifie l’authentification et la paire de chiffrement à utiliser pour ce profil.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**identification**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Spécifie la méthode d’authentification à utiliser pour se connecter au réseau local sans fil.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**Commutation autocommutateur**](wlan-profileschema-autoswitch-wlanprofile-element.md)            | [boolean](/dotnet/api/system.boolean) | Détermine le comportement d’itinérance d’un réseau connecté automatiquement lorsqu’un réseau plus préféré est à portée. Cet élément est facultatif et n’a aucun effet sur un réseau connecté manuellement.<br/> **Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md)    |                                                                   | Indique si la connexion au réseau local sans fil doit être automatique (« automatique ») ou initiée (« manuelle ») par l’utilisateur. Cet élément est facultatif.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md)    |                                                                   | Indique si le réseau est une infrastructure (« ESS ») ou ad-hoc (« IBSS »).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**connectivité**](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | Contient différents paramètres de connectivité. Cet élément est facultatif.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**connectivité**](wlan-profileschema-connectivity-ihv-element.md)                |                                                                   | Contient des paramètres de connectivité liés aux IHV.<br/> **Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**chiffre**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Définit le chiffrement des données à utiliser pour se connecter au réseau local sans fil.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**séquence**](wlan-profileschema-hex-ssid-element.md)                                 |                                                                   | Contient le SSID d’un réseau local sans fil au format hexadécimal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**FABRICANTS**](wlan-profileschema-ihv-wlanprofile-element.md)                          |                                                                   | Contient les paramètres facultatifs du fournisseur de matériel indépendant (IHV).<br/> **Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**keyIndex**](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | Spécifie l’index de clé à utiliser pour chiffrer le trafic sans fil. Cette valeur est utilisée uniquement lorsque [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) est défini sur « networkKey ».<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md)            | [string](/dotnet/api/system.string)   | Contient la clé réseau ou la phrase secrète.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | Type de clé.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**MSM**](wlan-profileschema-msm-wlanprofile-element.md)                          |                                                                   | Contient différents paramètres MSM. Cet élément est facultatif.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**nomme**](wlan-profileschema-name-wlanprofile-element.md)                        | [**nameType**](wlan-profileschema-nametype-simpletype.md)        | Nom du profil de réseau local sans fil.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**nomme**](wlan-profileschema-name-ssid-element.md)                               |                                                                   | Contient le SSID d’un réseau local sans fil.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**ne pas diffuser**](wlan-profileschema-nonbroadcast-ssidconfig-element.md)         | [boolean](/dotnet/api/system.boolean) | Indique si le réseau diffuse son SSID.<br/> **Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**OUI**](wlan-profileschema-oui-ouiheader-element.md)                            |                                                                   | Contient une hexBinary de 3 octets qui identifie le IHV.<br/> **Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md)                      |                                                                   | Identifie le IHV.<br/> **Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**phyType**](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | Spécifie la norme de réseau local sans fil 802,11 utilisée sur le réseau local sans fil. la valeur « n » est uniquement prise en charge sur Windows Vista avec SP1 et les versions ultérieures du système d’exploitation.<br/> **Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | Indique si la mise en cache PMK sera utilisée. Cet élément est valide uniquement pour les réseaux définis par WPA2.<br/> **Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**PMKCacheSize**](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | Spécifie le nombre d’entrées dans le cache PMK sur le client. Cet élément est valide uniquement pour les réseaux définis par WPA2 avec [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) défini sur « activé ». Si **PMKCacheMode** est activé et que cet élément est absent, la taille du cache est par défaut de 128 entrées.<br/> **Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**PMKCacheTTL**](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | Indique la durée, en minutes, pendant laquelle un cache PMK est conservé. Cet élément est valide uniquement pour les réseaux définis par WPA2 avec [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) défini sur « activé ».<br/> **Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**preAuthMode**](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | Détermine si la pré-authentification est utilisée par le client. La pré-authentification permet l’itinérance sécurisée sécurisée par WPA2. Cet élément est valide uniquement pour les réseaux définis par WPA2 avec [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) défini sur « activé ». Si **PMKCacheMode** est activé et que cet élément est absent, la valeur par défaut est Disabled.<br/> **Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.<br/>                                                                                                                                                                                                                                                                                         |
| [**preAuthThrottle**](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | Indique le nombre de tentatives lors de la préauthentification à des points d’accès voisins. Cet élément est valide uniquement pour les réseaux définis par WPA2 avec [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) défini sur « activé ». Si **PMKCacheMode** est activé et que cet élément est absent, le nombre de tentatives est défini par défaut sur 3.<br/> **Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.<br/>                                                                                                                                                                                                                                                                                                                              |
| [**protected**](wlan-profileschema-protected-sharedkey-element.md)                | [boolean](/dotnet/api/system.boolean) | Indique si la clé est chiffrée.<br/> **Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément doit avoir la valeur **false**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**caution**](wlan-profileschema-security-msm-element.md)                        |                                                                   | Contient différents paramètres de sécurité. Cet élément est facultatif.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**caution**](wlan-profileschema-security-ihv-element.md)                        |                                                                   | Contient des paramètres de sécurité spécifiques au IHV. Les paramètres de sécurité Microsoft et les paramètres de sécurité IHV s’excluent mutuellement. Si les deux jeux de paramètres de sécurité sont présents dans le même profil, le profil n’est pas valide.<br/> **Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**sharedKey**](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | Contient les informations sur la clé partagée. Cet élément est requis uniquement si des clés WEP ou PSK sont requises pour la paire authentification et chiffrement.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)                         |                                                                   | Spécifie le SSID d’un réseau local sans fil.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)            |                                                                   | Contient un ou plusieurs SSID avec d’autres paramètres communs. <br/> Un profil peut avoir plusieurs éléments [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) et chaque élément [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) peut avoir plusieurs éléments [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) . toutefois, Windows ne prend jamais en compte le premier élément [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) dans un élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .<br/> **Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Au plus un élément [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) peut apparaître dans un profil.<br/> |
| [**type**](wlan-profileschema-type-ouiheader-element.md)                          |                                                                   | Contient une valeur **hexBinary** de 1 octet qui est utilisée pour différencier les cartes réseau par le même IHV.<br/> **Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md)                      | [boolean](/dotnet/api/system.boolean) | Spécifie l’origine des paramètres de sécurité 802.1 X utilisés par un composant de sécurité IHV. Quand [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) a la valeur true, les composants de sécurité IHV utilisent les paramètres 802.1 x définis par Microsoft. Quand **useMSOneX** a la valeur false, les composants de sécurité IHV utilisent les paramètres 802.1 x fournis par le fournisseur. Par défaut, **useMSOneX** a la valeur false. Cet élément est facultatif.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [boolean](/dotnet/api/system.boolean) | Indique si 802.1 X est utilisé. Cet indicateur est facultatif.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Notes

La plupart des éléments enfants de l’élément WLANProfile se trouvent dans l' `https://www.microsoft.com/networking/WLAN/profile/v1` espace de noms. Il existe deux exceptions : l’élément [**FipsMode**](wlan-profileschema-fipsmode-authencryption-element.md) est dans l' `https://www.microsoft.com/networking/WLAN/profile/v2` espace de noms et l’élément [**Onex**](onexschema-onex-element.md) est dans l’espace de `https://www.microsoft.com/networking/OneX/v1` noms.

L’élément [**FipsMode**](wlan-profileschema-fipsmode-authencryption-element.md) peut être inséré en tant qu’enfant de l’élément [**authEncryption**](wlan-profileschema-authencryption-security-element.md) . L’élément [**Onex**](onexschema-onex-element.md) peut être inséré en tant qu’enfant de l’élément de [**sécurité (MSM)**](wlan-profileschema-security-msm-element.md) .

Pour afficher la liste des éléments enfants dans une structure de type arborescence, consultez [ \_ éléments de schéma de profil WLAN](wlan-profileschema-elements.md).

## <a name="examples"></a>Exemples

Pour afficher des exemples de profils, consultez la page exemples de profils [sans fil](wireless-profile-samples.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                |
| Composant redistribuable<br/>          | API de réseau local sans fil pour Windows XP avec SP2<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Exemples de profils sans fil](wireless-profile-samples.md)
</dt> </dl>

 

 
