---
title: Texture, objet
description: Dans Direct3D 10, vous spécifiez les échantillonneurs et les textures indépendamment. l’échantillonnage de texture est implémenté à l’aide d’un objet de texture basée sur un modèle. Cet objet de texture basé sur un modèle a un format spécifique, retourne un type spécifique et implémente plusieurs méthodes.
ms.assetid: e8cb483a-d831-4942-b6fe-61dd5edb1813
keywords:
- Objet texture HLSL
topic_type:
- apiref
api_name:
- Texture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14ac22ba8c9da7d69784d977e2b78b8f0b52a6a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524628"
---
# <a name="texture-object"></a>Texture, objet

Dans Direct3D 10, vous spécifiez les échantillonneurs et les textures indépendamment. l’échantillonnage de texture est implémenté à l’aide d’un objet de texture basée sur un modèle. Cet objet de texture basé sur un modèle a un format spécifique, retourne un type spécifique et implémente plusieurs méthodes.

Différences entre Direct3D9 et Direct3D10 :

- Dans Direct3D 9, les échantillonneurs sont liés à des textures spécifiques.
- Dans Direct3D 10, les textures et les échantillonneurs sont des objets indépendants. Chaque objet de texture basée sur un modèle implémente des méthodes d’échantillonnage de texture qui prennent à la fois la texture et l’échantillonneur comme paramètres d’entrée.



 

Voici la syntaxe permettant de créer tous les objets texture (à l’exception des objets à échantillonnages).



| Nom du \[ < *type* > \] de la |
|------------------------------------|



 

Les objets multiéchantillonnés (Texture2DMS et Texture2DMSArray) requièrent que la taille de la texture soit explicitement indiquée et exprimée sous la forme du nombre d’échantillons.



| Object2 \[ < *type, Samples* > \] *Name*; |
|---------------------------------------------|



 

## <a name="parameters"></a>Paramètres



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Élément</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Dessin</em><br/></td>
<td>Objet texture. Il doit s’agir de l’un des types suivants. <br/> 
<table>
<thead>
<tr class="header">
<th>Type de la</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Buffer</td>
<td>Buffer </td>
</tr>
<tr class="even">
<td>Texture1D</td>
<td>texture 1D</td>
</tr>
<tr class="odd">
<td>Texture1DArray</td>
<td>Tableau de textures 1D</td>
</tr>
<tr class="even">
<td>Texture2D</td>
<td>texture 2D</td>
</tr>
<tr class="odd">
<td>Texture2DArray</td>
<td>Tableau de textures 2D</td>
</tr>
<tr class="even">
<td>Texture3D</td>
<td>texture 3D</td>
</tr>
<tr class="odd">
<td>TextureCube</td>
<td>Texture de cube</td>
</tr>
<tr class="even">
<td>TextureCubeArray  </td>
<td>Tableau de textures de cube</td>
</tr>
<tr class="odd">
<td>Type object2</td>
<td>Description</td>
</tr>
<tr class="even">
<td>Texture2DMS</td>
<td>texture multiéchantillonnée 2D</td>
</tr>
<tr class="odd">
<td>Texture2DMSArray</td>
<td>Tableau de textures multiéchantillonnées 2D</td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li>Le type de mémoire tampon prend en charge la plupart des méthodes d’objets texture, à l’exception de GetDimensions,.</li>
<li>TextureCubeArray est disponible dans le nuancier modèle 4,1 ou version ultérieure.</li>
<li>Le modèle de nuanceur 4,1 est disponible dans Direct3D 10,1 ou version ultérieure.</li>
</ol></td>
</tr>
<tr class="even">
<td><p><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Entrer</em></p></td>
<td><p>Optionnel. Tout type HLSL <a href="dx-graphics-hlsl-scalar.md">scalaire</a> ou type <a href="dx-graphics-hlsl-vector.md"><strong>HLSL vectoriel</strong></a>, entouré par des crochets pointus. Le type par défaut est <strong>float4</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Nomme</em></p></td>
<td><p>Chaîne ASCII qui spécifie le nom de l’objet de texture.</p></td>
</tr>
<tr class="even">
<td><p><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Extraits</em></p></td>
<td><p>Nombre d’échantillons (plages comprises entre 1 et 128).</p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a>Exemple 1

Voici un exemple de déclaration d’un objet texture.


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a>Méthodes de l’objet texture

Chaque objet texture implémente certaines méthodes ; Voici le tableau qui répertorie toutes les méthodes. Consultez la page de référence pour chaque méthode pour voir les objets qui peuvent utiliser cette méthode.



