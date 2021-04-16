---
title: Algorithmes et schéma de profil de modèle de mappage de couleur WCS
description: Algorithmes et schéma de profil de modèle de mappage de couleur WCS
ms.assetid: 64b9871a-1b4f-4e9a-be4d-4c25b3198b91
keywords:
- Windows Color System (WCS), profil de modèle de mappage de gammes (GMMP)
- WCS (système de couleurs Windows), profil de modèle de mappage de gammes (GMMP)
- gestion des couleurs des images, profil de modèle de carte de couleurs (GMMP)
- gestion des couleurs, profil de modèle de carte de couleurs (GMMP)
- couleurs, profil de modèle de mappage de couleurs (GMMP)
- Système de couleurs Windows (WCS), profils
- WCS (système de couleurs Windows), profils
- gestion des couleurs des images, profils
- gestion des couleurs, profils
- couleurs, profils
- Profil de modèle de mappage de gammes (GMMP)
- GMMP (profil de modèle de mappage de gamme)
- Profil de modèle de mappage de gammes WCS
- schémas, profil de modèle de mappage de gammes (GMMP)
- algorithmes, profil de modèle de mappage de couleurs (GMMP)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3714e5d7592cb1fbbbfa98e238642a2fcb38bafd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104562681"
---
# <a name="wcs-gamut-map-model-profile-schema-and-algorithms"></a>Algorithmes et schéma de profil de modèle de mappage de couleur WCS

