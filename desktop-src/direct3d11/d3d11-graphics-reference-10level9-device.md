---
title: Méthodes 10Level9 ID3D11Device
description: Cette section répertorie les différences entre chaque niveau de fonctionnalité 10Level9 et le niveau de fonctionnalité D3D \_ \_ \_ 11 \_ 0 et supérieur pour les méthodes ID3D11Device.
ms.assetid: c3bc32a9-8d97-430b-be6a-b4935d7ac56c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400c7f321981f13b3e184a25139782c8a9d9a2ba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382397"
---
# <a name="10level9-id3d11device-methods"></a>Méthodes 10Level9 ID3D11Device

Cette section répertorie les différences entre chaque niveau de fonctionnalité 10Level9 et le niveau de fonctionnalité D3D \_ \_ \_ 11 \_ 0 et supérieur pour les méthodes [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .

-   [ID3D11Device :: CheckCounter](#id3d11devicecheckcounter)
-   [ID3D11Device :: CheckFormatSupport](#id3d11devicecheckformatsupport)
-   [ID3D11Device :: CheckMultisampleQualityLevels](#id3d11devicecheckmultisamplequalitylevels)
-   [ID3D11Device :: CreateBlendState](#id3d11devicecreateblendstate)
-   [ID3D11Device :: CreateBlendState1](#id3d11devicecreateblendstate1)
-   [ID3D11Device :: CreateBuffer](#id3d11devicecreatebuffer)
-   [ID3D11Device :: CreateCounter](#id3d11devicecreatecounter)
-   [ID3D11Device :: CreateDepthStencilView](#id3d11devicecreatedepthstencilview)
-   [ID3D11Device :: CreateDomainShader](#id3d11devicecreatedomainshader)
-   [ID3D11Device :: CreateGeometryShader](#id3d11devicecreategeometryshader)
-   [ID3D11Device :: CreateGeometryShaderWithStreamOutput](#id3d11devicecreategeometryshaderwithstreamoutput)
-   [ID3D11Device :: CreateHullShader](#id3d11devicecreatehullshader)
-   [ID3D11Device :: CreateInputLayout](#id3d11devicecreateinputlayout)
-   [ID3D11Device :: CreatePixelShader](#id3d11devicecreatepixelshader)
-   [ID3D11Device :: CreatePredicate](#id3d11devicecreatepredicate)
-   [ID3D11Device :: CreateQuery](#id3d11devicecreatequery)
-   [ID3D11Device :: CreateRasterizerState](#id3d11devicecreaterasterizerstate)
-   [ID3D11Device :: CreateRenderTargetView](#id3d11devicecreaterendertargetview)
-   [ID3D11Device :: CreateSamplerState](#id3d11devicecreatesamplerstate)
-   [ID3D11Device :: CreateShaderResourceView](#id3d11devicecreateshaderresourceview)
-   [ID3D11Device :: CreateTexture1D](#id3d11devicecreatetexture1d)
-   [ID3D11Device :: CreateTexture2D](#id3d11devicecreatetexture2d)
-   [ID3D11Device :: CreateTexture3D](#id3d11devicecreatetexture3d)
-   [ID3D11Device :: CreateUnorderedAccessView](#id3d11devicecreateunorderedaccessview)
-   [ID3D11Device :: CreateVertexShader](#id3d11devicecreatevertexshader)
-   [ID3D11Device :: OpenSharedResource](#id3d11deviceopensharedresource)
-   [Rubriques connexes](#related-topics)

## <a name="id3d11devicecheckcounter"></a>ID3D11Device :: CheckCounter



<table>
<thead>
<tr class="header">
<th>Niveau de fonctionnalité</th>
<th>Différences de comportement</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Les compteurs dépendants de l’appareil sont éventuellement pris en charge. Utilisez <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device :: CheckCounterInfo</strong></a> pour déterminer la prise en charge. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckformatsupport"></a>ID3D11Device :: CheckFormatSupport



<table>
<thead>
<tr class="header">
<th>Niveau de fonctionnalité</th>
<th>Différences de comportement</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Consultez formater la prise en charge par <a href="overviews-direct3d-11-devices-downlevel-intro.md">niveau de fonctionnalité</a>$ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckmultisamplequalitylevels"></a>ID3D11Device :: CheckMultisampleQualityLevels



<table>
<thead>
<tr class="header">
<th>Niveau de fonctionnalité</th>
<th>Différences de comportement</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Les niveaux de fonctionnalité n’assurent aucune garantie quant à la prise en charge MSAA. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateblendstate"></a>ID3D11Device :: CreateBlendState



| Niveau de fonctionnalité              | Différences de comportement                                                                                                                                                                                                                                                                                                                                             |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1  | AlphaToCoverageEnable doit avoir la **valeur false**.<br/> Les quatre premiers BlendEnables doivent tous avoir la même valeur.<br/> D3D11 \_ Blend \_ src \_ ALPHASAT non pris en charge.<br/> Mélange de couleurs à double source non pris en charge (SrcBlend ou DestBlend avec SRC1 dans le nom)<br/>                                                                                |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2  | AlphaToCoverageEnable doit avoir la **valeur false**.<br/> Les quatre premiers BlendEnables doivent tous avoir la même valeur.<br/> Les quatre premiers RenderTargetWriteMasks doivent tous avoir la même valeur.<br/> D3D11 \_ Blend \_ src \_ ALPHASAT non pris en charge.<br/> Mélange de couleurs à double source non pris en charge (SrcBlend ou DestBlend avec SRC1 dans le nom)<br/> |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3  | AlphaToCoverageEnable doit avoir la **valeur false**.<br/> Les quatre premiers BlendEnables doivent tous avoir la même valeur.<br/> D3D11 \_ Blend \_ src \_ ALPHASAT non pris en charge.<br/> Mélange de couleurs à double source non pris en charge (SrcBlend ou DestBlend avec SRC1 dans le nom)<br/>                                                                                |
| \_Niveau de fonctionnalité D3D \_ \_ 10 \_ 0 | Ajoute alpha-to-coverage                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="id3d11devicecreateblendstate1"></a>ID3D11Device :: CreateBlendState1



| Niveau de fonctionnalité              | Différences de comportement                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1  | Non pris en charge<br/>                                                                                                                                                                                                                                                                                                                                       |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2  | Non pris en charge<br/>                                                                                                                                                                                                                                                                                                                                       |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3  | Non pris en charge<br/>                                                                                                                                                                                                                                                                                                                                       |
| \_Niveau de fonctionnalité D3D \_ \_ 10 \_ 0 | Le membre *OutputMergerLogicOp* a été ajouté aux [**\_ \_ \_ \_ options d3d11 des données de la fonctionnalité d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options)pour déterminer la prise en charge des opérations logiques (opérations de logique au niveau du bit entre la sortie du nuanceur de pixels et le contenu de la cible de rendu, reportez-vous à [**d3d11 \_ Render \_ target \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)). |



 

## <a name="id3d11devicecreatebuffer"></a>ID3D11Device :: CreateBuffer



<table>
<thead>
<tr class="header">
<th>Niveau de fonctionnalité</th>
<th>Différences de comportement</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td>Les mémoires tampons ne peuvent pas avoir de vues de cible de rendu.<br/> Les mémoires tampons doivent avoir une seule des D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER ou D3D11_BIND_CONSTANT_BUFFER.<br/> Autorise uniquement les mémoires tampons d’index avec le format DXGI_FORMAT_R16_UINT. <br/></td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>
<td rowspan="2"> Les mémoires tampons ne peuvent pas avoir de vues de cible de rendu.<br/> Les mémoires tampons doivent avoir une seule des D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER ou D3D11_BIND_CONSTANT_BUFFER.<br/> Permet aux mémoires tampons d’index avec les formats DXGI_FORMAT_R16_UINT et DXGI_FORMAT_R32_UINT comme D3D_FEATURE_LEVEL_10_0 et versions ultérieures. <br/> $ {REMOVE} $<br />
</td>
</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatecounter"></a>ID3D11Device :: CreateCounter



<table>
<thead>
<tr class="header">
<th>Niveau de fonctionnalité</th>
<th>Différences de comportement</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedepthstencilview"></a>ID3D11Device :: CreateDepthStencilView



<table>
<thead>
<tr class="header">
<th>Niveau de fonctionnalité</th>
<th>Différences de comportement</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Ne prend pas en charge le stencil à deux côtés. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedomainshader"></a>ID3D11Device :: CreateDomainShader



<table>
<thead>
<tr class="header">
<th>Niveau de fonctionnalité</th>
<th>Différences de comportement</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Non pris en charge sur les fonctionnalités 9. * ou 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshader"></a>ID3D11Device :: CreateGeometryShader



<table>
<thead>
<tr class="header">
<th>Niveau de fonctionnalité</th>
<th>Différences de comportement</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshaderwithstreamoutput"></a>ID3D11Device :: CreateGeometryShaderWithStreamOutput



<table>
<thead>
<tr class="header">
<th>Niveau de fonctionnalité</th>
<th>Différences de comportement</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatehullshader"></a>ID3D11Device :: CreateHullShader



<table>
<thead>
<tr class="header">
<th>Niveau de fonctionnalité</th>
<th>Différences de comportement</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Non pris en charge sur les 9. * ou 10. * niveau de fonctionnalité. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateinputlayout"></a>ID3D11Device :: CreateInputLayout



| Niveau de fonctionnalité             | Différences de comportement                                                                                              |
|---------------------------|-------------------------------------------------------------------------------------------------------------------|
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1 | Ne prend pas en charge les \_ données d’entrée d3d11 \_ par \_ instance \_                                                                |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2 | Ne prend pas en charge les \_ données d’entrée d3d11 \_ par \_ instance \_                                                                |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3 | Le flux de vertex zéro doit \_ avoir \_ une entrée d3d11 par \_ \_ données de vertex, si des flux ont une \_ entrée d3d11 \_ par \_ vertex \_ |



 

Pour plus d’informations sur les formats pouvant être utilisés pour les données de vertex à chaque niveau de fonctionnalité, consultez la page formater la prise en charge par le [graphique au](overviews-direct3d-11-devices-downlevel-intro.md) niveau des fonctionnalités.

## <a name="id3d11devicecreatepixelshader"></a>ID3D11Device :: CreatePixelShader



| Niveau de fonctionnalité             | Différences de comportement                                    |
|---------------------------|---------------------------------------------------------|
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1 | Doit utiliser PS \_ 4 \_ 0 \_ niveau \_ 9 \_ 1                          |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2 | Doit utiliser PS \_ 4 \_ 0 \_ niveau \_ 9 \_ 1                          |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3 | Doit utiliser PS \_ 4 \_ 0 \_ niveau \_ 9 \_ 3 ou PS \_ 4 \_ 0 \_ niveau \_ 9 \_ 1 |



 

## <a name="id3d11devicecreatepredicate"></a>ID3D11Device :: CreatePredicate



<table>
<thead>
<tr class="header">
<th>Niveau de fonctionnalité</th>
<th>Différences de comportement</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatequery"></a>ID3D11Device :: CreateQuery



| Niveau de fonctionnalité             | Différences de comportement                                                                                                                                  |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1 | Les requêtes d’événements sont prises en charge. Les requêtes d’horodatage sont facultatives : appelez [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) pour déterminer la prise en charge.               |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2 | Les requêtes d’événement et d’occlusion sont prises en charge. Les requêtes d’horodatage sont facultatives : appelez [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) pour déterminer la prise en charge. |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3 | Les requêtes d’événement et d’occlusion sont prises en charge. Les requêtes d’horodatage sont facultatives : appelez [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) pour déterminer la prise en charge. |



 

## <a name="id3d11devicecreaterasterizerstate"></a>ID3D11Device :: CreateRasterizerState



<table>
<thead>
<tr class="header">
<th>Niveau de fonctionnalité</th>
<th>Différences de comportement</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">DepthClipEnable doit avoir la <strong>valeur true</strong>. DepthBiasClamp doit avoir la valeur 0. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreaterendertargetview"></a>ID3D11Device :: CreateRenderTargetView



<table>
<thead>
<tr class="header">
<th>Niveau de fonctionnalité</th>
<th>Différences de comportement</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Peut uniquement prendre en charge les affichages de cible de rendu des objets Texture2D. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatesamplerstate"></a>ID3D11Device :: CreateSamplerState



<table>
<thead>
<tr class="header">
<th>Niveau de fonctionnalité</th>
<th>Différences de comportement</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td>Le filtre de comparaison n’est pas pris en charge.<br/> La couleur de la bordure doit être comprise entre [0, 1]<br/> Le LOD minimal ne peut pas être fractionnaire<br/> Le LOD maximal doit être FLT_MAX<br/> L’anisotropie maximale est 2.<br/> D3D11_TEXTURE_ADDRESS_MIRRORONCE pas pris en charge.<br/></td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>
<td rowspan="2"> Le filtre de comparaison n’est pas pris en charge.<br/> La couleur de la bordure doit être comprise entre [0, 1]<br/> Le LOD minimal ne peut pas être fractionnaire<br/> Le LOD maximal doit être FLT_MAX<br/> L’anisotropie maximale est 16.<br/> $ {REMOVE} $<br />
</td>
</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateshaderresourceview"></a>ID3D11Device :: CreateShaderResourceView



| Niveau de fonctionnalité             | MostDetailedMip plus Miplevels a doit inclure LOD (plus petite sous-ressource | La vue doit inclure tous les éléments du tableau de ressources |
|---------------------------|------------------------------------------------------------------------------|-----------------------------------------------|
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1 | Oui                                                                          | Oui                                           |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2 | Oui                                                                          | Oui                                           |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3 | Oui                                                                          | Oui                                           |



 

## <a name="id3d11devicecreatetexture1d"></a>ID3D11Device :: CreateTexture1D



<table>
<thead>
<tr class="header">
<th>Niveau de fonctionnalité</th>
<th>Différences de comportement</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatetexture2d"></a>ID3D11Device :: CreateTexture2D

Les ressources Texture2D ont des limites de largeur et de hauteur qui diffèrent selon les [niveaux de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md). Dans les niveaux de fonctionnalité 9 \_ 3, les éléments suivants sont des minima garantis et les implémentations individuelles peuvent dépasser les exigences.



| Niveau de fonctionnalité             | Si MipCount > 1, les dimensions doivent être une puissance intégrale de deux | Dimension de texture minimale prise en charge | Les dimensions des textures de cube doivent être une puissance de deux | Si MISC \_ TEXTURECUBE est défini, arraySize est : | Si MISC \_ TEXTURECUBE n’est pas défini, arraySize a la valeur. |
|---------------------------|--------------------------------------------------------------|-------------------------------------|-----------------------------------------------|------------------------------------------------|----------------------------------------------------|
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1 | Oui                                                          | 2 048                                | Oui                                           | 6                                              | 1                                                  |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2 | Oui                                                          | 2 048                                | Oui                                           | 6                                              | 1                                                  |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3 | Oui                                                          | 4096                                | Oui                                           | 6                                              | 1                                                  |



 

Dans le tableau précédent, le nom complet de **\_ TEXTURECUBE divers** est [**d3d11 \_ Resource \_ misc \_ TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag).

Les éléments suivants sont vrais pour les 9 \_ \* [niveaux de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md):

-   Lors de l’utilisation de D3D11 \_ \_ par défaut ou de l’utilisation de d3d11 \_ \_ immuable, BindFlags ne peut pas être égal à zéro.
-   Lors de l’utilisation du \_ \_ \_ stencil de profondeur de liaison d3d11, miplevels a doit être 1.
-   Lors de l' \_ utilisation \_ de la ressource de nuanceur de liaison d3d11 \_ , SampleDesc. Count doit avoir la valeur 1.
-   Lors de l’utilisation d’une \_ liaison d3d11 \_ présente, la ressource ne peut pas avoir de \_ ressource de nuanceur de liaison d3d11 \_ \_ .
-   Lors de l’utilisation \_ de la ressource D3D10 DDI \_ \_ misc \_ Shared, le format ne peut pas être dxgi \_ format \_ R8G8B8A8 \_ UNORM ou dxgi \_ format R8G8B8A8 \_ \_ UNORM \_ sRGB.

## <a name="id3d11devicecreatetexture3d"></a>ID3D11Device :: CreateTexture3D



| Niveau de fonctionnalité             | Dimension maximum (tout axe) | Les dimensions doivent être une puissance de deux |
|---------------------------|------------------------------|---------------------------------|
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1 | 256                          | Oui                             |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2 | 512                          | Oui                             |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3 | 512                          | Oui                             |



 

Si la ressource est une \_ utilisation d3d11 \_ par défaut ou \_ une utilisation d3d11 \_ immuable, BindFlags ne peut pas être égal à zéro.

## <a name="id3d11devicecreateunorderedaccessview"></a>ID3D11Device :: CreateUnorderedAccessView



<table>
<thead>
<tr class="header">
<th>Niveau de fonctionnalité</th>
<th>Différences de comportement</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatevertexshader"></a>ID3D11Device :: CreateVertexShader



| Niveau de fonctionnalité             | Différences de comportement                                    |
|---------------------------|---------------------------------------------------------|
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1 | Doit utiliser vs \_ 4 \_ 0 \_ niveau \_ 9 \_ 1                          |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2 | Doit utiliser vs \_ 4 \_ 0 \_ niveau \_ 9 \_ 1                          |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3 | Doit utiliser vs \_ 4 \_ 0 \_ niveau \_ 9 \_ 3 ou vs \_ 4 \_ 0 \_ niveau \_ 9 \_ 1 |



 

## <a name="id3d11deviceopensharedresource"></a>ID3D11Device :: OpenSharedResource



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Niveau de fonctionnalité</th>
<th>Différences de comportement</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3"> Utilisez <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device :: CheckFeatureSupport</strong></a> avec la valeur <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> et la structure <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> pour déterminer si un format peut être partagé. Si le format peut être partagé, <strong>CheckFeatureSupport</strong> retourne l’indicateur <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> .<br/>
<blockquote>
[!Note]<br />
[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>] (/Windows/Desktop/API/dxgiformat/ne-dxgiformat-dxgi_format) et <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> ne peuvent jamais être partagés lors de l’utilisation du niveau de fonctionnalité 9, même si l’appareil indique une prise en charge facultative des fonctionnalités pour <strong>D3D11_FORMAT_SUPPORT_SHAREABLE</strong>. La tentative de création de ressources partagées avec des formats DXGI <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> et <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> échouera toujours, à moins que le niveau de fonctionnalité soit 10_0 ou supérieur.
</blockquote>
<br/> $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence 10Level9](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

