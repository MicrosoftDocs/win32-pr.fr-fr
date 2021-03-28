---
title: Principales énumérations Direct3D 11
description: Cette section contient des informations sur les énumérations principales.
ms.assetid: 1641713a-5ac8-4597-900b-1bba54f9f522
keywords:
- énumérations, Direct3D 11 Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b012ae34367ef849bebf3fb25780310fcb924ba9
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104383216"
---
# <a name="direct3d-11-core-enumerations"></a>Principales énumérations Direct3D 11

Cette section contient des informations sur les énumérations principales.

## <a name="in-this-section"></a>Contenu de cette section

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rubrique</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_async_getdata_flag"><strong>D3D11_ASYNC_GETDATA_FLAG</strong></a><br/></td>
<td>Indicateurs facultatifs qui contrôlent le comportement de <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-getdata"><strong>ID3D11DeviceContext :: GetData</strong></a>.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend"><strong>D3D11_BLEND</strong></a><br/></td>
<td>Facteurs de mélange, qui modulent les valeurs pour le nuanceur de pixels et la cible de rendu.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend_op"><strong>D3D11_BLEND_OP</strong></a><br/></td>
<td>Opération de fusion RVB ou alpha.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_clear_flag"><strong>D3D11_CLEAR_FLAG</strong></a><br/></td>
<td>Spécifie les parties du stencil de profondeur à effacer. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_color_write_enable"><strong>D3D11_COLOR_WRITE_ENABLE</strong></a><br/></td>
<td>Identifiez les composants de chaque pixel d’une cible de rendu accessibles en écriture pendant la fusion.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_comparison_func"><strong>D3D11_COMPARISON_FUNC</strong></a><br/></td>
<td>Options de comparaison.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_conservative_rasterization_mode"><strong>D3D11_CONSERVATIVE_RASTERIZATION_MODE</strong></a><br/></td>
<td>Indique si la pixellisation conservatrice est activée ou désactivée.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_conservative_rasterization_tier"><strong>D3D11_CONSERVATIVE_RASTERIZATION_TIER</strong></a><br/></td>
<td>Spécifie si le matériel et le pilote prennent en charge la pixellisation conservatrice et à quel niveau de niveau.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_context_type"><strong>D3D11_CONTEXT_TYPE</strong></a><br/></td>
<td>Spécifie le contexte dans lequel une requête se produit.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_copy_flags"><strong>D3D11_COPY_FLAGS</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette énumération est prise en charge par le runtime Direct3D 11,1, disponible sur les systèmes d’exploitation Windows 8 et versions ultérieures.
</blockquote>
<br/> Spécifie comment gérer le contenu existant d’une ressource pendant une opération de copie ou de mise à jour d’une région au sein de cette ressource.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter"><strong>D3D11_COUNTER</strong></a><br/></td>
<td>Options des compteurs de performances.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter_type"><strong>D3D11_COUNTER_TYPE</strong></a><br/></td>
<td>Type de données d’un compteur de performance.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_create_device_flag"><strong>D3D11_CREATE_DEVICE_FLAG</strong></a><br/></td>
<td>Décrit les paramètres utilisés pour créer un appareil.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_1_create_device_context_state_flag"><strong>D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG</strong></a><br/></td>
<td>Décrit les indicateurs utilisés pour créer un objet d’état de contexte de périphérique (<a href="/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a>) avec la méthode <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate"><strong>ID3D11Device1 :: CreateDeviceContextState</strong></a> .<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_cull_mode"><strong>D3D11_CULL_MODE</strong></a><br/></td>
<td>Indique que les triangles face à une direction particulière ne sont pas dessinés.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_depth_write_mask"><strong>D3D11_DEPTH_WRITE_MASK</strong></a><br/></td>
<td>Identifiez la partie d’une mémoire tampon de stencil de profondeur pour l’écriture des données de profondeur.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_device_context_type"><strong>D3D11_DEVICE_CONTEXT_TYPE</strong></a><br/></td>
<td>Options de contexte de périphérique.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE</strong></a><br/></td>
<td>Options de la fonctionnalité Direct3D 11.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11_3/ne-d3d11_3-d3d11_fence_flag"><strong>D3D11_FENCE_FLAG</strong></a><br/></td>
<td>Spécifie les options de clôture. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_fill_mode"><strong>D3D11_FILL_MODE</strong></a><br/></td>
<td>Détermine le mode de remplissage à utiliser lors du rendu des triangles.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter"><strong>D3D11_FILTER</strong></a><br/></td>
<td>Options de filtrage lors de l’échantillonnage de texture.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter_type"><strong>D3D11_FILTER_TYPE</strong></a><br/></td>
<td>Types de filtres d’agrandissement ou de minimisation de l’échantillonneur.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_filter_reduction_type"><strong>D3D11_FILTER_REDUCTION_TYPE</strong></a><br/></td>
<td>Spécifie le type de réduction du filtre de l’échantillonneur. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a><br/></td>
<td>Quelles ressources sont prises en charge pour un format donné et un appareil donné (consultez <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkformatsupport"><strong>ID3D11Device :: CheckFormatSupport</strong></a> et <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device :: CheckFeatureSupport</strong></a>).<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a><br/></td>
<td>Options de prise en charge des ressources non triées pour une ressource de nuanceur de calcul (voir <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device :: CheckFeatureSupport</strong></a>). <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_input_classification"><strong>D3D11_INPUT_CLASSIFICATION</strong></a><br/></td>
<td>Type de données contenues dans un emplacement d’entrée.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_logic_op"><strong>D3D11_LOGIC_OP</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette énumération est prise en charge par le runtime Direct3D 11,1, disponible sur les systèmes d’exploitation Windows 8 et versions ultérieures.
</blockquote>
<br/> Spécifie les opérations logiques à configurer pour une cible de rendu.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive"><strong>D3D11_PRIMITIVE</strong></a><br/></td>
<td>Indique comment le pipeline interprète les primitives Geometry ou d’entrée du nuanceur de coque. <br/></td>
</tr>
<tr>
<td><a href="/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)"><strong>D3D11_PRIMITIVE_TOPOLOGY</strong></a><br/></td>
<td>Comment le pipeline interprète les données de vertex qui sont liées à l’étape assembleur d’entrée. Ces valeurs de topologie primitives déterminent la façon dont les données de vertex sont restituées à l’écran.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query"><strong>D3D11_QUERY</strong></a><br/></td>
<td>Types de requêtes.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query_misc_flag"><strong>D3D11_QUERY_MISC_FLAG</strong></a><br/></td>
<td>Indicateurs qui décrivent le comportement des requêtes divers.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_raise_flag"><strong>D3D11_RAISE_FLAG</strong></a><br/></td>
<td>Option (s) pour déclencher une erreur vers une exception non continuable.<br/></td>
</tr>
<tr>
<td><a href="https://www.bing.com/search?q=<strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong>"><strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong></a><br/></td>
<td>Décrit le niveau de prise en charge de la mise en cache du nuanceur dans le pilote graphique actuel.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_shader_min_precision_support"><strong>D3D11_SHADER_MIN_PRECISION_SUPPORT</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette énumération est prise en charge par le runtime Direct3D 11,1, disponible sur les systèmes d’exploitation Windows 8 et versions ultérieures.
</blockquote>
<br/> Valeurs qui spécifient des niveaux de précision minimum aux étapes du nuanceur.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_shared_resource_tier"><strong>D3D11_SHARED_RESOURCE_TIER</strong></a><br/></td>
<td>Définit des constantes qui spécifient un niveau pour la prise en charge des ressources partagées.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_stencil_op"><strong>D3D11_STENCIL_OP</strong></a><br/></td>
<td>Opérations de stencil qui peuvent être effectuées pendant le test du stencil de profondeur.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texture_address_mode"><strong>D3D11_TEXTURE_ADDRESS_MODE</strong></a><br/></td>
<td>Identifiez une technique de résolution des coordonnées de texture qui se trouvent en dehors des limites d’une texture.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texturecube_face"><strong>D3D11_TEXTURECUBE_FACE</strong></a><br/></td>
<td>Différentes faces d’une texture de cube.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier"><strong>D3D11_TILED_RESOURCES_TIER</strong></a><br/></td>
<td>Indique le niveau de niveau auquel les ressources en mosaïques sont prises en charge.<br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>Rubriques connexes

[Référence de base](d3d11-graphics-reference-d3d11-core.md)