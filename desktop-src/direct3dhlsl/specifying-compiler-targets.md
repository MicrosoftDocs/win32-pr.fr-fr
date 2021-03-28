---
title: Spécification de cibles de compilateur
description: Ici, nous répertorions les cibles pour les différents profils pris en charge par D3DCompile \ Functions et le compilateur HLSL.
ms.assetid: 594E1C14-C1D4-4207-91A1-28892CE6D821
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68fc6c5a202ad537b02a20846d36526533240f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382735"
---
# <a name="specifying-compiler-targets"></a>Spécification de cibles de compilateur

Vous devez spécifier la cible de nuanceur (jeu de fonctionnalités de nuanceur) à compiler lorsque vous appelez la fonction [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile), [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2)ou [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) . Ici, nous répertorions les cibles pour les différents profils que les fonctions **D3DCompile \*** et le compilateur HLSL prennent en charge.

-   [Niveaux de fonctionnalité Direct3D 11,0 et 11,1](#direct3d-110-and-111-feature-levels)
-   [Niveau de fonctionnalité Direct3D 10,1](#direct3d-101-feature-level)
-   [Niveau de fonctionnalité Direct3D 10,0](#direct3d-100-feature-level)
-   [Niveaux de fonctionnalité Direct3D 9,1, 9,2 et 9,3](#direct3d-91-92-and-93-feature-levels)
-   [Modèle de nuanceur Direct3D 9 hérité 3,0](#legacy-direct3d-9-shader-model-30)
-   [Modèle de nuanceur Direct3D 9 hérité 2,0](#legacy-direct3d-9-shader-model-20)
-   [Modèle de nuanceur Direct3D 9 hérité 1. x](#legacy-direct3d-9-shader-model-1x)
-   [Effets hérités](#legacy-effects)
-   [Remarques](#notes)
-   [Rubriques connexes](#related-topics)

## <a name="direct3d-110-and-111-feature-levels"></a>Niveaux de fonctionnalité Direct3D 11,0 et 11,1

Voici les cibles de nuanceur que les niveaux de [fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 11,0 et 11,1 prennent en charge.



| Cible   | Description                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| CS \_ 5 \_ 0 | DirectCompute 5,0 ([nuanceur de calcul](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))                              |
| DS \_ 5 \_ 0 | [Nuanceur de domaine](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)             |
| GS \_ 5 \_ 0 | [Nuanceur Geometry](/previous-versions//bb205146(v=vs.85)) |
| HS \_ 5 \_ 0 | [Nuanceur de coque](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                   |
| PS \_ 5 \_ 0 | [Nuanceur de pixels](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 5 \_ 0 | [Nuanceur de sommets](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-101-feature-level"></a>Niveau de fonctionnalité Direct3D 10,1

Voici les cibles de nuanceur que le [niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 10,1 prend en charge.



| Cible   | Description                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| CS \_ 4 \_ 1 | DirectCompute 4,1 ([nuanceur de calcul](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹                             |
| GS \_ 4 \_ 1 | [Nuanceur Geometry](/previous-versions//bb205146(v=vs.85)) |
| PS \_ 4 \_ 1 | [Nuanceur de pixels](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 4 \_ 1 | [Nuanceur de sommets](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-100-feature-level"></a>Niveau de fonctionnalité Direct3D 10,0

Voici les cibles de nuanceur que le [niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 10,0 prend en charge.



| Cible   | Description                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| CS \_ 4 \_ 0 | DirectCompute 4,0 ([nuanceur de calcul](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹                             |
| GS \_ 4 \_ 0 | [Nuanceur Geometry](/previous-versions//bb205146(v=vs.85)) |
| PS \_ 4 \_ 0 | [Nuanceur de pixels](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 4 \_ 0 | [Nuanceur de sommets](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-91-92-and-93-feature-levels"></a>Niveaux de fonctionnalité Direct3D 9,1, 9,2 et 9,3

Voici les cibles de nuanceur que les [niveaux de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 9,1, 9,2 et 9,3 prennent en charge.

> [!Note]  
> Lorsque vous utilisez les \* \_ \_ \_ \_ \_ profils de nuanceur HLSL de 4 niveaux 9 x, vous utilisez implicitement les profils [Shader Model 2. x](dx-graphics-hlsl-sm2.md) pour prendre en charge le matériel compatible Direct3D 9. Les profils Shader Model 2. x prennent en charge un comportement de contrôle de Flow plus limité que le [modèle de nuanceur 4. x](dx-graphics-hlsl-sm4.md) et versions ultérieures.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Cible</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ps_4_0_level_9_1</td>
<td>[Nuanceur de pixels](/previous-versions//bb205146(v=vs.85)) pour 9,1 et 9,2 (limites similaires à ps_2_0)
<ul>
<li>64 instructions de texture arithmétique et 32</li>
<li>12 registres temporaires</li>
<li>4 niveaux de lectures dépendantes</li>
</ul></td>
</tr>
<tr class="even">
<td>ps_4_0_level_9_3</td>
<td><a href="/previous-versions//bb205146(v=vs.85)">Nuanceur de pixels</a> pour 9,3 (limites similaires à ps_2_x ² avec des fonctionnalités de nuanceur supplémentaires)
<ul>
<li>instructions 512</li>
<li>32 registres temporaires</li>
<li>Contrôle de Flow statique (profondeur maximale de 4)</li>
<li>Contrôle de workflow dynamique (profondeur maximale de 24)</li>
<li>D3DPS20CAPS_ARBITRARYSWIZZLE</li>
<li>D3DPS20CAPS_GRADIENTINSTRUCTIONS</li>
<li>D3DPS20CAPS_PREDICATION</li>
<li>D3DPS20CAPS_NODEPENDENTREADLIMIT</li>
<li>D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</li>
</ul></td>
</tr>
<tr class="odd">
<td>vs_4_0_level_9_1</td>
<td><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> pour 9,1 et 9,2 (semblable à vs_2_0)
<ul>
<li>instructions 256</li>
<li>12 registres temporaires</li>
<li>Contrôle de Flow statique (profondeur maximale de 1)</li>
</ul></td>
</tr>
<tr class="even">
<td>vs_4_0_level_9_3</td>
<td><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> pour 9,3 (semblable à vs_2_a ² avec des fonctionnalités de nuanceur supplémentaires et l’instanciation)
<ul>
<li>instructions 256</li>
<li>32 registres temporaires</li>
<li>Contrôle de Flow statique (profondeur maximale de 4)</li>
<li>D3DVS20CAPS_PREDICATION</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="legacy-direct3d-9-shader-model-30"></a>Modèle de nuanceur Direct3D 9 hérité 3,0

Voici les cibles de nuanceur pour le modèle de nuanceur Direct3D 9 hérité 3,0 ³.



| Cible    | Description                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| PS \_ 3 \_ 0  | [Nuanceur de pixels](/previous-versions//bb205146(v=vs.85)) 3,0               |
| \_logiciel PS 3 \_ | [Nuanceur de pixels](/previous-versions//bb205146(v=vs.85)) 3,0 (logiciel)    |
| vs \_ 3 \_ 0  | [Vertex shader](/previous-versions//bb205146(v=vs.85)) 3,0            |
| vs \_ 3 \_ SW | [Vertex shader](/previous-versions//bb205146(v=vs.85)) 3,0 (logiciel) |



 

## <a name="legacy-direct3d-9-shader-model-20"></a>Modèle de nuanceur Direct3D 9 hérité 2,0

Voici les cibles de nuanceur pour le modèle de nuanceur Direct3D 9 hérité 2,0 ³.



| Cible    | Description                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| PS \_ 2 \_ 0  | [Nuanceur de pixels](/previous-versions//bb205146(v=vs.85)) 2,0             |
| PS \_ 2 \_ a  | [Nuanceur de pixels](/previous-versions//bb205146(v=vs.85)) 2A              |
| PS \_ 2 \_ b  | [Nuanceur de pixels](/previous-versions//bb205146(v=vs.85)) 2b              |
| \_logiciel PS 2 \_ | Logiciel [nuanceur de pixels](/previous-versions//bb205146(v=vs.85)) 2,0    |
| vs \_ 2 \_ 0  | [Vertex shader](/previous-versions//bb205146(v=vs.85)) 2,0          |
| vs \_ 2 \_ a  | [Nuanceur de sommet](/previous-versions//bb205146(v=vs.85)) 2A           |
| vs \_ 2 \_ SW | Logiciel [vertex shader](/previous-versions//bb205146(v=vs.85)) 2,0 |



 

## <a name="legacy-direct3d-9-shader-model-1x"></a>Modèle de nuanceur Direct3D 9 hérité 1. x

Voici les cibles de nuanceur pour le modèle de nuanceur Direct3D 9 hérité 1. x ⁴.



| Cible   | Description                                                                                                                                                                       |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TX \_ 1 \_ 0 | Profil de nuanceur de texture qui utilise les fonctions D3DX9 ⁵ héritées [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) et [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx) |
| vs \_ 1 \_ 1 | [Vertex shader](/previous-versions//bb205146(v=vs.85)) 1,1                                                            |



 

## <a name="legacy-effects"></a>Effets hérités

Voici les objectifs des effets hérités.



| Cible   | Description                               |
|----------|-------------------------------------------|
| FX \_ 2 \_ 0 | Effets (FX) pour Direct3D 9 dans D3DX9 ⁵     |
| FX \_ 4 \_ 0 | Effets (FX) pour Direct3D 10,0 dans D3DX10 ⁵ |
| FX \_ 4 \_ 1 | Effets (FX) pour Direct3D 10,1 dans D3DX10 ⁵ |
| FX \_ 5 \_ 0 | Effets (FX) pour Direct3D 11 ⁵             |



 

## <a name="notes"></a>Notes

Voici quelques remarques à propos desquelles les sections précédentes font référence :

1.  les appareils de [niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10,0 et 10,1 peuvent éventuellement prendre en charge DirectCompute. Pour vérifier la prise en charge, utilisez [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) avec [**d3d11 \_ Feature \_ D3D10 \_ X \_ Hardware \_ options**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).
2.  le [niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9,3 requiert en fait un matériel conforme aux exigences du modèle de [nuanceur Direct3D 9 hérité 3,0](#legacy-direct3d-9-shader-model-30), mais ce niveau de fonctionnalité n’utilise pas les \_ cibles vs 3 \_ 0 ou PS \_ 3 \_ 0.
3.  Utilisez uniquement les modèles de nuanceur Direct3D 9 hérités avec l’API Direct3D 9. Utilisez plutôt les profils 9. x avec les API Direct3D 10. x et 11. x.
4.  Les fonctions de **D3DCompile \*** de nuanceur HLSL actuelles ne prennent pas en charge les nuanceurs de pixels hérités 1. x. La dernière version du langage HLSL pour la prise en charge de ces cibles était D3DX9 dans la version d’octobre 2006 du kit de développement logiciel (SDK) DirectX.
5.  Toutes les versions de D3DX et du SDK DirectX sont déconseillées. Pour plus d’informations, consultez [où est le kit de développement logiciel (SDK) DirectX ?](/windows/desktop/directx-sdk--august-2009-).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 