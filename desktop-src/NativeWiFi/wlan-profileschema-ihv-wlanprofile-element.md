---
description: Contient différents paramètres pour les fournisseurs de matériel indépendants.
ms.assetid: 4ad8c991-7849-41d6-9852-1ecadc372a2d
title: Élément IHV (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IHV
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d2d2902522c84ebe2939d42301a491521ac8a70f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524513"
---
# <a name="ihv-wlanprofile-element"></a>Élément IHV (WLANProfile)

L’élément IHV (WLANProfile) contient différents paramètres pour les fournisseurs de matériel indépendants. Si un profil comprend des paramètres de sécurité IHV, ceux-ci remplacent toute sécurité définie par Microsoft.

**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.

``` syntax
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
```

L’élément est défini par l’élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="child-elements"></a>Éléments enfants



| Élément                                                             | Type                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**connectivité**](wlan-profileschema-connectivity-ihv-element.md) |                                                                   | Contient des paramètres de connectivité liés aux IHV.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**OUI**](wlan-profileschema-oui-ouiheader-element.md)             |                                                                   | Contient une hexBinary de 3 octets qui identifie le IHV.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md)       |                                                                   | Identifie le IHV.<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**caution**](wlan-profileschema-security-ihv-element.md)         |                                                                   | Contient des paramètres de sécurité spécifiques au IHV. Les paramètres de sécurité Microsoft et les paramètres de sécurité IHV s’excluent mutuellement. Le profil entier n’est pas valide si les deux paramètres de sécurité sont présents.<br/>                                                                                                                                                                                            |
| [**entrer**](wlan-profileschema-type-ouiheader-element.md)           |                                                                   | Contient une valeur hexBinary de 1 octet qui est utilisée pour différencier les cartes réseau par le même IHV.<br/>                                                                                                                                                                                                                                                                                                        |
| [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md)       | [boolean](/dotnet/api/system.boolean) | Spécifie l’origine des paramètres de sécurité 802.1 X utilisés par un composant de sécurité IHV. Quand [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) a la valeur true, les composants de sécurité IHV utilisent les paramètres 802.1 x définis par Microsoft. Quand **useMSOneX** a la valeur false, les composants de sécurité IHV utilisent les paramètres 802.1 x fournis par le fournisseur. Par défaut, **useMSOneX** a la valeur false. Cet élément est facultatif.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
