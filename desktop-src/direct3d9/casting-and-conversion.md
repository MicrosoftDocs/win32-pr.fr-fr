---
description: Lors du transfert de valeurs entre l’application hôte et un paramètre d’effet, les données sont écrites comme prévu lorsque le type de données source (dans l’application hôte) correspond au type de données de destination (dans le paramètre d’effet).
ms.assetid: 4f3ef14a-7d67-45fe-9282-541221815d1f
title: Cast et conversion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b8ab6ec3fccd8dc57d503de18ffe1e9e321377
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110630"
---
# <a name="casting-and-conversion"></a>Cast et conversion

Lors du transfert de valeurs entre l’application hôte et un paramètre d’effet, les données sont écrites comme prévu lorsque le type de données source (dans l’application hôte) correspond au type de données de destination (dans le paramètre d’effet). Lorsque les types de données diffèrent, la conversion se produit lorsque les données sources sont réorganisées pour s’adapter à la destination.

DXSAS définit les règles de conversion de type suivantes. Il s’agit d’un sur-ensemble de l’effet (. FX) et des règles de conversion de type HLSL. DXSAS définit également des [modificateurs de valeur de paramètre](#parameter-value-modifiers) qui peuvent affecter la valeur transférée de l’application hôte vers un paramètre lié.

## <a name="type-casting"></a>Cast de type

Le tableau suivant répertorie le cast qui se produit lorsqu’un type de données est transféré vers un autre type de données :



| Type de source                                  | Type de destination                             | Comportement                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| float                                        | int                                          | Arrondi à zéro.                                                                                                                                                                                                                                                                                                                                                                                      |
| float, int                                   | bool                                         | Les valeurs qui ne sont pas égales à 0, basées sur une comparaison « différent de » à 0 (int) ou 0,0 (float), sont considérées comme étant vraies ; sinon, la valeur est considérée comme false.                                                                                                                                                                                                                                         |
| int                                          | float                                        |                                                                                                                                                                                                                                                                                                                                                                                                          |
| bool                                         | int, float                                   | La valeur false est convertie en zéro. True est converti en un.                                                                                                                                                                                                                                                                                                                                                     |
| texture1D, texture2D, texture3D, textureCUBE | texture                                      | La texture de destination est traitée comme le type de texture source.                                                                                                                                                                                                                                                                                                                                               |
| string                                       | texture1D, texture2D, texture3D, textureCUBE | La valeur de chaîne est traitée comme une adresse de ressource et résolue de la même façon que l' [annotation d’initialisation de paramètre](parameter-initialization-annotation.md). Si l’adresse de la ressource ne peut pas être résolue, le cast n’est pas valide et les applications hôtes doivent retourner une erreur. Si la ressource est correctement résolue, le type de l’expression est traité comme le même type que la ressource résolue. |



 

## <a name="class-casting"></a>Cast de classe

Outre les règles de conversion de type décrites ci-dessus, DXSAS définit l’ensemble des règles de cast nécessaires à la conversion entre les types de classe. Les matrices de colonnes (N x 1), les matrices de lignes (1 x N) et les structures numériques sont traitées comme des vecteurs.

Les paramètres de matrice Effect et les variables de matrice HLSL peuvent définir si la valeur est une matrice ligne-principale ou colonne-principale ; Toutefois, les API DirectX traitent toujours [**D3DMATRIX**](d3dmatrix.md) et [**D3DXMATRIX**](d3dxmatrix.md) en ligne-major.



| Classe source | Classe de destination | Comportement                                                                                                                                                                                                                                                                                                                                        |
|--------------|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Scalaire       | Scalaire            | Appliquez la conversion de type.                                                                                                                                                                                                                                                                                                                             |
| Scalaire       | Vecteur            | Répliquez la valeur source scalaire dans chaque composant du vecteur de destination après avoir appliqué le cast de type et le comportement de conversion décrits dans type casting.                                                                                                                                                                             |
| Scalaire       | Matrix            | Répliquez la valeur source scalaire dans chaque composant de la matrice de destination après avoir appliqué le cast de type et le comportement de conversion décrits dans type casting.                                                                                                                                                                             |
| Scalaire       | Object            | Cast non valide. Les applications hôtes doivent retourner une erreur.                                                                                                                                                                                                                                                                                           |
| Scalaire       | Structure         | Valide uniquement si la structure de destination contient uniquement des éléments numériques. S’il est valide, répliquez la valeur source scalaire dans chaque composant de la structure de destination après avoir appliqué le cast de type et le comportement de conversion décrits dans type casting.                                                                                        |
| Vecteur       | Scalaire            | Le scalaire de destination reçoit la valeur du premier composant du vecteur source après avoir appliqué le cast de type et le comportement de conversion décrits dans la conversion de [type](#type-casting).                                                                                                                                                       |
| Vecteur       | Vecteur            | Cast non valide si le vecteur de destination a plus de composants que le vecteur source. Le vecteur de destination reçoit les valeurs les plus à gauche du vecteur source après avoir appliqué le cast de type et le comportement de conversion décrits dans la conversion de [type](#type-casting). Les composants restants situés le plus à droite du vecteur source sont perdus.             |
| Vecteur       | Matrix            | Cast non valide, sauf si le vecteur source a le même nombre de composants que la matrice de destination. Si le cast est valide, le comportement de vector-to-vector cast est ensuite appliqué.                                                                                                                                                             |
| Vecteur       | Object            | Cast non valide. Les applications hôtes doivent retourner une erreur.                                                                                                                                                                                                                                                                                           |
| Vecteur       | Structure         | Valide uniquement si la structure de destination contient uniquement des éléments numériques et ne contient pas plus d’éléments que le vecteur source ne possède des composants. Les éléments de la structure de destination reçoivent les composants les plus à gauche du vecteur source après l’application du cast de type et du comportement de conversion décrits dans [type casting](#type-casting).      |
| Matrix       | Scalaire            | L’scalaire de destination reçoit la valeur de la valeur supérieure gauche de la matrice source après avoir appliqué le cast de type et le comportement de conversion décrits dans [type casting](#type-casting).                                                                                                                                                 |
| Matrix       | Vecteur            | Cast non valide, sauf si la matrice source a le même nombre de composants que le vecteur de destination. Si le cast est valide, le comportement de la conversion de vecteur à vecteur ci-dessus est ensuite appliqué.                                                                                                                                                       |
| Matrix       | Matrix            | Cast non valide si la matrice de destination a plus de composants que la matrice source. La matrice de destination reçoit les valeurs supérieures à gauche de la matrice source après avoir appliqué le cast de type et le comportement de conversion décrits dans la conversion de [type](#type-casting). Les composants inférieurs situés en bas à droite de la matrice source sont perdus. |
| Matrix       | Object            | Cast non valide. Les applications hôtes doivent retourner une erreur.                                                                                                                                                                                                                                                                                           |
| Matrix       | Structure         | La taille de la structure doit être égale à la taille de la matrice et tous les composants de la structure doivent être numériques.                                                                                                                                                                                                                          |
| Object       | Scalaire            | Cast non valide. Les applications hôtes doivent retourner une erreur.                                                                                                                                                                                                                                                                                           |
| Object       | Vecteur            | Cast non valide. Les applications hôtes doivent retourner une erreur.                                                                                                                                                                                                                                                                                           |
| Object       | Matrix            | Cast non valide. Les applications hôtes doivent retourner une erreur.                                                                                                                                                                                                                                                                                           |
| Object       | Object            | Valide si les types des objets sont identiques et conformément au comportement défini dans le cast de [type](#type-casting).                                                                                                                                                                                                                   |
| Structure    | Scalaire            | Valide si la structure source contient au moins un membre numérique. Le scalaire de destination reçoit la valeur du premier membre numérique de la structure source après avoir appliqué le cast de type et le comportement de conversion décrits dans la conversion de [type](#type-casting).                                                                                |
| Structure    | Vecteur            | La structure source doit être au moins égale à la taille du vecteur. Les premiers composants doivent être numériques jusqu’à la taille du vecteur de destination.                                                                                                                                                                                                    |
| Structure    | Matrix            | La structure source doit être au moins égale à la taille du vecteur. Les premiers composants doivent être numériques jusqu’à la taille du vecteur de destination.                                                                                                                                                                                                    |
| Structure    | Structure         | La structure de destination ne doit pas être supérieure à la structure source. Un cast valide doit exister entre tous les composants source et de destination respectifs.                                                                                                                                                                                       |



 

## <a name="parameter-value-modifiers"></a>Modificateurs de valeur de paramètre

Les annotations de modificateur de paramètre ajoutent des informations supplémentaires à un paramètre afin que les données du paramètre puissent être interprétées correctement. Par exemple, un vecteur peut devoir être exprimé avec des données normalisées ou une longueur peut être mesurée en pouces. Les annotations de modificateur de valeur de paramètre expriment ces informations supplémentaires afin que les applications hôtes puissent transformer les valeurs correctement lorsque les données sont transférées à un paramètre d’effet.

Il s’agit des modificateurs de paramètres suivants :



| Annotations de modificateur de valeur de paramètre | Description                                    |
|--------------------------------------|------------------------------------------------|
| [SasNormalize](#sasnormalize)        | Spécifiez si un vecteur est normalisé ou non. |
| [SasUnits](#sasunits)                | Spécifiez les unités de mesure d’un paramètre.  |



 

### <a name="sasnormalize"></a>SasNormalize

L’annotation SasNormalize indique que le paramètre associé doit être une valeur normalisée à chaque fois qu’elle est assignée. Cette annotation affecte uniquement les paramètres float2, float3 et float4.


```
string SasNormalize = "Value";
```



où la valeur est true ou false.

Voici un exemple :


```
float3 UpNormal
<
  bool SasNormalize = "True";
>;
```



### <a name="sasunits"></a>SasUnits

Les données des paramètres d’effet sont dans les unités suivantes :


```
string SasUnits = "Value";
```



où la valeur est l’une des suivantes :



| Type de mesure     | Valeur        | Description                    |
|----------------------|--------------|--------------------------------|
| Aucune unité             | chaîne vide | Aucune unité                       |
| Distance             | MM           | Millimètres                    |
|                      | cm           | Centimètres                    |
|                      | m            | Mètres                         |
|                      | kilomètres           | Kilomètres                     |
| Angle                | rad          | Radians                        |
| Temps                 | ms           | Millisecondes                   |
|                      | Archiv          | Secondes                        |
|                      | minute(s)          | Minutes                        |
|                      | heure(s)           | Heures                          |
| Vélocité linéaire      | mm/s       | Millimètres par seconde         |
|                      | cm/s       | Centimètres par seconde         |
|                      | m/s        | Mètres par seconde              |
|                      | m/h         | Mètres par heure                |
|                      | km/h        | Kilomètres par heure            |
| Accélération linéaire  | mm/s ²      | Millimètres par seconde au carré |
|                      | cm/s ²      | Centimètres par seconde au carré |
|                      | m/s ²       | Mètres par seconde au carré      |
|                      | m/h ²        | Mètres par heure au carré        |
|                      | km/h ²       | Kilomètres par heure au carré    |
| Vélocité angulaire     | rad/s      | Radians par seconde             |
| Accélération angulaire | rad/s ²     | Radians par seconde au carré     |
| Domaine                 | mm ²          | Millimètres au carré            |
|                      | cm ²          | Centimètres au carré            |
|                      | grammes           | Mètres carrés                 |
|                      | km²          | Kilomètres carrés             |
| Volume               | mm ³          | Millimètres cube              |
|                      | ³          | Cubes en centimètres              |
|                      | Cube           | Compteurs cubes                   |
|                      | km ³          | Kilomètres cubes               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur les annotations et sémantiques DirectX standard](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



