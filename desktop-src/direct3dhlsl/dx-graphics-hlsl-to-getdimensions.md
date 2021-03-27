---
title: GetDimensions, (objet texture HLSL DirectX)
description: Obtient des informations sur la taille de la texture. Le bloc de syntaxe affiche tous les paramètres possibles dans la déclaration de méthode. Le tableau de la section Notes montre quels paramètres sont implémentés pour chaque type d’objet texture.
ms.assetid: b72e54da-382a-4b90-bbfe-0b32effc7c05
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ad4be68049c92955c5ddb06a0c5eccfe2c26b77
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841649"
---
# <a name="getdimensions-directx-hlsl-texture-object"></a>GetDimensions, (objet texture HLSL DirectX)

Obtient des informations sur la taille de la texture. Le bloc de syntaxe affiche tous les paramètres possibles dans la déclaration de méthode. Le tableau de la section Notes montre quels paramètres sont implémentés pour chaque type d’objet texture.



|                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------|
| void Object. GetDimensions, (UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples); |



 

typeX indique qu’il existe deux types possibles : **uint** ou **float**.

## <a name="parameters"></a>Paramètres



| Élément                                                                                                                               | Description                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Dessin*<br/>                                     | Tout type d' [objet texture](dx-graphics-hlsl-to-type.md) , à l’exception d’un objet **buffer** .<br/>                                       |
| <span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*<br/>                             | \[dans \] un index de base zéro qui identifie le niveau de mipmap. Si cet argument n’est pas utilisé, le premier niveau MIP est supposé.<br/> |
| <span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Largeur*<br/>                                         | \[\]largeur de la texture, en texels.<br/>                                                                                     |
| <span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Celle*<br/>                                     | \[\]hauteur de la texture, en texels.<br/>                                                                                    |
| <span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Html*<br/>                             | \[\]nombre d’éléments dans un tableau.<br/>                                                                               |
| <span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Profondeur*<br/>                                         | \[\]profondeur de la texture, dans les texels.<br/>                                                                                     |
| <span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*<br/>     | \[\]nombre de niveaux de mipmap.<br/>                                                                                      |
| <span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*<br/> | \[\]nombre d’échantillons.<br/>                                                                                            |



 

## <a name="return-value"></a>Valeur de retour

None

## <a name="overloaded-methods"></a>Méthodes surchargées

Ce tableau répertorie toutes les différentes versions de la méthode. les versions diffèrent du nombre de paramètres d’entrée. Notez que pour chaque méthode qui accepte des paramètres entiers, il existe une méthode surchargée qui accepte les paramètres à virgule flottante.



| Type de Texture-Object | Paramètres d’entrée                                                               |
|---------------------|--------------------------------------------------------------------------------|
| Texture1D           | UINT MipLevel, UINT Width, UINT NumberOfLevels                                 |
| Texture1D           | Largeur UINT                                                                     |
| Texture1D           | UINT MipLevel, largeur float, float NumberOfLevels                               |
| Texture1D           | Largeur de la virgule flottante                                                                    |
| Texture1DArray      | UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels                  |
| Texture1DArray      | UINT Width, UINT, éléments                                                      |
| Texture1DArray      | UINT MipLevel, largeur float, éléments float, float NumberOfLevels               |
| Texture1DArray      | float Width, float, éléments                                                    |
| Texture2D           | UINT MipLevel, largeur UINT, UINT Height, UINT NumberOfLevels                    |
| Texture2D           | UINT Width, UINT, hauteur                                                        |
| Texture2D           | UINT MipLevel, largeur float, float height, float NumberOfLevels                 |
| Texture2D           | Largeur float, hauteur float                                                      |
| Texture2DArray      | UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels     |
| Texture2DArray      | UINT Width, UINT Height, UINT Elements                                         |
| Texture2DArray      | UINT MipLevel, largeur float, hauteur float, éléments float, float NumberOfLevels |
| Texture2DArray      | Largeur float, hauteur float, éléments float                                      |
| Texture3D           | UINT MipLevel, UINT Width, UINT hauteur, UINT Depth, UINT NumberOfLevels        |
| Texture3D           | UINT Width, hauteur UINT, profondeur UINT                                            |
| Texture3D           | UINT MipLevel, largeur float, hauteur float, profondeur float, float NumberOfLevels    |
| Texture3D           | Largeur float, hauteur float, profondeur float                                         |
| TextureCube         | UINT MipLevel, largeur UINT, UINT Height, UINT NumberOfLevels                    |
| TextureCube         | UINT Width, UINT, hauteur                                                        |
| TextureCube         | UINT MipLevel, largeur float, float height, UINT NumberOfLevels                  |
| TextureCube         | Largeur float, hauteur float                                                      |
| TextureCubeArray    | UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels     |
| TextureCubeArray    | UINT Width, UINT Height, UINT Elements                                         |
| TextureCubeArray    | UINT MipLevel, largeur float, hauteur float, éléments float, float NumberOfLevels |
| TextureCubeArray    | Largeur float, hauteur float, éléments float                                      |
| Texture2DMS         | UINT Width, UINT Height, UINT Samples                                          |
| Texture2DMS         | float Width, float height, float Samples                                       |
| Texture2DMSArray    | UINT Width, UINT Height, UINT Elements, UINT Samples                           |
| Texture2DMSArray    | Floating largeur, float height, float Elements, float Samples                       |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

1.  Retourne des dimensions pour le plus grand niveau de mipmap (avant toute chose).
2.  TextureCubeArray est disponible dans le nuancier modèle 4,1 ou version ultérieure.
3.  Le modèle de nuanceur 4,1 est disponible dans Direct3D 10,1 ou version ultérieure.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Texture-objet](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





