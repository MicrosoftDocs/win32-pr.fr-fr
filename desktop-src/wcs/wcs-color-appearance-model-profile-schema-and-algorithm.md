---
title: Algorithme et schéma de profil de modèle d’apparence de couleur WCS
description: Algorithme et schéma de profil de modèle d’apparence de couleur WCS
ms.assetid: 017588fe-cec9-4178-a912-7950cefc036c
keywords:
- Système de couleurs Windows (WCS), profil de modèle d’apparence de couleur (CAMP)
- WCS (système de couleurs Windows), profil de modèle d’apparence de couleur (CAMP)
- gestion des couleurs des images, profil de modèle d’apparence de couleur (CAMP)
- gestion des couleurs, profil de modèle d’apparence de couleur (CAMP)
- couleurs, profil de modèle d’apparence de couleur (CAMP)
- Système de couleurs Windows (WCS), profils
- WCS (système de couleurs Windows), profils
- gestion des couleurs des images, profils
- gestion des couleurs, profils
- couleurs, profils
- Profil de modèle d’apparence de couleur (CAMP)
- CAMP (modèle d’apparence de couleur)
- schémas, profil de modèle d’apparence de couleur (CAMP)
- algorithmes, profil de modèle d’apparence de couleur (CAMP)
- Profil du modèle d’apparence des couleurs WCS
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a928aebcfe02f1db39de2452a0b49e5c888bccc
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "106520216"
---
# <a name="wcs-color-appearance-model-profile-schema-and-algorithm"></a>Algorithme et schéma de profil de modèle d’apparence de couleur WCS

