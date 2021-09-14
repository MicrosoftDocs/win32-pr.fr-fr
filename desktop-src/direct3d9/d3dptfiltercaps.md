---
description: Constantes de filtrage de texture.
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06624f4f8779a866d440212c205baa9b4a84839a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922612"
---
# <a name="d3dptfiltercaps"></a>D3DPTFILTERCAPS

Constantes de filtrage de texture.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#définition</td>
<td>Description</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_CONVOLUTIONMONO</td>
<td>L’appareil prend en charge le filtrage de convolution monochrome. Ce filtre est représenté par le membre D3DTEXF_CONVOLUTIONMONO du type énuméré <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> . 
<table>
<tbody>
<tr class="odd">
<td>Différences entre Direct3D 9 et Direct3D 9Ex :<br/> Cet indicateur est disponible uniquement dans Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFPOINT</td>
<td>L’appareil prend en charge le filtrage par point-échantillon par étape pour agrandir les textures. Le filtre d’agrandissement de l’échantillon de point est représenté par le D3DTEXF_POINT membre du type énuméré <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MAGFLINEAR</td>
<td>L’appareil prend en charge le filtrage de l’interpolation bilinéaire par étape pour agrandir les des mipmaps. Le filtre d’interpolation bilinéaire mappage MIP est représenté par le membre D3DTEXF_LINEAR du type énuméré <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFANISOTROPIC</td>
<td>L’appareil prend en charge le filtrage anisotrope par étape pour agrandir les textures. Le filtre d’agrandissement anisotrope est représenté par le D3DTEXF_ANISOTROPIC membre du type énuméré <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</td>
<td>L’appareil prend en charge l’exemple de filtrage pyramidal par étape pour agrandir les textures. Le filtre d’agrandissement pyramidal est représenté par le D3DTEXF_PYRAMIDALQUAD membre du type énuméré <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</td>
<td>L’appareil prend en charge le filtrage gaussien Quad par étape pour agrandir les textures.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFPOINT</td>
<td>L’appareil prend en charge le filtrage par point-échantillon par étape pour les textures minimisation. Le filtre de réduction d’échantillon de point est représenté par le membre D3DTEXF_POINT du type énuméré <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFLINEAR</td>
<td>L’appareil prend en charge le filtrage linéaire par étape pour les textures minimisation. Le filtre de réduction linéaire est représenté par le D3DTEXF_LINEAR membre du type énuméré <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFANISOTROPIC</td>
<td>L’appareil prend en charge le filtrage anisotrope par étape pour les textures minimisation. Le filtre de minimisation anisotrope est représenté par le D3DTEXF_ANISOTROPIC membre du type énuméré <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</td>
<td>L’appareil prend en charge le filtrage par étape de l’exemple pyramidal pour les textures minimisation.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFGAUSSIANQUAD</td>
<td>L’appareil prend en charge le filtrage gaussien Quad par étape pour les textures minimisation.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MIPFPOINT</td>
<td>L’appareil prend en charge le filtrage par point-échantillon par étape pour des mipmaps. Le filtre mappage MIP point-Sample est représenté par le membre D3DTEXF_POINT du type énuméré <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MIPFLINEAR</td>
<td>L’appareil prend en charge le filtrage de l’interpolation bilinéaire par étape pour des mipmaps. Le filtre d’interpolation bilinéaire mappage MIP est représenté par le membre D3DTEXF_LINEAR du type énuméré <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
</tbody>
</table>



 

Ces constantes sont utilisées par les membres TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps et VertexTextureFilterCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Informations constantes



|  Condition requise                        | Valeur           |
|--------------------------|------------|
| En-tête                   | d3d9caps. h |
| Système d’exploitation minimal | Windows 98 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
