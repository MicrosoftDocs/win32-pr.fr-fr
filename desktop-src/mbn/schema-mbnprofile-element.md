---
description: Est l’élément racine qui identifie un profil haut débit mobile.
ms.assetid: 08302e7f-3024-439b-a2ad-a4ae9487b82b
title: Élément MBNProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MBNProfile
api_type:
- Schema
ms.openlocfilehash: 049ec22c170afda3a46620e2e94e2a16ae2708b4d6a69fcd0262baa69352a0a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943359"
---
# <a name="mbnprofile-element"></a>Élément MBNProfile

L’élément **MBNProfile** est l’élément racine qui identifie un profil haut débit mobile.

Il ne peut y avoir qu’un seul élément de ce type par document.

``` syntax
<xs:element name="MBNProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Name"
                type="nameType"
             />
            <xs:element name="Description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="ICONFilePath"
                type="iconFileType"
                minOccurs="0"
             />
            <xs:element name="IsDefault"
                type="boolean"
             />
            <xs:element name="ProfileCreationType"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="token"
                    >
                        <xs:enumeration
                            value="UserProvisioned"
                         />
                        <xs:enumeration
                            value="AdminProvisioned"
                         />
                        <xs:enumeration
                            value="OperatorProvisioned"
                         />
                        <xs:enumeration
                            value="DeviceProvisioned"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="SubscriberID"
                type="subscriberIdType"
             />
            <xs:element name="SimIccID"
                type="simIccIDType"
                minOccurs="0"
             />
            <xs:element name="HomeProviderName"
                type="providerNameType"
                minOccurs="0"
             />
            <xs:element name="AutoConnectOnInternet"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="ConnectionMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="manual"
                         />
                        <xs:enumeration
                            value="auto"
                         />
                        <xs:enumeration
                            value="auto-home"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="Context"
                type="contextType"
                minOccurs="0"
             />
            <xs:element name="DataRoamingPartners"
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

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                          | Type                                                           | Description                                               |
|----------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------|
| [**AutoConnectOnInternet**](schema-autoconnectoninternet-mbnprofile-element.md) | boolean                                                        | Indique si l’appareil se connecte automatiquement.<br/> |
| [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md)               |                                                                | Paramètres de connexion automatique de l’appareil.<br/>           |
| [**Contexte**](schema-context-mbnprofile-element.md)                             | [**contextType**](schema-contexttype-complextype.md)          | Paramètres de configuration de la connexion de données.<br/>              |
| [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md)     |                                                                | Fournisseurs de réseau préférés pour l’itinérance.<br/>       |
| [**Description**](schema-description-mbnprofile-element.md)                     | [**nameType**](schema-nametype-simpletype.md)                 | Description du profil.<br/>                    |
| [**HomeProviderName**](schema-homeprovidername-mbnprofile-element.md)           | [**providerNameType**](schema-providernametype-simpletype.md) | Nom du fournisseur d’hébergement.<br/>                     |
| [**ICONFilePath**](schema-iconfilepath-mbnprofile-element.md)                   | [**iconFileType**](schema-iconfiletype-simpletype.md)         | Chemin d’accès au fichier d’icône.<br/>                         |
| [**IsDefault**](schema-isdefault-mbnprofile-element.md)                         | boolean                                                        | Indique si le profil est la valeur par défaut.<br/>            |
| [**Nom**](schema-name-mbnprofile-element.md)                                   | [**nameType**](schema-nametype-simpletype.md)                 | Nom du profil.<br/>                           |
| [**ProfileCreationType**](schema-profilecreationtype-mbnprofile-element.md)     |                                                                | Informations sur le créateur du profil.<br/>         |
| [**SimIccID**](schema-simiccid-mbnprofile-element.md)                           | [**simIccIDType**](schema-simiccidtype-simpletype.md)         | Numéro d’identification SIM pour les appareils GSM.<br/>     |
| [**Abonné**](schema-subscriberid-mbnprofile-element.md)                   | [**subscriberIdType**](schema-subscriberidtype-simpletype.md) | Identificateur unique du profil.<br/>              |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



 

 