[Vue d’ensemble](#overview)

[Architecture de profil de modèle d’apparence de couleur (CAMP)](#color-appearance-model-profile-architecture)

[Schéma CAMP](#the-camp-schema)

[Éléments du schéma CAMP](#the-camp-schema-elements)

[Algorithme CAMP](#the-camp-algorithm)

### <a name="overview"></a>Vue d’ensemble

Ce schéma est utilisé pour spécifier le contenu d’un profil de modèle d’apparence de couleur (CAMP). Les algorithmes de base de référence associés sont décrits dans les sections suivantes.

Le CAMP est composé de balises XML qui fournissent des valeurs paramétriques aux variables de modèle d’apparence de couleur de ligne de base CIECAM02. Des détails sur les plages de paramètres sont fournis dans la spécification modèle d’apparence de couleur de ligne de base et recommandation CIECAM02.

### <a name="color-appearance-model-profile-architecture"></a>Architecture du modèle d’apparence de couleur

![Diagramme qui montre l’architecture du profil CAMP constituée de balises X M L.](images/camp-image002new.png)

### <a name="the-camp-schema"></a>Schéma CAMP


```C++
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema
  xmlns:cam="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Appearance Model profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:annotation>
    <xs:documentation>
      ColorAppearanceModel element contains viewing conditions
      parameters based on CIECAM02.
    </xs:documentation>
  </xs:annotation>
  <xs:element name="ColorAppearanceModel">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ProfileName" type="wcs:MultiLocalizedTextType"/>
        <xs:element name="Description" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="Author" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="ViewingConditions">
          <xs:complexType>
            <xs:sequence>
              <xs:choice>
                <xs:element name="WhitePoint" type="wcs:NonNegativeCIEXYZType"/>
                <xs:element name="WhitePointName">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="D50"/>
                      <xs:enumeration value="D65"/>
                      <xs:enumeration value="A"/>
                      <xs:enumeration value="F2"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:element>
              </xs:choice>
              <xs:element name="Background" type="wcs:NonNegativeCIEXYZType"/>
              <xs:choice>
                <xs:element name="ImpactOfSurround" type="xs:float"/>
                <xs:element name="Surround">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="Average"/>
                      <xs:enumeration value="Dim"/>
                      <xs:enumeration value="Dark"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:element>
              </xs:choice>
              <xs:element name="LuminanceOfAdaptingField" type="xs:float"/>
              <xs:element name="DegreeOfAdaptation" type="xs:float"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
        <xs:element name="NormalizeToMediaWhitePoint" minOccurs="0">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="True"/>
              <xs:enumeration value="False"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:element>
      </xs:sequence>
      <xs:attribute name="ID" type="xs:string" use="optional" />
    </xs:complexType>
  </xs:element>
</xs:schema>
```



## <a name="the-camp-schema-elements"></a>Éléments du schéma CAMP

## <a name="colorappearancemodel"></a>ColorAppearanceModel

Cet élément est une séquence de :

1.  Chaîne ProfileName,
2.  chaîne de description facultative,
3.  chaîne d’auteur facultative,
4.  Élément ViewingConditions.

**Conditions de validation :** Chaque sous-élément est validé par son propre type. Les longueurs de chaîne sont limitées à 10 000 caractères.

## <a name="namespace"></a>Espace de noms

xmlns : CAM = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "

targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "

## <a name="version"></a>Version

Version &gt; 0,1 ou &lt; = « 1,0 » avec la première version de Windows Vista.

**Conditions de validation :** Toute valeur de version &lt; = 2,0 est également valide pour prendre en charge des modifications sans rupture au format.

## <a name="documentation"></a>Documentation

Schéma de profil du modèle d’apparence des couleurs.

Copyright (C) Microsoft. Tous droits réservés.

**Conditions de validation :** Chaque sous-élément est validé par son propre type.

## <a name="surroundtype"></a>SurroundType

Cet élément est soit une énumération de paramètres CIECAM02 « Average », « Dim » ou « Dark », soit les paramètres quantitatifs réels de la recommandation CIECAM02 c, l’impact de l’entourage.

**Conditions de validation :** Le paramètre c peut être compris entre 0,525 et 0,69.

## <a name="viewingconditions"></a>ViewingConditions

Cet élément se compose des sous-éléments suivants :



| Élément                    | Type           |
|----------------------------|----------------|
| WhitePoint                 | WhitePointType |
| Arrière-plan                 | CIEXYZ         |
| Son                   | SurroundType   |
| LuminanceOfAdaptingField   | float          |
| DegreeOfAdaptation         | float          |
| NormalizeToMediaWhitePoint | Boolean        |



 

**Conditions de validation :** Les sous-éléments CIEXYZ sont validés par NonNegativeXYZType. LuminanceOfAdaptingField est un maximum de 10, 000cd/m ^ 2. Le DegreeOfAdaptation peut être compris entre 0,0 et 1,0. La valeur NormalizeToMediaWhitePoint peut être « true » ou « false ». Si le sous-élément NormalizeToMediaWhitePoint est absent, sa valeur par défaut est « true ». Consultez la section relative à l’algorithme CAMP suivante.

## <a name="whitepointtype"></a>WhitePointType

Cet élément est soit une énumération de la valeur de la source de lumière CIE (« D50 », « D65 », « A » ou « F2 »), soit un sous-élément CIEXYZ.

**Conditions de validation :** Chaque sous-élément est validé par son propre type.

## <a name="ciexyztype"></a>CIEXYZType

L’élément CIEXYZType est composé de trois éléments à virgule flottante IEEE simple précision NonNegativeFloatType, nommés « X », « Y » et « Z ». Ces mesures peuvent être absolues (non relatives) CIEXYZ 1931 valeurs réfléchissantes ou valeurs réfléchies absolues (non relatives) CIEXYZ 1931 (transmissif) dans candelas par unités au carré du compteur.

**Conditions de validation :** Cela signifie que seules les valeurs réelles sont valides et que les valeurs de mesure CIEXYZ négatives ne sont pas valides. Étant donné qu’il s’agit de valeurs absolues, les valeurs peuvent être comprises bien au-delà de 1.0 f. Une limite raisonnable pour toute valeur X, Y ou Z sera arbitrairement définie sur 10000.0 f.

 

### <a name="the-camp-algorithm"></a>Algorithme CAMP

Le modèle d’apparence des couleurs (CAM) est basé sur les équations du modèle d’apparence des couleurs CIE CIECAM02.

Cette classe implémente la modélisation de l’apparence des couleurs. Notez que le CAM WCS n’est *pas* remplaçable, par exemple, à l’aide d’un plug-in. L’objectif de conception est de n’avoir qu’un seul modèle d’apparence des couleurs. Le CAM est basé sur les recommandations CIECAM02.

CIECAM02 peut être utilisé de deux manières. Dans la direction de la colorimétrie à l’aspect, elle fournit un mappage de l’espace CIE XYZ à l’espace d’apparence de couleur. Dans la direction de l’apparence à la colorimétrie, il mappe l’espace d’apparence de couleur à l’espace XYZ. L’apparence des couleurs met en corrélation les clairs, J, chrominance, C et teinte, h. Ces trois valeurs forment un système de coordonnées cylindriques. Souvent, il s’avère plus pratique de travailler dans un système de coordonnées rectangulaires. par conséquent, calculez a = C COS h et b = C Sin h, pour fournir à CIECAM02 Jab.

Vous pouvez utiliser des valeurs de clarté CAM supérieures à 100. Le Comité CIE qui a formulé CIECAM02 n’a pas résolu le comportement de l’axe de luminosité pour les valeurs d’entrée avec une luminance supérieure au point blanc adopté ; autrement dit, pour les valeurs Y d’entrée supérieures à la valeur Y du point blanc adopté. L’expérimentation a montré que les équations de luminance dans CIECAM02 se comportent raisonnablement pour ces valeurs. La luminosité augmente de façon exponentielle et suit le même exposant (environ 1/3).

Les utilisateurs souhaitent parfois modifier la façon dont le degré d’adaptation (D) est calculé. La conception WCS permet aux utilisateurs de contrôler ce calcul en modifiant la valeur degreeOfadaptation dans les paramètres des conditions d’affichage.

Pour fournir une correspondance plus cohérente avec les attentes influencées par les utilisateurs, le degreeOfAdaptation dans le CAMPS par défaut est 1,0. Cela produit de meilleurs résultats dans tous les cas autres que le hachage absolu, où il peut être utile de permettre au WCS de calculer le degreeOfAdaptation (via degreeOfAdaptation =-1).

Au lieu d’utiliser une valeur surround « Average », « Dim » et « Dark », une valeur surround continue, calculée à partir de la valeur c, est fournie. La valeur de c doit être une valeur float comprise entre 0,525 et 0,69.

À partir de *c*, *NC* et *F* peuvent être calculés à l’aide d’une interpolation linéaire par morceaux entre les valeurs déjà fournies pour « Average », « Dim » et « Dark ». Ce modèle est illustré dans la figure 1 de la norme CIE 159:2004, la spécification CIECAM02.



| degreeOfAdaption                     | Comportement                                                                       |
|--------------------------------------|--------------------------------------------------------------------------------|
| -1.0                                 | ![Affiche une formule pour le comportement C I E C par défaut.](images/camp-image006.png)Il s’agit du comportement CIECAM02 par défaut.<br/> |
| 0,0 &lt; = degreeOfAdaption &lt; = 1,0 | *D* = degreeOfAdaptation (valeur fournie par l’utilisateur)                      |



 

Une certaine quantité de vérification des erreurs a également été ajoutée à l’implémentation. Les numéros d’équations suivants sont ceux utilisés dans la définition CIE 159:2004 de CIECAM02.

**ColorimetricToAppearanceColors**

Les valeurs d’entrée sont vérifiées pour le caractère raisonnable : si X ou Z &lt; 0,0, ou si Y &lt; -1,0, le HRESULT est E \_ INVALIDARG. Si-1,0 &lt; = Y &lt; 0,0, J, C et h sont tous définis sur 0,0.

Certaines conditions internes peuvent produire des résultats d’erreur. Au lieu de produire de tels résultats, les résultats internes sont découpés pour produire des valeurs dans la plage. Cela se produit pour les spécifications de couleurs qui seraient sombres et très probablement chromatiques : dans l’équation 7,23, si &lt; 0, a = 0. Dans l’équation 7,26, si t &lt; 0, t = 0.

**AppearanceToColorimetricColors**

Les valeurs d’entrée sont vérifiées pour obtenir un caractère raisonnable. Si C &lt; 0, c &gt; 300 ou J &gt; 500, HRESULT est E \_ INVALIDARG.

*R'<sub>a ;</sub>*, *G'<sub>a</sub>*; et *B'<sub>a ;</sub>*, (les équations 8,19-8,21) sont découpés dans la plage 399,9.

Pour tous les profils de modèle d’apparence des couleurs (CAMPs), le moteur WCS examine le point blanc adopté. Si Y n’est pas 100,0, le point blanc adopté est mis à l’échelle afin que Y soit égal à 100,0. La même mise à l’échelle sera appliquée à la valeur d’arrière-plan. Le facteur d’échelle est 100,0/adoptedWhitePoint. Y. Le même facteur d’échelle est appliqué à chacun des X, Y et Z. Si le champ NormalizeToMediaWhitePoint est défini sur « true » ou s’il est absent du CAMP, le moteur met également à l’échelle toutes les couleurs de l’appareil vers DeviceToColorimetric afin que la valeur Y du point blanc du média de l’appareil soit égale à 100,0. Les couleurs de l’appareil provenant de ColorimetricToDevice seront mises à l’échelle par l’inverse multiplicatif de ce facteur de mise à l’échelle. Si l’indicateur NormalizeToMediaWhitePoint a la valeur « false », les données de colorimétrie ne sont pas mises à l’échelle.

Pour certaines tâches, il est logique de mettre à l’échelle les valeurs colorimétriques provenant de DeviceToColorimetric. Les équations de luminosité hyperbolique dans le CAM sont vraiment conçues pour une luminance de point blanc de 100,0. Le seul endroit où une différence dans la luminance absolue (ou éclairage) entre en lecture est dans la luminance du champ d’adaptation. La came doit donc être initialisée avec un point blanc Y de 100,0. Mais si le point blanc moyen du modèle de périphérique est utilisé comme point blanc adopté, toutes les couleurs provenant de l’appareil doivent être mises à l’échelle en conséquence, ou le périphérique blanc ne sera pas fourni avec une valeur J de 100,0. Par conséquent, les valeurs Y doivent être mises à l’échelle dans les mesures. Les valeurs de mesure peuvent être mises à l’échelle avant d’initialiser le modèle d’appareil. Les résultats se trouvent déjà dans la plage appropriée. Mais cela rendrait le test du modèle d’appareil plus difficile, car les valeurs sortantes nécessitent une mise à l’échelle. Pour les tâches dans lesquelles le point blanc moyen de l’appareil est perçu comme un vrai blanc, la normalisation par le média de l’appareil est souhaitable.

La came est initialisée directement à partir du CAMP. Cela permet aux développeurs de bénéficier d’une certaine flexibilité dans l’initialisation du CAM, en fonction de la tâche qu’ils souhaitent effectuer. Dans certaines tâches, les observateurs ignorent tout Chroma dans les points blancs des médias, car ils « savent » de façon cognitive que les supports source et de destination sont « blancs ». Dans ce cas, les développeurs veulent initialiser les cames avant et inverse avec leurs points blancs de média respectifs. Dans certains cas, les observateurs peuvent comparer la couleur des arrière-plans du support. Dans ces cas-là, il est recommandé d’utiliser un CAM pour les deux appareils, et il peut être souhaitable de ne pas mettre à l’échelle les valeurs de colorimétrie de chaque appareil par le point blanc moyen de ce périphérique. Les différentes valeurs de tristimulus du média aboutissent à des valeurs d’apparence différentes dans CIECAM02.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de base de la gestion des couleurs](basic-color-management-concepts.md)
</dt> <dt>

[Schémas et algorithmes du système de couleurs Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





