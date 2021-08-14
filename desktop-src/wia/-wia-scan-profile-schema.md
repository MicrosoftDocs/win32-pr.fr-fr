---
description: le schéma de profil d’analyse définit un format XML qui peut être utilisé pour stocker les propriétés des éléments d’Acquisition d’images Windows (WIA), tels que les scanneurs et les appareils photo.
ms.assetid: e0848db3-652a-45be-a18b-99b82420c586
title: Analyser le schéma de profil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81091e75269206b6b3b5a89f86c6f92da5c1d2080d90382ac6af48c6d1cc32ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208015"
---
# <a name="scan-profile-schema"></a>Analyser le schéma de profil

le schéma de profil d’analyse définit un format XML qui peut être utilisé pour stocker les propriétés des éléments d’Acquisition d’images Windows (WIA), tels que les scanneurs et les appareils photo. Ces fichiers persistants permettent aux applications de fournir une analyse automatique sans demander aux utilisateurs de mémoriser les paramètres de propriété des éléments.

Tout appareil [**IWiaItem2**](-wia-iwiaitem2.md) peut avoir un profil de numérisation. Toutefois, les éléments **IWiaItem2** de type WIA la \_ catégorie \_ \_ fichier fini et la racine de catégorie WIA \_ \_ ne peuvent pas avoir de profils.

Les profils d’analyse sont créés et gérés par le biais des interfaces [**IScanProfile**](-wia-iscanprofile.md), [**IScanProfileMgr**](-wia-iscanprofilemgr.md)et [**IScanProfileUI**](-wia-iscanprofileui.md) . Les utilisateurs de votre application peuvent modifier les profils de manière limitée à l’aide de la méthode [**IScanProfileUI :: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .

Tous les profils d’analyse comportent les éléments suivants : `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` et `<Properties>` . Le profil par défaut d’un appareil possède également un `<Default>` élément.

L' `<ProfileGUID>` élément et l' `<DeviceID>` élément ne peuvent pas être modifiés une fois le profil de numérisation créé. Les valeurs de l' `<ProfileName>` élément et de l' `<WiaItem>` élément peuvent être modifiées. L' `<Default>` élément peut être ajouté ou supprimé. Cette opération peut être effectuée par programmation à l’aide des méthodes [**IScanProfile :: SetName**](-wia-iscanprofile-setname.md), [**IScanProfile :: SetItem**](-wia-iscanprofile-setitem.md)et [**IScanProfileMgr :: SetDefault**](-wia-iscanprofilemgr-setdefault.md) . Ces propriétés peuvent également être modifiées par les utilisateurs par le biais de la méthode [**IScanProfileUI :: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .

L' `<Properties>` élément contient des `<Property>` enfants. Utilisez-les pour ajouter n’importe quelle propriété d’élément ou d’appareil WIA au profil. Vous pouvez également développer votre propre image acquisition `<Property>` Children. Cela rend le schéma de profil d’analyse extensible. (Pour plus d’informations sur l’extension du schéma, consultez [définition des propriétés personnalisées](-wia-defining-custom-properties.md), [**IScanProfile :: GetProperty**](-wia-iscanprofile-getproperty.md)et [**IScanProfile :: SetProperty**](-wia-iscanprofile-setproperty.md).)

Voici le schéma complet du profil de numérisation. Voici un exemple de profil.


```
<?xml version="1.0"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema"
            targetNamespace="https://www.microsoft.com"
            xmlns="https://www.microsoft.com"
            elementFormDefault="qualified">

<xs:element name="ScanProfile">
            <xs:complexType>
            <xs:sequence>
                        <xs:element name="ProfileGUID" type="xs:string"/>
                        <xs:element name="DeviceID" type="xs:string"/>
<xs:element name="ProfileName" type="xs:string"/>
                        <xs:element name="Default" minOccurs="0">
                                    <xs:complexType>
                                    </xs:complexType>
                        </xs:element>
                        <xs:element name="WiaItem" type="xs:string"/>
                        <xs:element name="Properties" type="Properties"/>
            </xs:sequence>
            </xs:complexType>
</xs:element>
 
<xs:complexType name="Properties">
<xs:sequence>
            <xs:element name="Property" maxOccurs="unbounded" minOccurs="0">
            <xs:complexType>
            <xs:simpleContent>
                        <xs:extension base="xs:string">
                                    <xs:attribute name="id" type="xs:integer" use="required"/>
                                    <xs:attribute name="type" type="xs:integer" use="required"/>
                        </xs:extension>
            </xs:simpleContent>
            </xs:complexType>
            </xs:element>
</xs:sequence>
</xs:complexType>
 
</xs:schema>
```



Cliquez sur **afficher l’exemple** pour afficher un exemple de profil.


```
<ScanProfile>
    <ProfileGUID>
        {F862E217-32B0-4396-987A-2191224925CD}
    </ProfileGUID>
    <DeviceID>
        {6BDD1FC6-810F-11D0-BEC7-08002BE2092F}\0001
    </DeviceID>
    <ProfileName>
        Last used settings
    </ProfileName>
    <WiaItem>
        {FB607B1F-43F3-488B-855B-FB703EC342A6}
    </WiaItem>
    <Properties>
        <Property id="4103" type="3">
            3
        </Property>
        <Property id="4106" type="72">
            {B96B3CAB-0728-11D3-9D7B-0000F81EF32E}
        </Property>
        <Property id="6147" type="3">
            300
        </Property>
        <Property id="6154" type="3">
            0
        </Property>
        <Property id="6155" type="3">
            0
        </Property>
    </Properties>
</ScanProfile>
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[**IScanProfile :: GetProperty**](-wia-iscanprofile-getproperty.md)
</dt> <dt>

[**IScanProfile :: SetProperty**](-wia-iscanprofile-setproperty.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Constantes de propriété WIA](-wia-wia-property-constants.md)
</dt> <dt>

[Définition des propriétés personnalisées](-wia-defining-custom-properties.md)
</dt> </dl>

 

 



