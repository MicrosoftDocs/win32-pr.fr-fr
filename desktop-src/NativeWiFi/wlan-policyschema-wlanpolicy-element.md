---
description: Contient une stratégie de réseau local sans fil.
ms.assetid: 16ffb682-f88b-4ca1-a902-d2db5e347975
title: Élément WLANPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e9e56e25e51a3c6e798242b390f5d8b7341d7306455f1b15eb9e450830d3c9b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064699"
---
# <a name="wlanpolicy-element"></a>Élément WLANPolicy

L’élément **WLANPolicy** contient une stratégie de réseau local sans fil. Cet élément est l’élément racine unique d’un profil de stratégie sans fil.

L’espace de noms cible de l’élément **WLANPolicy** est `https://www.microsoft.com/networking/WLAN/policy/v1` .

``` syntax
<xs:element name="WLANPolicy">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="globalFlags">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enableAutoConfig"
                            type="boolean"
                         />
                        <xs:element name="showDeniedNetwork"
                            type="boolean"
                         />
                        <xs:element name="allowEveryoneToCreateAllUserProfiles"
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
            <xs:element name="networkFilter"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="allowList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
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
                        <xs:element name="blockList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
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
                        <xs:element name="denyAllIBSS"
                            type="boolean"
                            minOccurs="0"
                         />
                        <xs:element name="denyAllESS"
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
            <xs:element name="profileList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
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



| Élément                                                                                                                    | Type                                                                     | Description                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**allowEveryoneToCreateAllUserProfiles**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | boolean                                                                  | Spécifie si un utilisateur peut créer un profil tous les utilisateurs. <br/>                                                               |
| [**allowList**](wlan-policyschema-allowlist-networkfilter-element.md)                                                     |                                                                          | Liste des réseaux locaux sans fil auxquels un ordinateur doit être autorisé à se connecter. <br/>                                       |
| [**Noires**](wlan-policyschema-blocklist-networkfilter-element.md)                                                     |                                                                          | Liste des réseaux locaux sans fil auxquels un ordinateur ne doit pas se connecter.<br/>                                                    |
| [**denyAllESS**](wlan-policyschema-denyalless-networkfilter-element.md)                                                   | boolean                                                                  | Spécifie si l’accès à tous les réseaux d’infrastructure est bloqué. <br/>                                                           |
| [**denyAllIBSS**](wlan-policyschema-denyallibss-networkfilter-element.md)                                                 | boolean                                                                  | Spécifie si l’accès à tous les réseaux ad hoc est bloqué. <br/>                                                                   |
| [**descriptive**](wlan-policyschema-description-wlanpolicy-element.md)                                                    | [**nameType**](wlan-policyschema-nametype-simpletype.md)                | Description d’une stratégie de réseau local sans fil. <br/>                                                                                |
| [**enableAutoConfig**](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | boolean                                                                  | Spécifie si les ordinateurs utilisent le service de configuration automatique intégré (AutoConfig) pour gérer les connexions sans fil. <br/> |
| [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)                                                    |                                                                          | Contient les paramètres globaux du module d’auto-configuration (ACM). <br/>                                                    |
| [**nomme**](wlan-policyschema-name-wlanpolicy-element.md)                                                                  | [**nameType**](wlan-policyschema-nametype-simpletype.md)                | Nom d’une stratégie de réseau local sans fil. <br/>                                                                                       |
| [**réseaux**](wlan-policyschema-network-allowlist-element.md)                                                             | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | Un réseau autorisé. <br/>                                                                                                      |
| [**réseaux**](wlan-policyschema-network-blocklist-element.md)                                                             | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | Un réseau bloqué. <br/>                                                                                                       |
| [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)                                                |                                                                          | Liste des réseaux autorisés et refusés.<br/>                                                                                  |
| [**profileList**](wlan-policyschema-profilelist-wlanpolicy-element.md)                                                    |                                                                          | Contient une liste de profils à appliquer au niveau du domaine ou de l’ordinateur. <br/>                                                |
| [**showDeniedNetwork**](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | boolean                                                                  | spécifie si les réseaux refusés s’affichent dans le **Connecter à un assistant réseau** . <br/>                                         |



## <a name="remarks"></a>Remarques

Pour afficher la liste des éléments enfants dans une structure de type arborescence, consultez [ \_ éléments de schéma de stratégie WLAN](wlan-policyschema-elements.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 