| Texture, méthode                                                                     | Description                                                                                                       | vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [CalculateLevelOfDetail](dx-graphics-hlsl-to-calculate-lod.md)                    | Calculer le LOD, retourner un résultat ancré.                                                                       |          |           |          | x         |          |           |
| [CalculateLevelOfDetailUnclamped](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | Calcule le LOD, retourne un résultat non ancré.                                                                    |          |           |          | x         |          |           |
| [Gather](dx-graphics-hlsl-to-gather.md)                                           | Obtient les quatre échantillons (composant rouge uniquement) qui seraient utilisés pour l’interpolation bilinéaire lors de l’échantillonnage d’une texture. |          | x         |          | x         |          | x         |
| [GetDimensions](dx-graphics-hlsl-to-getdimensions.md)                             | Obtient la dimension de texture pour un niveau mipmap spécifié.                                                           | x        | x         | x        | x         | x        | x         |
| [GetDimensions, (MultiSample)](dx-graphics-hlsl-to-getdimensions.md)               | Obtient la dimension de texture pour un niveau mipmap spécifié.                                                           |          | x         |          | x         |          | x         |
| [GetSamplePosition](dx-graphics-hlsl-to-get-sample-position.md)                   | Obtient la position de l’échantillon spécifié.                                                                         |          | x         |          | x         |          | x         |
| [Load](dx-graphics-hlsl-to-load.md)                                               | Charger des données sans aucun filtrage ni échantillonnage.                                                                      | x        | x         | x        | x         | x        | x         |
| [Charger (multiéchantillonner)](dx-graphics-hlsl-to-load.md)                                 | Charger des données sans aucun filtrage ni échantillonnage.                                                                      |          | x         | x        | x         |          | x         |
| [Exemple](dx-graphics-hlsl-to-sample.md)                                           | Échantillonner une texture.                                                                                                 |          |           | x        | x         |          |           |
| [SampleBias](dx-graphics-hlsl-to-samplebias.md)                                   | Échantillonner une texture après avoir appliqué la valeur de biais au niveau de mipmap.                                              |          |           | x        | x         |          |           |
| [SampleCmp](dx-graphics-hlsl-to-samplecmp.md)                                     | Échantillonner une texture, en utilisant une valeur de comparaison pour rejeter des exemples.                                                     |          |           | x        | x         |          |           |
| [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | Échantillonner une texture (mipmap niveau 0 uniquement), en utilisant une valeur de comparaison pour rejeter les exemples.                               | x        | x         | x        | x         | x        | x         |
| [SampleGrad](dx-graphics-hlsl-to-samplegrad.md)                                   | Échantillonner une texture à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé.                         | x        | x         | x        | x         | x        | x         |
| [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)                                 | Échantillonner une texture sur le niveau de mipmap spécifié.                                                                   | x        | x         | x        | x         | x        | x         |



 

### <a name="return-type"></a>Type de retour

Le type de retour d’une méthode d’objet de texture est float4, sauf indication contraire, à l’exception des objets de texture d’anticrénelage à échantillonnages qui nécessitent toujours le type et le nombre d’échantillons spécifiés. Le type de retour est le même que le type de ressource de texture ([**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)). En d’autres termes, il peut s’agir de l’un des types suivants.



| Type                       | Description                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| float                      | 32 bits float (voir [règles à virgule flottante](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) pour les différences par rapport à IEEE float)                            |
| int                        | Entier 32 bits signé                                                                                                                                                   |
| nombre entier non signé               | Entier non signé 32 bits                                                                                                                                                 |
| ronfler                      | 32-bit float dans la plage comprise entre-1 et 1 (voir les [règles à virgule flottante](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) pour les différences par rapport à IEEE float) |
| unorm                      | virgule flottante 32 bits dans la plage de 0 à 1 inclusive (voir les [règles à virgule flottante](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) pour les différences par rapport à IEEE float)  |
| tout type ou struct de texture | Le nombre de composants retournés doit être compris entre 1 et 3 inclus.                                                                                                    |



 

En outre, le type de retour peut être n’importe quel type de texture, y compris une structure, mais il doit être inférieur à 4 composants tels qu’un type float1 qui retourne un composant.

## <a name="default-values-for-missing-components-in-a-texture"></a>Valeurs par défaut pour les composants manquants dans une texture

La valeur par défaut pour les composants manquants dans un type de ressource de texture est égale à zéro pour tout composant, à l’exception du composant alpha (A); la valeur par défaut pour le A manquant est un. La façon dont celle-ci apparaît dans le nuanceur dépend du type de ressource de texture. Il prend la forme du premier composant typé qui est réellement présent dans le type de ressource de texture (à partir de la gauche dans l’ordre RVBA). Si ce formulaire est UNORM ou FLOAT, la valeur par défaut pour le A manquant est 1,0 f. Si le formulaire est Saint ou UINT, la valeur par défaut pour le A manquant est 0x1.

Par exemple, lorsqu’un nuanceur lit [**le \_ format \_ dxgi \_ R24 \_ UNORM \_ x8**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , les valeurs par défaut pour G et B sont égales à zéro et la valeur par défaut est 1,0 f ; lorsqu’un nuanceur lit le type de ressource de texture [**dxgi \_ format \_ R16G16 \_ uint**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , la valeur par défaut de B est zéro et la valeur par défaut pour est 0x00000001 ; quand un nuanceur lit le [**\_ format dxgi \_ R16 \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) de ressource de la texture Saint, les valeurs par défaut pour G et B sont égales à zéro et la valeur par défaut de est 0x00000001.

## <a name="example-2"></a>Exemple 2

Voici un exemple d’échantillonnage de texture à l’aide d’une méthode de texture.


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cet objet est pris en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                        | Prise en charge |
|---------------------------------------------------------------------|-----------|
| [Nuancier modèle 4](dx-graphics-hlsl-sm4.md) et modèles de nuanceur supérieurs | Oui       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

