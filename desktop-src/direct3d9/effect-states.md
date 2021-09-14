---
description: Les États d’effet sont utilisés pour initialiser les États de pipeline en préparation du traitement des vertex et des pixels.
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: États d’effet (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b02cafd3bbd603716da99f5de613f06014a70f77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012761"
---
# <a name="effect-states-direct3d-9"></a>États d’effet (Direct3D 9)

Les États d’effet sont utilisés pour initialiser les États de pipeline en préparation du traitement des vertex et des pixels.


```
effect state [ [index] ] = expression;
```



Où :

-   État d’effet : similaire aux États de pipeline de fonction fixe traditionnels. La liste complète des États est fournie ci-dessous.
-   \[\[ \] index \] -Index entier facultatif. L’index identifie un état particulier dans un tableau d’États d’effet. Les crochets externes indiquent qu’un index est facultatif. Si un index est utilisé, veillez à utiliser les crochets intérieurs.
-   expression d’assignation d’état d’expression. Consultez [expressions (Direct3D 9)](expressions.md).

Chaque État a un type de données natif. Il s’agit du type de données dans lequel l’État attend des valeurs lorsque l’effet les affecte. Les types de données attendus par chaque État sont répertoriés ci-dessous.

Notez que l’interface Effect tentera d’effectuer un cast des valeurs vers le type approprié le plus tôt possible. Les valeurs littérales peuvent être converties au moment de la compilation. Les non-littéraux (c’est-à-dire les variables régulières) doivent être convertis lorsque les méthodes Set appropriées sont appelées. Par exemple, l’interface Effect effectue un cast des valeurs définies à l’aide de [**SetBool**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md)et d’autres fonctions similaires, si nécessaire. Pour de meilleures performances, assurez-vous que les valeurs passées à l’interface Effect sont déjà du type correct et n’auront pas besoin d’être castées. Si le runtime ne parvient pas à effectuer un cast d’une valeur, une erreur est retournée.

Les États d’effet peuvent être répartis dans les catégories suivantes :

-   [États légers](#light-states)
-   [États du matériau](#material-states)
-   [États de rendu](#render-states)
    -   [États de rendu de canal de pixels](#pixel-pipe-render-states)
    -   [États de rendu du canal de vertex](#vertex-pipe-render-states)
-   [États de l’échantillonneur](#sampler-states)
-   [États des étapes de l’échantillonneur](#sampler-stage-states)
-   [États du nuanceur](#shader-states)
-   [États constants du nuanceur](#shader-constant-states)
-   [États de la texture](#texture-states)
-   [États des étapes de texture](#texture-stage-states)
-   [États de la transformation](#transform-states)

## <a name="light-states"></a>États légers

Pour activer les meilleures performances pour appliquer un effet, tous les composants d’une lumière ou d’un matériau doivent être spécifiés dans le fichier d’effet. Les États que vous ne pouvez pas déclarer sont définis sur une valeur par défaut, car il n’existe aucun moyen pour Direct3D de définir les États légers individuellement.



| État clair            | Type   | Valeurs                                                                                                              |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| LightAmbient \[ n\]      | float4 | Consultez le membre ambiant de [**D3DLIGHT9**](d3dlight9.md).                                                           |
| LightAttenuation0 \[ n\] | float  | Consultez le membre Attenuation0 de [**D3DLIGHT9**](d3dlight9.md).                                                      |
| LightAttenuation1 \[ n\] | float  | Consultez le membre Attenuation1 de [**D3DLIGHT9**](d3dlight9.md).                                                      |
| LightAttenuation2 \[ n\] | float  | Consultez le membre Attenuation2 de [**D3DLIGHT9**](d3dlight9.md).                                                      |
| LightDiffuse \[ n\]      | float4 | Consultez le membre diffus de [**D3DLIGHT9**](d3dlight9.md).                                                           |
| LightDirection \[ n\]    | float3 | Consultez le membre direction de [**D3DLIGHT9**](d3dlight9.md).                                                         |
| \[N\]       | bool   | **True** ou **false**. Consultez l’argument bEnable dans [**Eclaircir**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).            |
| LightFalloff \[ n\]      | float  | [**D3DCOLORVALUE**](d3dcolorvalue.md). Consultez le membre de retrait de [**D3DLIGHT9**](d3dlight9.md).                   |
| LightPhi \[ n\]          | float  | Consultez le membre Phi de [**D3DLIGHT9**](d3dlight9.md).                                                               |
| LightPosition \[ n\]     | float3 | Consultez le membre position de [**D3DLIGHT9**](d3dlight9.md).                                                          |
| LightRange \[ n\]        | float  | Consultez le membre de plage de [**D3DLIGHT9**](d3dlight9.md).                                                             |
| LightSpecular \[ n\]     | float4 | Consultez le membre spéculaire de [**D3DLIGHT9**](d3dlight9.md).                                                          |
| LightTheta \[ n\]        | float  | Consultez le membre thêta de [**D3DLIGHT9**](d3dlight9.md).                                                             |
| LightType \[ n\]         | dword  | Même valeur que le tableau de n valeurs jusqu’à n [**D3DLIGHTTYPE**](./d3dlighttype.md) sans le \_ préfixe D3DLIGHT. |



 

Exemple :


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



Cela permet d’activer l’éclairage, d’éclairer le type, de définir la position de la lumière sur float3<10.0 f, 1.0 f, 23.0 f> et de définir la couleur ambiante sur float4<0,7 f, 0.0 f, 0.0 f, 1.0 f>.

## <a name="material-states"></a>États du matériau

Les États que vous ne pouvez pas déclarer sont définis sur une valeur par défaut, car il n’existe aucun moyen pour Direct3D de définir des États de matériau individuellement.



| État du matériau   | Type   | Valeurs                                         |
|------------------|--------|------------------------------------------------|
| Propriétés matériau  | float4 | Même valeur que l' [ **ambiant**](d3dmaterial9.md)  |
| MaterialDiffuse  | float4 | Valeur identique à la [ **diffusion**](d3dmaterial9.md)  |
| Matériau émissif | float4 | Même valeur que [ **émissif**](d3dmaterial9.md) |
| MaterialPower    | float  | Même valeur que l' [ **alimentation**](d3dmaterial9.md)    |
| MaterialSpecular | float4 | Même valeur que [ **spéculaire**](d3dmaterial9.md) |



 

Exemple :


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



Cela permet de définir la couleur diffuse sur float4<0,7 f, 0.0 f, 0.0 f, 1.0 f> et de rendre la puissance de la documentation 3.0 f.

## <a name="render-states"></a>États de rendu

Il existe deux types d’États de rendu :

-   [États de rendu de canal de pixels](#pixel-pipe-render-states)
-   [États de rendu du canal de vertex](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a>États de rendu de canal de pixels

Les États de rendu des fichiers Effects ont des noms semblables aux États de pipeline de fonction fixe, souvent avec le préfixe supprimé.




| | | État du rendu | Tapez | Valeurs | | AlphaBlendEnable | bool | True ou false. Mêmes valeurs que D3DRS_ALPHABLENDENABLE dans <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>. | | AlphaFunc | DWORD | Mêmes valeurs que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sans le préfixe D3DCMP_. Consultez D3DRS_ALPHAFUNC. | | AlphaRef | DWORD | Mêmes valeurs que D3DRS_ALPHAREF. | | AlphaTestEnable | DWORD | True ou false. Consultez D3DRS_ALPHATESTENABLE. | | BlendOp | DWORD | Mêmes valeurs que <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> sans le préfixe D3DBLENDOP_. | | ColorWriteEnable | DWORD | Combinaison d’opérations de bits de RED | VERT | BLEU | Lettres. Consultez D3DRS_COLORWRITEENABLE. | | DepthBias | float | Mêmes valeurs que D3DRS_DEPTHBIAS. | | DestBlend | DWORD | Mêmes valeurs que <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> sans le préfixe D3DBLEND_. | | DitherEnable | bool | True ou false. Mêmes valeurs que D3DRS_DITHERENABLE. | | FillMode | DWORD | Mêmes valeurs que <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> sans le préfixe D3DFILL_. | | LastPixel | DWORD | True ou false. Consultez D3DRS_LASTPIXEL. | | ShadeMode | DWORD | Mêmes valeurs que <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> sans le préfixe D3DSHADE_. | | SlopeScaleDepthBias | float | Mêmes valeurs que D3DRS_SLOPESCALEDEPTHBIAS. | | SrcBlend | DWORD | Mêmes valeurs que <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> sans le préfixe D3DBLEND_. | | SRGBWriteEnable | bool | True ou false. Mêmes valeurs que D3DRS_SRGBWRITEENABLE. | | StencilEnable | bool | True ou false. Mêmes valeurs que D3DRS_STENCILENABLE. | | StencilFail | DWORD | Mêmes valeurs que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sans le préfixe D3DSTENCILCAP_. Consultez D3DRS_STENCILFAIL. | | StencilFunc | DWORD | Mêmes valeurs que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sans le préfixe D3DCMP_. Consultez D3DRS_STENCILFUNC. | | StencilMask | DWORD | Mêmes valeurs que D3DRS_STENCILMASK. | | StencilPass | DWORD | Mêmes valeurs que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sans le préfixe D3DSTENCILCAP_. Consultez D3DRS_STENCILPASS. | | StencilRef | entier | Mêmes valeurs que D3DRS_STENCILREF. | | StencilWriteMask | DWORD | Mêmes valeurs que D3DRS_STENCILWRITEMASK. | | StencilZFail | DWORD | Mêmes valeurs que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sans le préfixe D3DSTENCILCAP_. Consultez D3DRS_STENCILZFAIL. | | TextureFactor | DWORD | Mêmes valeurs que <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>. Mêmes valeurs que D3DRS_TEXTUREFACTOR. | | Wrap0-Wrap15 | DWORD | Les valeurs sont les mêmes que les valeurs utilisées par D3DRS_WRAP0. Les valeurs autorisées sont :<ul><li>COORD0 (qui correspond à D3DWRAPCOORD_0)</li><li>COORD1 (qui correspond à D3DWRAPCOORD_1)</li><li>COORD2 (qui correspond à D3DWRAPCOORD_2)</li><li>COORD3 (qui correspond à D3DWRAPCOORD_3)</li><li>U (qui correspond à D3DWRAP_U)</li><li>V (qui correspond à D3DWRAP_V)</li><li>W (qui correspond à D3DWRAP_W)</li></ul> | | ZEnable | DWORD | Mêmes valeurs que <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> sans le préfixe D3DZB_. | | ZFunc | DWORD | Mêmes valeurs que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sans le préfixe D3DCMP_. Consultez D3DRS_ZFUNC. | | ZWriteEnable | bool | True ou false. Consultez D3DRS_ZWRITEENABLE. | 




 

Exemple :


```
AlphaBlendEnable = TRUE;
FillMode = WIREFRAME;
```



Cela active la fusion alpha et rend toutes les géométries affichées en filaire.

### <a name="vertex-pipe-render-states"></a>États de rendu du canal de vertex

Les États de rendu des fichiers Effects ont des noms semblables aux États de pipeline de fonction fixe, souvent avec le préfixe supprimé.



| État du rendu             | Type   | Valeurs                                                                                                                                        |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Ambiant                  | float4 | Mêmes valeurs que D3DRS \_ ambiant.                                                                                                                |
| AmbientMaterialSource    | dword  | Mêmes valeurs que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sans le \_ préfixe D3DMCS. Consultez D3DRS \_ AMBIENTMATERIALSOURCE.  |
| Découpage                 | bool   | Vrai ou faux. Mêmes valeurs que le \_ découpage D3DRS.                                                                                                |
| ClipPlaneEnable          | dword  | Combinaison d’opérations de bits de macros D3DCLIPPLANE0-D3DCLIPPLANE5. Consultez [**D3DCLIPPLANEn**](d3dclipplanen.md) et D3DRS \_ CLIPPLANEENABLE.           |
| ColorVertex              | bool   | Vrai ou faux. Mêmes valeurs que D3DRS \_ COLORVERTEX.                                                                                             |
| CullMode                 | dword  | Mêmes valeurs que [**D3DCULL**](./d3dcull.md) sans le \_ préfixe D3DCULL.                                                                 |
| DiffuseMaterialSource    | dword  | Mêmes valeurs que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sans le \_ préfixe D3DMCS. Consultez D3DRS \_ DIFFUSEMATERIALSOURCE.  |
| EmissiveMaterialSource   | dword  | Mêmes valeurs que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sans le \_ préfixe D3DMCS. Consultez D3DRS \_ EMISSIVEMATERIALSOURCE. |
| FogColor                 | dword  | Mêmes valeurs que [**D3DCOLOR**](d3dcolor.md). Consultez D3DRS \_ FOGCOLOR.                                                                             |
| FogDensity               | float  | Mêmes valeurs que D3DRS \_ FOGDENSITY.                                                                                                             |
| FogEnable                | bool   | Vrai ou faux. Mêmes valeurs que D3DRS \_ FOGENABLE.                                                                                               |
| FogEnd                   | float  | Mêmes valeurs que D3DRS \_ FOGEND.                                                                                                                 |
| FogStart                 | float  | Mêmes valeurs que D3DRS \_ FOGSTART.                                                                                                               |
| FogTableMode             | dword  | Mêmes valeurs que [**D3DFOGMODE**](./d3dfogmode.md). Consultez D3DRS \_ FOGTABLEMODE dans [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).     |
| FogVertexMode            | dword  | Mêmes valeurs que [**D3DFOGMODE**](./d3dfogmode.md) sans le \_ préfixe D3DFOG.                                                            |
| IndexedVertexBlendEnable | bool   | Vrai ou faux. Mêmes valeurs que D3DRS \_ INDEXEDVERTEXBLENDENABLE.                                                                                |
| Éclairage                 | bool   | Vrai ou faux. Mêmes valeurs que l' \_ éclairage D3DRS.                                                                                                |
| LocalViewer              | bool   | Vrai ou faux. Mêmes valeurs que D3DRS \_ LOCALVIEWER.                                                                                             |
| MultiSampleAntialias     | bool   | Mêmes valeurs que D3DRS \_ MULTISAMPLEANTIALIAS.                                                                                                   |
| MultiSampleMask          | dword  | Mêmes valeurs que D3DRS \_ MULTISAMPLEMASK.                                                                                                        |
| NormalizeNormals         | bool   | Vrai ou faux. Mêmes valeurs que D3DRS \_ NORMALIZENORMALS.                                                                                        |
| PatchSegments            | float  | Mêmes valeurs que nSegments dans [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).                                                         |
| PointScale \_ A            | float  | Mêmes valeurs que D3DRS \_ POINTSCALE \_ A.                                                                                                          |
| PointScale \_ B            | float  | Mêmes valeurs que D3DRS \_ POINTSCALE \_ B.                                                                                                          |
| PointScale \_ C            | float  | Mêmes valeurs que D3DRS \_ POINTSCALE \_ C.                                                                                                          |
| PointScaleEnable         | bool   | Mêmes valeurs que D3DRS \_ POINTSCALEENABLE.                                                                                                       |
| PointSize                | float  | Les mêmes valeurs que D3DRS sont \_ désignables.                                                                                                              |
| Repointer \_ min.           | float  | Les mêmes valeurs que D3DRS \_ redirigent \_ min.                                                                                                         |
| Délimiter \_ Max.           | float  | Les mêmes valeurs que D3DRS \_ redirigent \_ Max sans le \_ préfixe D3DRS.                                                                              |
| PointSpriteEnable        | bool   | Vrai ou faux. Mêmes valeurs que D3DRS \_ POINTSPRITEENABLE.                                                                                       |
| RangeFogEnable           | bool   | Vrai ou faux. Mêmes valeurs que D3DRS \_ RANGEFOGENABLE.                                                                                          |
| SpecularEnable           | bool   | Vrai ou faux. Mêmes valeurs que D3DRS \_ SpecularEnable.                                                                                          |
| SpecularMaterialSource   | dword  | Mêmes valeurs que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sans le \_ préfixe D3DMCS. Consultez D3DRS \_ SPECULARMATERIALSOURCE. |
| TweenFactor              | float  | Mêmes valeurs que D3DRS \_ TWEENFACTOR.                                                                                                            |
| VertexBlend              | dword  | Mêmes valeurs que [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) sans le \_ préfixe D3DVBF. Consultez D3DRS \_ VERTEXBLEND.                  |



 

Exemple :


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



Cela rend la couleur ambiante float4<0,7 f, 0.0 f, 0.0 f, 1.0 f>, définir le mode d’élimination des faces arrière pour qu’il s’affiche dans le sens inverse des aiguilles d’une montre et définir la couleur de brouillard sur rouge.

## <a name="sampler-states"></a>États de l’échantillonneur

Un état de l’échantillonneur représente un objet d’échantillonnage.



| State   | Type    | Valeurs                              |
|---------|---------|-------------------------------------|
| Échantillonneur | échantillonneur | **Null**, ou un bloc d’état de l’échantillonneur. |



 

## <a name="sampler-stage-states"></a>États des étapes de l’échantillonneur

Les États des étapes de l’échantillonneur sont utilisés pour échantillonner les textures. L’état de l’échantillonneur détermine les types de filtrage et les modes d’adressage des textures.



| État de l’échantillonneur       | Type                         | Valeurs                                                                                                                            |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Adressed \[ 16\]      | dword                        | Mêmes valeurs que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sans le \_ préfixe D3DTADDRESS. Consultez D3DSAMP \_ .      |
| AddressV \[ 16\]      | dword                        | Mêmes valeurs que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sans le \_ préfixe D3DTADDRESS. Consultez D3DSAMP \_ ADDRESSV.      |
| AddressW \[ 16\]      | dword                        | Mêmes valeurs que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sans le \_ préfixe D3DTADDRESS. Consultez D3DSAMP \_ ADDRESSW.      |
| BorderColor \[ 16\]   | [**D3DCOLOR**](d3dcolor.md) | Mêmes valeurs que [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) sans le \_ préfixe D3DTEXF. Consultez D3DSAMP \_ BORDERCOLOR. |
| MagFilter \[ 16\]     | dword                        | Mêmes valeurs que [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) sans le \_ préfixe D3DTEXF. Consultez D3DSAMP \_ MAGFILTER.   |
| MaxAnisotropy \[ 16\] | dword                        | Mêmes valeurs que D3DSAMP \_ MAXANISOTROPY sans le \_ préfixe D3DSAMP.                                                               |
| MaxMipLevel \[ 16\]   | int                          | Mêmes valeurs que D3DSAMP \_ MAXMIPLEVEL sans le \_ préfixe D3DSAMP.                                                                 |
| MinFilter \[ 16\]     | dword                        | Mêmes valeurs que D3DSAMP \_ MINFILTER sans le \_ préfixe D3DSAMP.                                                                   |
| MipFilter \[ 16\]     | dword                        | Mêmes valeurs que D3DSAMP \_ MIPFILTER sans le \_ préfixe D3DSAMP.                                                                   |
| MipMapLodBias \[ 16\] | float                        | Mêmes valeurs que D3DSAMP \_ MIPMAPLODBIAS sans le \_ préfixe D3DSAMP.                                                               |
| SRGBTexture         | bool                         | Même valeur que D3DSAMP \_ SRGBTEXTURE sans le \_ préfixe D3DSAMP.                                                                   |



 

Exemple :


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



Les valeurs UVW doivent être comprises entre 0 et 1.

## <a name="shader-states"></a>États du nuanceur

Il n’y a que deux États de nuanceur d’effet : l’un associé à un objet nuanceur vertex et l’autre à un objet nuanceur de pixels.



| État du nuanceur | Type         | Valeurs                                                                      |
|--------------|--------------|-----------------------------------------------------------------------------|
| PixelShader  | PixelShader  | **Null**, un bloc d’assembly, une cible de compilation ou un paramètre de nuanceur de pixels. |
| VertexShader | VertexShader | **Null**, un bloc d’assembly, une cible de compilation ou un paramètre de nuanceur de pixels. |



 

Exemple :


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



Cela compilera VSTexture, un nuanceur de sommets défini plus tôt dans le fichier. FX, à la version 1,1 du nuanceur de sommets, puis définira ce nuanceur compilé comme nuanceur de sommets. Le nuanceur de pixels est assigné à la **valeur null**.

## <a name="shader-constant-states"></a>États constants du nuanceur

Les États de constante de nuanceur sont utilisés pour accéder aux paramètres de constante de nuanceur.



| État constant du nuanceur | Type            | Valeurs                                       |
|-----------------------|-----------------|----------------------------------------------|
| PixelShaderConstant   | float \[ m \[ n\]\] | Tableau de valeurs float de m x n ; m et n sont facultatifs. |
| PixelShaderConstant1  | float4          | Un flottant 4D.                                |
| PixelShaderConstant2  | float4x2        | Deux valeurs en virgule flottante 4D.                               |
| PixelShaderConstant3  | float4x3        | Trois valeurs en virgule flottante 4D.                             |
| PixelShaderConstant4  | float4x4        | Quatre valeurs en virgule flottante 4D.                              |
| PixelShaderConstantB  | bool \[ m \[ n\]\]  | Tableau de bool m x n ; m et n sont facultatifs.  |
| PixelShaderConstantI  | int \[ m \[ n\]\]   | Tableau d’entiers m x n. m et n sont facultatifs.   |
| PixelShaderConstantF  | float \[ m \[ n\]\] | Tableau de valeurs à virgule flottante m x n. m et n sont facultatifs. |
| VertexShaderConstant  | float \[ m \[ n\]\] | Tableau de valeurs à virgule flottante m x n. m et n sont facultatifs. |
| VertexShaderConstant1 | float4          | Un flottant 4D.                                |
| VertexShaderConstant2 | float4x2        | Deux valeurs en virgule flottante 4D.                               |
| VertexShaderConstant3 | float4x3        | Trois valeurs en virgule flottante 4D.                             |
| VertexShaderConstant4 | float4x4        | Quatre valeurs en virgule flottante 4D.                              |
| VertexShaderConstantB | bool \[ m \[ n\]\]  | Tableau de bool m x n. m et n sont facultatifs.  |
| VertexShaderConstantI | int \[ m \[ n\]\]   | Tableau d’entiers m x n. m et n sont facultatifs.   |
| VertexShaderConstantF | float \[ m \[ n\]\] | Tableau de valeurs à virgule flottante m x n. m et n sont facultatifs. |



 

## <a name="texture-states"></a>États de la texture

Les États de texture initialisent les textures utilisées par le mélangeur de multitexture.



| État de la texture | Type    | Valeurs                            |
|---------------|---------|-----------------------------------|
| Texture \[ 8\]  | texture | **Null**, ou un paramètre de texture. |



 

## <a name="texture-stage-states"></a>États des étapes de texture

Les États de l’étape de texture définissent les textures et les étapes de texture dans le mélangeur de textures multiples.



| État de l’étape de texture        | Type  | Valeurs                                                                                                                                                    |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| AlphaOp \[ 8\]               | dword | Identique à [**D3DTEXTUREOP**](./d3dtextureop.md) sans le \_ préfixe D3DTOP. Consultez D3DTSS \_ ALPHAOP.                                                      |
| AlphaArg0 \[ 8\]             | dword | Identique à [D3DTA](d3dta.md) sans le \_ préfixe D3DTA. Consultez D3DTSS \_ ALPHAARG0.                                                                             |
| AlphaArg1 \[ 8\]             | dword | Identique à [D3DTA](d3dta.md) sans le \_ préfixe D3DTA. Consultez D3DTSS \_ ALPHAARG1.                                                                             |
| AlphaArg2 \[ 8\]             | dword | Identique à [D3DTA](d3dta.md) sans le \_ préfixe D3DTA. Consultez D3DTSS \_ ALPHAARG2.                                                                             |
| ColorArg0 \[ 8\]             | dword | Identique à [D3DTA](d3dta.md) sans le \_ préfixe D3DTA. Consultez D3DTSS \_ COLORARG0.                                                                             |
| ColorArg1 \[ 8\]             | dword | Identique à [D3DTA](d3dta.md) sans le \_ préfixe D3DTA. Consultez D3DTSS \_ COLORARG1.                                                                             |
| ColorArg2 \[ 8\]             | dword | Identique à [D3DTA](d3dta.md) sans le \_ préfixe D3DTA. Consultez D3DTSS \_ COLORARG2.                                                                             |
| ColorOp \[ 8\]               | dword | Identique à [**D3DTEXTUREOP**](./d3dtextureop.md) sans le \_ préfixe D3DTOP. Consultez D3DTSS \_ COLOROP.                                                      |
| BumpEnvLScale \[ 8\]         | float | Mêmes valeurs que D3DTSS \_ BUMPENVLSCALE sans le \_ préfixe D3DTSS TCI.                                                                                      |
| BumpEnvLOffset \[ 8\]        | float | Mêmes valeurs que D3DTSS \_ BUMPENVLOFFSET sans le \_ préfixe D3DTSS TCI.                                                                                     |
| BumpEnvMat00 \[ 8\]          | float | Mêmes valeurs que D3DTSS \_ BUMPENVMAT00.                                                                                                                      |
| BumpEnvMat01 \[ 8\]          | float | Mêmes valeurs que D3DTSS \_ BUMPENVMAT01.                                                                                                                      |
| BumpEnvMat10 \[ 8\]          | float | Mêmes valeurs que D3DTSS \_ BUMPENVMAT10.                                                                                                                      |
| BumpEnvMat11 \[ 8\]          | float | Mêmes valeurs que D3DTSS \_ BUMPENVMAT11.                                                                                                                      |
| ResultArg \[ 8\]             | dword | Identique à [D3DTA](d3dta.md) sans le \_ préfixe D3DTA. Consultez D3DTSS \_ RESULTARG.                                                                             |
| TexCoordIndex \[ 8\]         | dword | Mêmes valeurs que D3DTSS \_ TEXCOORDINDEX sans le \_ préfixe D3DTSS TCI.                                                                                      |
| TextureTransformFlags \[ 8\] | dword | Mêmes valeurs que les valeurs [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) sans le \_ préfixe D3DTTFF. Consultez D3DTSS \_ TEXTURETRANSFORMFLAGS. |



 

## <a name="transform-states"></a>États de la transformation

Définissez les États de transformation pour initialiser les matrices de transformation. Les effets utilisent des matrices transposées pour des performances optimales. Vous pouvez fournir des matrices transposées à un effet, ou un effet transposera automatiquement les matrices avant de les utiliser.



| Transformer l’État       | Type     | Valeurs                                                                                                                          |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| ProjectionTransform   | float4x4 | Matrice 4x4 de nombres à virgule flottante. Mêmes valeurs que \_ la projection D3DTS sans le \_ préfixe D3DTS.                                            |
| TextureTransform \[ 8\] | float4x4 | Matrice 4x4 de nombres à virgule flottante. Mêmes valeurs que [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) sans le \_ préfixe D3DTS. |
| ViewTransform         | float4x4 | Matrice 4x4 de nombres à virgule flottante. Mêmes valeurs que \_ la vue D3DTS sans le \_ préfixe D3DTS.                                                  |
| WorldTransform        | float4x4 | Matrice 4x4 de nombres à virgule flottante.                                                                                                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format d’effet](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
