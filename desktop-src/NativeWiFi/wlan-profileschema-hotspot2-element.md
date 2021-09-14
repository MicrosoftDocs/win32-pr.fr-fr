---
description: Étend le schéma de profil WLAN v1 pour prendre en charge les réseaux hotspot 2,0.
ms.assetid: DE30DBCB-80B9-43D0-8DE1-56BBA99DBF31
title: Élément Hotspot2 (WLANProfile)
ms.topic: reference
ms.date: 10/08/2019
topic_type:
- APIRef
- kbSyntax
api_name:
- Hotspot2
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0e372c1025a74dfb304cacdb0f3a4cf18bcdbabd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194764"
---
# <a name="hotspot2-wlanprofile-element"></a>Élément Hotspot2 (WLANProfile)

Étend le schéma de profil WLAN v1 pour prendre en charge les réseaux hotspot 2,0. La zone réactive 2,0 permet la connexion automatique aux services de Wi-Fi publics à l’aide des informations d’identification existantes et de l’appartenance aux réseaux de fournisseurs de services. Les fournisseurs de services spécifient la façon dont les connexions sont établies à l’aide des nouveaux éléments de schéma pour décrire les réseaux à utiliser et comment s’y authentifier.

``` syntax
<xs:element name="Hotspot2">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="DomainName"
                minOccurs="0"
             />
            <xs:element name="NAIRealm"
                minOccurs="0"
             />
            <xs:element name="Network3GPP"
                minOccurs="0"
             />
            <xs:element name="RoamingConsortium"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L’élément est défini par l’élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="child-elements"></a>Éléments enfants

| Élément | Type | Description |
|-|-|-|
| [**DomainName**](wlan-profileschema-hotspot2-domainname-element.md) | | Nom de domaine pour le fournisseur de réseau local de l’appareil, identifiant l’opérateur du réseau. |
| [**NAIRealm**](wlan-profileschema-hotspot2-nairealm-element.md) | | Liste d’identificateurs de domaine NAI (Network Access identifier). Les entrées de cette liste sont généralement de la forme user@domain . |
| [**Network3GPP**](wlan-profileschema-hotspot2-network3gpp-element.md) | | Liste des ID PLMN (public Land Mobile Network). |
| [**RoamingConsortium**](wlan-profileschema-hotspot2-roamingconsortium-element.md) | | Liste des identificateurs uniques (OUI) attribués par IEEE.  |

## <a name="examples"></a>Exemples

```xml
<Hotspot2>
  <DomainName>contoso.com</DomainName>
  <NAIRealm>
    <name>test1@contoso.com</name>
    <name>test2@contoso.com</name>
  </NAIRealm>
  <Network3GPP>
    <PLMNID>12345</PLMNID>
    <PLMNID>123456</PLMNID>
  </Network3GPP>
  <RoamingConsortium>
    <OUI>00AABB</OUI>
    <OUI>001122</OUI>
  </RoamingConsortium>
</Hotspot2>
```