-   [Vue d’ensemble](#overview)
-   [Architecture du profil de modèle de mappage de gamme](#gamut-map-model-profile-architecture)
-   [Génération de la limite de gamme](#generation-of-the-gamut-boundary)
-   [Schéma GMMP](#the-gmmp-schema)
-   [Éléments du schéma GMMP](#the-gmmp-schema-elements)
-   [GamutMapModel](#defaultbaselinegamutmapmodel-type)
    -   [Espace de noms](#namespace)
    -   [Version](#version)
    -   [Documentation](#documentation)
    -   [Type DefaultBaselineGamutMapModel](#defaultbaselinegamutmapmodel-type)
    -   [PlugInGamutMapType](#plugingamutmaptype)
    -   [ExtensionType](#extensiontype)
-   [Algorithmes de base GMMP](#the-gmmp-baseline-algorithms)
-   [Alignement des axes neutres](#aligning-the-neutral-axes)
    -   [Différence de couleur minimale (hachée)](#minimum-color-difference-mincd)
    -   [BasicPhoto](#basicphoto)
    -   [Vue d’ensemble](#overview)
    -   [Cas de l’interpréteur de couleurs simple](#the-case-of-single-gamut-shell)
    -   [Amélioration du noir](#black-enhancement)
    -   [Cas des interpréteurs de couleurs doubles](#the-case-of-dual-gamut-shells)
    -   [Raisons des modifications des recommandations CIE TC8-03](#reasons-for-changes-from-the-cie-tc8-03-recommendations)
    -   [Mappage de teinte](#hue-mapping)
-   [Description de la limite de la gamme et algorithmes de Shell de couleurs](#gamut-boundary-description-and-gamut-shell-algorithms)
    -   [Triangulation de la limite de gamme](#triangulation-of-the-gamut-boundary)
    -   [Éléments de ligne de limite](#boundary-line-elements)
    -   [Opération de gamme : CheckGamut](#gamut-operation-checkgamut)
    -   [Plan de teinte complet : Intersect](#full-hue-plane-intersect)
    -   [Opération de gamme : CheckGamut (suite)](#gamut-operation-checkgamut-continued)
    -   [Mappage de la gamme des couleurs de différence minimale](#minimum-color-difference-gamut-mapping)
    -   [Lissage des teintes](#hue-smoothing)
    -   [Définition des serveurs primaires et secondaires dans la description des limites de la gamme de couleurs](#setting-primaries-and-secondaries-in-the-gamut-boundary-description)
    -   [Définition de l’axe neutre dans la description des limites de la gamme de couleurs](#setting-the-neutral-axis-in-the-gamut-boundary-description)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

Ce schéma est utilisé pour spécifier le contenu d’un profil de modèle de mappage de gammes (GMMP). Les algorithmes de base de référence associés sont décrits dans la rubrique suivante.

Le schéma GMMP de base se compose d’informations d’en-tête communes, d’une référence facultative à un plug-in de modèle de carte de couleurs préféré et de balises d’extension.

En outre, le GMMP fournit des informations explicites sur le modèle de mappage de gamme ciblé, et fournit une stratégie sur le modèle de mappage de la gamme de modèles de base de référence à utiliser si le modèle ciblé n’est pas disponible. Le schéma peut inclure des informations d’extension privées, mais il n’inclura aucune autre information superflue.

## <a name="gamut-map-model-profile-architecture"></a>Architecture du profil de modèle de mappage de gamme

![Diagramme illustrant le profil de modèle de carte de couleurs.](images/gmmp-image002.png)

L’échantillonnage de l’espace colorimétrique du périphérique de sortie s’effectue en itérant les colorants de 0,0 à 1,0 avec une étape fractionnaire, en cumulant toutes les combinaisons de chaque couleur à chaque étape, puis en les convertissant de l’espace de couleur de l’appareil vers l’espace d’apparence de couleur à l’aide de la méthode DM ::D eviceToColorimetricColors suivie de la méthode CAM :: ColorimetricToAppearanceColors. Vous trouverez ci-dessous un exemple de cette opération pour RVB.


```C++
For (red= 0.0; red <= 1.0; red += redStep) {

     For (green = 0.0; green <= 1.0; green += greenStep) {

          For (blue = 0.0; blue <= 1.0; blue += blueStep) {

               Colorants[0] = red; colorants[1] = green; colorants[2] = blue;

               pRGBDM->DeviceToColorimetricColors(1, colorants, &amp;XYZ);

               pCAM->ColorimetricToAppearanceColors(1, &amp;XYZ, &amp;JCh);

          }

     }

}

```



## <a name="generation-of-the-gamut-boundary"></a>Génération de la limite de gamme

Il y a trois composants à la limite de la gamme : les primaires, les échantillons neutres et les coques. Les principaux sont générés en utilisant les unités primaires des appareils et en appliquant la transformation DeviceToColorimetric/ColorimetricToAppearance. Les échantillons neutres sont générés en échantillonnant l’espace de couleur de l’appareil dans la zone neutre et en appliquant la même transformation. Pour les trois appareils de couleur (RVB ou CMJ), les échantillons neutres sont définis comme ayant tous les colorants égaux, par exemple R = = G = = B. Pour le format CMJN, les échantillons neutres sont définis comme ayant C = = M = = Y = = 0.

Les facteurs qui influencent les données utilisées pour créer la limite de gamme sont les exemples de données (appareils de base uniquement) et les conditions d’affichage. La taille de l’étape utilisée pour l’échantillonnage complet de l’espace de couleur (pour les moniteurs et pour l’interpréteur de commandes plausible) est une constante interne et n’est pas disponible pour une manipulation externe. La modification des conditions d’affichage modifie le comportement du modèle d’apparence des couleurs (CAM) et modifie la forme de la limite de la gamme. vous devez donc générer une limite de la gamme liée au profil des conditions d’affichage. Si des exemples de données sont utilisés, comme dans le cas des imprimantes de référence et des périphériques de capture, les exemples auront un impact important sur la forme de la gamme de référence et affectent le comportement du modèle lui-même.

Pour les périphériques d’entrée, tels que les appareils photo et les scanneurs, des échantillonnages différents sont utilisés pour générer l’interpréteur de commandes de référence et l’interpréteur de commandes plausible. L’interpréteur de commandes de référence est généré à partir des mesures utilisées pour initialiser le modèle d’appareil. L’interpréteur de commandes plausible est généré de la même façon que l’illustration précédente pour les périphériques de sortie. La différence est que lorsque vous entrez une cible standard, vous ne recevez pas de valeurs entièrement saturées (où R, G ou B = 255). Vous devez extrapoler à l’aide du modèle d’appareil pour estimer ces valeurs.

## <a name="the-gmmp-schema"></a>Schéma GMMP


```C++
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema 
  xmlns:gmm="http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Gamut Map Model profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:element name="GamutMapModel">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ProfileName" type="wcs:MultiLocalizedTextType"/>
        <xs:element name="Description" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="Author" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="DefaultBaselineGamutMapModel">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="HPMinCD_Absolute"/>
              <xs:enumeration value="HPMinCD_Relative"/>
              <xs:enumeration value="SGCK"/>
              <xs:enumeration value="HueMap"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:element>
        <xs:element name="PlugInGamutMapModel" minOccurs="0">
          <xs:complexType>
            <xs:sequence>
              <xs:any namespace="##other" processContents="skip"
                minOccurs="0" maxOccurs="unbounded" />
            </xs:sequence>
            <xs:attribute name="GUID" type="wcs:GUIDType" use="required"/>
          </xs:complexType>
        </xs:element>
      </xs:sequence>
      <xs:attribute name="ID" type="xs:string" use="optional" />
    </xs:complexType>
  </xs:element>
</xs:schema>
```



## <a name="the-gmmp-schema-elements"></a>Éléments du schéma GMMP

## <a name="gamutmapmodel"></a>GamutMapModel

Cet élément est une séquence des sous-éléments suivants :

1.  Chaîne ProfileName,
2.  DefaultBaselineGamutMapModel,
3.  Chaîne de description facultative,
4.  Chaîne d’auteur facultative,
5.  PlugInGamutMap facultatif, et
6.  ExtensionType facultatif.

**Conditions de validation** : chaque sous-élément est validé par son propre type.

### <a name="namespace"></a>Espace de noms

xmlns : MGM = " http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel "

targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel "

### <a name="version"></a>Version

Version « 1,0 » avec la première version de Windows Vista.

**Conditions de validation** : 1,0 dans Windows Vista. &lt;Les Versions 2,0 sont également valides afin de prendre en charge les modifications sans rupture au format.

### <a name="documentation"></a>Documentation

Schéma de profil de modèle de mappage de gamme.

Copyright (C) Microsoft. Tous droits réservés.

**Conditions de validation** : chaque sous-élément est validé par son propre type.

### <a name="defaultbaselinegamutmapmodel-type"></a>Type DefaultBaselineGamutMapModel

UINT (type)

Valeurs d’énumération :

<dl> « \_ Absolute Absolute »  
« Relative hachée \_ »  
« genoux de la SIG \_ »  
"HueMap"  
</dl>

**Conditions de validation** : les valeurs doivent correspondre à l’une des énumérations ci-dessus.

### <a name="plugingamutmaptype"></a>PlugInGamutMapType

Cet élément est une séquence d’un GUID GUIDType et de tous les sous-éléments.

**Conditions de validation** : le GUID est utilisé pour faire correspondre le GUID de la dll du plug-in MGM. Il y a un maximum de 100 000 sous-éléments personnalisés.

### <a name="extensiontype"></a>ExtensionType

Cet élément est une séquence facultative de tous les sous-éléments.

**Conditions de validation** : il peut y avoir un maximum de 100 000 sous-éléments.

## <a name="the-gmmp-baseline-algorithms"></a>Algorithmes de base GMMP

## <a name="aligning-the-neutral-axes"></a>Alignement des axes neutres

La plupart des algorithmes de mappage de gammes ont un objectif de mapper l’axe neutre de l’appareil source à l’axe neutre du périphérique de destination : autrement dit, le blanc passe au blanc, noir à noir et gris à gris. Cela est traité en partie par la mise à l’échelle de la luminosité des couleurs sources pour correspondre à la plage de luminosité du périphérique de destination. Mais cela ne traite pas complètement le problème.

Il s’agit d’une propriété physique de la plupart des appareils de création d’images dont la chromatique de l’appareil ne correspond pas exactement à la chromatique du périphérique noir. Par exemple, le blanc du moniteur dépend de la somme des chromatiques et des luminances relatives des trois primaires, tandis que le noir du moniteur dépend de la réflectivité de la surface d’affichage. Le blanc de l’imprimante dépend de la chromatique du papier, tandis que le noir de l’imprimante dépend de l’encre ou du toner utilisé. Modèle d’apparence qui mappe exactement le blanc de l’appareil à l’axe neutre de l’espace d’apparence (Chroma exactement égal à zéro) ne mappe pas le noir du périphérique à l’axe neutre. Étant donné que l’œil est plus sensible aux différences chromatiques au fur et à mesure que les légères augmentent, les nuances de gris sont représentées comme plus chromatiques que le noir de l’appareil. (La figure 1 illustre la courbure des axes neutres dans deux dimensions. En fait, les axes neutres forment une courbe plus complexe en trois dimensions.)

Alors que la FAO prédit que ces couleurs neutres d’appareil apparaissent chromatiques, les observateurs réels semblent compenser. La plupart des gens ne considèrent pas ces valeurs neutres d’appareil comme des valeurs chromatiques. Pour la plupart des modèles de mappage de gamme, vous devez donc continuer à mapper la source neutre aux neutres de périphérique.

Pour mapper des sources neutres à des neutres de périphérique, ajustez les limites de la gamme source et de destination et chaque pixel quand vous appliquez l’algorithme de mappage de la gamme. Ajustez tout d’abord chaque valeur dans la couleur source afin que l’axe neutre de l’appareil source à la luminosité de la couleur source se situe directement sur l’axe neutre de l’espace d’apparence. (Voir la partie gauche de la figure 1.) Ajustez ensuite la description de la gamme de l’appareil de destination de manière à ce que chaque couleur sur l’axe neutre de l’appareil de destination à la luminosité de la couleur de la limite de la gamme de l’appareil de destination soit directement sur l’axe neutre de l’espace d’apparence. (Voir la partie droite de la figure 1.)

![Diagramme qui montre le graphique de la limite de gammes sources à gauche et la limite de la gamme de destination à droite.](images/gmmp-image004.png)

**Figure 1** : alignement des axes neutres illustrés. Gauche : ajustement des points source par rapport à l’axe neutre du périphérique source. Droite : réglage de la description de la limite de la gamme de destination par rapport à la description de la limite de la gamme de destination.

Notez que vous ajustez chaque valeur de pixel source par rapport à l’axe neutre à cette valeur de luminosité. Cela permet de s’assurer que les neutres du périphérique source se situeront sur l’axe neutre du modèle d’apparence. Vous allez également déplacer toutes les autres couleurs à cette luminosité de la même quantité, afin qu’il n’y ait aucune discontinuité dans la représentation de la gamme source. Vous devez passer d’un volume à l’autre à différents niveaux de luminosité, car les neutres de l’appareil source ne sont pas représentés comme étant aussi chromatiques aux différents niveaux de luminosité. En clair, il ne s’agit pas d’une transformation simple.

La gestion des valeurs de l’appareil de destination est un peu plus délicate. Au départ, vous ajustez l’ensemble de la limite de la gamme de destination de la même manière, mais en fonction de l’axe neutre de l’appareil de destination. Cela est illustré à la figure 1 sur le côté droit. Cet ajustement garantit que les valeurs de gris de la source sont mappées aux valeurs de gris de destination. Il s’agit de l’espace dans lequel les algorithmes de mappage de la gamme de couleurs fonctionnent.

Toutefois, cet espace ne décrit pas précisément le comportement réel du périphérique de destination. Vous devez inverser le mappage avant que les couleurs mappées de la gamme de couleurs soient transmises au modèle d’apparence et au modèle d’appareil de destination. Vous décalez toutes les valeurs mappées par le contraire du décalage appliqué précédemment à l’axe neutre du périphérique de destination. Cela mappe l’axe neutre de destination à la valeur représentée à l’origine par le CAM. Il procède de la même façon pour la limite de la gamme et pour toutes les valeurs intermédiaires.

![Diagramme qui affiche un graphique pour annuler l’alignement de l’axe neutre du périphérique de destination.](images/gmmp-image008.png)

**Figure 2** : annuler l’alignement de l’axe neutre du périphérique de destination

### <a name="minimum-color-difference-mincd"></a>Différence de couleur minimale (hachée)

Différence de couleur minimale (hachée) versions relatives et absolues (équivalent à l’intention de colorimétrie ICC).

> [!Note]  
> Le MGM haché est approprié pour le mappage des graphiques et des dessins de ligne contenant des couleurs « logo » (tons directs), des dégradés de couleur de logo avec certaines couleurs non compatibles et pour la dernière étape de la vérification des transformations. Bien que le MGM haché puisse être utilisé pour les images photographiques entièrement dans la gamme de destination, il n’est pas recommandé pour le rendu général des images photographiques. Le mappage des couleurs en dehors de la gamme aux couleurs sur la surface de la gamme de destination peut entraîner des artefacts indésirables, tels que des irrégularités de teinte ou de chrominance dans des dégradés lisses qui traversent la limite de la gamme. BasicPhoto est recommandé pour les images photographiques. Si une image ou un ton est requis pour un mappage de gamme autre que BasicPhoto, l’alternative consiste à créer un MGM de plug-in qui implémente ce mappage, au lieu d’utiliser hached.

 

Les couleurs de la gamme restent inchangées. Pour les couleurs non imprimables, la clarté et la chrominance sont ajustées en recherchant le point dans la gamme de destination qui a la distance de couleur minimale par rapport aux points d’entrée hors gamme. La distance de couleur est calculée dans l’espace JCh. Toutefois, vous affectez à la distance de luminosité (J) et à la distance de couleur (C) ou teinte (h) une distance différente. Une fonction de pondération dépendante de la chrominance est utilisée pour la distance en luminosité, de sorte que la pondération est plus petite pour la chrominance et plus grande pour une chrominance importante jusqu’à ce qu’une chrominance de seuil soit atteinte, après quoi le poids reste à 1, c’est-à-dire le même poids que la distance dans la couleur ou la teinte. Cela suit l’utilisation recommandée pour CMC et CIEDE2000. Il existe deux variantes : Colorimétrie relative et Colorimétrie absolue.

**Colorimétrie relative :** Tout d’abord, alignez les axes neutres de source et de destination comme décrit précédemment. Découpez ensuite la couleur source ajustée à la limite de la gamme de destination ajustée. (Voir figure 4. Mise en correspondance de Chroma le long de la lumière constante.) Réajustez les valeurs de l’appareil de destination comme décrit précédemment. Dans le cas d’une limite de gamme de destination monochrome, le découpage Chroma signifie que la valeur Chroma (C) est définie à zéro (0,0).

**Colorimétrie absolue :** Cela est similaire à la colorimétrie relative, mais sans l’alignement de l’axe neutre source et de destination. La valeur source est découpée directement en l’axe neutre de destination. Notez que si les limites de la gamme source et de destination sont monochromes, le comportement est identique à celui de la variante de Colorimétrie relative ; autrement dit, l’alignement des axes neutres est effectué, puis le Chroma est coupé à zéro. Cela garantit qu’une sortie raisonnable est atteinte même si les milieux et les colorants sont très différents.

![Diagramme qui affiche un graphique pour le découpage haché sur la gamme ajustée.](images/gmmp-image010.png)

**Figure 3** : découpage haché sur la gamme ajustée

### <a name="basicphoto"></a>BasicPhoto

### <a name="overview"></a>Vue d’ensemble

BasicPhoto : équivalent de l’intention de préférence, d’un graphique ou de la perception de ICC.

Cet algorithme est une variante de la mise à l’échelle du genou sigmoidal et de la mise à l’échelle du coude de crête (SGCK) qui est décrite par la CIE TC8-03 dans CIE156:2004. Cet algorithme variant prend en charge les descripteurs de limites de couleurs (GBDs) avec deux interpréteurs de couleurs. autrement dit, GBDs avec un shell de référence et un interpréteur de commandes plausible. L’algorithme SGCK, qui suppose à l’origine un seul interpréteur de couleurs dans le GBD, est basé sur l' \_ algorithme du genou SIG (Braun 1999), qui intègre la mise à l’échelle de la lumière du sigmoidal et de la fonction de genou proposée par Braun et Fairchild (1999), combinée à la dépendance chroma de GCUSP (Morovic, 1998). Elle conserve les constantes de teintes perçues, par exemple l’angle de teinte dans les Jab corrigés par la teinte, et utilise une mise à l’échelle de la luminosité sigmoidal générique (indépendante de l’image) qui est appliquée selon une méthode dépendante de la chrominance et un chroma de fonction de genou de 90%. La variante est mise à l’échelle le long des lignes de clarté constante.

### <a name="the-case-of-single-gamut-shell"></a>Cas de l’interpréteur de couleurs simple

Il est utile de passer en revue l’algorithme dans le cas où les GBDs source et de destination n’ont qu’un seul interpréteur de couleurs. Dans ce cas, l’algorithme comprend les calculs suivants.

Tout d’abord, effectuez le mappage de luminosité initial à l’aide de la formule suivante :

![Affiche la formule pour le mappage de la clarté initiale.](images/gmmp-image012.png) (1)

où *j ₒ* est la lumière d’origine et *j <sub>R</sub>* est la luminosité de la reproduction.

![Affiche la deuxième formule de mappage de luminosité.](images/gmmp-image014.png) (2)

Lorsque la limite de la gamme source est monochrome, la valeur de Chroma est égale à zéro pour la limite monochrome en raison de l’alignement de l’axe neutre. Cela entraînera le cas dégenerate où C est égal à zéro. Dans ce cas, *p <sub>C</sub>* est défini sur 1.

*p <sub>C</sub>* est un facteur de pondération dépendant de la chrominance (Morovic, 1998) qui dépend de la chrominance de la couleur d’origine, C et *J <sub>S</sub>* sont le résultat de la luminosité d’origine qui est mappée à l’aide d’une fonction sigmoidal.

 

Pour calculer *J <sub>S</sub>* (Braun et Fairchild, 1999), une table de recherche unidimensionnelle (LUT) entre les valeurs de luminosité d’origine et de reproduction est d’abord configurée sur la base d’une ou plusieurs fonctions normales cumulatives.

![Affiche une formule pour calculer J s.](images/gmmp-image016.png) (3)

où x ₀ et S sont respectivement la moyenne et l’écart type de la distribution normale et *i* = 0, 1, 2... *m*,*m* est le nombre de points utilisés dans lut. *S <sub>i</sub>* est la valeur de la fonction normale *cumulative pour*  / *m* pour cent. Les paramètres dépendent de la clarté du point noir de la gamme de reproduction et peuvent être interpolés à partir du tableau 1. Pour plus d’informations sur le calcul de ces paramètres, consultez Braun et Fairchild (1999, p. 391).

:::row:::
    :::column:::
        J <sub>minOut</sub>
    :::column-end:::
    :::column:::
       5.0
    :::column-end:::
    :::column:::
        10.0
    :::column-end:::
    :::column:::
        15.0
    :::column-end:::
    :::column:::
        20,0
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        ₀ x
    :::column-end:::
    :::column:::
       53,7
    :::column-end:::
    :::column:::
        56,8
    :::column-end:::
    :::column:::
        58,2
    :::column-end:::
    :::column:::
        60,6
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        S
    :::column-end:::
    :::column:::
       43,0
    :::column-end:::
    :::column:::
        40,0
    :::column-end:::
    :::column:::
        35,0
    :::column-end:::
    :::column:::
        34,5
    :::column-end:::
:::row-end:::


**Tableau 1** : calcul du paramètre de compression BasicPhoto lightity

Pour utiliser des S comme un mappage de luminosité LUT (S <sub>lut</sub> ), il doit d’abord être normalisé dans la plage de luminosité de \[ 0100 \] . Les données normalisées sont ensuite mises à l’échelle dans la plage dynamique de l’appareil de destination, comme illustré dans l’équation 4, où *j* min. et *j*<sub>Max</sub> . sont les valeurs de luminosité du point noir et du point blanc du milieu de reproduction, respectivement.<sub></sub>

![Affiche la formule pour S comme un LUT de mappage de luminosité.](images/gmmp-image018.png) (4)

À ce stade, les valeurs *j S* peuvent être obtenues à partir de la <sub>lut</sub> s en interpolant entre les points *m* des valeurs *j O* et *j s* correspondantes, et en utilisant l’équation suivante comme entrée.

![Affiche la formule pour obtenir les valeurs J S.](images/gmmp-image020.png) (5)

J <sub>minin</sub> est la valeur de luminosité du point noir du support d’origine, j <sub>MAXIN</sub> est la valeur de luminosité du point blanc du support d’origine et j <sub>O</sub> est la luminosité d’origine. Pour référence ultérieure, vous pouvez dénoter *par la* fonction sigmoidal définie comme indiqué dans la figure 4 ci-dessous.

![Diagramme qui montre le graphique pour le mappage de chrominance le long de la lumière constante.](images/gmmp-image024.png)

**Figure 4** : placage de Chroma le long de la lumière constante

Deuxièmement, si la limite de la gamme de destination est chromatique, compressez la chrominance le long des lignes de la lumière constante (l) et effectuez la compression comme suit.

![Affiche la formule permettant d’effectuer la compression Chroma.](images/gmmp-image026.png)  (6)

où *d* représente la distance par rapport à *E* sur *l*; *g* représente la limite de la gamme moyenne ; *r* représente la reproduction ; et *o* la figure 5 d’origine.

![Diagramme qui montre le graphique de la compression de chrominance et de luminosité dans BasicPhoto.](images/gmmp-image028.png)

**Figure 5** : compression de chrominance et de luminosité dans BasicPhoto

Si la limite de la gamme de destination est monochrome, la valeur de chrominance est découpée à zéro.

Troisièmement, utilisez un clip haché (décrit plus haut) pour éliminer toute erreur résiduelle.

### <a name="black-enhancement"></a>Amélioration du noir

L’algorithme précédent peut être modifié pour améliorer le noir lorsque la destination est un périphérique d’impression. Le problème est lié au choix de *J <sub>minOut</sub>*, qui ne correspond généralement pas à la couleur la plus sombre qu’une imprimante peut produire.

Plus précisément, la couleur avec la densité la plus élevée, obtenue en plaçant des encres de 100% (ou une couverture maximale possible, si la limitation de GCR/encre est activée), n’est généralement pas « neutre » dans l’espace d’apparence de la couleur. Voir figure 6. En d’autres termes, si la luminosité minimale neutre est utilisée pour l’appareil de destination, l’échelle de luminosité construite est mappée à une luminosité minimale qui n’est pas la densité la plus élevée qui peut être obtenue par l’imprimante. Considérez le cas d’utilisation supplémentaire de l’analyse sur l’imprimante. Le noir du moniteur, R = G = B = 0, est alors imprimé comme n’étant pas la densité la plus élevée. L’impact sur la qualité de l’image est qu’il y a un manque de profondeur et de contraste.

![Diagramme qui montre comment le point noir de l’appareil peut être plus sombre que la luminosité minimale neutre.](images/gmmp-seqfigure01.png)

**Figure 6** : le point noir du périphérique peut être plus sombre que la luminosité minimale neutre.

Supposons que la destination « point noir de l’appareil » est Jkakbk/JkCkh k. Si C k n’est pas égal à zéro, le point noir de l’appareil n’est pas neutre par rapport à CAM02. Si vous utilisez J k pour la « luminosité minimale neutre » de destination dans la construction de l’échelle de luminosité ; autrement dit, la définition de

*J <sub>minOut</sub> = JK*

et l’appliquer à l’interpréteur de couleurs source, vous obtenez la configuration illustrée à la figure 7. Dans la figure, le plan de teinte correspond à h k.

![Diagramme montrant l’échelle d’éclairage modifié avec le point noir du périphérique de destination.](images/gmmp-seqfigure02.png)

**Figure 7** : géométrie utilisant l’échelle de luminosité modifiée avec le point noir de l’appareil de destination

Pour permettre à l’algorithme de compression Chroma suivant de se poursuivre, vous devez aligner les lightnesses maximal et minimum sur les coques source et de destination. Pour ce faire, vous pouvez ajuster l’interpréteur de commandes de destination entre J <sub>neutralMin</sub> et j k en décalant les points vers la gauche. En outre, cette transformation doit être appliquée à l’ensemble de l’espace Jab, pas seulement au plan de teinte correspondant à h k.

La transformation est

![Affiche la formule de la transformation.](images/gmmp-seqfigure03.png)

La figure 8 illustre l’effet de la transformation.

![Diagramme qui montre l’effet de l’échelle de luminosité modifiée avec le point noir du périphérique de destination.](images/gmmp-seqfigure04.png)

**Figure 8** : géométrie utilisant l’échelle de luminosité modifiée avec le point noir de l’appareil de destination

Après l’application de l’algorithme de compression Chroma habituel, le point doit ensuite être « déplacé en arrière »; autrement dit, la transformation inverse doit être appliquée pour obtenir la couleur mappée finale.

![Affiche la formule de la transformation inverse pour obtenir la couleur mappée finale.](images/gmmp-seqfigure05.png)

### <a name="the-case-of-dual-gamut-shells"></a>Cas des interpréteurs de couleurs doubles

L’objectif est de généraliser le \_ genou SIG pour l’interpréteur de couleurs unique dans le cas où l’appareil source GBD ou l’appareil de destination GBD a une structure à deux shells. L’interpréteur de commandes interne sera appelé le shell de référence, tandis que l’interpréteur de commandes externe sera appelé l’interpréteur de commandes plausible. Vous souhaitez prendre en compte les cas suivants.

(a) les GBD source GBD et de destination ont une structure à deux shells.

(b) la source GBD a une structure à deux shells ; le GBD de destination n’a qu’un seul Shell.

(c) la source GBD a un seul Shell ; le GBD de destination a une structure à deux shells.

(d) les GBD source GBD et de destination n’ont qu’un seul Shell.

Le cas (d) est le cas de l’interpréteur de couleurs unique abordé précédemment. Pour les cas (a), (b) et (c), vous pouvez généraliser la mise à l’échelle de la luminosité pour utiliser les informations supplémentaires de la structure de l’interpréteur de commandes double. Dans les cas (b) et (c) où la source ou la destination n’a qu’un seul Shell, vous introduisez un « shell de référence induit », qui sera abordé dans une section suivante, « environnement de référence induit ». L’algorithme général pour deux shells est décrit pour la casse (a). Une fois que la construction de l’interpréteur de commandes de référence est expliquée, l’algorithme peut également être appliqué aux cas (b) et (c). Comme pour la compression Chroma, le taux de compression est déterminé par les plus grands shells disponibles. En d’autres termes, si l’interpréteur de commandes plausible et le shell de référence sont disponibles, l’interpréteur de commandes plausible sera utilisé. dans le cas contraire, l’interpréteur de commandes de référence sera utilisé.

*Mise à l’échelle de la luminosité généralisée*

L’existence de deux shells pour les GBD source et de destination signifie que vous devez mapper un ensemble de quatre points du GBD source à un jeu correspondant dans le GBD de destination.

![Montre comment mapper un ensemble de quatre points à un jeu correspondant.](images/gmmp-image030.png)

Les indices ont les significations suivantes.

o ou r : « original » (source) ou « reproduction » (destination)

min ou Max : luminosité minimale neutre ou luminosité maximale neutre

PLA ou Ref : Shell ou Shell de référence plausible

L’ordre dans chaque quadruple est également la grandeur relative attendue de ces points.

La carte de mise à l’échelle de la luminosité utilise les deux premières équations comme l’interpréteur de commandes unique, mais *J S* est défini de manière par morceaux comme suit.

![Affiche la formule pour J S de manière par morceaux.](images/gmmp-image032.png) (7)

En d’autres termes, il est sigmoidal dans l’interpréteur de commandes de référence et linéaire en dehors de. Voir figure 9.

![Diagramme qui affiche un graphique pour la fonction de redimensionnement de luminosité pour deux shells GBDs.](images/gmmp-image033.png)

**Figure 9** : fonction de redimensionnement de luminosité pour deux shells GBDs

**SHELL DE RÉFÉRENCE INDUIT**

Lorsqu’un GBD a un shell et que l’autre GBD a deux interpréteurs de commandes, vous devez créer un « shell de référence » pour le GBD avec un seul Shell. L’interpréteur de commandes existant, qui serait appelé le shell de référence, sera remplacé par l’interpréteur de commandes « plausible ». En fait, vous n’avez pas besoin de créer un shell dans l’espace Jab complet. Étant donné que la mise à l’échelle de la luminosité utilise uniquement *j Max* et *j min*, vous devez uniquement créer ces valeurs pour l’environnement de référence induit. Il existe deux cas, en fonction de la GBD qui a deux interpréteurs de charge.

Cas 1 : la source GBD a deux interpréteurs de tâches ; le GBD de destination a un shell.

Déterminer le shell de référence induite de destination sur l’axe neutre ; autrement dit, J <sub>r, \ min, \ Ref</sub> et J <sub>r, \ Max, \ Ref</sub> de l’interpréteur de commandes. Cette opération s’effectue à l’aide de l’algorithme suivant.

![Affiche l’algorithme permettant de déterminer l’interpréteur de commandes de référence induite de destination.](images/gmmp-induced01.png)

Les facteurs ? <sub>faible</sub> et ? contrôle <sub>élevé</sub> la séparation entre l’interpréteur de commandes plausible et l’interpréteur de commandes de référence. La valeur 1 signifie que les valeurs J <sub>min</sub> ou j m ₐ ₓ coïncident. Leurs valeurs sont « induites » de l’interpréteur de commandes de référence source et de l’interpréteur de commandes source plausible.

![Affiche la formule des valeurs de l’interpréteur de commandes de référence source et de l’interpréteur de commandes source plausible.](images/gmmp-induced02.png)

Les « facteurs manœuvre » F <sub>Low</sub> et f <sub>High</sub> sont des *paramètres ajustables* qui doivent se situer entre 0 et 1. Si la valeur est 0, les ₓ J <sub>min</sub> ou j m ₐ sont directement induits à partir des interpréteurs de la source. Dans ce cas, choisissez F <sub>Low</sub> = 0,95 et f <sub>High</sub> = 0,1.

Cas 2 : la source GBD a un shell ; le GBD de destination a deux shells.

Déterminer le shell de référence induit par la source sur l’axe neutre ; autrement dit, les J <sub>o, \ min, \ Ref</sub> et J <sub>o, \ Max, \ Ref</sub> de l’interpréteur de commandes. Cette opération s’effectue à l’aide de l’algorithme suivant.

![Affiche l’algorithme permettant de déterminer le shell de référence induite de destination sur l’axe neutre.](images/gmmp-induced03.png)

Encore une fois, quels sont les facteurs ? <sub>faible</sub> et ? contrôle <sub>élevé</sub> la séparation entre l’interpréteur de commandes plausible et l’interpréteur de commandes de référence. La valeur 1 signifie que les valeurs J <sub>min</sub> ou j m ₐ ₓ coïncident. Leurs valeurs sont « induites » de l’interpréteur de commandes de référence source et de l’interpréteur de commandes source plausible :

![Affiche l’algorithme pour contrôler la séparation entre l’interpréteur de commandes de référence et l’interpréteur de commandes source plausible.](images/gmmp-induced04.png)

### <a name="reasons-for-changes-from-the-cie-tc8-03-recommendations"></a>Raisons des modifications des recommandations CIE TC8-03

BasicPhoto diffère des recommandations TC8-03 CIE des manières suivantes.

1.  Chroma n’est pas compressé vers le sommet, mais le long des lignes de clarté constante.
2.  La plage de luminosité utilise la luminosité de la couleur la plus sombre dans la gamme plutôt que le point auquel la limite de gammes traverse l’axe neutre.
3.  BasicPhoto prend en charge à la fois un interpréteur de couleurs de référence et un interpréteur de couleurs plausible, si une limite de gamme dans la transformation a deux interpréteurs de commandes.
4.  BasicPhoto utilise CIECAM02 ; au lieu d’utiliser CIECAM97s pour convertir en D65 à 400 cd/m2, puis en utilisant l’espace de couleurs brute IPT.

La première modification a été apportée pour éviter les problèmes d’inversion de tonalité qui peuvent se produire lors de l’utilisation de la compression vers un sommet. Comme illustré à la figure 10, la compression de crête peut entraîner des inversions de tonalité. Cela peut se produire lorsque les couleurs de chrominance élevée sont plus claires que les couleurs de couleur inférieure. Étant donné que SGCK compresse chaque pixel indépendamment dans la clarté et le Chroma, il n’est pas garanti qu’il conserve la relation de clarté entre les valeurs de pixel après la compression. L’inconvénient de cette décision à compresser sur les lignes de clarté constante est que vous pouvez subir des pertes de chrominance, en particulier dans les zones où la limite de la gamme de destination est très plate, comme c’est le cas des jaunes brillants.

![Diagramme qui affiche l’inversion des tons provoquée par SGCK.](images/gmmp-toneinversion.png)

**Figure 10** : inversion des tons provoquée par SGCK

![Affiche une image d’origine d’un théière.](images/originalteapot.jpg)![Affiche le résultat SGCK de l’image théière.](images/badteapot.jpg)![Affiche le résultat BasicPhoto de l’image théière.](images/betterteapot.jpg)

**Figure 11** : image d’origine, résultat SGCK et résultat BasicPhoto

La figure 11 illustre cette inversion de tonalité. Sur la gauche se trouve une image originale capturée par un appareil photo numérique. au centre, l’image est reproduite par SGCK ; et à droite, l’image est reproduite par BasicPhoto. L’image à gauche se trouve dans l’espace de couleurs de l’appareil photo numérique, les images centrale et droite se trouvent dans l’espace colorimétrique d’un écran LCD. Dans l’image d’origine, la partie supérieure du théière est plus sombre que le bas, car le bas reflète la nappe sur laquelle il est assis. Dans l’image SGCK, la partie supérieure est en fait plus claire que le bas, en raison de l’inversion des tons. En outre, il est difficile de voir les éléments reflétés dans la partie inférieure du théière. À droite, BasicPhoto a corrigé l’inversion des tons et les articles réfléchis sont plus clairement distingués.

La deuxième modification a été apportée pour améliorer la reproduction des couleurs presque noires sur les imprimantes où le noir noir ne se trouve pas directement sur l’axe neutre CIECAM02. La figure 12 suivante montre une image convertie en sRVB ; reproduit pour une imprimante à jet d’encre RGB utilisant SGCK ; et reproduit pour la même imprimante à l’aide de BasicPhoto. L’image au centre n’utilise pas la totalité de l’appareil noir, et par conséquent, elle n’a pas de contraste visible dans l’original. Le contraste est rétabli avec BasicPhoto.

![Affiche l’image d’origine d’un Playset.](images/playstructure.jpg)![Affiche l’image de la Playset reproduite pour une imprimante à jet d’encre R G B à l’aide de SGCK.](images/playstructurebad.jpg)![Affiche l’image de la Playset reproduite pour une imprimante à jet d’encre R G B à l’aide de BasicPhoto.](images/betterplaystructure.jpg)

**Figure 12** : noir amélioré

La troisième modification a été apportée pour améliorer la reproduction des couleurs des appareils photo numériques. En particulier dans les cas où l’appareil photo numérique a été profilé à l’aide d’une cible de référence, une description de la gamme de couleurs générée à partir de couleurs mesurées peut ne pas inclure toutes les couleurs qui peuvent être capturées dans une scène réelle. Au lieu de découper toutes les couleurs jusqu’à la gamme de la cible de couleur mesurée, vous autorisez l’extrapolation à produire une limite de gamme plausible. L’algorithme BasicPhoto est conçu pour prendre en charge une telle limite de gamme extrapolée.

La quatrième modification a été apportée car CIECAM02 fonctionne bien pour le mappage de gammes. Le processus recommandé par TC8-03 de conversion des couleurs de l’appareil en D65 à 400 cd/m2, puis à l’aide de l’espace de couleurs brute IPT est à la fois le calcul fastidieux et le temps.

### <a name="hue-mapping"></a>Mappage de teinte

HueMap est l’équivalent de l’intention de saturation ICC.

Si la limite de la gamme source ou la limite de la gamme de destination ne contient pas de préfixes, ce modèle revient au modèle haché (relatif) décrit dans la section précédente. par exemple, les appareils pour lesquels les disques primaires ne peuvent pas être déterminés (profils ICC avec plus de quatre canaux) ou les profils ICC monochrome.

Cet algorithme commence par ajuster la teinte de la valeur de couleur d’entrée. Ensuite, il ajuste simultanément la clarté et le Chroma à l’aide d’un mappage d’inclinaison. Enfin, elle découpe la valeur de couleur pour s’assurer qu’elle est dans la gamme.

La première étape consiste à déterminer les « roues de teintes ». Recherchez les valeurs JCh pour les couleurs primaires et secondaires pour les appareils source et de destination. Vous envisagez uniquement les composants de teinte. Il en résulte une roue de teinte principale ou secondaire avec six points de couleur pour chaque appareil. (Voir figure 13.)

![Diagramme qui montre les roues teintes avec six points de couleur.](images/gmmp-figure12.png)

**Figure 13** : roues de teinte

Vous pouvez obtenir de meilleurs résultats si la source bleue principale n’est pas pivotée vers la base de destination bleue principale. Au lieu de cela, l’angle de teinte primaire bleu source est utilisé comme angle de teinte primaire bleu de destination.

Ensuite, effectuez les rotations de teinte pour chaque couleur d’entrée à partir de l’image source,

a) à l’aide de l’angle de teinte de la couleur d’entrée, déterminez l’emplacement de la couleur sur la roue de teinte source par rapport aux deux couleurs primaires ou secondaires adjacentes. L’emplacement peut être considéré comme un pourcentage de la distance entre les primaires. Par exemple, la teinte de la couleur d’entrée est 40 pour cent de la valeur de teinte de magenta à la valeur de teinte rouge.

b) sur la roue teinte de destination, recherchez l’angle de teinte associé, par exemple, 40% du magenta au rouge. Cette valeur correspond à l’angle de teinte de destination.

En règle générale, les principaux serveurs primaires et secondaires n’ont pas les mêmes angles de teinte que les serveurs primaires et secondaires de destination ; autrement dit, l’angle de teinte de destination est généralement différent de l’angle de teinte source.

Par exemple, supposons que les roues teintes produisent les valeurs suivantes :

Source M = 295 degrés, source R = 355 degrés.

Destination M = 290 degrés, destination R = 346 degrés.

Si l’angle de teinte de la couleur d’entrée est de 319 degrés, il s’agit de 40% de l’angle (24 degrés) entre la source M et la source R. L’angle de M à R est de 60 degrés et l’angle de M à la teinte d’entrée est de 24 degrés. Calculer l’angle sur la destination, qui est de 40% de la destination M vers la destination R (22 degrés), l’angle de teinte de la couleur de destination est donc de 312 degrés.

Ensuite, calculez les points de référence de teinte pour la teinte source et la teinte de destination. Pour calculer le point de référence de teinte pour une valeur h (teinte) particulière, vous devez rechercher la valeur J (luminosité) et la valeur C (chrominance).

-   Recherchez la valeur J du point de référence de teinte en interpolant entre les valeurs J pour les points primaires ou secondaires adjacents, en utilisant la position relative de la teinte. par exemple, 40 pour cent dans cet exemple.
-   Recherchez la valeur C maximale à cette valeur J et à la valeur h. Vous avez maintenant la JCh du point de référence de teinte pour cette teinte.

![Diagramme qui affiche une feuille de teinte.](images/gmmp-figure13.png)

**Figure 14** : feuille de teinte (visualisation d’une tranche de limites de gamme à une teinte spécifique)

L’étape suivante consiste à calculer le mappage d’inclinaison pour chaque pixel. Tout d’abord, Visualisez une feuille de teinte de la gamme source pour l’angle de teinte de couleur source et une feuille de teinte de la gamme de destination pour l’angle de teinte de destination calculé lors de la rotation de la teinte. Les feuilles de teinte sont créées en acceptant une « tranche » de la surface limite de la gamme JCh à un angle de teinte spécifique (voir figure 14).

Remarque : pour des raisons d’optimisation des performances, les feuilles de teinte ne sont pas réellement créées ; elles sont décrites et présentées ici à des fins de visualisation uniquement. Les opérations sont exécutées directement sur la surface limite de la gamme à la teinte spécifiée. Vous calculez ensuite les points de référence de teinte pour déterminer le mappage d’inclinaison.

-   Effectuez une mise à l’échelle claire pour mapper les points noirs et blancs de la feuille source sur la feuille de destination (voir figure 15). Les points noir et blanc de la feuille de teinte source sont mappés de manière linéaire aux points noirs et blancs de la feuille de teinte de destination, en mettant à l’échelle toutes les coordonnées J de la limite source. La valeur de la couleur d’entrée mappée par teinte est mise à l’échelle de la même manière.

![Diagramme qui montre le mappage de luminosité.](images/gmmp-figure14.png)

**Figure 15** : mappage de luminosité

-   Déterminez les points de référence de teinte pour chaque feuille de teinte. Appliquez un mappage d’inclinaison à la feuille source afin que les points de référence source et de destination coïncident (voir figure 16). Le point de référence pour une gamme à une teinte spécifique est le point de référence de teinte interpolé entre les primaires adjacentes. Le point de référence de la feuille de teinte source est mappé linéairement au point de référence de la feuille de teinte de destination, à l’aide d’une opération d’inclinaison qui verrouille l’axe J, en conservant les points noirs et les points blancs à l’arrêt. Les points noirs, les points blancs et les points de référence de la teinte source et de la teinte de destination ne doivent pas coïncider.
-   Appliquez le mappage d’inclinaison à la valeur de couleur d’entrée de luminosité ajustée. Les coordonnées J et C de la valeur de couleur source sont mises à l’échelle proportionnellement, par rapport à la distance à partir de l’axe J.
-   Ensuite, une compression légère dépendante de la chrominance vers la valeur J du point de référence de teinte est effectuée sur le point de couleur mappé en cisaillement. La compression vers la référence de teinte J est effectuée de façon similaire à la gamma, où les blancs, les noirs, les gris et les points de la référence de teinte J ne sont pas affectés. Tous les autres points tendent vers la référence de teinte J en douceur, ce qui est légèrement plus proche de la référence de teinte J, avec une constante de chrominance restante. La dépendance Chroma garantit que les couleurs neutres ne sont pas affectées, et l’effet est augmenté sur les couleurs avec un plus grand Chroma.

Voici une description mathématique de la compression de luminosité vers la référence de teinte J, ou en ajustant la valeur J du point de destination. Il s’agit du point de destination, car il a été mis en correspondance avec la gamme de destination.

Tout d’abord, calculez « factorC » (facteur de dépendance Chroma) pour le point de destination, ce qui détermine l’effet de la compression de la luminosité. Les points proches ou sur l’axe des J auront peu ou pas de compression. les points plus éloignés de l’axe des J (65536 couleurs) auront une plus grande compression appliquée. Multiplier par 0,5 pour garantir que factorC est inférieur à 1, car il est possible que sourceC soit légèrement supérieur à referenceC, mais pas deux fois plus grand.

factorC = (destinationC/referenceC) ? 0,5

où :

destinationC est la valeur C du point de destination.

referenceC est la valeur C du point de référence de teinte.

Ensuite, déterminez si le point de destination J se trouve au-dessus ou en dessous de la référence de teinte J. Si c’est le cas, procédez comme suit :

1.  Calcule « factorJ » pour le point de destination par rapport au referenceJ. Cette valeur factorJ sera comprise entre 0 et 1 (0 si sur le referenceJ ; 1 si au maxJ).
2.  factorJ = (destinationJ-referenceJ)/(maxJ-referenceJ)

    où :

    destinationJ est la valeur J du point de destination.

    referenceJ est la valeur J du point de référence de teinte.

    maxJ est la valeur J maximale de la gamme.

3.  Appliquez une fonction d’alimentation de type gamma à factorJ, ce qui réduira la factorJ d’une certaine quantité. Cet exemple utilise la puissance de 2 (le carré). Soustraire le factorJ réduit du factorJ d’origine et multipliez le résultat par la plage « J-Range totale » au-dessus du referenceJ principal pour rechercher le « deltaJ », qui représente la modification de J après la compression de la lumière, mais sans inclure la dépendance Chroma.
4.  deltaJ = (factorJ-(factorJ ? factorJ)) ? (maxJ - referenceJ)

5.  Appliquez factorC à deltaJ (plus le Chroma est élevé, plus l’effet est élevé) et calculez la nouvelle valeur J pour le point de destination.
6.  destinationJ = destinationJ-(deltaJ ? factorC)

Si J-value pour le point de destination est inférieur à referenceJ, un calcul similaire aux étapes précédentes A-C est effectué à l’aide de minJ au lieu de maxJ pour trouver la plage dans J afin de calculer le factorJ, et en tenant compte de la polarité des opérations « sous-jacentes » du referenceJ.

factorJ = (referenceJ-destinationJ)/(referenceJ-minJ)

deltaJ = (factorJ-(factorJ ? factorJ)) ? (referenceJ - minJ)

destinationJ = destinationJ + (deltaJ ? factorC)

où :

minJ est la valeur J minimale de la gamme.

La chrominance pour les points de couleur d’entrée est développée de façon linéaire (lorsque cela est possible) le long de la lumière constante proportionnellement à la valeur de chrominance maximale des gammes source et de destination à cette teinte et à la luminosité. Combinée à la compression de luminosité dépendante de la couleur précédente, cela permet de préserver la saturation, car le mappage d’inclinaison à l’aide des points de référence provoque parfois une décompression du point source vers la chrominance (voir figure 16).

![Diagramme qui montre le mappage d’inclinaison pour faire correspondre les points de référence de teinte, avant le cisaillement sur la gauche, après cisaillement à droite.](images/gmmp-shearmapping.png)

**Figure 16** : mappage de cisaillement, compression de luminosité vers la référence de teinte J et expansion Chroma

Vous trouverez ci-dessous une description mathématique du processus d’extension Chroma ou en ajustant la valeur C du point de destination. Il s’agit du point de destination, car il a été mappé et clair compressé dans la gamme de destination.

1.  Avant le mappage d’inclinaison, déterminez sourceExtentC (l’étendue de chrominance à la luminosité et la teinte du point source).
2.  Après le mappage d’inclinaison et la compression de luminosité qui transforme le point source en point de destination, déterminez le destExtentC (l’étendue de chrominance à la luminosité et la teinte du point de destination).
3.  Si la valeur de sourceExtentC est supérieure à celle de destExtentC, aucun ajustement de chrominance au point de destination n’est nécessaire et vous pouvez ignorer l’étape suivante.
4.  Ajustez destinationC (la chrominance du point de destination) pour qu’elle tienne dans l’étendue de chrominance de destination à cette légèreté et teinte.
5.  destinationC = destinationC ? (destExtentC / sourceExtentC)

    où :

    destinationC est le point de destination C-value.

    sourceExtentC est la valeur C maximale de la gamme de sources à la luminosité et à la teinte du point source.

    destExtentC est la valeur C maximale de la gamme de destination au niveau de la luminosité et de la teinte du point de destination.

Enfin, effectuez le découpage à distance minimal. Si la couleur d’entrée de la teinte, de la luminosité et de l’inclinaison est toujours légèrement en dehors de la gamme de destination, découpez-la (déplacez-la) vers le point le plus proche sur la limite de la gamme de destination (voir figure 17).

![Diagramme qui montre le découpage de distance minimal.](images/gmmp-figure15.png)

**Figure 17** : découpage de distance minimal

## <a name="gamut-boundary-description-and-gamut-shell-algorithms"></a>Description de la limite de la gamme et algorithmes de Shell de couleurs

La fonction de limite de gamme d’appareils utilise le moteur de modèle d’appareil et les paramètres analytiques pour dériver une limite de gamme d’appareils couleur, décrite comme une liste de vertex indexée de la coque de la gamme d’appareils. La coque est calculée différemment selon que vous travaillez avec des appareils supplémentaires, tels que des moniteurs et des projecteurs, ou des appareils de soustraction. La liste des vertex indexés est stockée dans CIEJab. La structure de la liste de vertex indexée est optimisée pour l’accélération matérielle par DirectX.

Cette approche présente de nombreuses solutions bien connues. Si vous recherchez « the convexe coque DirectX » sur le Web, vous recevez plus de 100 accès. Par exemple, il existe une référence de 1983 sur cette rubrique spécifique (Computer Graphics théorie and application, "Shiphulls, b-spline surfaces et CADCAM," pp. 34-49) avec des références de mise à jour de 1970 à 1982 dans la rubrique.

La collection de points peut être déterminée à partir des informations disponibles en externe, comme suit :

-   Les points de l’interpréteur de commandes de référence pour les analyses sont générés à l’aide d’un échantillonnage du cube de couleur dans l’espace de couleur de l’appareil.
-   Les points de l’interpréteur de commandes de référence pour les imprimantes et les périphériques de capture sont obtenus à partir des exemples de données utilisés pour initialiser le modèle.
-   Les points de l’interpréteur de commandes de référence pour ScRVB et sRVB sont générés à l’aide d’un échantillonnage du cube de couleur pour sRVB.
-   Les points de l’interpréteur de commandes plausible pour les appareils de capture sont générés à l’aide d’un échantillonnage du cube de couleur dans l’espace de couleur de l’appareil.
-   Les points de l’interpréteur de commandes de référence pour les projecteurs sont générés à l’aide d’un échantillonnage d’un Polyhedron dans le cube de couleur dans l’espace de couleur de l’appareil.
-   Les points de l’interpréteur de commandes possible pour les espaces de couleurs à plage dynamique étendue sont générés à l’aide d’un échantillonnage du cube couleur dans l’espace lui-même.

Vous pouvez créer une liste de vertex qui décrit de manière efficace la gamme des appareils couleur, en fonction d’un profil d’appareil et des services de support système.

Pour les périphériques de sortie, la limite de gammes décrit la plage des couleurs qui peuvent être affichées par l’appareil. Une limite de gamme est générée à partir des mêmes données que celles utilisées pour modéliser le comportement de l’appareil. Conceptuellement, vous générez un échantillon de la plage de couleurs que l’appareil peut produire, mesurez les couleurs, convertissez les mesures en espace d’apparence, puis utilisez les résultats pour créer la limite de la gamme.

Les périphériques d’entrée sont plus compliqués. Chaque pixel dans une image d’entrée doit avoir une valeur. Chaque pixel doit pouvoir représenter toute couleur trouvée dans le monde réel d’une manière ou d’une autre. Dans ce sens, aucune couleur n’est « hors gamme » pour un appareil d’entrée, car elles peuvent toujours être représentées.

Tous les formats d’images numériques ont une plage dynamique fixe. En raison de cette limitation, il existe toujours des stimuli distincts qui mappent à la même valeur numérique. Par conséquent, vous ne pouvez pas établir un mappage un-à-un entre les couleurs réelles et les valeurs de l’appareil photo numérique. Au lieu de cela, la limite de la gamme est formée en estimant une plage de couleurs réelles qui peuvent produire les réponses numériques de l’appareil photo. Vous utilisez cette plage estimée comme gamme de couleurs pour le périphérique d’entrée.

Les réplicas primaires sont inclus pour fournir un mappage de la gamme de types d’intentions de graphiques professionnels.

Dans un véritable style orienté objet, vous devez faire abstraction de la représentation sous-jacente de la limite de la gamme. Cela vous permet de modifier la représentation à l’avenir. Pour comprendre le descripteur de limite de gamme (GBD) utilisé dans la nouvelle CTE, vous devez d’abord comprendre comment les algorithmes de mappage de la gamme (GMAs) fonctionnent. Traditionnellement, GMAs a été conçu pour répondre aux besoins de la communauté graphique ; autrement dit, pour reproduire des images qui ont déjà été rendues correctement pour l’appareil sur lequel l’image d’entrée a été créée. L’objectif de Graphic Arts GMAs est de faire la meilleure reproduction possible de l’image d’entrée sur le périphérique de sortie. Le nouveau CTE GBD est conçu pour résoudre quatre problèmes clés.

Étant donné que l’image d’entrée est rendue pour le périphérique d’entrée, toutes les couleurs s’ajustent à la plage entre le point blanc du média et le point noir. Supposons que l’image soit une photographie d’une scène dans laquelle il existe un blanc diffus, tel qu’une personne dans un tee-shirt blanc, et une mise en surbrillance spéculaire, telle que la réflexion de la lumière sur une fenêtre ou un pare-feu chrome. La scène est rendue sur le support d’entrée afin que la surbrillance spéculaire soit mappée sur le point blanc du milieu, et le blanc diffus est mappé sur une couleur neutre plus sombre que le point blanc du milieu. Le choix de la façon de mapper les couleurs de la scène vers le support d’entrée est à la fois une décision dépendante de la scène et une décision esthétique. Si la surbrillance spéculaire était manquante dans la scène d’origine, le blanc diffus serait probablement mappé au point blanc du moyen. Dans une scène avec un grand nombre de détails de surbrillance, une plage de plus en plus est laissée entre le blanc spéculaire et le blanc diffus. Dans une scène où la mise en surbrillance n’est pas significative, il peut s’agir d’une très petite plage.

Pour les images prérendues, le mappage de gammes est relativement simple. Fondamentalement, le point blanc du support d’origine est mappé sur le point blanc de la couleur du milieu de reproduction, le point noir source est mappé sur le point noir de destination et la plus grande partie du mappage est terminée. Les différents GMAs d’existence fournissent des variations pour le mappage d’autres points sur l’échelle de ton du moyen source et différentes façons de gérer les valeurs de chrominance non imprimables. Toutefois, la correspondance entre le blanc et le noir et le noir est cohérente tout au long de ces variations. Cette implémentation requiert que le blanc se trouve au-dessus d’un J \* de 50 et le noir sous un j \* de 50.

Tous les codages de couleurs limitent les plages de couleurs pour les images d’entrée. L’encodage de couleur IEC standard ScRVB (IEC 61966-2-2) fournit 16 bits pour chacun des trois canaux de couleur rouge, vert et bleu (RVB). Dans cet encodage, le noir de référence n’est pas encodé en tant que triple RVB (0, 0, 0), mais en tant que (4096, 4096, 4096). Le blanc de référence est encodé sous la forme (12288, 12288, 12288). L’encodage ScRVB peut être utilisé pour représenter les surbrillances spéculaires et les détails des ombres. Il comprend des triplets RVB qui ne sont pas physiquement disponibles, car ils nécessitent des quantités négatives de lumière et des encodages qui se trouvent en dehors du locus spectral CIE. En clair, aucun appareil ne peut produire toutes les couleurs de la gamme ScRVB. En fait, aucun appareil ne peut produire toutes les couleurs qu’un utilisateur peut voir. Ainsi, les appareils ne peuvent pas remplir la gamme ScRVB, et il est utile de pouvoir représenter la partie de la gamme à remplir. Chaque appareil a une plage de valeurs dans l’espace ScRVB qu’il peut produire. Il s’agit des couleurs « attendues » pour l’appareil. Il serait surprenant que l’appareil produise des couleurs en dehors de cette gamme. Il existe une transformation définie à partir de l’espace ScRVB en espace d’apparence, de sorte que chaque appareil possède également une plage de valeurs d’apparence qu’il est supposé reproduire.

Dans ScRVB et l’entrée des appareils de capture caractérisés par une cible fixe, il est possible d’obtenir une valeur en dehors de la plage de valeurs attendues. Si quelqu’un étalonne une caméra à une cible de test ; puis capture une scène avec des surbrillances spéculaires, il peut y avoir des pixels plus clairs que le point blanc de la cible. La même chose peut se produire si un rouge se produisant naturellement est plus chromatique que le rouge de la cible. Si quelqu’un prend une image ScRVB d’un appareil, puis modifie manuellement les couleurs de l’image, il est possible de créer des pixels qui se trouvent en dehors de la plage attendue de la gamme d’appareils, même s’ils se trouvent dans la gamme de couleurs ScRVB complète.

Un deuxième problème peut ne pas être lié au premier lieu. Cela se produit lorsque vous utilisez une cible de couleur pour caractériser un périphérique d’entrée, tel qu’un appareil photo ou un scanneur. Les cibles réfléchissantes sont généralement produites sur papier et contiennent un certain nombre de correctifs colorés. Manufaturers fournissent des fichiers de données avec des mesures de couleur prises dans une condition de visualisation fixe pour chaque correctif de couleur. Les outils de profilage de couleur créent un mappage entre ces valeurs mesurées et les valeurs retournées par les capteurs de couleur dans les périphériques. Le problème est que souvent ces cibles de couleur ne couvrent pas la plage complète des valeurs de l’appareil. Par exemple, le scanneur ou l’appareil photo peut retourner la valeur (253, 253, 253) pour le point blanc de référence, et un correctif rouge de référence peut avoir une valeur RVB (254, 12, 4). Celles-ci représentent la plage de valeurs attendues pour le périphérique d’entrée, en fonction des valeurs cibles. Si vous caractérisez l’appareil d’entrée en fonction des réponses à la cible, vous vous attendez à ce que les couleurs se trouvent uniquement dans cette plage étroite. Cette plage est non seulement inférieure à la plage des couleurs que l’homme peut voir, mais elle est plus petite que la plage de couleurs que l’appareil peut produire.

Dans les deux cas, il est difficile d’estimer la gamme de l’image ou du périphérique d’entrée, en dépit de l’existence d’une gamme de référence ou de mesures. Dans le premier problème, la gamme plausible de l’appareil d’entrée est inférieure à la gamme complète de ScRVB. Dans le deuxième problème, la gamme de référence de la cible est inférieure à la gamme complète possible de l’appareil d’entrée.

Le troisième problème concerne le mappage de tonalité. De nombreux modèles de limites de gamme qui peuvent représenter correctement les images prérendues utilisées dans les arts graphiques ont été proposés, par exemple, les Braun et Fairchild de la plage de montagne GBD (Braun \[ 97 \] ), et le descripteur de limite maxima du segment de Morovic (Morovic \[ 98 \] ). Toutefois, ces modèles fournissent uniquement des informations sur les extrêmes de la gamme de l’appareil ; il manque des informations sur d’autres points dans le mappage des tons. Sans ces informations, GMAs peut uniquement effectuer des estimations approximatives du mappage de ton optimal. Pire encore, ces modèles ne fournissent aucune aide pour la plage dynamique étendue dans ScRVB et dans les images d’appareil photo numérique.

Comment ce problème est-il résolu dans les industries photographiques et Videographic ? L’appareil photo capture une image. Les experts peuvent débattre de la quantité de rendu qui se produit sur l’appareil de capture. mais ils conviennent qu’il ne s’agit pas d’une valeur significative. Les deux technologies ne mappent pas un blanc diffus dans une scène capturée sur le point blanc du moyen. De même, ils ne mappent pas le point noir de la scène au point noir du milieu. Le comportement d’un film photographique est décrit dans espace de densité à l’aide d’une courbe caractéristique, souvent appelée un facteur d’impacteur et Driffield, ou une courbe H&D. La courbe affiche la densité de la scène d’origine et la densité résultante sur le film. La figure 18 illustre une courbe H&D standard. L’axe des x représente une exposition plus grande au journal. L’axe des y représente la densité sur la diapositive. Cinq points de référence sont marqués sur la courbe : noir sans détail, qui représente la densité minimale sur la valeur négative ; noir avec détail ; Référence de la carte grise blanc avec détail ; et blanc sans détail. Notez qu’il y a un espace entre le noir sans détail (qui représente le noir du périphérique) et le noir avec détail (noir foncé). De même, il y a de l’espace entre le blanc avec des détails (diffusion en blanc) et le blanc sans détails (qui représente l’appareil blanc).

![Diagramme qui montre les courbes H et D pour le film de diapositive.](images/gmmp-image079.png)

**Figure 18** : courbe H&D pour le film coulissant

L’industrie vidéo fournit « espace » et « footroom » dans les images. Dans la spécification ITU 709, la luminance (appelée Y) est encodée en 8 bits, avec une plage comprise entre 0 et 255. Toutefois, le noir de référence est encodé à 15 et le blanc de référence est encodé sous la forme 235. Cela laisse la plage d’encodage comprise entre 236 et 255 pour représenter des surbrillances spéculaires.

L’industrie vidéo présente un système de boucles essentiellement fermé. Bien qu’il existe de nombreux fournisseurs de matériel différents, les systèmes vidéo sont basés sur des appareils de référence. Il existe un encodage standard pour les images vidéo. Il n’est pas nécessaire de communiquer une limite de gamme avec des images vidéo, car toutes les images sont encodées pour la reproduction sur le même appareil de référence. Le film est également une boucle fermée, car il n’est pas nécessaire de transmettre des données intermédiaires entre différents composants. Vous souhaitez une solution qui permet d’obtenir des images à partir d’appareils avec des gammes variables et représentant à la fois des scènes prérendues et non rendues à reproduire à la sortie avec des gammes différentes.

Le quatrième problème que la nouvelle CTE doit résoudre est le suivant : couleurs visuellement grises produites par un appareil, par exemple, quand la couleur rouge = vert = bleu sur une analyse, ne se trouve souvent pas sur l’axe neutre de la came (lorsque la chrominance = 0,0). Cela pose de bonnes difficultés pour GMAs. Pour que les GMAs fonctionnent correctement, vous devez ajuster la description de la gamme de l’appareil et des points d’entrée afin que l’axe neutre de l’appareil se trouve sur l’axe neutre de l’espace d’apparence. Vous devez ajuster les points de l’axe neutre selon une quantité similaire. Dans le cas contraire, vous ne pouvez pas effectuer de dégradations fluides via l’image. À la sortie de l’outil GMA, vous annulez ce mappage, par rapport à l’axe neutre de l’appareil de sortie. On parle alors de redressement « Chiropractic » de l’axe. À l’instar d’un Chiropractor, vous pouvez non seulement redresser le squelette (axe neutre), mais ajuster le reste du corps pour le déplacer en même temps que le squelette. À l’instar d’un Chiropractor, vous n’ajustez pas la structure du même montant tout au long de l’espace. Au lieu de cela, vous ajustez différentes sections différemment.

![Diagramme qui affiche la courbure de l’axe neutre du périphérique par rapport à l’axe neutre CIECAM.](images/gmmp-image081.png)

**Figure 19 :** Courbure de l’axe neutre du périphérique par rapport à l’axe neutre CIECAM

La nouvelle CTE requiert un modèle de limite de plage qui peut être utilisé pour représenter les images sources rendues et non rendues, fournir des informations sur l’apparence des éléments neutres de l’appareil et fournir des informations pour les images de mappage de tons avec une plage de luminance large.

![Diagramme qui montre les trois interpréteurs de couleurs.](images/gmmp-image083.png)

**Figure 20** : trois shells de gamme

La limite de la gamme est composée de trois coques qui définissent trois régions.

Dans la nouvelle CTE, l’interpréteur de commandes externe de la gamme est formé avec une coque convexe, créée à partir de points d’échantillonnage dans la gamme d’appareils. Une coque est formée en utilisant un ensemble de points d’échantillonnage et en l’entourant d’une surface. Une coque convexe a la propriété supplémentaire qui est convexe partout. Par conséquent, il ne s’agit pas de la plus petite coque possible qui peut être adaptée aux données. Mais l’expérimentation a montré que l’ajustement des points d’échantillonnage entraîne trop fortement les artefacts inadaptés dans les images, tels que l’absence d’ombrage lissé. La coque convexe semble résoudre ces problèmes.

Dans l’algorithme, les valeurs d’apparence de couleur sont obtenues pour un ensemble de points échantillonnés à partir de l’appareil. Pour les moniteurs et les imprimantes, les valeurs d’apparence des couleurs sont obtenues en générant des échantillons, puis en les mesurant. Vous pouvez également créer un modèle d’appareil, puis exécuter des données de synthèse par le biais du modèle d’appareil pour prédire les valeurs mesurées. Les valeurs mesurées sont ensuite converties de l’espace colorimétrique (XYZ) à l’espace d’apparence (Jab), et la coque est entourée autour des points.

Le point clé de cet algorithme est que le point blanc adopté utilisé dans la conversion de colorimétrie en espace d’apparence ne doit pas nécessairement être le point blanc du milieu. Au lieu de cela, vous pouvez sélectionner un point plus éloigné à l’intérieur de la gamme et sur l’axe neutre (ou à proximité). Ce point aura ensuite une valeur J-100. Les échantillons avec une valeur Y mesurée supérieure au point blanc adopté se terminent par une valeur J supérieure à 100.

Si vous placez le point blanc diffus de la scène comme point blanc adopté pour la conversion de l’espace colorimétrique, les surbrillances spéculaires de la scène seront facilement détectées comme ayant une valeur J supérieure à 100.

Étant donné que le modèle de couleurs CIECAM02 est basé sur le système visuel humain, une fois qu’un blanc adopté est sélectionné, le niveau de luminance du point noir (J = 0) est automatiquement déterminé par le modèle. Si l’image d’entrée a une plage dynamique étendue, il est possible qu’il y ait des valeurs qui correspondent à des J-valeurs inférieures à zéro.

La figure 21 suivante montre les neutres de périphérique qui s’exécutent dans le centre de l’plausible et les gammes de référence.

![Diagramme qui montre l’axe neutre du périphérique ajouté à la limite de la gamme.](images/gmmp-image085.png)

**Figure 21** : axe neutre de l’appareil ajouté à la limite de la gamme

Tous les mappages de gammes impliquent le découpage d’une plage d’entrée vers une gamme de sortie ou la compression de la gamme d’entrée pour l’ajuster à la gamme de sortie. Les algorithmes plus complexes sont formés par compression et découpage dans différentes directions, ou en divisant la gamme en différentes régions, puis en effectuant le découpage ou la compression dans les différentes régions.

La nouvelle CTE étend ce concept pour prendre en charge les régions d’une gamme possible, une gamme plausible et une gamme de référence, et permet à GMAs de les mapper de différentes façons. En outre, les GMAs ont des informations sur l’axe neutre de l’appareil. La discussion suivante décrit comment gérer les situations où les gammes de référence et les gammes de référence plausibles se sont réduites les unes sur les autres.

![Diagramme qui montre le G M A avec deux descripteurs de gamme non réduits.](images/gmmp-image091.png)

**Figure 22** : GMA avec deux descripteurs de gamme non réduits

Cet exemple peut s’afficher si vous mappez à partir d’un périphérique d’entrée, tel qu’une caméra ou un scanneur caractérisé par une cible réfléchissante, à un espace ScRVB. Ici, les couleurs plausibles plus claires que le blanc de référence sont des surbrillances spéculaires. Dans la pratique, la caractérisation d’une caméra avec une cible peut ne pas générer la plage complète des valeurs possibles dans l’appareil photo. Toutefois, les surbrillances spéculaires et les couleurs très chromatiques se trouvent en nature. (Les cibles transmissées ont généralement un correctif qui est la densité minimale possible sur le support. Avec une telle cible, les surbrillances spéculaires sont comprises dans la plage de la cible.) Le noir de référence pour une cible réfléchissante est le début de la région noire de l’ombre. Autrement dit, il y a probablement des couleurs dans les ombres qui sont plus sombres que le noir sur la cible. Si l’image contient de nombreux contenus intéressants dans cette région, il peut être utile de conserver cette variation tonale.

![Diagramme qui montre le G M A avec une gamme de destination réduite.](images/gmmp-image095.png)

**Figure 23** : graphique des couleurs de destination réduites

La figure 23 illustre un algorithme de mappage de gammes possibles lorsque la gamme de destination fournit uniquement la plage du blanc de l’appareil à la couleur noire, et qu’il n’y a pas de couleurs possibles en dehors de cette gamme. Cela peut se produire pour les périphériques de sortie standard, tels que les imprimantes. Les couleurs possibles sont mappées sur le bord de la gamme de destination. Mais il n’y a pas de courbe de tonalité pour le périphérique de sortie. Le GMA doit sélectionner un point neutre de luminance inférieure à utiliser comme destination de mappage pour le blanc de référence. Pour ce faire, un algorithme sophistiqué peut effectuer cette opération en histogramming le lightnesses dans l’image source et en observant le nombre de chutes de la plage attendue, mais plus claire que le blanc de référence. Plus lightnesses, plus l’espace est nécessaire sur le périphérique de destination entre les points mappés pour les surbrillances spéculaires et le blanc de référence. Un algorithme plus simple peut choisir une distance arbitraire par rapport à l’échelle de luminosité à partir du blanc de l’appareil, par exemple 5%. Une approche similaire s’applique pour le mappage du noir maximal et du noir de l’ombre.

Une fois que vous avez généré la courbe de tonalité de destination, vous pouvez mapper dans une méthode similaire à celle utilisée dans la figure 23 précédente. Tous les points de la courbe de tonalité de destination se trouvent dans la gamme d’appareils, et tous les points du mappage doivent se trouver dans la gamme d’appareils.

Si vous inversez les figures gauches et les figures de droite, ainsi que les directions des flèches de la figure 23, vous pouvez décrire le cas où l’image source n’a qu’une gamme de référence, et les trois gammes du périphérique de sortie ne se sont pas réduites les unes sur les autres. Il peut s’agir, par exemple, d’un mappage d’une analyse à ScRVB. Là encore, le GMA doit synthétiser les points de contrôle pour les cinq points sur la courbe de tonalité pour l’image source. Certains mappages peuvent placer tous les points de la courbe de tonalité dans la gamme de l’appareil ScRVB, tandis que les autres mappages peuvent utiliser davantage de la gamme ScRVB en mappant le blanc diffus à la référence blanche et en autorisant le blanc spéculaire à mapper à une valeur plus claire.

Enfin, vous avez le cas où les deux appareils disposent uniquement de la gamme de référence, ce qui est le fonctionnement de la plupart des algorithmes de mappage de gamme. Vous pouvez résoudre ce cas en revenant simplement aux algorithmes actuels. Sinon, si vous avez un moyen raisonnable de déterminer les cinq points de référence pour les appareils source et de destination, vous pouvez faire en sorte de mapper les points de référence.

Les gammes d’appareils contiennent plus de cinq points de référence sur l’axe neutre. Ils représentent uniquement les limites entre les régions potentielles de l’image. Entre chacun des points de référence, vous pouvez utiliser l’une des techniques de mappage de gammes existantes. Par conséquent, vous pouvez découper la plage des couleurs inattendues et compresser toutes les couleurs entre le blanc et le noir attendus, ou vous pouvez découper toutes les couleurs en dehors de la plage de référence et les compresser dans cette plage. Il existe de nombreuses possibilités, qui peuvent être implémentées dans différents GMAs. En outre, les GMAs peuvent être compressés et découpés de différentes façons. Toutes ces combinaisons sont couvertes dans cette invention.

Jusqu’ici, dans cette discussion, la gamme a été traitée comme s’il s’agissait uniquement d’une fonction de l’appareil sur lequel l’image a été créée, capturée ou affichée. Toutefois, il n’y a aucune raison pour laquelle toutes les images d’un appareil doivent avoir la même gamme. Le GMAs dépend des données du GBD. Si le descripteur est modifié entre des images, le GMAs n’a aucun moyen de le savoir. En particulier, si les images n’ont pas de surbrillances spéculaires, GMAs est plus performant si le descripteur de gamme n’indique pas que les couleurs sont plus claires que le blanc diffus.

Dans la nouvelle architecture CTE, il est possible d’utiliser plus d’un GMA. L’utilisation de plusieurs GMAs est fondamentalement mal définie. Par exemple, si un appareil de capture associe un GMA à son apparence, il a tendance à le faire avec une gamme de destination « ciblée ». Il en va de même pour les périphériques de sortie et les gammes de sources « ciblées ». La gamme sRVB est une gamme de couleurs implicites couramment ciblée. Par conséquent, il est fortement recommandé d’utiliser un seul GMA, si la prévisibilité est une priorité. Un seul flux de travail GMA doit être la valeur par défaut pour tous les workflows, en particulier les workflows consommateur et prosumer. Si le mappage de la gamme de couleurs pour la reproduction préférée doit être effectué une seule fois, il y a des cas où plusieurs processus de mappage sont inclus. Tout d’abord, pour la vérification, vous effectuez un mappage par défaut à la gamme de l’appareil cible final, puis un rendu colorimétrique à la gamme de l’appareil de vérification. Deuxièmement, certains types de mappage sont utilisés pour modifier les caractéristiques de l’image, mais ne sont pas inclus pour être mappés à une gamme d’appareils, par exemple, en ajustant la courbe tonale ou la chromatique. Si plusieurs GMAs sont utilisés, l’interface de transformation prend un tableau de cartes de gammes liées, c’est-à-dire des cartes de gamme qui ont été initialisées avec une paire de descriptions de limites de gamme. Lorsqu’il existe plusieurs mappages de couleurs, la limite de gamme d’entrée pour une carte de gammes qui suit doit être identique à la limite de la gamme de sortie de son prédécesseur.

La fonction de limite de gamme d’appareils prend le moteur de modèle d’appareil et les paramètres analytiques et dérive une limite de gamme d’appareils couleur décrite comme une liste de vertex ordonnée de la forme convexe de la gamme d’appareils. La liste de vertex triée est stockée dans CIEJab. La structure de la liste de vertex triée est optimisée pour l’accélération matérielle par DirectX. Cette approche a de nombreuses solutions bien connues (recherchez « the convexe coque DirectX » sur le Web et vous pouvez obtenir plus de 100 résultats). Il existe également une référence de 1983 sur cette rubrique (Computer Graphics théorie and application, "Shiphulls, b-spline surfaces et CADCAM" pp. 34-49), avec des références qui mettent à jour de 1970 à 1982 dans la rubrique.

Deux techniques différentes peuvent être utilisées pour calculer les triangles dans l’interpréteur de couleurs. Pour les autres appareils autres que les appareils RGB supplémentaires, vous calculez une coque convexe. Vous pouvez envisager d’examiner la prise en charge de la coque non convexe pour d’autres appareils si vous disposez d’un accès direct à ces appareils pour valider la robustesse, les performances et la fidélité des algorithmes. Il s’agit d’un processus bien connu qui ne nécessite pas de description supplémentaire. La technique utilisée pour les appareils RGB supplémentaires est décrite ci-dessous.

Différents GBDs présentent des avantages et des inconvénients. La représentation de la coque convexe garantit de superbes propriétés géométriques, telles que les tranches de teintes convexes qui fournissent un point d’intersection unique avec un rayon émanant d’un point sur l’axe neutre. L’inconvénient de la représentation convexe de la coque est également la convexité. Il est connu que de nombreux appareils, en particulier des appareils d’affichage, ont des gammes de couleurs qui sont loin d’être convexes. Si la gamme réelle s’écarte considérablement de l’hypothèse de convexité, la représentation convexe de la coque serait inexacte, éventuellement dans la mesure où elle ne représente pas la réalité.

Une fois que vous avez adopté un GBD qui donne une représentation raisonnablement exacte de la gamme réelle, d’autres problèmes se posent, d’autres en raison du concept de la tranche de teinte. Il y a au moins deux situations pathologiques. Dans la figure 24 ci-dessous, une gamme de CRT génère des tranches de teinte avec des « îlots ». Dans la figure 25, une gamme d’imprimantes génère une tranche de teinte avec une partie de l’axe neutre manquant. Les tranches de teinte pathologique ne sont pas provoquées par des limites de gammes pathologiques particulièrement dans ces cas. Ils sont provoqués par le concept de la tranche de teinte, car (a) qu’il est utilisé le long de la teinte constante, et (b) qu’il ne prend qu’une moitié du plan qui correspond à l’angle de teinte.

![Diagramme qui montre une vue supérieure et une vue latérale du « courbure » dans les teintes bleues.](images/gmmp-image097.jpg)

**Figure 24** : un moniteur CRT standard présente une gamme de couleurs qui montre le « courbure » caractéristique des teintes bleues. Si les tranches de teinte sont prises dans cette plage de teinte, les îlots isolés peuvent apparaître dans les tranches de teinte.

![Diagramme d’une gamme avec un « Gap » dans son axe neutre.](images/gmmp-image099.jpg)

**Figure 25** : une imprimante peut avoir une gamme avec « Gap » dans son axe neutre. Quand une tranche de teinte est prise (ce qui n’est que la moitié du plan), il y a un « retrait » sur la partie de la limite qui est l’axe neutre. Cela peut être difficile à résoudre par algorithme.

Pour résoudre ces pathologies, une nouvelle infrastructure est proposée et abandonne le concept de tranche de teinte utilisé comme point de départ. Au lieu de cela, le Framework utilise le jeu d’éléments de ligne de limite, ou les lignes qui se trouvent sur la limite de la gamme. Elles ne fournissent pas nécessairement une visualisation géométrique cohérente comme les tranches de teinte, mais elles prennent en charge toutes les opérations de gamme courantes. Outre la résolution des problèmes mentionnés précédemment, cette approche suggère également que la construction de tranches de teinte, même quand cela est possible, est un gaspillage de calcul.

### <a name="triangulation-of-the-gamut-boundary"></a>Triangulation de la limite de gamme

Le point de départ est un GBD qui se compose d’une triangulation de la limite de la gamme. Les méthodes connues de construction de GBDs fournissent généralement cette triangulation. Pour la béton, une méthode de construction de GBDs pour les appareils additives est décrite ici. Ces appareils incluent des moniteurs (CRT et LCD) et des projecteurs. La géométrie simple du cube vous permet d’introduire un treillis normal sur le cube. Les faces limites du cube peuvent être facettisées de différentes manières, comme celle illustrée dans la figure 26. L’architecture fournit soit un modèle d’appareil pour l’appareil afin que les valeurs colorimétriques des points de treillis puissent être obtenues algorithmiquement, soit des mesures ont été effectuées directement pour ces points. L’architecture fournit également CIECAM02, afin que vous puissiez supposer que les données de départ ont déjà été mappées à l’espace CIECAM02 Jab. Ensuite, chaque point de treillis sur les faces limites du cube RGB a un point correspondant dans l’espace Jab. Les connexions des points qui forment l’ensemble des triangles dans l’espace RVB induitnt également un ensemble de triangles dans l’espace Jab. Cet ensemble de triangles constitue une triangulation raisonnable de la limite de gamme si (a) le treillis sur le cube RVB est suffisamment parfait, et (b) la transformation de l’espace de l’appareil vers l’espace de couleurs uniforme est topologique. autrement dit, il mappe la limite à la limite et n’active pas la gamme à l’intérieur de sorte que les points intérieurs deviennent des points de limite.

![Diagramme illustrant une méthode simple pour triangluate la limite de gamme d’un appareil avec R G B comme espace de périphérique.](images/gmmp-image100.png)

**Figure 26** : méthode simple pour trianguler la limite de gamme d’un appareil avec RVB comme espace d’appareil

### <a name="boundary-line-elements"></a>Éléments de ligne de limite

L’essentiel de cette infrastructure est le concept d’éléments de ligne de limite ; ensemble de segments de ligne (a) situés sur la limite de la gamme, et (b) sur un plan. Dans ce cas, le plan est un plan de teinte. Chaque segment de ligne est le résultat de l’intersection du plan avec un triangle de limites de couleurs. Bien que de nombreux chercheurs aient utilisé la construction de l’intersection d’un plan avec des triangles de limites, ils analysent généralement la relation entre ces segments de ligne et tentent de construire un objet géométrique cohérent à partir des segments de ligne. Différents algorithmes ont été conçus pour suivre ces segments de ligne l’un après l’autre jusqu’à ce qu’une tranche de teinte entière soit obtenue, et de nombreuses tentatives ont été effectuées pour accélérer le processus de recherche.

Cette approche est différente. Vous croisez le plan avec les triangles pour obtenir les segments de ligne. Vous envisagez ensuite ces segments de ligne comme des objets conceptuels de *base* . Il est nécessaire d’analyser la relation entre les segments de ligne ; vous n’avez pas besoin de savoir comment elles sont interconnectées les unes avec les autres. Ce point de vue résout le problème de la tranche de teinte avec des îlots. Les approches connues qui tentent de construire la tranche de teinte supposent que, si l’une d’entre elles commence par un segment de ligne et la suit sur le segment de ligne suivant, et ainsi de suite ; Il finit par revenir au point de départ, à partir duquel une tranche de teinte entière serait construite. Malheureusement, cette approche pourrait manquer l’île (et dans le pire scénario, le continent). En ne permettant pas d’obtenir une image géométrique cohérente ; autrement dit, la tranche de teinte vous permet de gérer facilement le problème de l’îlot. Une autre différence importante dans cette approche est que, pour accélérer la construction des segments de ligne, elle utilise un « filtre triangulaire ». Le filtre triangulaire lève certains triangles qui ne produisent absolument pas de segments de ligne qui seraient utiles dans l’opération de gamme actuelle. Étant donné que l’intersection d’un triangle avec le plan est coûteuse en calcul, cela améliore la vitesse. Un effet secondaire est que vous ne pouvez pas construire la tranche de teinte, car certains segments de ligne seraient manquants en raison du filtrage de triangle.

### <a name="gamut-operation-checkgamut"></a>Opération de gamme : CheckGamut

L’exemple suivant explique le fonctionnement de l’infrastructure, et la façon dont CheckGamut est exécuté, autrement dit, le fonctionnement de la vérification de la présence d’une couleur dans la gamme.

L’infrastructure générale est illustrée dans la figure 27 suivante. Il existe plusieurs composants. Les composants étiquetés en italiques sont des composants qui peuvent être différents dans l’implémentation en fonction de l’opération de gamme en question. Les autres composants sont invariants pour toutes les opérations de gamme. Pour commencer, l' ***entrée*** est un jeu d’attributs de couleur. Dans le cas de CheckGamut, il s’agit de la couleur de la requête. Dans la figure 27 et la discussion suivante, il est supposé que l’angle de teinte est parmi les attributs de couleur d’entrée ou peut être obtenu à partir de ceux-ci. C’est clairement le cas si l’entrée est le point de couleur entier, dans Jab ou JCh, à partir duquel vous pouvez ensuite calculer l’angle de teinte. Notez que l’angle de teinte n’est nécessaire que si des plans de teinte sont utilisés. En fonction de l’opération de gamme en question, il n’est pas nécessaire d’utiliser le plan de teinte. Par exemple, dans la construction de la routine CheckGamut, vous souhaiterez peut-être utiliser des plans de constante J. Il s’agit d’une généralisation qui ne sera pas utilisée ou traitée plus en détail ; Toutefois, il peut être utile de mémoriser cette flexibilité de la méthodologie pour prendre en charge d’autres opérations de gamme lorsque le plan de teinte peut ne pas être le meilleur choix.

![Diagramme qui montre le Flow pour prendre en charge les opérations de gamme.](images/gmmp-image112.jpg)

**Figure 27** : infrastructure pour prendre en charge les opérations de gamme

L’angle de teinte, qui est obtenu directement à partir des entrées ou calculées à partir des entrées, est utilisé pour initialiser le plan de teinte appelé **plan de teinte complet** dans la figure. « Full » est mis en évidence, car il s’agit du plan complet, pas seulement du demi-plan contenant la teinte. Le plan complet contient à la fois l’angle de teinte d’entrée et l’angle 180 degrés opposés à celui-ci. La fonctionnalité clé du plan de teinte est la fonction Intersect, qui est expliquée dans la sous-section suivante, Full teinte plan : Intersect. Supposons que le GBD a déjà été construit et que l’ensemble des **triangles de limite de gamme** est disponible. Croisent les triangles qui ont survécu au **_filtre triangulaire_* _ avec le plan teinte à l’aide de Intersect. Le _composant filtre triangulaire * est étiqueté en italique, ce qui signifie que le composant varie en fonction des différentes opérations de gamme. Le *filtre triangulaire* pour CheckGamut est expliqué dans la section opération de gamme : CheckGamut (suite). Le résultat de l’intersection d’un triangle avec le plan de teinte est soit vide, soit un **élément de ligne de limite** , c’est-à-dire une paire de points distincts. Si le résultat n’est pas vide, il est passé dans le *_processeur d’éléments de ligne_* *_ , qui est à nouveau différent selon l’opération de gamme. Le _processeur d’élément de ligne * met à jour la structure de données interne, ***données traitées internes**_ , dont le contenu ou la disposition dépend également de l’opération de gamme. En règle générale, les _données traitées internes * contiennent la « réponse » au problème, qui est continuellement mise à jour avec chaque nouvel élément de ligne de limite trouvé. Lorsque tous les éléments de ligne de limite ont été traités, la réponse a été trouvée. Il reste à y accéder via l'**adaptateur de sortie***_. Étant donné que la _Internal données traitées * est spécifique à l’opération de gamme, l' *adaptateur de sortie* est également spécifique à l’opération de gamme.

### <a name="full-hue-plane-intersect"></a>Plan de teinte complet : Intersect

La fonction Intersect calcule l’intersection entre le plan de teinte et un triangle. Comme c’est le cas, cette fonction est importante pour deux raisons.

Tout d’abord, l’intersection de chaque bord du triangle avec le plan peut produire trois points d’intersection, une situation géométriquement impossible. La raison pour laquelle cela peut se produire dans le calcul est que, lorsque des calculs sont effectués dans une virgule flottante, par exemple au format IEEE, il y a des incertitudes, ou « bruit numérique », à chaque étape qui affecte la conclusion de savoir si un bord croise le plan. Lorsque le plan croise les bords dans une situation de quasi-absence, les points d’intersection sont proches les uns des autres et la détermination de la présence d’un point d’intersection dans le bord est aléatoire. Bien que le bruit dans les valeurs numériques des points soit faible, la conclusion qualitative qu’il y a plus de deux points d’intersection est à la fois très impossible et difficile à gérer correctement dans l’algorithme.

Deuxièmement, cette fonction se trouve dans la boucle critique pour chaque bord de chaque triangle filtré. il est donc important que vous optimisiez son efficacité le plus possible.

Pour résoudre le premier problème de bruit numérique, effectuez les calculs dans des entiers. Pour résoudre le deuxième problème d’optimisation de son efficacité, mettez en cache l’attribut le plus utilisé de chaque vertex ou le « produit scalaire » associé à chaque vertex. Le passage à des entiers est un moyen classique de garantir la cohérence géométrique. L’idée de base est que, si vous devez effectuer une quantification, faites-le au début. Ensuite, les calculs suivants peuvent être effectués dans des entiers, et si les entiers sont suffisamment larges pour éviter tout risque de dépassement de capacité, les calculs peuvent être effectués avec une précision infinie. Fonction de quantification suivante utile à cet effet.

ScaleAndTruncate (x) = partie entière de x \* 10000

Le facteur d’échelle 10000 signifie que le nombre à virgule flottante en entrée a quatre décimales, ce qui est suffisamment précis pour cette application. En fonction de la plage de valeurs de l’espace d’apparence de couleur, vous souhaitez choisir un type d’entier avec des bits suffisamment larges pour contenir les calculs intermédiaires. Dans la plupart des espaces d’apparence des couleurs, la plage de chaque coordonnée est comprise entre-1 000 et 1 000. La coordonnée quantifiée a une valeur absolue possible maximale de 1 000 \* 10 000 = 10 millions. Comme vous le verrez, la quantité intermédiaire est un produit scalaire, qui est la somme de deux produits de coordonnées. par conséquent, elle a une valeur absolue possible maximale de 2 \* (10 millions) ₂ = 2 ? 10 ₁ ₄. Le nombre de bits requis est le journal ₂ (2 ? 10 ₁ ₄) = 47,51. Un choix pratique pour le type entier est, par conséquent, des entiers 64 bits.

Pour garantir que l’intersection d’un plan avec un triangle donne toujours soit un jeu vide, soit un ensemble de deux points, vous devez considérer le triangle comme un tout, et non comme des bords individuels du triangle séparément. Pour comprendre la situation géométrique, prenez en compte les « distances signées » des vertex du triangle à partir du plan de teinte. Ne Calculez pas ces distances signées directement ; au lieu de cela, vous calculez les produits points des vecteurs de position des vertex avec le vecteur normal quantifié sur le plan. Plus précisément, lors de l’initialisation du plan de teinte, le vecteur normal quantifié est calculé comme suit.

NormalVector = (ScaleAndTruncate (-Sin (teinte)), ScaleAndTruncate (COS (teinte)))

Notez que ce vecteur est un vecteur à deux dimensions. Vous pouvez utiliser un vecteur à deux dimensions, car le plan de teinte est vertical ; le troisième composant du vecteur normal est donc toujours égal à zéro. En outre, une table de recherche de produits point est initialisée pour avoir une entrée pour chaque vertex à partir des triangles de limite de gamme et le produit scalaire correspondant défini sur une valeur non valide.

Au cours d’une opération d’intersection du plan de teinte avec un triangle, le produit scalaire de chaque vertex du triangle est recherché. Si la valeur de la table de recherche est la valeur non valide, le produit scalaire est calculé à l’aide de l’expression suivante.

NormalVector. a \* ScaleAndTruncate (vertex. a) + NormalVector. b \* ScaleAndTruncate (vertex. b)

Là encore, le composant J-Component du vertex n’est jamais utilisé, car le vecteur normal est horizontal. Ce produit est ensuite enregistré dans la table de recherche afin qu’il ne soit pas nécessaire de le recalculer si le produit scalaire du vertex est interrogé ultérieurement.

La mise en cache permet de déterminer rapidement si une arête croise le plan, après que les produits points ont été représentées dans la table de recherche, qui est générée progressivement à mesure que les vertex sont traités.

![Diagramme qui montre l’intersection du plan de teinte avec un triangle.](images/gmmp-image114.jpg)

**Figure 28** : intersection entre le plan de teint et un triangle

Pour le triangle de la figure 28 afin d’intersecter le plan de teinte dans un segment de ligne non dégénérée, les produits points des vertex doivent être dans l’un des modèles suivants, lorsqu’ils sont triés dans l’ordre croissant.

0, 0, +; -, 0, 0 ; -, 0, +; -,-,+; -,+,+

Un point de terminaison du segment de ligne se produit lorsque le plan est croisé par un bord avec des vertex qui ont des signes différents dans le produit scalaire. Si le signe est égal à zéro, le sommet se situe à droite sur le plan, et l’intersection entre le bord et le plan est le sommet lui-même. Notez également que les cas 0, 0, 0 ; -,-, 0 ; 0, +, + ne sont pas signalés. Le premier cas (0, 0, 0) signifie que le triangle entier se trouve sur le plan. Cela n’est pas signalé, car chaque bord du triangle doit appartenir à un triangle voisin qui ne se trouve pas également entièrement sur le plan. Le bord est signalé quand ce triangle est pris en compte. Les deux autres cas (-,-, 0 et 0, +, +) correspondent à la configuration géométrique selon laquelle le triangle touche le plan dans un sommet. Ces cas ne sont pas signalés, car ils ne donnent pas lieu à un segment de ligne non dégénérée.

L’algorithme précédent détermine quand calculer une intersection entre un bord du triangle et le plan de teinte. Une fois qu’une arête est déterminée, l’intersection est calculée à l’aide des équations paramétriques. Si l’un des points est égal à zéro, l’intersection est le vertex lui-même, donc aucun calcul n’est nécessaire. En supposant que les deux produits point des sommets de l’arête ne sont pas nuls, vertex1 est le vertex avec un point *négatif* dotProduct1 produit ; et Vertex2 est le vertex avec un point *positif* dotProduct2. Cet ordre est important pour s’assurer que le point d’intersection calculé ne dépend pas de la façon dont l’ordre des sommets s’affiche dans la représentation de l’arête. Le concept géométrique de l’arête est symétrique par rapport à ses sommets. L’aspect de calcul de l’utilisation des équations paramétriques de l’arête présente l’asymétrie (le choix du sommet de départ), qui peut fournir un point d’intersection légèrement différent en raison du bruit numérique et du conditionnement des équations linéaires à résoudre. Ceci dit, le point d’intersection, intersection, est donné par le code suivant.

t = dotProduct1/(dotProduct1-dotProduct2)

ensembles. J = vertex1. J + t \* (Vertex2. J-vertex1. J

intersection. a = vertex1. a + t \* (Vertex2. a-vertex1. a)

intersection. b = vertex1. b + t \* (Vertex2. b-vertex1. b)

### <a name="gamut-operation-checkgamut-continued"></a>Opération de gamme : CheckGamut (suite)

L’algorithme géométrique de base utilisé pour la vérification de la gamme est de compter le nombre de croisements de rayon. Pour un point de requête donné, envisagez un rayon commençant par le point de requête et pointant vers le haut (direction J). Compter le nombre de fois que ce rayon traverse la limite de la gamme. Si ce nombre est pair, le point de requête est hors gamme. Si ce nombre est impair, le point est à l’intérieur de. En principe, cet algorithme peut être implémenté en 3D, il est généralement dû à des difficultés provoquées par des situations dégénérées, telles que le rayon (en partie) sur un triangle limite, ou un degeneracy dimensionnel inférieur, tel que le rayon à l’extrémité d’un triangle de limite. Même en 2D, vous devez gérer ces situations de dégénération ; mais le problème est plus simple et a été résolu de manière satisfaisante. Consultez \[ O’Rourke \] .

Pour un point d’entrée donné Jab, déterminez son angle de nuance h comme suit.

h = ATAN (b/a),

Initialisez le plan de teinte, puis déterminez les éléments de ligne de limite correspondant à ce plan de teinte. Étant donné que les éléments de ligne de limite sont pertinents uniquement s’ils croisent le rayon vers le haut, configurez un filtre de triangle pour supprimer les triangles qui donnent des éléments de ligne qui n’intersectent pas le rayon vers le haut. Dans ce cas, envisagez le cadre englobant du triangle. Le rayon vers le haut ne croise pas le triangle si le point de requête est en dehors de la « Shadow » convertie par le cadre englobant si une source de lumière était juste au-dessus. Gonflez-la légèrement avec une tolérance préfixée pour autoriser le bruit numérique afin de ne pas lever par inadvertance des triangles qui pourraient donner des éléments de ligne utiles. Le résultat est le cylindre rectangulaire semi-infini présenté dans la figure 29. Il est possible d’implémenter efficacement le point de requête à l’intérieur ou à l’extérieur de ce cylindre à l’aide d’inégalités simples.

![Affiche le filtre triangulaire pour CheckGamut.](images/gmmp-image116.jpg)

**Figure 29** : filtre de triangle pour CheckGamut

CheckGamut comporte trois composants de gamme de l’opération : *données traitées internes*,*processeur des éléments de ligne* et adaptateur de *sortie*. Les *données traitées internes* sont une liste d’éléments de ligne traités par le *processeur d’éléments de ligne*. Dans ce cas, le *processeur d’élément de ligne* ajoute simplement un élément de ligne à la liste. La structure de données interne pour les *données traitées internes* peut être une liste liée ou un tableau dont la taille peut croître.

L' *adaptateur de sortie* est un module qui accède à la liste des éléments de ligne, détermine si un élément de ligne croise le rayon vers le haut (nombre 1) ou non (nombre 0). L’addition de tous ces nombres donne un nombre total. L' *adaptateur de sortie* génère en fin de compte une réponse de « Oui » (in-large) ou « no » (non imprimable), selon que le nombre total est impair ou même. L’étape où vous déterminez si un élément de ligne franchit le rayon vers le haut mérite une attention, car c’est là que se trouve le problème de degeneracy et que le problème de surcomptage survient. À la suite de \[ O’Rourke \] , pour qu’un élément de ligne croise le rayon, le point de terminaison droit (le point de terminaison avec une plus grande chrominance) doit être strictement sur le côté droit du rayon. Cela garantit que, si un point de terminaison se trouve exactement sur le rayon, il n’est compté qu’une seule fois. La même règle résout également la situation dégénérée dans laquelle l’élément de ligne se trouve exactement sur le rayon. Vous n’incrémentez pas le nombre pour cet élément de ligne.

La figure 30 montre les éléments de ligne résultants d’un exemple de gamme avec le point de requête à différentes positions.

![Diagramme qui montre les éléments de ligne résultants d’un échantillon de gamme avec le point de requête à différentes positions.](images/gmmp-image118.jpg)

**Figure 30** : fonctionnement de CheckGamut

### <a name="minimum-color-difference-gamut-mapping"></a>Mappage de la gamme des couleurs de différence minimale

Le mappage de la gamme de couleurs de différence minimale, MinDEMap, a une spécification simple : si une couleur est dans la gamme, ne rien faire. Si une couleur est hors de la gamme, projetez-la sur le point le plus proche sur la limite de la gamme. Le mot clé « le plus proche » n’est pas bien défini tant que vous n’avez pas spécifié l’équation de différence de couleur à utiliser. Dans la pratique, pour faciliter et accélérer le calcul, la distance euclidienne de l’espace d’apparence de couleur choisi, ou une variante de celle-ci, est utilisée comme mesure de différence de couleur. L’avantage de la mesure euclidienne est qu’elle est compatible avec le produit scalaire de l’espace, ce qui permet d’utiliser l’algèbre linéaire. En détail, si un « produit scalaire » est défini dans l’espace, une distance peut être définie comme la racine carrée du produit scalaire du vecteur de différence avec lui-même. Un produit scalaire peut généralement être défini par un tableau 3x3 positif positif A.

u ? v = u <sub>T</sub> AV

la partie droite est la multiplication habituelle de la matrice. Si un est la matrice d’identité, le produit scalaire standard est récupéré. Dans la pratique, si Jab est l’espace colorimétrique, vous ne souhaitez pas mélanger les composants, de sorte qu’une matrice diagonale autre que la matrice d’identité peut être utilisée. En outre, vous souhaiterez peut-être conserver l’échelle de a et de b sans changer afin que la mesure de la teinte soit conservée. Une variante utile du produit euclidienne dot standard est donc la suivante.

w <sub>j</sub> (composant de vous) (composant j de v) + (un composant de vous) (un composant de v) + (composant b de vous) (composant b de v)

où w <sub>J</sub> est un nombre positif. Une autre variante consiste à laisser w <sub>J</sub> varier avec le point de requête d’entrée :

w <sub>j \ =</sub> w <sub>j</sub> (queryPoint)

Le résultat final est une mesure de distance qui est asymétrique en ce qui concerne les deux points, et avec différents poids relatifs sur la clarté et la chrominance ou la teinte que le point de requête d’entrée varie. Cela est conforme à quelques observations sur la perception de la couleur humaine selon laquelle les différences de couleur ne sont pas pondérées de manière égale dans toutes les dimensions. Il a été constaté que les gens sont moins sensibles aux différences de luminosité que les différences de teinte et de chrominance.

La fonction Weight suivante est utile.

w <sub>J</sub> = k ₂-k ₁ (C-c m ₐ ₓ) n

où k ₂ = 1, k ₁ = 0,75/(C m ₐ ₓ) n, C m ₐ ₓ = 100, n = 2 et C est le plus petit de Chroma du point de requête et C m ₐ ₓ.

pour qu’un poids de 0,25 soit placé sur le terme J lorsque Chroma est égal à zéro et un poids de 1 lorsque Chroma est 100. La tendance à placer moins de poids sur J lorsque Chroma est petit et plus poids sur J lorsque Chroma est important suit l’utilisation recommandée pour CMC et CIEDE2000.

![Graphique qui affiche la fonction Weight sur le composant J de la métrique.](images/gmmp-image119.png)

**Figure 31** : fonction Weight sur le composant J de la métrique

Utilisez l’espace jab pour l’exemple suivant. Le calcul est requis pour effectuer des recherches dans tous les triangles de limite afin de déterminer le point le plus proche dans la mesure euclidienne. Vous trouverez ci-dessous une approche simple pour rendre ce processus aussi efficace que possible, sans introduire d’hypothèses supplémentaires susceptibles d’accélérer le processus, mais également de se retrouver uniquement dans une réponse approximative. Tout d’abord, il est nécessaire de comprendre la procédure géométrique de projection d’un point sur le triangle donné. Une description est indiquée ici.

Une projection orthogonale sur le plan infini contenant le triangle est exécutée pour la première fois. La distance la plus petite entre le point de requête et le plan peut être déterminée en deux étapes.

**(a)** calculer le vecteur normal de l’unité sur le triangle.

**(b)** calculer le produit scalaire du vecteur normal de l’unité et un vecteur formé à partir du point de requête et d’un point sur le triangle ; autrement dit, l’un de ses sommets. Étant donné que le vecteur normal a une longueur d’unité, la valeur absolue de ce produit scalaire correspond à la distance entre le point de requête et le plan.

Le point projeté n’est peut-être pas la réponse, car il peut se trouver à l’extérieur du triangle. Par conséquent, vous devez d’abord effectuer une vérification. Le calcul est équivalent au calcul des coordonnées Barycentric du point projeté par rapport au triangle. Si le point projeté est déterminé comme étant à l’intérieur du triangle, il s’agit de la réponse. Si ce n’est pas le cas, le point le plus proche est acquis sur l’un des bords du triangle. Effectuez une recherche sur chacun des trois bords. La détermination de la projection du point de requête sur un bord est un processus similaire à la projection sur le triangle, mais une dimension moins. Une projection orthogonale est d’abord calculée. Si le point projeté se trouve sur le bord, il s’agit de la réponse. Si ce n’est pas le cas, le point le plus proche est acquis sur l’un des deux points de terminaison. Effectuez une recherche sur les deux points de terminaison ; autrement dit, calculez la distance entre chaque point de requête et comparez celle qui est la plus petite.

Un examen minutieux révèle qu’il y a beaucoup de recherches répétées lorsque vous parcourez tous les triangles, car une arête est toujours partagée par deux triangles et un sommet partagé par au moins trois bords. En outre, vous n’êtes pas très intéressé par la recherche du point le plus proche d’un triangle particulier. au lieu de cela, vous êtes intéressé par la recherche du point le plus proche de la limite de gamme entière. Toutefois, un triangle particulier est celui dans lequel cette est effectuée. Il existe deux stratégies que vous pouvez utiliser pour accélérer la recherche.

**Stratégie I**. Chaque vertex sera traité, au plus une fois. Chaque Edge sera traité, au plus une fois.

**Stratégie II**. À tout moment dans la recherche, vous avez le meilleur candidat avec la distance la plus appropriée. Si vous pouvez déterminer, par une vérification rapide, qu’un triangle ne peut pas donner une meilleure distance, il est inutile de poursuivre le calcul. Vous n’avez pas besoin du point et de la distance les plus proches pour ce triangle.

![Diagramme qui montre le déroulement du démappage minimal.](images/gmmp-image120.png)

**Figure 32** : configuration minimale des schémas de mappage

La figure 32 montre le déroulement général de la logique du mappage de gammes MinDEMap. Pour un point de requête, la fonction CheckGamut est appelée en premier. Si le point est dans la gamme, la carte est une absence d’opération. Si le point est hors de la gamme, appelez ProjectPointToBoundary. Passons maintenant à la figure 33. À ce stade, il est supposé que les valeurs suivantes ont été calculées.

**(a)** vecteur normal d’unité à chaque triangle de limite de couleurs par rapport au produit scalaire standard.

**(b)** liste de vertex et liste d’arêtes, en plus de la liste de triangles.

![Diagramme qui affiche la routine « ProjectPointToBoundary ».](images/gmmp-image122.jpg)

**Figure 33** : routine ProjectPointToBoundary

Il s’agit d’une surcharge constante, qui aurait un coût réduit si des requêtes suffisantes pour cette limite de gamme sont effectuées. En règle générale, c’est le cas lorsque vous générez un LUT de transformation d’un appareil vers un autre, où il n’y a que deux couleurs fixes, et la transformation LUT s’exécute par points sur la grille échantillonnée de manière uniforme. Vous précalculez les vecteurs normaux en ce qui concerne le produit scalaire standard, même si la notion de la perpendiculaire sera basée sur le produit scalaire pondéré, qui dépend du point de requête, comme expliqué précédemment. En effet, un vecteur normal en ce qui concerne le produit scalaire pondéré peut être obtenu facilement à partir du vecteur normal en ce qui concerne le produit scalaire standard. Si n ₀ est un vecteur normal par rapport au produit scalaire standard,

n = (J-Component de n ₀/w <sub>J</sub>, un composant de n ₀, b-Component de n ₀)

est perpendiculaire au triangle en ce qui concerne le produit scalaire pondéré. En raison de cette relation, il est toujours bénéfique de précalculer n ₀, même s’il doit être ajusté en fonction du point de requête.

La routine ProjectPointToBoundary commence par la réinitialisation de l’historique traité des sommets et des bords. Il s’agit de tables d’indicateurs BOOLÉENs qui assurent le suivi de la visite d’un sommet ou d’un bord. Elle réinitialise également la variable ShortestDistance sur « Infinity », qui est la valeur encodée maximale dans le système de nombres à virgule flottante utilisé. Elle s’exécute ensuite via une boucle, en recherchant le point le plus proche de chaque triangle à l’aide de l’appel ProcessTriangle. ProcessTriangle est la routine permettant de mettre à jour la variable ShortestDistance et est clairement dans la boucle critique. L’une des optimisations consiste à s’arrêter lorsque le résultat est suffisant. Après chaque appel à ProcessTriangle, la variable ShortestDistance est examinée. S’il répond à un seuil prédéfini, vous pouvez arrêter. Le seuil prédéfini dépend de l’espace colorimétrique utilisé et de la précision requise du système d’imagerie des couleurs. Pour une application classique, vous ne souhaitez pas effectuer de travail inutile si la différence de couleur est inférieure à ce qui peut être déterminé par la vision humaine. Pour CIECAM02, cette différence de couleur est de 1. Utilisez une valeur de seuil de 0,005 dans l’implémentation, toutefois, pour conserver la précision des calculs, car il peut s’agir uniquement d’une étape intermédiaire dans une chaîne de transformations.

ProcessTriangle implémente la stratégie II précédente. En obtenant un vecteur normal du vecteur normal d’unité précalculée au triangle en ce qui concerne le produit scalaire standard, il calcule la distance entre le point de requête et le plan infini contenant le triangle en formant le produit scalaire du vecteur normal d’unité et du queryVector, le vecteur à partir de l’un des sommets du triangle, vertex1, au point de requête. , queryPoint.

queryVector = queryPoint-vertex1

distance = \| normalVector \* queryVector \| / \| \| normalVector\|\|

Il s’agit d’un calcul relativement peu coûteux, et la distance est nécessaire pour effectuer d’autres calculs. Si cette distance n’est pas inférieure à la distance la plus récente, ShortestDistance, ce triangle ne produira pas une plus grande distance, car il ne fournira pas de meilleure distance que le plan le contenant. Dans ce cas, vous retournez le contrôle à la boucle triangle. Si la distance est inférieure à ShortestDistance, il est possible que vous ayez un point plus proche, si ce point se trouve à l’intérieur du triangle. Vous devez effectuer des calculs « matériels » (bien qu’il ne s’agisse pas de l’algèbre linéaire) pour le déterminer. Si les deux autres sommets du triangle sont Vertex2 et vertex3, forment les vecteurs de base firstBasisVector et secondBasisVector.

firstBasisVector = Vertex2-vertex1

secondBasisVector = vertex3-vertex1

Utilisez le système linéaire suivant d’équations pour résoudre les problèmes que vous et v.

firstBasisVector \* queryVector = (firstBasisVector \* firstBasisVector) u + (firstBasisVector \* secondBasisVector) v

secondBasisVector \* queryVector = (secondBasisVector \* firstBasisVector) u + (secondBasisVector \* secondBasisVector) v

et les conditions pour que le point projeté se situe à l’intérieur du triangle sont les suivantes :

0 ≤ u ≤ 1, 0 ≤ v ≤ 1 et u + v ≤ 1

Après ce calcul, s’il est déterminé que le point projeté se trouve dans le triangle, vous avez trouvé un nouveau point le plus proche ; la distance que vous avez calculée au début correspond à la nouvelle distance la plus petite. Dans ce cas, mettez à jour les variables ShortestDistance et ClosestPoint. Si le point projeté se trouve en dehors du triangle, vous pouvez trouver un point plus proche sur l’un de ses bords. Vous pouvez donc appeler la routine ProcessEdge sur chacun des trois bords.

![Diagramme qui montre le déroulement des routines ProcessEdge et ProcessVertex.](images/gmmp-image124.jpg)

**Figure 34** : routines ProcessEdge et ProcessVertex

La routine ProcessEdge implémente la stratégie I, illustrée dans la figure 34. ProcessEdge commence par vérifier si le bord a été traité avant. Dans ce cas, aucune autre action n’est effectuée. Si ce n’est pas le cas, il calcule la projection orthogonale du point de requête sur la ligne infinie contenant le bord. L’algèbre linéaire impliquée dans le calcul est semblable aux équations triangulaires précédentes. Toutefois, le calcul est plus simple, mais il n’est pas décrit ici. Si le point projeté se trouve dans le bord, vous trouvez la distance entre le point projeté et le point de requête. Si cette distance est inférieure à ShortestDistance, vous avez trouvé un nouveau point le plus proche. Mettez à jour à la fois ShortestDistance et ClosestPoint. Si le point projeté se trouve en dehors du bord, appelez ProcessVertex sur les deux points de terminaison. Avant de retourner le contrôle, mettez à jour l’historique du bord afin que ce bord soit marqué comme « traité ».

Enfin, vous donnez une description de ProcessVertex. La routine ProjectVertex implémente également la stratégie I et gère une table d’historique des vertex. Comme illustré à la figure 34, il vérifie d’abord si le Vertex a été traité avant. Dans ce cas, aucune autre action n’est effectuée. Si ce n’est pas le cas, elle calcule la distance entre le sommet et le point de requête. Si la distance est inférieure à ShortestDistance, mettez à jour ShortestDistance et ClosestPoint. À la fin, il met à jour l’historique des vertex afin que ce vertex soit marqué comme « traité ».

Lorsque la boucle de contrôle externe a épuisé tous les triangles ou a quitté avant que le seuil de différence de couleur soit atteint, la variable ClosestPoint est accédée. Il s’agit du résultat de MinDEMap. L’appelant peut également récupérer ShortestDistance s’il s’intéresse à la distance de la couleur mappée par rapport à la couleur de la requête.

### <a name="hue-smoothing"></a>Lissage des teintes

![Diagramme qui affiche deux vues principales du lissage des teintes, l’original sur le dessus et la teinte lissé en bas.](images/gmmp-image125.png)

**Figure 35** : lissage des teintes

Un problème survient avec les opérations dont la teinte est restreinte ; autrement dit, l’opération prend uniquement en compte les variables dans un plan de teinte. La figure 35 montre un exemple de gamme de couleurs « discontinues » dans les teintes bleues. Dans cette plage de teinte, pour certains angles de teinte, la limite de gamme est tangentielle au plan de teinte. En effet, cela entraîne une modification de la structure topologique des tranches de teinte. Dans l’exemple illustré, lorsque le plan de teinte passe au-dessus de cette plage de teinte, un « îlot » émerge et des sous-fusions. Cette modification de la topologie entraîne l’interruption des opérations spécifiques de la teinte. Par exemple, le sommet à la teinte fixe change brusquement lorsque l’angle de teinte change dans cette plage.

Il y a une raison de la science des couleurs pour laquelle il est souhaitable de conserver la teinte dans certaines opérations. Pour résoudre le problème précédent, les triangles de limite de gamme d’origine doivent être « teint lissée ». En règle générale, un lissage de teinte d’un ensemble de triangles de limite de gamme est un ensemble de triangles de sorte que (a) représente la limite d’une nouvelle « gamme », qui peut ne pas correspondre à la gamme réelle des appareils, et qui contient la gamme définie par l’ensemble d’origine des triangles. et (b) les triangles du nouvel ensemble sont délimités du fait qu’ils sont parallèles aux plans de teinte.

Un moyen pratique d’obtenir un ensemble de triangles lissés, est de prendre la forme convexe des sommets d’origine. Comme illustré à la figure 35, les tranches de teinte de la coque convexe varient harmonieusement dans la plage de teinte problématique sans modification soudaine de la topologie.

### <a name="setting-primaries-and-secondaries-in-the-gamut-boundary-description"></a>Définition des serveurs primaires et secondaires dans la description des limites de la gamme de couleurs

Certaines méthodes de mappage de gamme de couleurs, telles que HueMap, dépendent de l’emplacement des serveurs principaux et secondaires de l’appareil. Pour les appareils additives, les disques primaires sont rouge, vert et bleu (R, G et B); et les secondaires sont cyan, magenta et jaune (C, M et Y). Pour les appareils de soustraction, les disques primaires sont C, M et Y ; et les secondaires sont R, G et B. Le GBD effectue le suivi de ces six valeurs, plus le blanc et le noir (W et K), dans un tableau de valeurs de couleur Jab. Ces valeurs sont définies dans la description de la limite de la gamme quand elle est créée. Pour les périphériques de sortie, les disques primaires peuvent être déterminés en exécutant des combinaisons de valeurs de contrôle d’appareil via le modèle d’appareil. Pour les appareils de capture, cette approche n’est pas adaptée à la création du GBD de référence, car il est presque impossible de capturer une image qui génère une valeur d’appareil pure entièrement saturée, telle que (0,0, 0,0, 1,0). Les profils d’appareil WCS contiennent les index des primaires dans la cible de capture. Étant donné que ces valeurs ne sont pas contenues dans un profil ICC, utilisez des valeurs mesurées à partir d’une cible de scanneur classique après la conversion en Jab, par rapport aux conditions d’affichage ICC.

### <a name="setting-the-neutral-axis-in-the-gamut-boundary-description"></a>Définition de l’axe neutre dans la description des limites de la gamme de couleurs

Le HueMap et les méthodes de mappage de gammes hachées relatives utilisent l’axe neutre de l’appareil pour le redressement. Pour les périphériques de sortie de ligne de base, l’axe neutre peut être déterminé en exécutant des valeurs neutres de périphérique (R = G = B ou C = M = Y) par le biais de la méthode DeviceToColorimetric, puis par le biais de la méthode ColorimetricToAppearance de l’objet CIECAM02. Toutefois, les périphériques de capture ne retournent pas toujours une valeur de périphérique neutre lorsqu’ils sont présentés avec un échantillon neutre. Cela est particulièrement vrai lorsque l’éclairage ambiant n’est pas parfaitement neutre. Les profils de périphérique WCS contiennent les index des échantillons neutres dans la cible. Utilisez ces exemples pour définir l’axe neutre. Étant donné que ces informations ne sont pas disponibles pour les profils ICC, vous devez utiliser la même méthode que celle utilisée pour les périphériques de sortie. exécutez des exemples indépendants de l’appareil par le biais de la méthode DeviceToColorimetric, puis associez les valeurs d’entrée et les résultats colorimétriques.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de base de la gestion des couleurs](basic-color-management-concepts.md)
</dt> <dt>

[Schémas et algorithmes du système de couleurs Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 




