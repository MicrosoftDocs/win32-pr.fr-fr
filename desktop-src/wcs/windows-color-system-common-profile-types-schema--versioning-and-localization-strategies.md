---
title: Schéma des types de profils communs du système de couleurs Windows, stratégies de gestion des versions et de localisation
description: Schéma des types de profils communs du système de couleurs Windows, stratégies de gestion des versions et de localisation
ms.assetid: 295522c6-7c53-47f6-9b98-aeee2b0e34fc
keywords:
- Windows Système de couleurs (WCS), types de profils communs
- WCS (Windows Color System), types de profils communs
- gestion des couleurs des images, types de profils communs
- gestion des couleurs, types de profils communs
- couleurs, types de profils communs
- Windows Système de couleurs (WCS), profils
- WCS (Windows Color System), profils
- gestion des couleurs des images, profils
- gestion des couleurs, profils
- couleurs, profils
- Windows Système de couleurs (WCS), contrôle de version
- WCS (Windows Color System), contrôle de version
- gestion des couleurs des images, contrôle de version
- gestion des couleurs, contrôle de version
- couleurs, contrôle de version
- Windows Système de couleurs (WCS), localisation
- WCS (Windows Color System), localisation
- gestion des couleurs des images, localisation
- gestion des couleurs, localisation
- couleurs, localisation
- Types de profils communs WCS
- profiler les consommateurs
- types de profils communs
- schémas, types de profils communs
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c9df44fa7095d8cbcd3df6de00c92ba2d4ab2ddb7ef7d3565a820e925265ea0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442289"
---
# <a name="windows-color-system-common-profile-types-schema-versioning-and-localization-strategies"></a>Schéma des types de profils communs du système de couleurs Windows, stratégies de gestion des versions et de localisation

