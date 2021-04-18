---
title: Schéma des types de profils communs du système de couleurs Windows, stratégies de gestion des versions et de localisation
description: Schéma des types de profils communs du système de couleurs Windows, stratégies de gestion des versions et de localisation
ms.assetid: 295522c6-7c53-47f6-9b98-aeee2b0e34fc
keywords:
- Système de couleurs Windows (WCS), types de profils communs
- WCS (système de couleurs Windows), types de profils communs
- gestion des couleurs des images, types de profils communs
- gestion des couleurs, types de profils communs
- couleurs, types de profils communs
- Système de couleurs Windows (WCS), profils
- WCS (système de couleurs Windows), profils
- gestion des couleurs des images, profils
- gestion des couleurs, profils
- couleurs, profils
- Système de couleurs Windows (WCS), contrôle de version
- WCS (Windows Color System), contrôle de version
- gestion des couleurs des images, contrôle de version
- gestion des couleurs, contrôle de version
- couleurs, contrôle de version
- Système de couleurs Windows (WCS), localisation
- WCS (système de couleurs Windows), localisation
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
ms.openlocfilehash: 4814b652b654b6416b42a7a3484950273a93ea96
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106520258"
---
# <a name="windows-color-system-common-profile-types-schema-versioning-and-localization-strategies"></a><span data-ttu-id="fa436-127">Schéma des types de profils communs du système de couleurs Windows, stratégies de gestion des versions et de localisation</span><span class="sxs-lookup"><span data-stu-id="fa436-127">Windows Color System Common Profile Types schema, Versioning and Localization Strategies</span></span>

