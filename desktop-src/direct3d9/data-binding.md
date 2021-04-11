---
description: Utilisez la collection SasHostParameterValue pour définir la collection de valeurs d’application hôte, ainsi que leur type et leurs membres, exposés aux effets.
ms.assetid: 3fef353d-323a-4cc1-a8c9-2bf154754835
title: Liaison de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b67305d4acc8a4ed9e0827203e4602db26a99da
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317593"
---
# <a name="data-binding"></a>Liaison de données

Utilisez la [collection SasHostParameterValue](#sashostparametervalue-collection) pour définir la collection de valeurs d’application hôte, ainsi que leur type et leurs membres, exposés aux effets. Utilisez l’annotation [SasBindAddress](#sasbindaddress) dans un fichier Effect pour associer un paramètre Effect à son paramètre correspondant dans l’application hôte.

## <a name="sashostparametervalue-collection"></a>Collection SasHostParameterValue

Le SasHostParameterValue est défini à l’aide de la syntaxe de fichier Effect (. FX). Bien que la syntaxe soit très similaire à la syntaxe des fichiers Effects, certaines différences existent. Par exemple, les types d’objets, tels que les Texture2D, les échantillonneurs et les chaînes, ne sont pas valides dans les fichiers d’effets réels, mais sont valides dans le SasHostParameterValue. Une application hôte peut implémenter SasHostParameterValue de quelque manière que ce soit, à condition qu’elle soit conforme à la description ci-dessous. la définition réelle se trouve dans le fichier include d’effet standard DXSAS ( \[ SDK racine \] /Utilities/source/SAS/SAS.FXH).

Notez que les tableaux dans le SasHostParameterValue, tels que les lumières ou les caméras, ont une longueur illimitée. Cela signifie que les effets peuvent être liés à n’importe quel index arbitraire dans ces tableaux et que les applications hôtes doivent fournir des valeurs par défaut significatives dans les cas où aucune valeur d’application ne peut être fournie.

Certains types et constantes doivent être définis dans le DXSAS standard include, comme indiqué dans la définition de l’inclusion standard. Cela permet aux effets de lier facilement des valeurs agrégées des SasHostParameterValue à des paramètres d’effet structurés.



| Collection SasHostParameterValue    | Type            | Membre                                       |
|-------------------------------------|-----------------|----------------------------------------------|
| [Time](#time)                       | float           | SAS. Time. Now                                 |
|                                     | float           | SAS. Time. Last                                |
|                                     | int             | SAS. Time. FrameNumber                         |
| [Mappage d’environnement](#environment-map) | textureCUBE     | SAS. EnvironmentMap                           |
| [Appareil photo](#camera)                   | SasCamera       | SAS. Camera                                   |
|                                     | float4x4        | SAS. Camera. WorldToView                       |
|                                     | float4x4        | SAS. Camera. projection                        |
|                                     | float2          | SAS. Camera. NearFarClipping                   |
| [Clair](#light)                     | SasAmbientLight | AmbientLight \[ ZeroOrMore \] ;                  |
|                                     | int             | SAS. NumAmbientLights                         |
|                                     | SasAmbientLight | DirectionalLight \[ ZeroOrMore \] ;              |
|                                     | int             | SAS. NumDirectionalLights                     |
|                                     | SasAmbientLight | PointLight \[ ZeroOrMore \] ;                    |
|                                     | int             | SAS. NumPointLights                           |
|                                     | SasAmbientLight | \[ZeroOrMore Spotlight \] ;                     |
|                                     | int             | SAS. NumSpotLights                            |
| [Shadow](#shadow)                   | float4x4        | SAS. Shadow \[ ZeroOrMore \] . WorldToShadow       |
|                                     | texture2D       | SAS. Shadow \[ ZeroOrMore \] . ShadowMap           |
| [Élémentaire](#skeleton)               | float4x4        | SAS. Skeleton. MeshToJointToWorld \[ OneOrMore\] |
|                                     | int             | SAS. squelette. NumJoints                       |



 

### <a name="time"></a>Temps

La valeur d’horloge virtuelle ou d’heure de l’application hôte. Les membres sont les suivants :

-   SAS. Time. Now : la valeur de l’horloge virtuelle de l’application hôte au point où l’effet sera rendu.
-   SAS. Time. Last : la valeur de Now au rendu précédent.
-   SAS. Time. FrameNumber : valeur de compteur incrémentée une fois par frame rendu.

Les effets doivent correctement gérer le fait que les valeurs de ces membres peuvent éventuellement être encapsulées pendant des temps d’exécution très longs. Now et Last peuvent avoir des valeurs très élevées.

### <a name="environment-map"></a>Mappage d’environnement

Carte d’environnement cubique. Les applications hôtes doivent fournir une texture de cube valide si un effet tente de se lier à SAS. EnvironmentMap.

### <a name="camera"></a>Appareil photo

Caméra actuellement affichée. Les membres sont les suivants :

-   SAS. Camera. WorldToView : matrice de vue universelle composite pour l’appareil photo.
-   SAS. Camera. projection : matrice de projection pour l’appareil photo.
-   SAS. Camera. NearFarClipping : valeurs des plans de découpage near et Far.

### <a name="light"></a>Clair

Une ou plusieurs lumières de scène. La collection d’éclairages est déclarée sous la forme d’un tableau où :

-   Color : couleur RVB. La valeur par défaut est (0,0,0).
-   Direction : direction de la lumière. La valeur par défaut est (0,0,0).
-   Plage : distance à partir de la lumière où les rayons lumineux n’ont aucun effet sur la scène. La valeur par défaut est 0.
-   Thêta-angle de cône interne d’une lumière concentrée, mesuré en radians. La valeur par défaut est 0.
-   Phi : angle de cône externe d’une lumière concentrée, mesuré en radians. La valeur par défaut est 0.

Le nombre d’indicateurs doit être défini sur le nombre d’éclairages liés au tableau associé. Les effets peuvent choisir d’ignorer le nombre d’éclairages et de se lier à n’importe quel élément de l’un des tableaux de la lumière. Par conséquent, les applications hôtes doivent fournir une liaison valide pour les éléments au-delà du nombre de lumières dans le tableau.

ZeroOrMore implique que le tableau peut avoir un nombre quelconque d’éléments.

### <a name="shadow"></a>Shadow

Les mémoires tampons secondaires qui se composent des éléments suivants :

-   WorldToShadow : tableau de matrices.
-   ShadowMap : fichier de texture 2D.

ZeroOrMore implique que le tableau peut avoir n’importe quel nombre d’éléments (zéro correspond à un tableau vide).

Un effet déclarerait un échantillonneur comme suit :


```
texture2D Shadow 
<
  string SasBindAddress = "Sas.Shadow[0].ShadowMap";
>;

sampler ShadowSampler = shadow_sampler(Shadow);
```



### <a name="skeleton"></a>Élémentaire

Ensemble des frames qui composent l’objet en cours de rendu. Les exemples de frame sont des segments et des transformations. notamment :

-   MeshToJointToWorld : tableau de matrices.
-   NumJoints : nombre de jointures dans le squelette.

OneOrMore implique que le tableau a au moins un et peut contenir un nombre quelconque d’éléments.

La définition prend en charge les objets de maillage rigides et dépouillés à l’aide du même ensemble de valeurs de [collection SasHostParameterValue](#sashostparametervalue-collection) avec une interprétation différente.

## <a name="sasbindaddress"></a>SasBindAddress

Cette annotation est ajoutée au début d’un fichier Effect pour associer un paramètre Effect à son paramètre correspondant défini dans la [collection SasHostParameterValue](#sashostparametervalue-collection). L’annotation est déclarée comme suit :


```
string SasBindAddress = "SasHostParameterValue";
```



Cet exemple lie la matrice Effect World à la matrice MeshToJointToWorld :


```
float4x3 World
<
  string SasBindAddress = "Sas.Skeleton.MeshToJointToWorld[0]";
>;
```



Cette annotation indique à l’application hôte qu’elle doit définir la valeur de la matrice d’effet universel à l’aide des données de la matrice MeshToJointToWorld.

La syntaxe d’annotation d’adresse de liaison a été définie pour être très similaire à la syntaxe utilisée par [**ID3DXEffect**](id3dxeffect.md) pour récupérer et définir des paramètres d’effet. La seule différence entre les méthodes DXSAS et **ID3DXEffect** est l’ajout du jeton d’index astérisque. Voici un autre exemple d’utilisation de l’index d’astérisques :


```
float3 LightColors[6]
<
  string SasBindAddress = "Sas.Light[*].Color";
>;
```



Le jeton d’index d’astérisque indique que tous les éléments du tableau de valeurs envirnmant de l’hôte particulier (couleur dans ce cas) doivent être liés dans le paramètre associé. Plusieurs jetons d’index d’astérisques permettent de lier des effets à des sous-éléments d’un tableau de structures sans avoir à lier la totalité de la structure elle-même. Cet exemple lie les valeurs de couleur des six premières lumières à un paramètre d’effet.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur les annotations et sémantiques DirectX standard](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