-   [Schéma des types de profil commun WCS v1](#wcs-common-profile-types-schema-v1)
-   [Ajouts au schéma des types de profils communs WCS](#wcs-common-profile-types-schema-v2-additions)
-   [Contrôle de version du schéma de profil WCS](#wcs-profile-schema-versioning)
-   [Localisation du profil WCS](#wcs-profile-localization)
    -   [Exprimant des éléments localisables](#expressing-localizable-elements)
    -   [Prise en charge des schémas](#schema-support)
    -   [Sélection de la langue](#selecting-the-language)
    -   [Profils intégrés](#built-in-profiles)
-   [Rubriques connexes](#related-topics)

## <a name="wcs-common-profile-types-schema-v1"></a>Schéma des types de profil commun WCS v1

Les éléments suivants fournissent la définition de schéma v 1.0 pour les types de profils communs WCS.


```XML
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:import namespace="http://www.w3.org/XML/1998/namespace" />

  <xs:annotation>
    <xs:documentation xml:lang="en">
      Common types used in WCS profile schemas.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:simpleType name="NonNegativeFloatType">
    <xs:restriction base="xs:float">
      <xs:minInclusive value="0"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="NonNegativeCIEXYZType">
    <xs:attribute name="X" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Y" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Z" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:simpleType name="GUIDType">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="LocalizedTextType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute ref="xml:lang" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="MultiLocalizedTextType">
    <xs:sequence>
      <xs:element name="Text" type="wcs:LocalizedTextType" minOccurs="1" />
    </xs:sequence>
  </xs:complexType>

</xs:schema>

```



Seuls les encodages UTF-8 ou UTF-16 sont pris en charge. Tous les autres encodages XML sont fortement déconseillés afin de préserver une interopérabilité optimale.

## <a name="wcs-common-profile-types-schema-v2-additions"></a>Ajouts au schéma des types de profils communs WCS

dans Windows 7, le schéma des types de profils communs wcs a été mis à jour pour inclure les types afin de prendre en charge le [schéma d’étalonnage wcs](wcs-calibration-schema.md).


```XML
  <xs:complexType name="ParameterizedCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="wcs:ParameterizedCurveType"/>
      <xs:element name="GreenTRC" type="wcs:ParameterizedCurveType"/>
      <xs:element name="BlueTRC" type="wcs:ParameterizedCurveType"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="ParameterizedCurveType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset1" type="xs:float" use="optional"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="optional"/>
    <xs:attribute name="Offset2" type="xs:float " use="optional"/>
    <xs:attribute name="TransitionPoint" type="wcs:NonNegativeFloatType" use="optional"/>
    <xs:attribute name="Offset3" type="xs:float" use="optional"/>
  </xs:complexType>

  <xs:simpleType name="FloatList">
    <xs:list itemType="xs:float"/>
  </xs:simpleType>

  <xs:complexType name="OneDimensionLutType">
    <xs:sequence>
      <xs:element name="Input" type="wcs:FloatList"/>
      <xs:element name="Output" type="wcs:FloatList"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="HDRToneResponseCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="wcs:OneDimensionLutType"/>
      <xs:element name="GreenTRC" type="wcs:OneDimensionLutType"/>
      <xs:element name="BlueTRC" type="wcs:OneDimensionLutType"/>
    </xs:sequence>
    <xs:attribute name="TRCLength" use="required">
      <xs:simpleType>
        <xs:restriction base="xs:int">
          <xs:minInclusive value="2" />
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
```



## <a name="wcs-profile-schema-versioning"></a>Contrôle de version du schéma de profil WCS

Dans cette annexe, le terme « consommateur de profils » fait référence au logiciel WCS, ou à un composant logiciel tiers qui consomme des profils WCS.

Les versions plus récentes des consommateurs de profils pourront utiliser des profils WCS écrits conformément aux anciennes versions des schémas. Pour tirer pleinement parti des fonctionnalités définies dans la version la plus récente des schémas, la version la plus récente d’un consommateur de profils est généralement requise. Toutefois, les consommateurs de profils plus anciens peuvent utiliser des profils écrits selon des versions plus récentes des schémas. Le consommateur de profils peut ignorer les éléments et les attributs XML qu’il ne comprend pas. Les résultats sont corrects, mais les performances ou la fidélité peuvent être dégradées par rapport aux résultats obtenus avec la version la plus récente du profil consommateur.

Voici les instructions de contrôle de version pour les consommateurs de profils :

-   Une version donnée d’un consommateur de profil doit reconnaître tous les éléments et attributs d’un espace de noms de version, ou aucun d’entre eux.
-   Si un consommateur de profils rencontre un élément ou un attribut à partir d’un espace de noms qu’il ne comprend pas, il doit traiter ce problème comme une condition d’erreur, sauf si le profil contient des indications explicites sur le traitement de secours.
-   La [spécification Open Packaging](https://www.microsoft.com/whdc/xps/xpspkg.mspx) définit un URI d’espace de noms supplémentaire, l’espace de noms de compatibilité du balisage, qui définit les éléments et les attributs qui fournissent ce guide de traitement de secours.
-   Toutes les versions de tous les consommateurs de profils doivent reconnaître et respecter tous les éléments et attributs de l’espace de noms de compatibilité du balisage.
-   Les consommateurs de profils basés sur une nouvelle version des schémas de profil doivent prendre en charge tous les espaces de noms de version précédemment définis.

Dans la version 1.0, WCS reconnaît les éléments et les attributs des espaces de noms suivants :

-   https://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel
-   https://schemas.microsoft.com/windows/2005/02/color/GamutMapModel
-   https://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
-   https://schemas.microsoft.com/winfx/2005/06/markup-compatibility

L’exemple suivant illustre la compatibilité du balisage.


```XML
<?xml version="1.0" encoding="utf-8" ?>
<ColorAppearanceModel
  xmlns=http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
  xmlns:cam2=http://schemas.microsoft.com/windows/2007/08/color/ColorAppearanceModel
  xmlns:mc=http://schemas.microsoft.com/winfx/2005/02/markup-compatibility
  xs:schemaLocation="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel ColorAppearanceModel.xsd"
  xmlns:xs='http://www.w3.org/2001/XMLSchema-instance'
  mc:Ignorable="cam2">

  <ProfileName>Default profile for ICC viewing conditions</ProfileName>
  <mc:AlternateContent>
    <mc:Choice Requires="cam2">
      <cam2:AudioDescription source="ProfileExplanation.wav"/>
    </mc:Choice>
    <mc:Fallback>
      <Description>Appropriate for a print in a D50 viewing booth</Description>
        </mc:Fallback>
  </mc:AlternateContent>
  <Author>Microsoft</Author>

  <ViewingConditions>
    <WhitePointName>D50</WhitePointName>
    <Background X="19.3" Y="20.0" Z="16.5" />
    <Surround>Average</Surround>
    <LuminanceOfAdaptingField>31.8</LuminanceOfAdaptingField>
    <DegreeOfAdaptation>-1</DegreeOfAdaptation>
    <cam2:Humidity>30%</cam2:Humidity>
  </ViewingConditions>

</ColorAppearanceModel>
```



## <a name="wcs-profile-localization"></a>Localisation du profil WCS

**Requirements**

Les profils WCS contiennent certains éléments tels que ProfileName et description qui contiennent du texte explicite. Ce texte peut être localisé.

Les instructions de contrôle de version pour les créateurs de profils sont les suivantes :

-   Pour les profils créés par des tiers, tels que les fabricants d’imprimantes, l’auteur du profil doit incorporer du texte descriptif dans plusieurs langues.
-   Les éléments suivants doivent être localisables : 

    | Élément     | CDMP | GMMP | Camping |
    |-------------|------|------|------|
    | ProfileName | x    | x    | x    |
    | Description | x    | x    | x    |
    | Auteur      | x    | x    | x    |

    

     

### <a name="expressing-localizable-elements"></a>Exprimant des éléments localisables

Au lieu de contenir directement du texte, chaque élément localisable contient un ou plusieurs sous-éléments WCS : Text, chacun d’entre eux devant spécifier l’attribut XML : lang. Comme décrit dans la section [XML specification](http://www.w3.org/TR/REC-xml/) 2,12 (« Language identification »), la valeur de l’attribut XML : lang doit être un identificateur de langue RFC 3066 IETF, par exemple « en-US », « en » ou « FR-fr ». Dans les schémas WCS, la valeur de l’attribut XML : lang ne doit pas être la chaîne vide "", même si XML l’autorise dans le cas général. Par exemple :


```XML
<cdm:ColorDeviceModel ... />
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceeModel>
```



Deux éléments WCS : Text ne peuvent pas avoir le même attribut XML : lang. Chaque schéma de profil WCS doit appliquer cette contrainte séparément pour chaque élément localisable. Seuls les codages UTF-8 et UTF-16 sont pris en charge.

### <a name="schema-support"></a>Prise en charge des schémas

La conception utilise les types XSD WCS : LocalizedText et WCS : MultiLocalizedType définis dans le schéma de type de profil commun WCS :


```XML
    <xs:complexType name="LocalizedText">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="xml:lang" type="xs:string" use="required"/>
            <xs:extension/>
        <xs:simpleContent/>
    </xs:complexType/>

    <xs:complexType name="MultiLocalizedType">
        <xs:element name="Text" type="cam:LocalizedText" minOccurs="1"/>
    </xs:complexType>
```



Chaque schéma de profil WCS déclare que chaque élément localisable doit être de type MultiLocalizedType, par exemple :


```XML
<xs:schema 
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
    xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
    targetNamespace=
        "http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
    version="1.0">
    <xs:import namespace=
        "http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"/>

    <xs:element name="cdm:Description" type="wcs:MultiLocalizableType" minOccurs="0"/>

    <xs:unique name="uniqueDescriptionLanguage">
      <xs:selector xpath="cdm:ColorDeviceModel/cdm:Description/wcs:Text"/>
      <xs:field xpath="@xml:lang"/>
    </unique>

    ...
</xs:schema>
```



Le schéma CDMP applique la contrainte selon laquelle chaque enfant WCS : Text de l’élément CDM : description doit avoir un attribut XML : lang unique. Elle applique la même contrainte pour les autres éléments localisables. Les schémas CAMP et GMMP sont identiques.

### <a name="selecting-the-language"></a>Sélection de la langue

Lorsque vous choisissez la version linguistique d’un élément localisable à afficher, le code de l’application doit sélectionner la « version la plus proche » dans la « langue actuelle ». La « version la plus proche » et la « langue actuelle » signifient réellement dépend de la plateforme. Voir ci-dessous. Si le profil ne contient pas une version de langage qui correspond à la langue actuelle, l’application doit sélectionner la première version dans le profil (le premier élément enfant WCS : Text de l’élément localisable).

sur Windows Vista, la sélection de la langue s’effectue comme suit : chaque thread a une liste associée de « langues d’interface utilisateur préférées », que vous pouvez obtenir en appelant [**GetThreadPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages). La liste est retournée dans l’ordre des préférences de l’utilisateur. Par exemple, sur un système configuré pour l’anglais des États-Unis, la liste retournée par **GetThreadPreferredUILanguages** est {"en-US", "fr"}. Cela signifie : 1) anglais (États-Unis), le cas échéant. 2) sinon, utilisez une variante régionale de l’anglais, telle que « en-GB » ou simplement « fr ».

Pour chaque langue de cette liste, dans l’ordre de la liste, le code de l’interface utilisateur recherche un élément WCS : Text dont l’attribut XML : lang correspond exactement à. La première version correspondante est utilisée. Si aucune version ne correspond, le premier élément WCS : Text est utilisé.

### <a name="built-in-profiles"></a>Profils intégrés

les profils WCS standard fournis avec Windows Vista, tels que srvb. cdmp, ont les mêmes propriétés localisables que les autres profils.

la solution de Windows standard consiste à placer les chaînes localisées dans une DLL MUI et à y faire référence comme suit :


```XML
<cdm:Description resourceId="mscms.dll,-101">
    <wcs:Text xml:lang="en-US">Hello, world!</wcs:Text>
<cdm:Description>
```



sur un système Windows, le texte de description est extrait de l’ID de ressource 101 dans la version localisée appropriée des ressources MUI pour mscms.dll. les systèmes Non-Windows utilisent le sous-élément wcs : Text, comme décrit ci-dessus.

Nous introduisons un attribut d’ID global unique facultatif sur l’élément racine de chaque schéma de profil WCS. Le profil standard wcsRGB. CDMP peut se présenter comme suit :


```XML
<cdm:ColorDeviceModel
    ID=http://schemas.microsoft.com/2005/02/color/profiles/wcsRGB.cdmp
    ... >
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello.</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour.</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceModel>
```



Pour les profils de couleurs WCS fournis avec Windows, le panneau de la vue des couleurs affiche des informations descriptives à partir des ressources, plutôt que des éléments de texte WCS : dans les profils. cela permet à Windows d’afficher des informations localisées pour ces profils dans toutes les langues prises en charge, sans que les profils themlselves contiennent des informations descriptives dans toutes les langues.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de base de la gestion des couleurs](basic-color-management-concepts.md)
</dt> <dt>

[Schémas et algorithmes du système de couleurs Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 