-   [<span data-ttu-id="fa436-128">Schéma des types de profil commun WCS v1</span><span class="sxs-lookup"><span data-stu-id="fa436-128">WCS Common Profile Types Schema V1</span></span>](#wcs-common-profile-types-schema-v1)
-   [<span data-ttu-id="fa436-129">Ajouts au schéma des types de profils communs WCS</span><span class="sxs-lookup"><span data-stu-id="fa436-129">WCS Common Profile Types Schema V2 Additions</span></span>](#wcs-common-profile-types-schema-v2-additions)
-   [<span data-ttu-id="fa436-130">Contrôle de version du schéma de profil WCS</span><span class="sxs-lookup"><span data-stu-id="fa436-130">WCS Profile Schema Versioning</span></span>](#wcs-profile-schema-versioning)
-   [<span data-ttu-id="fa436-131">Localisation du profil WCS</span><span class="sxs-lookup"><span data-stu-id="fa436-131">WCS Profile Localization</span></span>](#wcs-profile-localization)
    -   [<span data-ttu-id="fa436-132">Exprimant des éléments localisables</span><span class="sxs-lookup"><span data-stu-id="fa436-132">Expressing localizable elements</span></span>](#expressing-localizable-elements)
    -   [<span data-ttu-id="fa436-133">Prise en charge des schémas</span><span class="sxs-lookup"><span data-stu-id="fa436-133">Schema Support</span></span>](#schema-support)
    -   [<span data-ttu-id="fa436-134">Sélection de la langue</span><span class="sxs-lookup"><span data-stu-id="fa436-134">Selecting the Language</span></span>](#selecting-the-language)
    -   [<span data-ttu-id="fa436-135">Profils intégrés</span><span class="sxs-lookup"><span data-stu-id="fa436-135">Built-in profiles</span></span>](#built-in-profiles)
-   [<span data-ttu-id="fa436-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fa436-136">Related topics</span></span>](#related-topics)

## <a name="wcs-common-profile-types-schema-v1"></a><span data-ttu-id="fa436-137">Schéma des types de profil commun WCS v1</span><span class="sxs-lookup"><span data-stu-id="fa436-137">WCS Common Profile Types Schema V1</span></span>

<span data-ttu-id="fa436-138">Les éléments suivants fournissent la définition de schéma v 1.0 pour les types de profils communs WCS.</span><span class="sxs-lookup"><span data-stu-id="fa436-138">The following provides the v1.0 schema definition for the WCS Common Profile Types.</span></span>


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



<span data-ttu-id="fa436-139">Seuls les encodages UTF-8 ou UTF-16 sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fa436-139">Only UTF-8 or UTF-16 encodings are supported.</span></span> <span data-ttu-id="fa436-140">Tous les autres encodages XML sont fortement déconseillés afin de préserver une interopérabilité optimale.</span><span class="sxs-lookup"><span data-stu-id="fa436-140">All other XML encodings are strongly discouraged in order to preserve optimum interoperability.</span></span>

## <a name="wcs-common-profile-types-schema-v2-additions"></a><span data-ttu-id="fa436-141">Ajouts au schéma des types de profils communs WCS</span><span class="sxs-lookup"><span data-stu-id="fa436-141">WCS Common Profile Types Schema V2 Additions</span></span>

<span data-ttu-id="fa436-142">Dans Windows 7, le schéma des types de profils communs WCS a été mis à jour pour inclure les types afin de prendre en charge le [schéma d’étalonnage WCS](wcs-calibration-schema.md).</span><span class="sxs-lookup"><span data-stu-id="fa436-142">In Windows 7, the WCS Common Profile Types schema has been updated to include types to support the [WCS Calibration schema](wcs-calibration-schema.md).</span></span>


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



## <a name="wcs-profile-schema-versioning"></a><span data-ttu-id="fa436-143">Contrôle de version du schéma de profil WCS</span><span class="sxs-lookup"><span data-stu-id="fa436-143">WCS Profile Schema Versioning</span></span>

<span data-ttu-id="fa436-144">Dans cette annexe, le terme « consommateur de profils » fait référence au logiciel WCS, ou à un composant logiciel tiers qui consomme des profils WCS.</span><span class="sxs-lookup"><span data-stu-id="fa436-144">In this Appendix, the term "profile consumer" refers to the WCS software, or to a third-party software component that consumes WCS profiles.</span></span>

<span data-ttu-id="fa436-145">Les versions plus récentes des consommateurs de profils pourront utiliser des profils WCS écrits conformément aux anciennes versions des schémas.</span><span class="sxs-lookup"><span data-stu-id="fa436-145">Newer versions of profile consumers will be able to consume WCS profiles written according to older versions of the schemas.</span></span> <span data-ttu-id="fa436-146">Pour tirer pleinement parti des fonctionnalités définies dans la version la plus récente des schémas, la version la plus récente d’un consommateur de profils est généralement requise.</span><span class="sxs-lookup"><span data-stu-id="fa436-146">To take full advantage of features defined in the newest version of the schemas, the newest version of a profile consumer will generally be required.</span></span> <span data-ttu-id="fa436-147">Toutefois, les consommateurs de profils plus anciens peuvent utiliser des profils écrits selon des versions plus récentes des schémas.</span><span class="sxs-lookup"><span data-stu-id="fa436-147">However, older profile consumers can consume profiles written according to newer versions of the schemas.</span></span> <span data-ttu-id="fa436-148">Le consommateur de profils peut ignorer les éléments et les attributs XML qu’il ne comprend pas.</span><span class="sxs-lookup"><span data-stu-id="fa436-148">The profile consumer can ignore XML elements and attributes that it does not understand.</span></span> <span data-ttu-id="fa436-149">Les résultats sont corrects, mais les performances ou la fidélité peuvent être dégradées par rapport aux résultats obtenus avec la version la plus récente du profil consommateur.</span><span class="sxs-lookup"><span data-stu-id="fa436-149">The results will be correct, but performance or fidelity may degraded as compared to the results achieved with the newest version of the profile consumer.</span></span>

<span data-ttu-id="fa436-150">Voici les instructions de contrôle de version pour les consommateurs de profils :</span><span class="sxs-lookup"><span data-stu-id="fa436-150">The following are versioning guidelines for profile consumers:</span></span>

-   <span data-ttu-id="fa436-151">Une version donnée d’un consommateur de profil doit reconnaître tous les éléments et attributs d’un espace de noms de version, ou aucun d’entre eux.</span><span class="sxs-lookup"><span data-stu-id="fa436-151">A given version of a profile consumer must recognize either all of the elements and attributes from a version namespace, or none of them.</span></span>
-   <span data-ttu-id="fa436-152">Si un consommateur de profils rencontre un élément ou un attribut à partir d’un espace de noms qu’il ne comprend pas, il doit traiter ce problème comme une condition d’erreur, sauf si le profil contient des indications explicites sur le traitement de secours.</span><span class="sxs-lookup"><span data-stu-id="fa436-152">If a profile consumer encounters an element or attribute from a namespace that it does not understand, it must treat this as an error condition, unless the profile contains explicit guidance on fallback processing.</span></span>
-   <span data-ttu-id="fa436-153">La [spécification Open Packaging](https://www.microsoft.com/whdc/xps/xpspkg.mspx) définit un URI d’espace de noms supplémentaire, l’espace de noms de compatibilité du balisage, qui définit les éléments et les attributs qui fournissent ce guide de traitement de secours.</span><span class="sxs-lookup"><span data-stu-id="fa436-153">The [Open Packaging Specification](https://www.microsoft.com/whdc/xps/xpspkg.mspx) defines an additional namespace URI, the markup compatibility namespace, which defines elements and attributes that provide this fallback processing guidance.</span></span>
-   <span data-ttu-id="fa436-154">Toutes les versions de tous les consommateurs de profils doivent reconnaître et respecter tous les éléments et attributs de l’espace de noms de compatibilité du balisage.</span><span class="sxs-lookup"><span data-stu-id="fa436-154">All versions of all profile consumers must recognize and respect all the elements and attributes in the markup compatibility namespace.</span></span>
-   <span data-ttu-id="fa436-155">Les consommateurs de profils basés sur une nouvelle version des schémas de profil doivent prendre en charge tous les espaces de noms de version précédemment définis.</span><span class="sxs-lookup"><span data-stu-id="fa436-155">Profile consumers based on a new version of the profile schemas must support all previously defined version namespaces.</span></span>

<span data-ttu-id="fa436-156">Dans la version 1.0, WCS reconnaît les éléments et les attributs des espaces de noms suivants :</span><span class="sxs-lookup"><span data-stu-id="fa436-156">In the v1.0 release, WCS recognizes elements and attributes from the following namespaces:</span></span>

-   https://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel
-   https://schemas.microsoft.com/windows/2005/02/color/GamutMapModel
-   https://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
-   https://schemas.microsoft.com/winfx/2005/06/markup-compatibility

<span data-ttu-id="fa436-157">L’exemple suivant illustre la compatibilité du balisage.</span><span class="sxs-lookup"><span data-stu-id="fa436-157">The following demonstrates an example of markup compatibility.</span></span>


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



## <a name="wcs-profile-localization"></a><span data-ttu-id="fa436-158">Localisation du profil WCS</span><span class="sxs-lookup"><span data-stu-id="fa436-158">WCS Profile Localization</span></span>

<span data-ttu-id="fa436-159">**Configuration requise**</span><span class="sxs-lookup"><span data-stu-id="fa436-159">**Requirements**</span></span>

<span data-ttu-id="fa436-160">Les profils WCS contiennent certains éléments tels que ProfileName et description qui contiennent du texte explicite.</span><span class="sxs-lookup"><span data-stu-id="fa436-160">WCS profiles contain certain elements such as ProfileName and Description which contain human-readable text.</span></span> <span data-ttu-id="fa436-161">Ce texte peut être localisé.</span><span class="sxs-lookup"><span data-stu-id="fa436-161">This text is localizable.</span></span>

<span data-ttu-id="fa436-162">Les instructions de contrôle de version pour les créateurs de profils sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="fa436-162">The following are versioning guidelines for profile creators:</span></span>

-   <span data-ttu-id="fa436-163">Pour les profils créés par des tiers, tels que les fabricants d’imprimantes, l’auteur du profil doit incorporer du texte descriptif dans plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="fa436-163">For profiles created by 3rd parties such as printer manufacturers, the profile author should incorporate descriptive text in multiple languages.</span></span>
-   <span data-ttu-id="fa436-164">Les éléments suivants doivent être localisables :</span><span class="sxs-lookup"><span data-stu-id="fa436-164">The following elements should be localizable:</span></span> 

    | <span data-ttu-id="fa436-165">Élément</span><span class="sxs-lookup"><span data-stu-id="fa436-165">Element</span></span>     | <span data-ttu-id="fa436-166">CDMP</span><span class="sxs-lookup"><span data-stu-id="fa436-166">CDMP</span></span> | <span data-ttu-id="fa436-167">GMMP</span><span class="sxs-lookup"><span data-stu-id="fa436-167">GMMP</span></span> | <span data-ttu-id="fa436-168">Camping</span><span class="sxs-lookup"><span data-stu-id="fa436-168">CAMP</span></span> |
    |-------------|------|------|------|
    | <span data-ttu-id="fa436-169">ProfileName</span><span class="sxs-lookup"><span data-stu-id="fa436-169">ProfileName</span></span> | <span data-ttu-id="fa436-170">x</span><span class="sxs-lookup"><span data-stu-id="fa436-170">x</span></span>    | <span data-ttu-id="fa436-171">x</span><span class="sxs-lookup"><span data-stu-id="fa436-171">x</span></span>    | <span data-ttu-id="fa436-172">x</span><span class="sxs-lookup"><span data-stu-id="fa436-172">x</span></span>    |
    | <span data-ttu-id="fa436-173">Description</span><span class="sxs-lookup"><span data-stu-id="fa436-173">Description</span></span> | <span data-ttu-id="fa436-174">x</span><span class="sxs-lookup"><span data-stu-id="fa436-174">x</span></span>    | <span data-ttu-id="fa436-175">x</span><span class="sxs-lookup"><span data-stu-id="fa436-175">x</span></span>    | <span data-ttu-id="fa436-176">x</span><span class="sxs-lookup"><span data-stu-id="fa436-176">x</span></span>    |
    | <span data-ttu-id="fa436-177">Auteur</span><span class="sxs-lookup"><span data-stu-id="fa436-177">Author</span></span>      | <span data-ttu-id="fa436-178">x</span><span class="sxs-lookup"><span data-stu-id="fa436-178">x</span></span>    | <span data-ttu-id="fa436-179">x</span><span class="sxs-lookup"><span data-stu-id="fa436-179">x</span></span>    | <span data-ttu-id="fa436-180">x</span><span class="sxs-lookup"><span data-stu-id="fa436-180">x</span></span>    |

    

     

### <a name="expressing-localizable-elements"></a><span data-ttu-id="fa436-181">Exprimant des éléments localisables</span><span class="sxs-lookup"><span data-stu-id="fa436-181">Expressing localizable elements</span></span>

<span data-ttu-id="fa436-182">Au lieu de contenir directement du texte, chaque élément localisable contient un ou plusieurs sous-éléments WCS : Text, chacun d’entre eux devant spécifier l’attribut XML : lang.</span><span class="sxs-lookup"><span data-stu-id="fa436-182">Instead of directly containing text, each localizable element contains one or more wcs:Text sub-elements, each of which must specify the xml:lang attribute.</span></span> <span data-ttu-id="fa436-183">Comme décrit dans la section [XML specification](http://www.w3.org/TR/REC-xml/) 2,12 (« Language identification »), la valeur de l’attribut XML : lang doit être un identificateur de langue RFC 3066 IETF, par exemple « en-US », « en » ou « FR-fr ».</span><span class="sxs-lookup"><span data-stu-id="fa436-183">As described in the [XML specification](http://www.w3.org/TR/REC-xml/) Section 2.12 ("Language Identification"), the value of the xml:lang attribute must be an IETF RFC 3066 language identifier such as "en-US", "en", or "fr-FR".</span></span> <span data-ttu-id="fa436-184">Dans les schémas WCS, la valeur de l’attribut XML : lang ne doit pas être la chaîne vide "", même si XML l’autorise dans le cas général.</span><span class="sxs-lookup"><span data-stu-id="fa436-184">In WCS schemas, the value of the xml:lang attribute must not be the empty string "", even though XML allows this in the general case.</span></span> <span data-ttu-id="fa436-185">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="fa436-185">For example:</span></span>


```XML
<cdm:ColorDeviceModel ... />
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceeModel>
```



<span data-ttu-id="fa436-186">Deux éléments WCS : Text ne peuvent pas avoir le même attribut XML : lang.</span><span class="sxs-lookup"><span data-stu-id="fa436-186">No two wcs:Text elements can have the same xml:lang attribute.</span></span> <span data-ttu-id="fa436-187">Chaque schéma de profil WCS doit appliquer cette contrainte séparément pour chaque élément localisable.</span><span class="sxs-lookup"><span data-stu-id="fa436-187">Each WCS profile schema must enforce this constraint separately for each localizable element.</span></span> <span data-ttu-id="fa436-188">Seuls les codages UTF-8 et UTF-16 sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fa436-188">Only UTF-8 and UTF-16 encodings are supported.</span></span>

### <a name="schema-support"></a><span data-ttu-id="fa436-189">Prise en charge des schémas</span><span class="sxs-lookup"><span data-stu-id="fa436-189">Schema Support</span></span>

<span data-ttu-id="fa436-190">La conception utilise les types XSD WCS : LocalizedText et WCS : MultiLocalizedType définis dans le schéma de type de profil commun WCS :</span><span class="sxs-lookup"><span data-stu-id="fa436-190">The design makes use of the XSD types wcs:LocalizedText and wcs:MultiLocalizedType defined in the WCS Common Profile Type schema:</span></span>


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



<span data-ttu-id="fa436-191">Chaque schéma de profil WCS déclare que chaque élément localisable doit être de type MultiLocalizedType, par exemple :</span><span class="sxs-lookup"><span data-stu-id="fa436-191">Each WCS profile schema declares each localizable element to be of type MultiLocalizedType, for example:</span></span>


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



<span data-ttu-id="fa436-192">Le schéma CDMP applique la contrainte selon laquelle chaque enfant WCS : Text de l’élément CDM : description doit avoir un attribut XML : lang unique.</span><span class="sxs-lookup"><span data-stu-id="fa436-192">The CDMP schema enforces the constraint that each wcs:Text child of the cdm:Description element must have a unique xml:lang attribute.</span></span> <span data-ttu-id="fa436-193">Elle applique la même contrainte pour les autres éléments localisables.</span><span class="sxs-lookup"><span data-stu-id="fa436-193">It enforces the same constraint for the other localizable elements.</span></span> <span data-ttu-id="fa436-194">Les schémas CAMP et GMMP sont identiques.</span><span class="sxs-lookup"><span data-stu-id="fa436-194">The CAMP and GMMP schemas do the same.</span></span>

### <a name="selecting-the-language"></a><span data-ttu-id="fa436-195">Sélection de la langue</span><span class="sxs-lookup"><span data-stu-id="fa436-195">Selecting the Language</span></span>

<span data-ttu-id="fa436-196">Lorsque vous choisissez la version linguistique d’un élément localisable à afficher, le code de l’application doit sélectionner la « version la plus proche » dans la « langue actuelle ».</span><span class="sxs-lookup"><span data-stu-id="fa436-196">When deciding which language version of a localizable element to display, application code should select the "closest version" to the "current language".</span></span> <span data-ttu-id="fa436-197">La « version la plus proche » et la « langue actuelle » signifient réellement dépend de la plateforme. Voir ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="fa436-197">What "closest version" and "current language" actually mean is platform-dependent; see below.</span></span> <span data-ttu-id="fa436-198">Si le profil ne contient pas une version de langage qui correspond à la langue actuelle, l’application doit sélectionner la première version dans le profil (le premier élément enfant WCS : Text de l’élément localisable).</span><span class="sxs-lookup"><span data-stu-id="fa436-198">If the profile does not contain a language version that matches the current language, the application should select the first version in the profile (the first wcs:Text child element of the localizable element).</span></span>

<span data-ttu-id="fa436-199">Sur Windows Vista, la sélection de la langue s’effectue comme suit : chaque thread a une liste associée de « langues d’interface utilisateur préférées », que vous pouvez obtenir en appelant [**GetThreadPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages).</span><span class="sxs-lookup"><span data-stu-id="fa436-199">On Windows Vista, the language selection is done as follows: Each thread has an associated list of "preferred UI languages", which can be obtained by calling [**GetThreadPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages).</span></span> <span data-ttu-id="fa436-200">La liste est retournée dans l’ordre des préférences de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fa436-200">The list is returned in order of user preference.</span></span> <span data-ttu-id="fa436-201">Par exemple, sur un système configuré pour l’anglais des États-Unis, la liste retournée par **GetThreadPreferredUILanguages** est {"en-US", "fr"}.</span><span class="sxs-lookup"><span data-stu-id="fa436-201">For instance, on a system set up for US English, the list returned by **GetThreadPreferredUILanguages** is { "en-US", "en" }.</span></span> <span data-ttu-id="fa436-202">Cela signifie : 1) anglais (États-Unis), le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="fa436-202">This means: 1) US English if present.</span></span> <span data-ttu-id="fa436-203">2) sinon, utilisez une variante régionale de l’anglais, telle que « en-GB » ou simplement « fr ».</span><span class="sxs-lookup"><span data-stu-id="fa436-203">2) Otherwise, use any regional variant of English, such as "en-GB" or just plain "en".</span></span>

<span data-ttu-id="fa436-204">Pour chaque langue de cette liste, dans l’ordre de la liste, le code de l’interface utilisateur recherche un élément WCS : Text dont l’attribut XML : lang correspond exactement à.</span><span class="sxs-lookup"><span data-stu-id="fa436-204">For each language in that list, in list order, the UI code looks for a wcs:Text element whose xml:lang attribute is an exact match.</span></span> <span data-ttu-id="fa436-205">La première version correspondante est utilisée.</span><span class="sxs-lookup"><span data-stu-id="fa436-205">The first matching version is used.</span></span> <span data-ttu-id="fa436-206">Si aucune version ne correspond, le premier élément WCS : Text est utilisé.</span><span class="sxs-lookup"><span data-stu-id="fa436-206">If no version matches, the first wcs:Text element is used.</span></span>

### <a name="built-in-profiles"></a><span data-ttu-id="fa436-207">Profils intégrés</span><span class="sxs-lookup"><span data-stu-id="fa436-207">Built-in profiles</span></span>

<span data-ttu-id="fa436-208">Les profils WCS standard fournis avec Windows Vista, tels que sRVB. CDMP, ont les mêmes propriétés localisables que les autres profils.</span><span class="sxs-lookup"><span data-stu-id="fa436-208">The standard WCS profiles shipped with Windows Vista, such as sRGB.cdmp, have the same localizable properties as other profiles.</span></span>

<span data-ttu-id="fa436-209">La solution Windows standard consiste à placer les chaînes localisées dans une DLL MUI et à y faire référence comme suit :</span><span class="sxs-lookup"><span data-stu-id="fa436-209">The standard Windows solution would be to put the localized strings in a MUI DLL, and refer to them like this:</span></span>


```XML
<cdm:Description resourceId="mscms.dll,-101">
    <wcs:Text xml:lang="en-US">Hello, world!</wcs:Text>
<cdm:Description>
```



<span data-ttu-id="fa436-210">Sur un système Windows, le texte de description est extrait de l’ID de ressource 101 dans la version localisée appropriée des ressources MUI pour mscms.dll.</span><span class="sxs-lookup"><span data-stu-id="fa436-210">On a Windows system, the description text would be extracted from resource ID 101 in the appropriate localized version of the MUI resources for mscms.dll.</span></span> <span data-ttu-id="fa436-211">Les systèmes non-Windows utiliseraient les sous-éléments WCS : Text comme décrit ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="fa436-211">Non-Windows systems would use the wcs:Text sub-elements as described above.</span></span>

<span data-ttu-id="fa436-212">Nous introduisons un attribut d’ID global unique facultatif sur l’élément racine de chaque schéma de profil WCS.</span><span class="sxs-lookup"><span data-stu-id="fa436-212">We introduce an optional, globally unique ID attribute on the root element of each WCS profile schema.</span></span> <span data-ttu-id="fa436-213">Le profil standard wcsRGB. CDMP peut se présenter comme suit :</span><span class="sxs-lookup"><span data-stu-id="fa436-213">The standard profile wcsRGB.cdmp might look like this:</span></span>


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



<span data-ttu-id="fa436-214">Pour les profils de couleurs WCS fournis avec Windows, le panneau de la vue des couleurs affiche des informations descriptives à partir des ressources, plutôt que des éléments de texte WCS : dans les profils.</span><span class="sxs-lookup"><span data-stu-id="fa436-214">For the WCS color profiles shipped with windows, the Color CPL displays descriptive information from the resources, rather than from the wcs:Text elements in the profiles.</span></span> <span data-ttu-id="fa436-215">Cela permet à Windows d’afficher des informations localisées pour ces profils dans toutes les langues prises en charge, sans exiger que les profils themlselves contiennent des informations descriptives dans toutes les langues.</span><span class="sxs-lookup"><span data-stu-id="fa436-215">This allows Windows to display localized information for these profiles in all supported languages, without requiring the profiles themlselves to contain descriptive information in all languages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa436-216">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fa436-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa436-217">Concepts de base de la gestion des couleurs</span><span class="sxs-lookup"><span data-stu-id="fa436-217">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="fa436-218">Schémas et algorithmes du système de couleurs Windows</span><span class="sxs-lookup"><span data-stu-id="fa436-218">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 