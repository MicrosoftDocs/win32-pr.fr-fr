---
description: Un bloc d’État peut être utilisé pour capturer uniquement l’état du vertex (consultez États d’enregistrement et de restauration des blocs d’État (Direct3D 9)).
ms.assetid: cb898228-dc45-4a2a-a82e-8d64523e9b85
title: Enregistrement des États de vertex avec un StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8f3ebef7bda74e30d84ff193a80df6bc6ce7eae83a648f9b7e1d05b89bdb269
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026109"
---
# <a name="saving-vertex-states-with-a-stateblock-direct3d-9"></a>Enregistrement des États de vertex avec un StateBlock (Direct3D 9)

Un bloc d’État peut être utilisé pour capturer uniquement l’état du vertex (consultez États d' [enregistrement et de restauration des blocs d’État (Direct3D 9)](state-blocks-save-and-restore-state.md)). L’état suivant est état du vertex :

-   État du rendu de vertex (voir [pipeline de vertex : état de rendu](#vertex-pipeline-render-state)).
-   État de l’échantillonneur de vertex (voir [pipeline de vertex : état de l’échantillonneur](#vertex-pipeline-sampler-state)).
-   État de la texture de vertex (voir [pipeline de vertex : état](#vertex-pipeline-texture-state)de la texture).
-   Segments en mode NPatch à partir de [**IDirect3DDevice9 :: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).
-   Chaque lumière de [**IDirect3DDevice9 :: SetLight**](/windows/desktop/api), et si la lumière est activée ou non avec [**IDirect3DDevice9 :: éclaircie**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).
-   Le nuanceur de sommets actuel et chacune des constantes de nuanceur vertex.
-   Pour chaque flux de vertex, stockez la valeur de diviseur à partir de [**IDirect3DDevice9 :: SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).
-   Déclaration de vertex actuelle.

Pour capturer l’état du vertex avec un bloc d’État, spécifiez D3DSBT \_ VERTEXSTATE lors de l’appel de [**IDirect3DDevice9 :: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).

## <a name="vertex-pipeline-render-state"></a>Pipeline de vertex : état de rendu

Les États de rendu des appareils affectent le comportement de presque toutes les parties du pipeline. Les États de rendu sont définis en appelant [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).

Le tableau suivant répertorie tous les États de rendu qui définissent l’état du vertex :



| États de rendu                           | Valeur par défaut          |
|-----------------------------------------|------------------------|
| D3DRS \_ CULLMODE                         | \_CCW D3DCULL           |
| D3DRS \_ FOGCOLOR                         | 0                      |
| D3DRS \_ FOGTABLEMODE                     | D3DFOG \_ aucun           |
| D3DRS \_ FOGSTART                         | 0                      |
| D3DRS \_ FOGEND                           | 1                      |
| D3DRS \_ FOGDENSITY                       | 1                      |
| D3DRS \_ RANGEFOGENABLE                   | **FALSE**              |
| D3DRS \_ ambiant                          | 0                      |
| D3DRS \_ COLORVERTEX                      | **TRUE**               |
| D3DRS \_ FOGVERTEXMODE                    | D3DFOG \_ aucun           |
| \_Découpage D3DRS                         | **TRUE**               |
| \_Éclairage D3DRS                         | **TRUE**               |
| D3DRS \_ LOCALVIEWER                      | **TRUE**               |
| D3DRS \_ EMISSIVEMATERIALSOURCE           | \_Matériau D3DMCS       |
| D3DRS \_ AMBIENTMATERIALSOURCE            | \_Matériau D3DMCS       |
| D3DRS \_ DIFFUSEMATERIALSOURCE            | D3DMCS \_ COLOR1         |
| D3DRS \_ SPECULARMATERIALSOURCE           | D3DMCS \_ COLOR2         |
| D3DRS \_ VERTEXBLEND                      | Désactivation de D3DVBF \_        |
| D3DRS \_ CLIPPLANEENABLE                  | 0                      |
| D3DRS \_ pointe                        | Dépend du pilote       |
| D3DRS \_ pointe \_ min.                   | 1                      |
| D3DRS \_ POINTSPRITEENABLE                | **FALSE**              |
| D3DRS \_ POINTSCALEENABLE                 | **FALSE**              |
| D3DRS \_ POINTSCALE \_ A                    | 1                      |
| D3DRS \_ POINTSCALE \_ B                    | 0                      |
| D3DRS \_ POINTSCALE \_ C                    | 0                      |
| D3DRS \_ MULTISAMPLEANTIALIAS             | **TRUE**               |
| D3DRS \_ MULTISAMPLEMASK                  | 0xffffffff             |
| D3DRS \_ PATCHEDGESTYLE                   | D3DPATCHEDGE \_ discret |
| D3DRS \_ pointe \_ Max.                   | 1                      |
| D3DRS \_ INDEXEDVERTEXBLENDENABLE         | **FALSE**              |
| D3DRS \_ TWEENFACTOR                      | 0                      |
| D3DRS \_ POSITIONDEGREE                   | D3DDEGREE \_ cubique       |
| D3DRS \_ NORMALDEGREE                     | D3DDEGREE \_ linéaire      |
| D3DRS \_ MINTESSELLATIONLEVEL             | 1                      |
| D3DRS \_ MAXTESSELLATIONLEVEL             | 1                      |
| D3DRS \_ ADAPTIVETESS \_ X                  | 0                      |
| D3DRS \_ ADAPTIVETESS \_ Y                  | 0                      |
| D3DRS \_ ADAPTIVETESS \_ Z                  | 1                      |
| D3DRS \_ ADAPTIVETESS \_ W                  | 0                      |
| D3DRS \_ ENABLEADAPTIVETESSELLATION "/> | **FALSE**              |



 

## <a name="vertex-pipeline-sampler-state"></a>Pipeline de vertex : état de l’échantillonneur

Les États de l’échantillonneur contrôlent les rubriques connexes relatives à l’échantillonnage, telles que le filtrage, la mosaïque et les modes d’adresse des coordonnées de texture. Utilisez [**IDirect3DDevice9 :: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) pour configurer l’état de l’échantillonneur (y compris celui utilisé dans l’unité du paveur pour échantillonner les mappages de déplacement). Les États de l’échantillonneur ont été renommés avec un \_ préfixe « D3DSAMP » pour permettre la détection des erreurs au moment de la compilation lors du Portage à partir de DirectX 8.

Le tableau suivant répertorie tous les États de l’échantillonneur qui configurent l’état du vertex :



| États de l’échantillonneur      | Valeur par défaut |
|---------------------|---------------|
| D3DSAMP \_ DMAPOFFSET | 256           |



 

## <a name="vertex-pipeline-texture-state"></a>Pipeline de vertex : état de la texture

Les États de texture contrôlent les opérations de fusion de texture du mélangeur à textures multiples. Utilisez [**IDirect3DDevice9 :: SetTextureStageState**](/windows/desktop/api) pour définir les États de texture. Utilisez [**IDirect3DDevice9 :: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) pour associer une texture à une étape d’échantillonnage.

Le tableau suivant répertorie tous les États de texture qui définissent l’état du vertex :



| États de la texture                | Valeur par défaut    |
|-------------------------------|------------------|
| D3DTSS \_ TEXCOORDINDEX         | 0                |
| D3DTSS \_ TEXTURETRANSFORMFLAGS | Désactivation de D3DTTFF \_ |



 

D3DTSS \_ TEXCOORDINDEX est un état de traitement de vertex de fonction fixe. Si un nuanceur de sommet programmable est utilisé, cet État est ignoré.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[État de l’enregistrement et de la restauration des blocs d’État](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
