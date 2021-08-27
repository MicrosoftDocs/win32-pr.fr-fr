---
description: Cette section explique comment vérifier la prise en charge du format pour le matériel de niveau de fonctionnalité Direct3D à l’aide d’appels d’API.
ms.assetid: 0C40C73E-06F3-41FA-AA27-2C0B730B357B
title: Prise en charge de la fonctionnalité de vérification du matériel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eecaebdb3b8d4825e2be72bf9fa9758186f5f192832e1442779b90d05c62c9a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025689"
---
# <a name="checking-hardware-feature-support"></a>Prise en charge de la fonctionnalité de vérification du matériel

Cette section explique comment vérifier la prise en charge du format pour le matériel de niveau de fonctionnalité Direct3D à l’aide d’appels d’API.

Pour D3D11, utilisez [**ID3D11Device :: CheckFormatSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkformatsupport) pour vérifier par programme les informations dans les sections précédentes. Pour D3D12, utilisez [**ID3D12 :: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Mettre en forme la cible</th>
<th>D3D12</th>
<th>D3D11</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Buffer</td>
<td>D3D12_FORMAT_SUPPORT1_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Mémoire tampon du vertex assembleur d’entrée</td>
<td>D3D12_FORMAT_SUPPORT1_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Tampon d’index assembleur d’entrée</td>
<td>D3D12_FORMAT_SUPPORT1_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Mémoire tampon de sortie de flux</td>
<td>D3D12_FORMAT_SUPPORT1_SO_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_SO_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Texture1D</td>
<td>D3D12_FORMAT_SUPPORT1_TEXTURE1D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_TEXTURE1D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Texture2D</td>
<td>D3D12_FORMAT_SUPPORT1_TEXTURE2D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_TEXTURE2D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Texture3D</td>
<td>D3D12_FORMAT_SUPPORT1_TEXTURE3D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_TEXTURE3D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>TextureCube</td>
<td>D3D12_FORMAT_SUPPORT1_TEXTURECUBE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_TEXTURECUBE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Nuanceur LD</td>
<td>D3D12_FORMAT_SUPPORT1_SHADER_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_SHADER_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Exemple de nuanceur (n’importe quel filtre)</td>
<td>D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Sample_c du nuanceur (filtre de comparaison)</td>
<td>D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Exemple de nuanceur (mono 1_bit_filter)</td>
<td>D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Nuanceur gather4</td>
<td>D3D12_FORMAT_SUPPORT1_SHADER_GATHER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_SHADER_GATHER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Gather4_c de nuanceur</td>
<td>D3D12_FORMAT_SUPPORT1_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>MIP</td>
<td>D3D12_FORMAT_SUPPORT1_MIP (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_MIP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Génération automatique de mipmap</td>
<td><blockquote>
[!Note]<br />
D3D12 n’a plus de fonctionnalité de génération de mipmap dédiée. Les applications doivent les implémenter de manière autonome à l’aide de nuanceurs.
</blockquote>
<br/></td>
<td>D3D11_FORMAT_SUPPORT_MIP_AUTOGEN (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>RenderTarget</td>
<td>D3D12_FORMAT_SUPPORT1_RENDER_TARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_RENDER_TARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>RenderTarget Blendable</td>
<td>D3D12_FORMAT_SUPPORT1_BLENDABLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_BLENDABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Sortie fusion Logic op</td>
<td>D3D12_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP</td>
<td>D3D11_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="even">
<td>Cible de la profondeur/du stencil</td>
<td>D3D12_FORMAT_SUPPORT1_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>UAV et SRV bruts</td>


</tr>
<tr class="even">
<td>UAV et SRV structurés</td>


</tr>
<tr class="odd">
<td>UAV typé</td>
<td>D3D12_FORMAT_SUPPORT1_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Magasin typé UAV</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="odd">
<td>Charge typée UAV</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="even">
<td>UAV Atomic Add</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="odd">
<td>Opérations de bits atomiques UAV</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="even">
<td>UAV Atomic CMP&Store/CMP&Exch</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="odd">
<td>Exchange Atomic UAV</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="even">
<td>Min/max signé UAV</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="odd">
<td>UAV Atomic non signé min/max</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="even">
<td>UC verrouillable</td>
<td><blockquote>
[!Note]<br />
Seul un format exclut l’accès au processeur (420_OPAQUE).
</blockquote>
<br/></td>
<td>D3D11_FORMAT_SUPPORT_CPU_LOCKABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>RenderTarget multiéchantillon 4x</td>
<td>D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>8x-échantillonnage RenderTarget</td>
<td>D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Autre nombre d’échantillons en RT</td>
<td>D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Résolution d’échantillonnages</td>
<td>D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Charge d’échantillonnage</td>
<td>D3D12_FORMAT_SUPPORT1_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Afficher Scan-Out</td>
<td>D3D12_FORMAT_SUPPORT1_DISPLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_DISPLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Cast dans la disposition binaire</td>
<td>D3D12_FORMAT_SUPPORT1_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Prise en charge du décodeur vidéo</td>
<td>D3D12_FORMAT_SUPPORT1_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Entrée du processeur vidéo</td>
<td>D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Sortie du processeur vidéo</td>
<td>D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Ressource partagée</td>
<td><blockquote>
[!Note]<br />
Les textures de tous les formats peuvent être des ressources validées partagées ou être placées dans des tas partagés.
</blockquote>
<br/></td>
<td>D3D11_FORMAT_SUPPORT2_SHAREABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="even">
<td>Mémoire tampon en dessous castable même entièrement typée</td>
<td>D3D12_FORMAT_SUPPORT1_BACK_BUFFER_CAST (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td><blockquote>
[!Note]<br />
Aucune API disponible.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Ressource en mosaïque</td>
<td>D3D12_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="even">
<td>Encodeur vidéo</td>
<td>D3D12_FORMAT_SUPPORT1_VIDEO_ENCODER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_VIDEO_ENCODER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Superposition Multiplan</td>
<td>D3D12_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Niveaux de fonctionnalité matérielle D3D12](/windows/desktop/direct3d12/hardware-feature-levels)
</dt> <dt>

[**\_format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> <dt>

[**\_ \_ Prise en charge du format d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support)
</dt> <dt>

[**\_Format d3d11 \_**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2)
</dt> <dt>

[Guide de programmation pour DXGI](dx-graphics-dxgi-overviews.md)
</dt> </dl>

