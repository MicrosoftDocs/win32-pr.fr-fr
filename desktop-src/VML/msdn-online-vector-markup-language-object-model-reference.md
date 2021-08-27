---
title: Référence du modèle objet VML
description: cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 092190bc12a4c2cc8c15817529a16524f17bdef1
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624305"
---
# <a name="vml-object-model-reference"></a>Référence du modèle objet VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Dans cette rubrique :

-   [Introduction](#introduction)
-   [Exemple](#example)
-   [Configuration de VML](#setting-up-vml)
-   [Informations de référence sur VML OM](#vml-om-reference)
    -   [Élément Shape](#shape-element)
-   [Sous-éléments de l’élément Shape](#subelements-of-the-shape-element)
    -   [Élément d’arrière-plan](#background-element)
    -   [Élément extrusion](#extrusion-element)
    -   [Fill, élément](#fill-element)
    -   [élément Group](#group-element)
    -   [Élément ImageData](#imagedata-element)
    -   [Élément Path](#path-element)
    -   [Élément Shadow](#shadow-element)
    -   [Élément Skew](#skew-element)
    -   [Stroke, élément](#stroke-element)
    -   [Élément TextPath](#textpath-element)
-   [Types de données utilisés dans le modèle d’objet VML](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a>Introduction

[Langage VML (VML)](https://www.w3.org/TR/NOTE-datetime.html) est un langage textuel qui utilise [XML](https://www.w3.org/TR/REC-xml.mdl) pour étendre le code HTML en vue d’afficher des informations graphiques vectorielles. Le Document Object Model VML (DOM) définit une interface de programmation pour la manipulation des éléments de document. Cela permet à l’utilisateur de créer et de modifier dynamiquement des graphiques vectoriels via une interface de plateforme et une interface indépendante du langage. Le DOM VML est conforme à la spécification [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) .

VML utilise l’élément [Shape](#shape-element) comme bloc de construction de base pour les images vectorielles. Une fois qu’une forme est créée, vous pouvez modifier la forme par le biais des attributs ou des sous-éléments attachés. Par exemple, pour modifier la couleur d’une forme, assignez une valeur de couleur à l’attribut **FillColor** .


```HTML
myshape.fillcolor = "red"
```



Plusieurs des attributs d’une forme sont également des sous- [éléments](/windows) et ont leurs propres attributs, y compris les éléments suivants :

-   [Contexte](#background-element)
-   [Extrusion](#extrusion-element)
-   [Remplir](#fill-element)
-   [Groupe](#group-element)
-   [Imagedata](#imagedata-element)
-   [Chemin d’accès](#path-element)
-   [Shadow](#shadow-element)
-   [Appliquez](#skew-element)
-   [Stroke](#stroke-element)
-   [TextPath](#textpath-element)

VML OM utilise plusieurs [types de données](/windows) pour définir des paramètres. Les types de données précédés de « VG » sont des énumérations et celles précédées de « IVg » sont des objets. Cliquez ici pour obtenir une liste. Les types de données mineurs sont répertoriés avec des paramètres spécifiques.

## <a name="example"></a>Exemple

Le code VBScript suivant montre comment créer une forme simple :


```HTML
        Set MyRect = Document.CreateElement("v:Rect")
        Set R = MyDiv.AppendChild(MyRect)
        R.Style.Position = "absolute"
        R.Style.Width = 20
        R.Style.Height = 20
        R.Style.Top = 50
        R.Style.Left = 50
        R.FillColor = "red"
```



Dans l’exemple ci-dessus, une forme est créée à l’aide de la méthode Document Object Model **createElement**. La forme est une forme Rect prédéfinie VML. Même si l’objet existe, il ne peut pas faire partie du document tant qu’il n’est pas attaché au document. À l’aide de la méthode **AppendChild** , le Rect est devenu l’enfant d’un élément **div** appelé MyDiv. Quelques attributs de style minimum (**position**, **largeur**, **hauteur**, **haut**, **gauche**) sont définis pour attribuer une taille spécifique à la forme. Enfin, une couleur est assignée avec l’attribut **FillColor** . Notez que vous pouvez utiliser n’importe quel langage de script ou n’importe quel langage pouvant fonctionner avec des interfaces Document Object Model.

## <a name="setting-up-vml"></a>Configuration de VML

L’une des implémentations de VML est par le biais de Microsoft Internet Explorer 5,0 ou version ultérieure. Pour configurer correctement l’objet de rendu dans une page Web, les ajouts suivants doivent être effectués :

1.  Le schéma doit être configuré dans le <HTML> comme suit :
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  Le comportement de rendu doit faire partie du style du document :
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

L’exemple suivant montre un exemple de page Web HTML configuré correctement pour VML montrant la création dynamique d’une forme.


```HTML
<HTML xmlns:v="urn:schemas-microsoft-com:vml">
<HEAD>
<STYLE>
v\:* { behavior: url(#default#VML); display:inline-block}
</STYLE>
<TITLE>VML Sample</TITLE>
</HEAD>
<BODY>
<DIV id="MyDiv"></DIV>
<SCRIPT ID="MYSCRIPT" LANGUAGE="VBScript">
<!--
Set MyRect = Document.CreateElement("v:Rect")
Set R = MyDiv.AppendChild(MyRect)
R.Style.Position = "absolute"
R.Style.Width = 20
R.Style.Height = 20
R.Style.Top = 50
R.Style.Left = 50
R.FillColor = "red"
-->
</SCRIPT>
</BODY>
</HTML>
```



notez que dans les versions bêta, une balise d’objet ActiveX et un style de comportement différent était requis.

## <a name="vml-om-reference"></a>Informations de référence sur VML OM

Cette référence définit l’élément de [forme](#shape-element) , les sous- [éléments](/windows)et les [types de données](/windows) utilisés par le modèle objet de Vml.

### <a name="shape-element"></a>Élément Shape

Les formes sont les blocs de construction des images graphiques définies par langage VML (VML). La forme est l’élément de niveau supérieur et plusieurs sous-éléments permettent de définir la nature de chaque forme.

VML fournit des formes prédéfinies :

**Attributs de forme**

-   **Arc**
-   **Apprendre**
-   **Ligne**
-   **Polyligne**
-   **Rect**
-   **RoundRect**



|   Sous-élément           |    Description                                                                                                                                                                                                                                                                                                                                                                              |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ajustement          | [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md). Liste délimitée par des virgules de nombres qui correspondent aux paramètres des formules de repère qui définissent le chemin d’accès de la forme. Les valeurs peuvent être omises pour permettre l’utilisation des valeurs par défaut. Il peut y avoir jusqu’à 8 valeurs d’ajustement.                                                                                                   |
| Alt          | Chaîne. Texte de remplacement associé à Shape. Utilisé pour l’exploration non graphique.                                                                                                                                                                                                                                                                                                 |
| Bouton       | [VgTriState](msdn-online-vml-vgtristate.md). Affiche le comportement du bouton sur clic.                                                                                                                                                                                                                                                                                                 |
| BWMode       | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Détermine le mode de rendu de la forme en noir et blanc dans les applications, ou lorsqu’elle est imprimée sur des imprimantes noir et blanc. Les valeurs sont les suivantes : **couleur**, **auto**, **nuances de gris**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **noir**, **blanc**, **dédessiné**. Valeur par défaut : **auto**. |
| BWNormal     | VgBlackWhiteMode. Quand BWMode est auto, cette propriété est consultée pour savoir comment afficher la forme en noir et blanc normal. Les valeurs sont les suivantes : **couleur**, **auto**, **nuances de gris**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **noir**, **blanc**, **dédessiné**. Valeur par défaut : **auto**.                                                |
| BWPure       | VgBlackWhiteMode. Quand BWMode est auto, cette propriété est consultée pour savoir comment afficher la forme dans les e/s pures. Les valeurs sont les suivantes : **couleur**, **auto**, **nuances de gris**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **noir**, **blanc**, **dédessiné**. Valeur par défaut : **auto**.                                                              |
| ChildShapes  | IVgGroupShapes. Collection d’autres formes de ce groupe. Cette collection prend en charge les méthodes de longueur et d’élément standard.                                                                                                                                                                                                                                                       |
| Chromakey    | [IVgColor](msdn-online-vml-ivgcolor.md). Valeur de couleur qui est transparente et qui affiche tout ce qui se trouve derrière la forme.                                                                                                                                                                                                                                                             |
| Control1     | [Vector2d](msdn-online-vml-ivgvector2d-data-type.md). Point de contrôle pour la courbe.                                                                                                                                                                                                                                                                                                  |
| Control2     | [Vector2d](msdn-online-vml-ivgvector2d-data-type.md). Point de contrôle pour la courbe.                                                                                                                                                                                                                                                                                                  |
| CoordOrigin  | [Vector2d](msdn-online-vml-ivgvector2d-data-type.md) Coordonnées situées dans le coin supérieur gauche du rectangle de conteneur. Plage comprise entre 0 et l’infini.                                                                                                                                                                                                                               |
| CoordSize    | [Vector2d](msdn-online-vml-ivgvector2d-data-type.md). Largeur et hauteur de l’espace de coordonnées à l’intérieur du rectangle de référence de cette forme. S’il n’est pas spécifié, il est identique à la largeur et à la hauteur du rectangle. Plage comprise entre 0 et l’infini. Valeur par défaut : « 1000, 1000 ».                                                                                               |
| EndAngle     | [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md). Angle de fin de la forme.                                                                                                                                                                                                                                                                                          |
| Extrusion    | IVgExtrusion. Spécifie la valeur de l’objet d’extrusion pour cette forme. Pour plus d’informations, consultez l’élément [extrusion](msdn-online-vml-extrusion-element.md) .                                                                                                                                                                                                                               |
| Remplir         | VgFillFormat. Spécifie la valeur de remplissage de cette forme. Pour plus d’informations, consultez l’élément [Fill](msdn-online-vml-fill-element.md) .                                                                                                                                                                                                                                                |
| FillColor    | [IVgColor](msdn-online-vml-ivgcolor.md). Couleur principale du pinceau à utiliser pour remplir le tracé de cette forme.                                                                                                                                                                                                                                                                  |
| Spécifié       | [VgTriState](msdn-online-vml-vgtristate.md). Si la valeur est true, le chemin d’accès qui définit la forme est rempli. Par défaut, il est rempli à l’aide d’une couleur unie, sauf s’il existe un sous-élément Fill qui spécifie des propriétés de remplissage plus complexes. Si la valeur est false, le remplissage est transparent.                                                                                                           |
| Livre         | VgFlipOrientation. Les valeurs sont les suivantes : X XY YX                                                                                                                                                                                                                                                                                                                                         |
| ForceDash    | [VgTriState](msdn-online-vml-vgtristate.md). Indique qu’un contour en pointillés doit être rendu lorsqu’il n’y a aucune ligne et aucun remplissage pour une forme. Ce comportement est généralement utile pour rendre les formes invisibles visibles dans la modification des applications afin qu’elles puissent être sélectionnées et exploitées, par exemple dans une image interactive.                                                                 |
| Formules     | IVgFormulas. Tableau de formules qui définit une forme.                                                                                                                                                                                                                                                                                                                          |
| Du         | [Vector2d](msdn-online-vml-ivgvector2d-data-type.md). Point de départ de la ligne.                                                                                                                                                                                                                                                                                                   |
| HRef         | [Chaîne](#data-types-used-in-the-vml-object-model). URL à laquelle accéder si l’utilisateur clique sur cette forme.                                                                                                                                                                                                                                                                                 |
| ImageData    | IVgImageData. Informations d’image si la forme est une image. Pour plus d’informations, consultez l’élément ImageData.                                                                                                                                                                                                                                                                       |
| OnEd         | [VgTriState](msdn-online-vml-vgtristate.md). Masque tous les descripteurs à l’exception des poignées en haut à gauche et en bas à droite, comme dans les poignées pour un segment de ligne droite.                                                                                                                                                                                                                             |
| Opacity      | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Opacité de la forme entière. Nombre compris entre 0,0 et 1,0.                                                                                                                                                                                                                                                           |
| Chemin d’accès         | IVgPath. Chaîne contenant les commandes qui définissent le chemin d’accès.                                                                                                                                                                                                                                                                                                                  |
| Points       | [IVgPoints](msdn-online-vml-ivgpoints-data-type.md). Collection de points définissant une forme.                                                                                                                                                                                                                                                                                   |
| Imprimer        | [VgTriState](msdn-online-vml-vgtristate.md). Si la valeur est true, cette forme est destinée à être imprimée.                                                                                                                                                                                                                                                                                        |
| Rotation     | [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md). Définit la rotation de la forme. La valeur est propagée au style de forme.                                                                                                                                                                                                                                              |
| Scale        | [Vector2d](msdn-online-vml-ivgvector2d-data-type.md). Échelle de la forme.                                                                                                                                                                                                                                                                                                           |
| Shadow       | IVgShadow. Spécifie l’ombre de cette forme. Pour plus d’informations, consultez l’élément [Shadow](msdn-online-vml-shadow-element.md) .                                                                                                                                                                                                                                                        |
| Arborescence          | Réservé.                                                                                                                                                                                                                                                                                                                                                                        |
| StartAngle   | [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md). Angle de début de la forme.                                                                                                                                                                                                                                                                                        |
| Trait       | VgStrokeFormat. Pour plus d’informations, consultez élément Stroke.                                                                                                                                                                                                                                                                                                                                  |
| StrokeColor  | [IVgColor](msdn-online-vml-ivgcolor.md). Couleur principale du pinceau à utiliser pour rayer le tracé de cette forme.                                                                                                                                                                                                                                                                |
| Rayé      | [VgTriState](msdn-online-vml-vgtristate.md). Si la valeur est true, le chemin d’accès qui définit la forme est rayé.                                                                                                                                                                                                                                                                              |
| StrokeWeight | [VGLength](msdn-online-vml-vglength.md). Largeur du pinceau à utiliser pour rayer le tracé. Les plages sont comprises entre 0 et 1584.                                                                                                                                                                                                                                                           |
| TextPath     | IVgTextPath. Spécifie l’objet TextPath de la forme. Pour plus d’informations, consultez l’élément [TextPath](msdn-online-vml-textpath-element.md) .                                                                                                                                                                                                                                  |
| À           | [Vector2d](msdn-online-vml-ivgvector2d-data-type.md). Point de terminaison de la ligne.                                                                                                                                                                                                                                                                                                        |
| Type         | Chaîne. Type de forme.                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a>Sous-éléments de l’élément Shape

Les sous-éléments suivants font partie du modèle d’objet VML.

-   [Contexte](#background-element)
-   [Extrusion](#extrusion-element)
-   [Remplir](#fill-element)
-   [Groupe](#group-element)
-   [Imagedata](#imagedata-element)
-   [Chemin d’accès](#path-element)
-   [Shadow](#shadow-element)
-   [Appliquez](#skew-element)
-   [Stroke](#stroke-element)
-   [TextPath](#textpath-element)

### <a name="background-element"></a>Élément d’arrière-plan

Décrit le remplissage de l’arrière-plan d’une page à l’aide des remplissages VML.


|   Attribut        |   Description                                                                                                                                                                                      |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BWMode    | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Détermine la façon dont la forme s’affiche dans une vue en noir et blanc dans des applications ou à l’impression.                                     |
| BWNormal  | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Quand BWMode est auto, cette propriété est consultée pour savoir comment afficher la forme en noir et blanc normal.                        |
| BWPure    | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Quand BWMode est auto, cette propriété est consultée pour savoir comment afficher la forme en noir et blanc pur.                          |
| Remplir      | VgFillFormat. Spécifie le remplissage de cette forme. Pour plus d’informations, consultez l’élément [Fill](msdn-online-vml-fill-element.md) .                                                             |
| FillColor | [IVgColor](msdn-online-vml-ivgcolor.md). Couleur principale du pinceau à utiliser pour remplir le tracé de cette forme. Doublon de la valeur de couleur dans l’élément Fill. La valeur par défaut est blanc. |



 

### <a name="extrusion-element"></a>Élément extrusion

Décrit une extrusion 3D de la forme.

**Attributs**



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>AutoRotationCenter</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Si la valeur est true, le centre de rotation du groupe d’objets 3D (en fait, il n’y a qu’un seul objet dans le groupe) est déterminé automatiquement comme étant le centre du groupe ; dans le cas contraire, il est déterminé par les paramètres RotationCenter, qui sont une fraction de la forme avec 0, 0, le centre.</td>
</tr>
<tr class="even">
<td>Profondeur</td>
<td><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>. Quantité d’extrusion vers l’arrière. Est compris entre 0 et 32767.</td>
</tr>
<tr class="odd">
<td>Luminosité</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Luminosité globale de la scène. La valeur par défaut est &quot; 20 000 &quot; .</td>
</tr>
<tr class="even">
<td>Couleur</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Couleur de l’extrusion. Utilisé uniquement si ColorMode est personnalisé. Dans le cas contraire, définit automatiquement la couleur de l’effet d’extrusion sur la même valeur que FillColor.</td>
</tr>
<tr class="odd">
<td>ColorMode</td>
<td>Vg3DColorMode. Les valeurs sont les suivantes :
<ul>
<li>Auto (par défaut)</li>
<li>Custom</li>
</ul></td>
</tr>
<tr class="even">
<td>Diffusion</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Rapport entre l’incident et la lumière diffuse. Les valeurs inférieures à 1,0 sont normales, mais les valeurs supérieures à un peuvent générer des effets intéressants.</td>
</tr>
<tr class="odd">
<td>Edge</td>
<td><a href="msdn-online-vml-vglength.md">VgLength</a>. Définit la taille d’un bord biseauté arrondi simulé. Est compris entre 0 et 32767 dans la valeur de type virgule flottante. La valeur par défaut est &quot; 1PT &quot; .</td>
</tr>
<tr class="even">
<td>Facette</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Définit la facette de la scène. La valeur par défaut est &quot; 30 000 &quot; .</td>
</tr>
<tr class="odd">
<td>ForeDepth</td>
<td><a href="msdn-online-vml-vglength.md">VgLength</a>. Quantité d’extrusion vers l’avant. Est compris entre 0 et 32767.</td>
</tr>
<tr class="even">
<td>LightFace</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Determimes si la face avant de l’objet répond aux modifications de l’éclairage 3D, par exemple quand un objet pivote.</td>
</tr>
<tr class="odd">
<td>LightHarsh</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Éclairage sévère de la source de lumière principale. La valeur par défaut est FALSE.</td>
</tr>
<tr class="even">
<td>LightHarsh2</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Éclairage sévère de la source de lumière secondaire. La valeur par défaut est FALSE.</td>
</tr>
<tr class="odd">
<td>LightLevel</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>. Intensité de la source de lumière principale. La valeur par défaut est &quot; 38000 &quot; .</td>
</tr>
<tr class="even">
<td>LightLevel2</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>. Intensité de la source de lumière secondaire. La valeur par défaut est &quot; 38000 &quot; .</td>
</tr>
<tr class="odd">
<td>LightPosition</td>
<td>Vector3D. Position de la source de lumière principale. La valeur par défaut est &quot; 50000, 0, 10000 &quot; .</td>
</tr>
<tr class="even">
<td>LightPosition2</td>
<td>Vector3D. Position de la source de lumière secondaire. La valeur par défaut est &quot; -50000, 0, 10000 &quot; .</td>
</tr>
<tr class="odd">
<td>LockRotationCenter</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. &quot;Lockrotationcenter &quot; signifie que la rotation du groupe est définie par l’angle de rotation [1] degrés autour de l’axe y sur la page suivie de l’angle de rotation [0] degrés sur l’axe x. Quand LockRotationCenter a la valeur false, la rotation est définie en tant que degrés d’orientation-angle sur le vecteur défini par l’orientation. Par exemple, lockrotationcenter = false OrientationAngle = 45 orientation = (0, 1, 0) équivaut à lockrotationcenter = true RotationAngle = (0, 45).</td>
</tr>
<tr class="even">
<td>Métallique</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Fait en sorte que la lumière réfléchie modèle éclairé soit la couleur matérielle au lieu de la couleur de la source de lumière, ce qui rend l’objet plus métallique.</td>
</tr>
<tr class="odd">
<td>Activé</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Active et désactive l’affichage de l’effet de l’extrusion.</td>
</tr>
<tr class="even">
<td>Orientation</td>
<td>Vector3D. Orientation de l’appareil photo.</td>
</tr>
<tr class="odd">
<td>OrientationAngle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>. Angle entre l’orientation de l’appareil photo et le plan XY.</td>
</tr>
<tr class="even">
<td>Verticale</td>
<td>Vg3DExtrudePlane. Autorise l’extrusion des plans orthogonals au plan de l’écran. Requiert la spécification de ForeDepth et de l’effet de profondeur pour les unités de dessin au lieu de EMU. Les valeurs sont les suivantes :
<ul>
<li>XY</li>
<li>ZX</li>
<li>YZ</li>
</ul></td>
</tr>
<tr class="odd">
<td>Rendu</td>
<td>Vg3DRenderMode. Les valeurs sont les suivantes :
<ul>
<li>Unie (par défaut)</li>
<li>WireFrame</li>
<li>BoundingCube</li>
</ul></td>
</tr>
<tr class="even">
<td>RotationAngle</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>. AngleX, AngleY ou AngleZ est contrôlé par l’attribut ShapeRotation.</td>
</tr>
<tr class="odd">
<td>RotationCenter</td>
<td>Vector3D. Centre de rotation.</td>
</tr>
<tr class="even">
<td>Brillance</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Détermine la façon dont la réflexion spéculaire concentrée ou répartie est. Une valeur élevée est comprendra de 8 à 10 et se traduirait par un miroir, et une valeur basse serait de 2 à 3 et sequinedrait des vêtements de ré. Les valeurs 3 à 7 sont recommandées. Des valeurs élevées reflètent les sources de lumière de repérage.</td>
</tr>
<tr class="odd">
<td>SkewAmt</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>. Si le type est Parallel, l’attribut détermine la quantité d’inclinaison. Est compris entre 0 et 100.</td>
</tr>
<tr class="even">
<td>SkewAngle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>. Si le type est Parallel, l’attribut détermine le degré d’inclinaison. La valeur par défaut est &quot; -45 &quot; .</td>
</tr>
<tr class="odd">
<td>Specularity</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Rapport entre l’incident et le modèle éclairé de lumière réfléchie. Les valeurs inférieures à 1,0 sont normales, mais les valeurs supérieures à un peuvent générer des effets intéressants.</td>
</tr>
<tr class="even">
<td>Type</td>
<td>VgExtrusionType. Les valeurs sont les suivantes :
<ul>
<li>Parallèle (par défaut)</li>
<li>Perspective</li>
</ul></td>
</tr>
<tr class="odd">
<td>Point</td>
<td>Vector3D. Point à partir duquel la scène est affichée.</td>
</tr>
<tr class="even">
<td>ViewpointOrigin</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>. Peut avoir des valeurs comprises entre 0,5 et-0,5 pour positionner l’origine du point de vue dans le cadre englobant de la forme.</td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a>Fill, élément

Décrit comment remplir un tracé pour obtenir des remplissages plus complexes qu’une couleur unie.

**Attributs**



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>AlignShape</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Alignez l’image avec la forme. Si la valeur est false, l’image est alignée avec la fenêtre.</td>
</tr>
<tr class="even">
<td>Angle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>. Angle de rotation du dégradé. 0 degré est le long de l’axe horizontal de gauche à droite.</td>
</tr>
<tr class="odd">
<td>Aspect</td>
<td><strong>VgAspectType</strong>. L’attribut ImageSize est ajusté pour conserver l’aspect de l’image. Ces valeurs comprennent :
<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ignorer</td>
<td>Ignorer les problèmes d’aspect.</td>
</tr>
<tr class="even">
<td>Au moins</td>
<td>L’image est au moins aussi grande que la taille de l’image.</td>
</tr>
<tr class="odd">
<td>AtMost</td>
<td>L’image n’est pas plus grande que la taille de l’image.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Couleur</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> Couleur de remplissage principale. Identique à l’attribut FillColor dans Shape.</td>
</tr>
<tr class="odd">
<td>Couleur2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Couleur secondaire d’un remplissage lorsque le type d’image est Pattern ou un remplissage dégradé.</td>
</tr>
<tr class="even">
<td>Couleurs</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>. Les couleurs intermédiaires dans le dégradé et leurs positions relatives le long du dégradé, par exemple &quot; 30% de rouge, 70% bleu, 90% vert &quot; . La couleur primaire (attribut Color dans Shape) est 0% et la couleur secondaire (attribut Color2) est 100%.</td>
</tr>
<tr class="odd">
<td>Priorité</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>. Point focal pour le remplissage dégradé linéaire. Les valeurs sont comprises entre-100 et + 100.</td>
</tr>
<tr class="even">
<td>FocusPosition</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>. Position du rectangle le plus profond pour les dégradés radiaux. Le vecteur est une fraction (0,0-1,0) de la largeur et de la hauteur de la forme.</td>
</tr>
<tr class="odd">
<td>FocusSize</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a> Taille du rectangle le plus profond pour les dégradés radiaux. Le vecteur est une fraction (0,0 à 1,0) de la largeur et de la hauteur de la forme.</td>
</tr>
<tr class="even">
<td>Méthode</td>
<td>VgSigmaType. Ces valeurs comprennent :
<ul>
<li>Aucune</li>
<li>Linéaire</li>
<li>Sigma</li>
<li>Quelconque</li>
</ul>
<p>La valeur par défaut est Sigma.</p></td>
</tr>
<tr class="odd">
<td>Activé</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Active l’affichage du remplissage. Identique à l’attribut Fill dans Shape.</td>
</tr>
<tr class="even">
<td>Opacity</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Opacité du remplissage.</td>
</tr>
<tr class="odd">
<td>Opacity2</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Opacité secondaire pour les dégradés.</td>
</tr>
<tr class="even">
<td>Origine</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>. Point relatif au coin supérieur gauche de l’image qui est traité comme l’origine de l’image. La valeur par défaut est le centre de l’image. Le vecteur est une fraction (de 0,0 à 1,0) de la largeur et de la hauteur de l’image.</td>
</tr>
<tr class="odd">
<td>Position</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>. Point dans le rectangle de référence de la forme pour positionner l’origine de l’image. La valeur par défaut est le centre du rectangle de conteneur. Le vecteur est une fraction (0,0-1,0) de la largeur et de la hauteur de l’image.</td>
</tr>
<tr class="even">
<td>Taille</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>. Taille de l’image. La valeur par défaut est la taille en pixels de l’image. Peut être spécifié en coordonnées absolues ou en pourcentage.</td>
</tr>
<tr class="odd">
<td>Source</td>
<td><a href="#data-types-used-in-the-vml-object-model">Chaîne</a>. URL vers une image à charger pour les remplissages d’image et de motif. Cet attribut doit toujours être présent et pointer vers des données d’image valides pour qu’une image s’affiche.</td>
</tr>
<tr class="even">
<td>Type</td>
<td>VgFillType. qui peut être l’un des suivants :
<ul>
<li>Arrière-plan</li>
<li>Frame</li>
<li>Dégradé</li>
<li>GradientCenter</li>
<li>GradientRadial</li>
<li>GradientTitle</li>
<li>GradientUnscaled</li>
<li>Modèle</li>
<li>Unie</li>
<li>Tile</li>
</ul>
Les mosaïques, les modèles et les frames requièrent que les attributs d’image soient fournis. Les attributs gradient et GradientRadial requièrent que les attributs de dégradé soient fournis.</td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a>élément Group

Un groupe est une collection de formes individuelles qui peuvent être positionnées et transformées en une unité.



|   Attribut        |   Description                                                                                                                                                                                      |
|--------|----------------------------------------------------------------------------------------------|
| Élément   | [IVgShape](#data-types-used-in-the-vml-object-model). Élément spécifié dans le tableau de formes. |
| Longueur | [Integer](#data-types-used-in-the-vml-object-model). Nombre de formes dans ce groupe.         |



 

### <a name="imagedata-element"></a>Élément ImageData

Décrit une image à afficher en haut d’une forme.



|   Attribut        |   Description                                                                                                                                                                                      |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anticrénelage     | [VgTriState](msdn-online-vml-vgtristate.md). Affichez l’image dans deux couleurs uniquement (généralement en noir et blanc).                                                                                                                                                                                                                                                     |
| BlackLevel  | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Permet de définir le niveau de manière à ce que les noirs apparaissent comme des véritables noirs et que toutes les autres couleurs soient visibles en tant que nuances au-dessus du noir.                                                                                                                                                                        |
| Chromakey   | [IVgColor](msdn-online-vml-ivgcolor.md). Couleur transparente de l’image.                                                                                                                                                                                                                                                                                         |
| CropBottom  | [VgNumber](#data-types-used-in-the-vml-object-model). Distance de rognage à partir du bas de l’image exprimée sous la forme d’un pourcentage de la taille de l’image.                                                                                                                                                                                                                           |
| CropLeft    | [VgNumber](#data-types-used-in-the-vml-object-model). Distance de rognage à partir du bord gauche de l’image exprimée sous la forme d’une fraction de la taille de l’image (de 0,0 à 1,0). Toutefois, « out-recadrage » est pris en charge et, par conséquent, les valeurs inférieures à 0 et supérieures à 1 sont prises en charge ; par exemple,-5, 20 découpent les limites 25X la taille de l’image avec 4/5 d’un côté de l’image. |
| CropRight   | [VgNumber](#data-types-used-in-the-vml-object-model). Distance de rognage à partir de la droite de l’image exprimée sous la forme d’un pourcentage de la taille de l’image.                                                                                                                                                                                                                            |
| CropTop     | [VgNumber](#data-types-used-in-the-vml-object-model). Distance de rognage à partir du haut de l’image exprimée sous la forme d’un pourcentage de la taille de l’image.                                                                                                                                                                                                                              |
| EmbossColor | [IVgColor](msdn-online-vml-ivgcolor.md). Il s’agit d’un pourcentage de la couleur de l’ombre pour créer un effet d’image en relief.                                                                                                                                                                                                                                 |
| Maîtrise        | [VgPositiveNumber](#data-types-used-in-the-vml-object-model). Ajuste l’intensité de toutes les couleurs. Définit essentiellement le degré de luminosité du blanc. Est compris entre 0 et 32767.                                                                                                                                                                                           |
| Gamma       | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Correction gamma. L’amélioration de l’image donne une image plus contrastée.                                                                                                                                                                                                                                           |
| Nuances de gris   | [VgTriState](msdn-online-vml-vgtristate.md). Affichez l’image en nuances de gris.                                                                                                                                                                                                                                                                              |
| Source         | [Chaîne](#data-types-used-in-the-vml-object-model). URL vers une image à charger pour les remplissages d’image et de motif. Cet attribut doit toujours être présent et pointer vers des données d’image valides pour qu’une image s’affiche.                                                                                                                                                           |



 

### <a name="path-element"></a>Élément Path

Définit le chemin d’accès qui compose la forme, à l’aide d’une chaîne qui contient un ensemble complet de commandes de « mouvement du stylet ».



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Limo</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>. Définit le point d’étirement de la forme ; par exemple, pour une forme Giraffe, le point Limo serait sur le cou. par conséquent, lorsque la forme est redimensionnée, le cou est étiré et le reste de la forme conserve ses dimensions.</td>
</tr>
<tr class="even">
<td>TextBoxRect</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>. Tableau contenant les rectangles qui définissent l’emplacement où le texte doit être placé.</td>
</tr>
<tr class="odd">
<td>V</td>
<td><a href="#data-types-used-in-the-vml-object-model">Chaîne</a>. Correspond à l’attribut v de la balise Path. Notez que le chemin d’accès peut correspondre à un attribut ou à un élément de chemin d’accès.</td>
</tr>
<tr class="even">
<td>Valeur</td>
<td><a href="#data-types-used-in-the-vml-object-model">Chaîne</a>. Représentation textuelle des commandes qui définissent le chemin d’accès. Les valeurs de coordonnée X ou y peuvent être une référence à une formule dans le formulaire &quot; @# &quot; où # est le nombre ordinal de la formule, par exemple, &quot; @2 &quot; . Cette chaîne d’attribut est constituée d’un ensemble complet de commandes, notamment les suivantes : <br/> 
<table>
<thead>
<tr class="header">
<th>Commande</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AE (angleellipseto)</td>
<td><strong>Centre</strong>(x, y) <strong>taille</strong>(w, h), angle de <strong>début</strong>, <strong>angle de fin</strong><br/> Dessinez un segment d’une ellipse. Une ligne droite est dessinée à partir du point actuel jusqu’au point de départ du segment.<br/></td>
</tr>
<tr class="even">
<td>Al (angleelipse)</td>
<td>Identique à AE, sauf qu’il existe un m implicite vers le point de départ du segment.</td>
</tr>
<tr class="odd">
<td>AR (ARC)</td>
<td>Identique à. Toutefois, un nouveau sous-tracé est démarré par un m implicite jusqu’au point de départ de l’arc.</td>
</tr>
<tr class="even">
<td>à (ArcTo)</td>
<td><strong>end</strong> <strong>gauche</strong>, <strong>haut</strong>, <strong>droite</strong>, <strong>bas</strong>, <strong>début</strong>(x, y) (x, y) <br/> Les quatre premières valeurs définissent le cadre englobant d’une ellipse. Les quatre derniers définissent deux vecteurs radials. Un segment de l’ellipse est dessiné qui commence à l’angle défini par le vecteur de démarrage RADIUS et se termine à l’angle défini par le vecteur de fin. Une ligne droite est dessinée à partir du point actuel jusqu’au début de l’arc. L’arc est toujours dessiné dans le sens inverse des aiguilles d’une passe. <br/></td>
</tr>
<tr class="odd">
<td>c (curveTo)</td>
<td><strong>Control1</strong>(x, y) <strong>Control2</strong>(x, y) <strong>à</strong>(x, y) <br/> Dessinez une courbe de Bézier cubique à partir du point actuel jusqu’à la coordonnée donnée par les deux derniers paramètres, les points de contrôle donnés par les quatre premiers paramètres. Le point actuel devient le point de terminaison de la courbe de Bézier.<br/></td>
</tr>
<tr class="even">
<td>e (fin)</td>
<td>Terminer l’ensemble de sous-chemins en cours. Un ensemble donné de sous-chemins (délimités par fin) est rempli à l’aide de eofill. Les ensembles de sous-tracés suivants sont remplis indépendamment et superposés sur ceux qui existent déjà.</td>
</tr>
<tr class="odd">
<td>l (LineTo)</td>
<td>x, y<br/> Dessine une ligne du point actuel jusqu’à la coordonnée x, y donnée, qui devient le nouveau point actuel. Des paires de coordonnées supplémentaires peuvent être spécifiées pour former une polyligne, par exemple &quot; l 10, 13, 45, 27, 89,-12 &quot; .<br/></td>
</tr>
<tr class="even">
<td>m (MoveTo)</td>
<td>x, y<br/> Démarre un nouveau sous-tracé à la coordonnée x, y donnée.<br/></td>
</tr>
<tr class="odd">
<td>NF (NoFill)</td>
<td>L’ensemble actuel de sous-chemins (délimité par fin) n’est pas rempli.</td>
</tr>
<tr class="even">
<td>NS (noStroke)</td>
<td>L’ensemble actuel de sous-chemins (délimité par fin) n’est pas rayé.</td>
</tr>
<tr class="odd">
<td>QB (quadraticbezier)</td>
<td>(<strong>ControlPoint</strong>(x, y)) *,<strong>end</strong>(x, y) <br/> Définit une ou plusieurs courbes de Bézier quadratiques au moyen de points de contrôle et d’un point de terminaison. Les points intermédiaires (sur la courbe) sont obtenus par interpolation entre des points de contrôle successifs similaires aux polices TrueType. Le sous-tracé n’a pas besoin d’être un début, auquel cas le sous-tracé est fermé et le dernier point définit le point de départ.<br/></td>
</tr>
<tr class="even">
<td>qx (ellipticalquadrantx)</td>
<td><strong>fin</strong>(x, y) <br/> Un quart d’ellipse est dessiné du point actuel au point de terminaison donné. Le segment elliptique est initialement tangent à une ligne parallèle à l’axe x ; autrement dit, le segment démarre horizontalement.<br/></td>
</tr>
<tr class="odd">
<td>qy (ellipticalquadranty)</td>
<td><strong>fin</strong>(x, y) <br/> Identique à qx, à ceci près que le segment elliptique est initialement tangent à une ligne parallèle à l’axe y ; autrement dit, le segment démarre verticalement.<br/></td>
</tr>
<tr class="even">
<td>r (rlineto)</td>
<td>x, y <br/> Dessinez une ligne du point actuel vers la coordonnée relative (CPX + x, cpy + y). Si des paires de coordonnées supplémentaires sont fournies, chaque nouveau point est calculé par rapport au dernier.<br/></td>
</tr>
<tr class="odd">
<td>t (rmoveto)</td>
<td>x, y<br/> Démarrez un nouveau sous-chemin d’accès aux coordonnées relatives (CPX + x, cpy + y) où CPX, cpy correspond à la position actuelle. <br/></td>
</tr>
<tr class="even">
<td>v (curveTo)</td>
<td><strong>Control1</strong>(x, y) <strong>Control2</strong>(x, y) <strong>à</strong> (x, y) <br/> Courbe de Bézier cubique utilisant les coordonnées données relatives au point actuel. Tous les points sont calculés par rapport au même point de départ.<br/></td>
</tr>
<tr class="odd">
<td>WA (clockwisearcto)</td>
<td>Identique à, mais l’arc est dessiné dans le sens des aiguilles d’une montre.</td>
</tr>
<tr class="even">
<td>WR (clockwisearc)</td>
<td>Identique à AR mais est dessiné dans le sens des aiguilles d’une montre.</td>
</tr>
<tr class="odd">
<td>x (fermer)</td>
<td>Fermer le sous-tracé en cours en dessinant une ligne droite à partir du point actuel sur le point MoveTo d’origine.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a>Élément Shadow

Décrit un effet d’ombrage sur une forme.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Couleur</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Couleur de l’ombre principale. La valeur par défaut est RVB (128128128)</td>
</tr>
<tr class="even">
<td>Couleur2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Couleur de la deuxième ombre, ou mise en surbrillance dans une ombre de relief ou d’empreinte. La valeur par défaut est RVB (203203203).</td>
</tr>
<tr class="odd">
<td>Matrice</td>
<td><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>. Matrice de transformation de perspective au format &quot; Sxx, SXY, syx, SYY, PX, py &quot; [s = Scale, p = perspective]. Les éléments s spécifient la façon dont l’ombre doit être mise à l’échelle par rapport à la forme, et les éléments p spécifient la façon dont l’ombre doit être faussée par rapport à la forme. Par exemple, la matrice suivante redimensionne la forme d’un facteur de 2 et l’incline par un facteur de 4 dans toutes les directions : <br/> &quot;2, 2, 2, 2, 4, 4&quot;<br/> Cette matrice est utilisée uniquement si le type de l’ombre est défini sur perspective.<br/></td>
</tr>
<tr class="even">
<td>Masquée</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. L’ombre peut être consultée si aucun remplissage n’est présent sur la forme. La valeur par défaut est FALSE.</td>
</tr>
<tr class="odd">
<td>Offset</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>. Quantité de décalage x, y à partir de l’emplacement de la forme. La valeur par défaut est &quot; 2pt, 2pt &quot; .</td>
</tr>
<tr class="even">
<td>Offset2</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>. Nombre de décalages x, y à partir de l’emplacement de la forme ?. Les valeurs sont soit une mesure absolue, soit une valeur fractionnaire de forme (-0,5 à + 0,5).</td>
</tr>
<tr class="odd">
<td>Activé</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Active ou désactive l’affichage de l’ombre.</td>
</tr>
<tr class="even">
<td>Opacity</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Opacité de l’effet d’ombre.</td>
</tr>
<tr class="odd">
<td>Origine</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a> Paire de valeurs fractionnaires de forme comprise entre-0,5 et + 0,5.</td>
</tr>
<tr class="even">
<td>Type</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>. Les valeurs sont les suivantes :
<ul>
<li>Unique (valeur par défaut)</li>
<li>Double</li>
<li>Perspective</li>
<li>ShapeRelative</li>
<li>DrawingRelative</li>
<li>Relief</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a>Élément Skew

Décrit un effet d’inclinaison de perspective sur une forme. L’inclinaison est appliquée aux données de graphique vectoriel, et non aux données d’image.



|   Attribut        |   Description                                                                                                                                                                                      |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Matrice | [IVgSkewMatrix](#data-types-used-in-the-vml-object-model). Matrice de transformation de perspective sous la forme «Sxx, SXY, syx, SYY, PX, py « \[ s = Scale, p = perspective \] . Si le décalage est en unités absolues alors que PX, py sont en unités UME ^-1 ; Sinon, il s’agit d’une fraction inverse de la taille de la forme. |
| Offset | [IvgSkewOffset](#data-types-used-in-the-vml-object-model). Quantité de décalage x, y à partir de l’emplacement de la forme. La valeur par défaut est « 2pt, 2pt ».                                                                                                                                                   |
| Activé     | [VgTriState](msdn-online-vml-vgtristate.md). Active ou désactive l’affichage de l’inclinaison.                                                                                                                                                                                             |
| Origine | [Vector2d](msdn-online-vml-ivgvector2d-data-type.md). Paire de valeurs fractionnaires de forme comprise entre-0,5 et + 0,5.                                                                                                                                                                     |



 

### <a name="stroke-element"></a>Stroke, élément

Décrit comment dessiner le tracé si un point au-delà d’une ligne pleine avec une couleur unie est souhaité.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Couleur</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Couleur de la ligne. Identique à l’attribut StrokeColor dans Shape mais le remplace.</td>
</tr>
<tr class="even">
<td>Couleur2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Couleur secondaire. Utilisé quand FillType est un modèle.</td>
</tr>
<tr class="odd">
<td>DashStyle</td>
<td><strong>VgLineDashStyle</strong>. Format du style des tirets. Peut être une valeur spécifique ou une séquence de nombres avec un modèle de tiret défini par l’utilisateur. Les valeurs sont les suivantes :
<ul>
<li>Unie (par défaut)</li>
<li>ShortDash</li>
<li>ShortDot</li>
<li>ShortDashDot</li>
<li>ShortDashDotDot</li>
<li>Points</li>
<li>Tiret</li>
<li>Tiret-point</li>
<li>LongDash</li>
<li>LongDashDot</li>
<li>LongDashDotDot</li>
</ul></td>
</tr>
<tr class="even">
<td>EndArrow</td>
<td><strong>VgArrowheadStyle</strong>. Pointe de flèche pour la fin de la ligne. Les valeurs sont les suivantes :
<ul>
<li>Aucun (par défaut)</li>
<li>Bloquer</li>
<li>Classique</li>
<li>Losange</li>
<li>Ovale</li>
<li>Ouvrir</li>
<li>Chevron</li>
<li>DoubleChevron</li>
</ul></td>
</tr>
<tr class="odd">
<td>EndArrowLength</td>
<td><strong>VgArrowHeadLength</strong>. Longueur de la flèche pour la fin de la ligne. Les valeurs sont les suivantes :
<ul>
<li>Court</li>
<li>Moyenne (par défaut)</li>
<li>Long</li>
</ul></td>
</tr>
<tr class="even">
<td>EndArrowWidth</td>
<td><strong>VgArrowheadWidth</strong>. Largeur de la flèche pour la fin de la ligne. Les valeurs sont les suivantes :
<ul>
<li>Restreindre</li>
<li>Moyenne (par défaut)</li>
<li>Large</li>
</ul></td>
</tr>
<tr class="odd">
<td>Extrem</td>
<td><strong>VgLineEndCapStyle</strong>. Les valeurs sont les suivantes :
<ul>
<li>À deux dimensions</li>
<li>Carré</li>
<li>Round</li>
</ul></td>
</tr>
<tr class="even">
<td>FillType</td>
<td><strong>VgLineFillType</strong>. Les valeurs sont les suivantes :
<ul>
<li>Unie (par défaut)</li>
<li>Tile</li>
<li>Modèle</li>
<li>Frame</li>
</ul></td>
</tr>
<tr class="odd">
<td>ImageAlignShape</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Alignez l’image avec la forme. Si la valeur est false, l’image est alignée avec la fenêtre.</td>
</tr>
<tr class="even">
<td>ImageAspect</td>
<td><strong>VgAspectType</strong>. L’attribut ImageSize est ajusté pour conserver l’aspect de l’image. Ces valeurs comprennent :
<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ignorer</td>
<td>Ignorer les problèmes d’aspect.</td>
</tr>
<tr class="even">
<td>Au moins</td>
<td>L’image est au moins aussi grande que la taille de l’image.</td>
</tr>
<tr class="odd">
<td>AtMost</td>
<td>L’image n’est pas plus grande que la taille de l’image.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>ImageSize</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>. Taille de l’image avec laquelle former le pinceau. La valeur par défaut est la taille de l’image.</td>
</tr>
<tr class="even">
<td>JoinStyle</td>
<td><strong>VgLineJoinStyle</strong>. Les valeurs sont les suivantes :
<ul>
<li>Round (joint arrondi)</li>
<li>Biseau (joint biseauté)</li>
<li>Mitre (articulation à onglet)</li>
</ul></td>
</tr>
<tr class="odd">
<td>LineStyle</td>
<td><strong>VgLineStyle</strong>. Les valeurs sont les suivantes :
<ul>
<li>Unique</li>
<li>ThinThin (1:1:1)</li>
<li>ThinThick (1:1:2)</li>
<li>ThickThin (2:1:1)</li>
<li>ThickBetweenThin (1:1:2:1:1)</li>
</ul></td>
</tr>
<tr class="even">
<td>MiterLimit</td>
<td><a href="msdn-online-vml-vglength.md">Longueur</a>. Distance maximale entre le point interne et le point externe d’une jointure. Ce nombre est un multiple de l’épaisseur de la ligne. Est compris entre 0 et 32 767.</td>
</tr>
<tr class="odd">
<td>Activé</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Active ou désactive l’affichage de la ligne. Identique à l’attribut Stroke dans Shape, mais le remplace.</td>
</tr>
<tr class="even">
<td>Opacity</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Opacité du trait.</td>
</tr>
<tr class="odd">
<td>Source</td>
<td>Chaîne. URL vers une image à charger pour les remplissages d’image et de motif. Cet attribut doit toujours être présent et pointer vers des données d’image valides pour qu’une image s’affiche.</td>
</tr>
<tr class="even">
<td>StartArrow</td>
<td><strong>VgArrowheadStyle</strong>. Pointe de flèche pour le début de la ligne. Les valeurs sont les suivantes :
<ul>
<li>Aucun (par défaut)</li>
<li>Bloquer</li>
<li>Classique</li>
<li>Losange</li>
<li>Ovale</li>
<li>Ouvrir</li>
<li>Chevron</li>
<li>DoubleChevron</li>
</ul></td>
</tr>
<tr class="odd">
<td>StartArrowLength</td>
<td>VgArrowHeadLength. Longueur de la flèche pour le début de la ligne. Les valeurs sont les suivantes :
<ul>
<li>Court</li>
<li>Moyenne (par défaut)</li>
<li>Long</li>
</ul></td>
</tr>
<tr class="even">
<td>StartArrowWidth</td>
<td>VgArrowheadWidth. Largeur de la flèche pour le début de la ligne. Les valeurs sont les suivantes :
<ul>
<li>Étroit moyen (par défaut) large</li>
</ul></td>
</tr>
<tr class="odd">
<td>Poids</td>
<td><a href="msdn-online-vml-vglength.md">VgLength</a>. Largeur de la ligne. Est compris entre 0 et 1584.
<div class="alert">
<blockquote>
[!Note]<br />
L’attribut DashStyle permet à l’utilisateur de spécifier un modèle de tirets personnalisé. Cette opération s’effectue à l’aide d’une série de nombres. Les styles de tirets sont définis en termes de longueur du tiret (partie dessinée du trait) et de la longueur de l’espace entre les tirets. Les longueurs sont relatives à la largeur de la ligne ; une longueur de &quot; 1 &quot; est égale à la largeur de ligne. Le style d’extrémité est appliqué à chaque tiret. les styles de flèche ne le sont pas. La chaîne définit d’abord la longueur du tiret, puis la longueur de l’espace. Cela peut être répété pour former des styles de tiret complexes. La chaîne doit toujours contenir une paire de nombres ; Si elle contient un nombre impair de nombres, la dernière peut être ignorée. Le tableau suivant répertorie des valeurs typiques et une description de l’effet prévu. &quot;0 &quot; signifie un point qui doit être quatre symétrique (avec des extrémités arrondies, il doit s’agir d’un cercle). Si l’extrémité de la ligne est plate, une visionneuse doit choisir un tiret de système d’exploitation intégré si possible (c’est-à-dire un point rapide à dessiner). Voici quelques exemples.
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td>&quot;2 2&quot;</td>
<td>des tirets courts (chaque tiret et l’espace entre deux fois la largeur de la ligne)</td>
</tr>
<tr class="even">
<td>&quot;1 2&quot;</td>
<td>point (chaque tiret correspond à la largeur de la ligne, tandis que chaque espace est deux fois plus large que la largeur de la ligne)</td>
</tr>
<tr class="odd">
<td>&quot;4 2&quot;</td>
<td>Dash (chaque tiret correspond à quatre fois la largeur de la ligne, tandis que chaque espace est deux fois plus large que la largeur de la ligne)</td>
</tr>
<tr class="even">
<td>&quot;8 2&quot;</td>
<td>long tiret</td>
</tr>
<tr class="odd">
<td>&quot;4 2 1 2&quot;</td>
<td>tiret-point</td>
</tr>
<tr class="even">
<td>&quot;8 2 1 2&quot;</td>
<td>long-tiret-point</td>
</tr>
<tr class="odd">
<td>&quot;8 2 1 2 1 2&quot;</td>
<td>point-tiret long</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a>Élément TextPath

Décrit un tracé vectoriel basé sur les données de texte, la police et les styles fournis. Le chemin d’accès du texte est déformé pour se conformer à un élément de **chemin d’accès** , s’il est fourni.



|   Attribut        |   Description                                                                                                                                                                                      |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| FitPath  | [VgTriState](msdn-online-vml-vgtristate.md). Dimensionne le texte pour remplir le tracé sur lequel il se trouve.                                 |
| FitShape | [VgTriState](msdn-online-vml-vgtristate.md). Étire le tracé du texte vers les bords de la zone de forme.                      |
| Activé       | [VgTriState](msdn-online-vml-vgtristate.md). Détermine si les chemins d’accès aux caractères sont affichés ou non.                    |
| String   | Chaîne. Texte à afficher sous la forme d’un tracé de texte.                                                                                    |
| SupprEspace     | [VgTriState](msdn-online-vml-vgtristate.md). Supprime tout espace supplémentaire réservé pour les jambages ascendants et descendants s’il n’est pas utilisé. |
| Cadencé   | [VgTriState](msdn-online-vml-vgtristate.md). Utilisez une mesure x droite au lieu de mesurer le long du tracé.                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a>Types de données utilisés dans le modèle d’objet VML

Les types de données suivants sont utilisés par le modèle objet VML.

-   [Double](/windows)
-   [Fixe](/windows)
-   [Integer](/windows)
-   [IVgAdjustments](/windows)
-   [IVgColor](/windows)
-   [IVgEquation](/windows)
-   [IVgFixedRectangle](/windows)
-   [IVgFixedRectangleArray](/windows)
-   [IVgFormula](/windows)
-   [IVgFormulas](/windows)
-   [IVgGradientColorArray](/windows)
-   [IVgPoints](/windows)
-   [IVgSkewMatrix](/windows)
-   [IVgSkewOffset](/windows)
-   [IVgVector2D](/windows)
-   [IVgVector3D](/windows)
-   [Durée](/windows)
-   [Mesure](/windows)
-   [Chaîne](/windows)
-   [VgBlackWhiteMode](/windows)
-   [VgFraction](/windows)
-   [VgTriState](/windows)

**Double (type de données)**

Entier double précision avec une plage comprise entre-Infinity et Infinity.

**Type de données fixe**

Nombre à virgule flottante avec une plage comprise entre-32 766,0 et 32 766,0.

**Integer (type de données)**

Entier compris entre-Infinity et Infinity.

**Type de données IVgAdjustments**

Collection d’ajustements d’une forme qui peut être utilisée pour modifier les dimensions d’une forme. Les ajustements peuvent être utilisés en tant qu’espaces réservés temporaires ou pour une raison quelconque, vous pouvez utiliser des variables. La collection ne contient que 8 ajustements.



| Attribut | Description                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exists     | [IVgTriState](msdn-online-vml-vgtristate.md). Détermine si un ajustement spécifié existe. Notez qu’un index doit être utilisé ; en d’autres cas, Exists (Item) doit être utilisé pour récupérer l’existence d’un élément.                                                                                                                                                                   |
| Élément       | [Long](#data-types-used-in-the-vml-object-model). Tableau d’ajustements indexés de 0 à 7. Notez que les ajustements peuvent être spécifiés pour SPARC. autrement dit, les valeurs de tableau intermédiaire ne peuvent pas toujours être remplies. Par exemple, les éléments 1, 3 et 5 peuvent avoir des valeurs pour une longueur de 3, avec l’élément (0), l’élément (2) et l’élément (4) spécifiés. Pour voir si un élément existe, utilisez l’attribut exists. |
| Longueur     | [Integer](#data-types-used-in-the-vml-object-model). Nombre d’ajustements. Ne peut pas être supérieur à 8.                                                                                                                                                                                                                                                                          |
| Valeur      | [Chaîne](#data-types-used-in-the-vml-object-model). Représentation textuelle des valeurs numériques, avec des virgules entre chaque nombre.                                                                                                                                                                                                                                                    |



 

**IVgColor**

Spécifie une couleur.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attributs</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>RGB</td>
<td><strong>VgRGBType</strong>. Valeur RVB (longue) de la couleur. Valide uniquement si le type est RVB.</td>
</tr>
<tr class="even">
<td>R</td>
<td><a href="#data-types-used-in-the-vml-object-model">Integer</a>. Composant rouge de la couleur. Peut être compris entre 0 et 255.</td>
</tr>
<tr class="odd">
<td>G</td>
<td><a href="#data-types-used-in-the-vml-object-model">Integer</a>. Composant vert de la couleur. Peut être compris entre 0 et 255.</td>
</tr>
<tr class="even">
<td>B</td>
<td><a href="#data-types-used-in-the-vml-object-model">Integer</a>. Composant bleu de la couleur. Peut être compris entre 0 et 255.</td>
</tr>
<tr class="odd">
<td>String</td>
<td><a href="#data-types-used-in-the-vml-object-model">Chaîne</a>. Représentation textuelle de la couleur. Les types de couleur nommés suivants sont pris en charge :
<ul>
<li>Noir (#000000)</li>
<li>Silver (#C0C0C0)</li>
<li>Gris (#808080)</li>
<li>Blanc (#FFFFFF)</li>
<li>Marron (#800000)</li>
<li>Rouge (#FF0000)</li>
<li>Violet (#800080)</li>
<li>Fuchsia (#FF00FF)</li>
<li>Vert (#008000)</li>
<li>Chaux (#00FF00)</li>
<li>Vert olive (#808000)</li>
<li>Jaune (#FFFF00)</li>
<li>Bleu marine (#000080)</li>
<li>Bleu (#0000FF)</li>
<li>Bleu-vert (#008080)</li>
<li>Aqua (#00FFFF)</li>
</ul></td>
</tr>
<tr class="even">
<td>Type</td>
<td><strong>VgColorType</strong>. Type de couleur. L’un des types suivants :
<ul>
<li>Mixte</li>
<li>named</li>
<li>RGB</li>
<li>Schéma</li>
</ul></td>
</tr>
</tbody>
</table>



 

**IVgEquation**

Équations utilisées pour les formules.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Opération</td>
<td><strong>VgEquationOperationType</strong> Nom de l’opération à effectuer sur les paramètres. Les opérations suivantes peuvent être utilisées dans une équation :
<table>
<thead>
<tr class="header">
<th>Opération</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Abs</td>
<td>Valeur absolue. <br/> <strong>ABS</strong>(v) <br/></td>
</tr>
<tr class="even">
<td>Atan2</td>
<td>Arithmétique polaire--résultats en unités FD (degrés multiplié par 65536).<br/> <strong>atan2</strong>(P1, v) <br/></td>
</tr>
<tr class="odd">
<td>Cos</td>
<td>Cosinus, argument en unités FD (degrés multiplié par 65536).<br/> v * <strong>COS</strong>(P1) <br/></td>
</tr>
<tr class="even">
<td>Cosatan2</td>
<td>Préserve la précision complète dans le calcul intermédiaire.<br/> v * <strong>cos (atan2 (</strong> P2, P1 <strong>))</strong><br/></td>
</tr>
<tr class="odd">
<td>Ellipse</td>
<td>Ellipse</td>
</tr>
<tr class="even">
<td>Si</td>
<td>Test de condition if. v > 0 <strong>?</strong> P1 : P2</td>
</tr>
<tr class="odd">
<td>Max</td>
<td>Valeur la plus grande de deux valeurs. <br/> <strong>Max</strong>(v, P1) <br/></td>
</tr>
<tr class="even">
<td>ExtracChaîne</td>
<td>Moyenne (v + P1)/2</td>
</tr>
<tr class="odd">
<td>Min</td>
<td>La plus petite des deux valeurs. <strong>min</strong>(v, P1)</td>
</tr>
<tr class="even">
<td>Mod</td>
<td>Modulo.</td>
</tr>
<tr class="odd">
<td>Produit</td>
<td>Utilisé pour la multiplication et la Division. v * P1/P2</td>
</tr>
<tr class="even">
<td>Sin</td>
<td>Sinus, argument en unités FD (degrés multiplié par 65536). <br/> v * <strong>Sin</strong>(P1) <br/></td>
</tr>
<tr class="odd">
<td>Sinatan2</td>
<td>Préserve la précision complète dans le calcul intermédiaire. v * <strong>Sin</strong>(<strong>atan2</strong>(P2, P1))</td>
</tr>
<tr class="even">
<td>Sqrt</td>
<td>Le résultat est positif et arrondit à la valeur inférieure. <br/> <strong>sqrt</strong>(v) <br/></td>
</tr>
<tr class="odd">
<td>Sum</td>
<td>Utilisé pour l’addition et la soustraction.<br/> v + P1 P2<br/></td>
</tr>
<tr class="even">
<td>Sumangle</td>
<td>Angle existant (mis à l’échelle par 65536), où P1 et P2 sont exprimés en degrés.<br/> v + P1 * 65536 + P2 * 65536<br/></td>
</tr>
<tr class="odd">
<td>Tan</td>
<td>Tangente, l’argument est en unités FD (degrés multiplié par 65536). <br/> v * Tan (P1)<br/></td>
</tr>
<tr class="even">
<td>Val</td>
<td>Définit une valeur de repère à partir d’une autre valeur.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Param1</td>
<td><strong>Integer</strong>. Premier paramètre.</td>
</tr>
<tr class="odd">
<td>Paramtype1</td>
<td><strong>VgFormulaParamType</strong>. Type du premier paramètre. Les valeurs suivantes sont admises :
<table>
<thead>
<tr class="header">
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valeur</td>
<td>Le paramètre est une valeur simple.</td>
</tr>
<tr class="even">
<td>AdjustmentReference</td>
<td>Le paramètre est une référence à un ajustement. Par exemple, si le premier paramètre est 1, la valeur du premier ajustement sera utilisée.</td>
</tr>
<tr class="odd">
<td>FormulaReference</td>
<td>Le paramètre est le résultat d’une référence au résultat d’une formule précédente. Par exemple, si le premier paramètre a la valeur 2, le résultat de la formule 2 sera utilisé.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Param2</td>
<td><strong>Integer</strong>. Deuxième paramètre.</td>
</tr>
<tr class="odd">
<td>Paramtype2</td>
<td><strong>VgFormulaParamType</strong> Type de paramètre 2.</td>
</tr>
<tr class="even">
<td>Val</td>
<td><strong>Integer</strong>. Résultat.</td>
</tr>
<tr class="odd">
<td>Valtype2</td>
<td><strong>VgFormulaParamType</strong>. Type du résultat.</td>
</tr>
</tbody>
</table>



 

**IVgFixedRectangle**

Spécifie un rectangle fixe.



| Attribut | Description                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| Valeur      | [Chaîne](#data-types-used-in-the-vml-object-model). Valeur de texte spécifiant le chemin d’accès.         |
| Gauche       | [Double](#data-types-used-in-the-vml-object-model). Coordonnée la plus à gauche du rectangle.   |
| Haut        | [Double](#data-types-used-in-the-vml-object-model). Coordonnée la plus grande du rectangle.    |
| Right      | [Double](#data-types-used-in-the-vml-object-model). Coordonnée la plus à droite du rectangle.  |
| Bas     | [Double](#data-types-used-in-the-vml-object-model). Coordonnée la plus basse du rectangle. |



 

**IVgFixedRectangleArray**

Tableau de rectangles fixes.



| Attribut | Description                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| Valeur      | [Chaîne](#data-types-used-in-the-vml-object-model). Représentation textuelle d’un tableau.                           |
| Longueur     | [Integer](#data-types-used-in-the-vml-object-model). Nombre de rectangles dans ce tableau.                    |
| Élément       | [IVgFixedRectangle](#data-types-used-in-the-vml-object-model). Objet Rectangle à l’index spécifié. |



 

Type de données **IVgFormula**

Définitions des formules qui peuvent varier le tracé d’une forme ou être utilisées à d’autres fins de calcul. Les formules peuvent être basées sur l’attribut **Adj** d’une forme, ce qui peut changer. Les formules peuvent également faire référence à d’autres formules.



| Attribut| Description                                           |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eqn        | [IVgEquation](#data-types-used-in-the-vml-object-model). Chaque formule définit une valeur unique comme résultat de l’évaluation de l’expression. L’expression est définie par cet attribut et présente la forme générale d’une opération suivie de jusqu’à trois arguments, qui peuvent être des valeurs d’ajustement (par exemple, \# 2), des résultats de formules antérieures (par exemple, @2 ), des nombres fixes ou des valeurs prédéfinies. |



 

**Type de données IVgFormulas**

Collection d’objets de formule.



| Attribut | Description                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Longueur     | [Integer](#data-types-used-in-the-vml-object-model). Nombre d’objets de formule dans la collection.                                                |
| Élément       | [IVgFormula](#data-types-used-in-the-vml-object-model). Formule spécifique. Notez que le tableau de formules peut être hérité de le type de forme. |



 

**IVgGradientColorArray**

Tableau de couleurs qui définissent un dégradé (plage de couleurs fusionnée).



| Attribut | Description                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| Valeur      | [Chaîne](#data-types-used-in-the-vml-object-model). Spécifie le tableau de couleurs ; par exemple, «Red. 2 ; vert. 4 ; noir. 7» |
| Longueur     | [Integer](#data-types-used-in-the-vml-object-model). Nombre de couleurs dans le tableau.                                          |



 



| Méthode     | Description                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AddColor    | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Ajoute une nouvelle couleur au point de terminaison spécifié par fraction. La nouvelle couleur est blanche par défaut et est la valeur de retour. La couleur peut ensuite être modifiée par référence. |
| RemoveColor | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Supprime une couleur au point de terminaison spécifié par fraction. Remarque : si 0,0 ou 1,0 n’existe pas, il est implicite et le blanc de couleur est utilisé à ce stade.          |



 

**Type de données IVgPoints**

Tableau de points qui définissent une forme.



| Attribut | Description                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| Valeur      | [Chaîne](#data-types-used-in-the-vml-object-model). Représentation textuelle d’un tableau.           |
| Longueur     | [Integer](#data-types-used-in-the-vml-object-model). Nombre de points dans ce tableau.        |
| Élément       | [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md). Point au niveau de l’index spécifié. |



 

**Type de données IVgSkewMatrix**

Matrice utilisée pour incliner des formes, une matrice de transformation de perspective sous la forme "*Sxx, SXY, syx, SYY, PX, py* " \[ *s* = Scale, *p* = perspective \] . Si le décalage est en unités absolues, alors *PX, py* sont en unités UME ^-1 ; Sinon, il s’agit d’une fraction inverse de la taille de la forme.



| Attribut   | Description                                         |
|--------------|-----------------------------------------------------|
| XtoX         | [Double](#data-types-used-in-the-vml-object-model). |
| YtoX         | [Double](#data-types-used-in-the-vml-object-model). |
| XtoY         | [Double](#data-types-used-in-the-vml-object-model). |
| YtoY         | [Double](#data-types-used-in-the-vml-object-model). |
| PerspectiveX | [Double](#data-types-used-in-the-vml-object-model). |
| Perspective | [Double](#data-types-used-in-the-vml-object-model). |



 

**IVgSkewOffset**

Spécifie le décalage de l’inclinaison.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attributs</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valeur</td>
<td><a href="#data-types-used-in-the-vml-object-model">Chaîne</a>. Représentation textuelle du décalage.</td>
</tr>
<tr class="even">
<td>X</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Composant X. Pourcentage ou mesure. Si aucune unité n’est présente, le type ShapeRelative est implicite ; Sinon, le type absolu est implicite.</td>
</tr>
<tr class="odd">
<td>O</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Composant Y.</td>
</tr>
<tr class="even">
<td>Type</td>
<td><strong>VgSkewTransformType</strong>. Spécifie le type de transformation. Les valeurs valides sont les points d’entier compris entre-Infinity et Infinity. 
<table>
<thead>
<tr class="header">
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ShapeRelative</td>
<td>Les valeurs du décalage sont des pourcentages (proportions) de la taille de la forme d’origine ; par exemple, une valeur de 0,5 signifie un décalage de la moitié de la taille de la forme.</td>
</tr>
<tr class="even">
<td>Absolu</td>
<td>Les valeurs sont des unités absolues.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

**Type de données IVgVector2D**

Spécifie un vecteur à deux dimensions constitué de deux nombres **doubles** .



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attributs</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valeur</td>
<td><strong>Chaîne</strong>. Représentation textuelle des deux nombres vectorisés séparés par un espace.</td>
</tr>
<tr class="even">
<td>X</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Composant X de ce vecteur.</td>
</tr>
<tr class="odd">
<td>O</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Composant Y de ce vecteur.</td>
</tr>
<tr class="even">
<td>Type</td>
<td><strong>VgVectorType</strong>. Unités attendues pour ce vecteur. Les valeurs sont les suivantes :
<ul>
<li>Mesure</li>
<li>Longueur</li>
<li>AngleInDegrees</li>
<li>Fraction</li>
<li>Nombre entier de pourcentage</li>
</ul></td>
</tr>
</tbody>
</table>



 

**Type de données IVgVector3D**

Spécifie un vecteur à trois dimensions composé de trois nombres **doubles** .



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Valeur</td>
<td><strong>Chaîne</strong>. Représentation textuelle de trois nombres vectorisés séparés par un espace.</td>
</tr>
<tr class="even">
<td>X</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Composant X de ce vecteur.</td>
</tr>
<tr class="odd">
<td>O</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Composant Y de ce vecteur.</td>
</tr>
<tr class="even">
<td>Z</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Composant Z de ce vecteur.</td>
</tr>
<tr class="odd">
<td>Type</td>
<td><strong>VgVectorType</strong>. Unités attendues pour ce vecteur. Les valeurs sont les suivantes :
<ul>
<li>Mesure</li>
<li>Longueur</li>
<li>AngleInDegrees</li>
<li>Fraction</li>
<li>Nombre</li>
<li>Pourcentage</li>
<li>Integer</li>
</ul></td>
</tr>
</tbody>
</table>



 

**Type de données de longueur**

Nombre à virgule flottante avec une plage comprise entre 0 et l’infini.

**Type de données Measure**

Nombre à virgule flottante de-Infinity à Infinity.

**Type de données String**

Données de caractères de n’importe quelle longueur.

**VgBlackWhiteMode**

Mode de rendu pour le noir et le blanc. Les valeurs possibles sont les suivantes :

-   **Couleur**
-   **Automatique**
-   **Semble**
-   **LightGrayScale**
-   **InverseGray**
-   **GrayOutline**
-   **BlackTextAndLines**
-   **HighContrast**
-   **Noir**
-   **White**
-   **Dédessiné**

**Type de données VgFraction**

Nombre à virgule flottante avec une plage comprise entre 0,0 et 1,0. Les fractions peuvent également être spécifiées sous la forme d’un pourcentage. par exemple, « 50% ».

**Type de données VgTriState**

Énumération utilisée pour les valeurs qui peuvent être de l’un des trois États suivants :

-   **TRUE**
-   **FALSE**
-   **CONDITIONS MIXTES**
