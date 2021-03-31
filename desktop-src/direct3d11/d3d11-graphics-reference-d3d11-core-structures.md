---
title: Principales structures Direct3D 11
description: Cette section contient des informations sur les structures principales.
ms.assetid: 2a45182a-7114-4075-b8b8-147f52fe7aa9
keywords:
- structures, Direct3D 11 Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7025de822265d86e5da9f1da3855d2542c76abf5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382292"
---
# <a name="direct3d-11-core-structures"></a>Principales structures Direct3D 11

Cette section contient des informations sur les structures principales.

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
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_blend_desc"><strong>D3D11_BLEND_DESC</strong></a><br/></td>
<td>Décrit l’état de fusion que vous utilisez dans un appel à <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-createblendstate"><strong>ID3D11Device :: CreateBlendState</strong></a> pour créer un objet d’état de fusion. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1"><strong>D3D11_BLEND_DESC1</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette structure est prise en charge par le runtime Direct3D 11,1, disponible sur les systèmes d’exploitation Windows 8 et versions ultérieures.
</blockquote>
<br/> Décrit l’état de fusion que vous utilisez dans un appel à <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1"><strong>ID3D11Device1 :: CreateBlendState1</strong></a> pour créer un objet d’état de fusion. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_box"><strong>D3D11_BOX</strong></a><br/></td>
<td>Définit une zone 3D.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_desc"><strong>D3D11_COUNTER_DESC</strong></a><br/></td>
<td>Décrit un compteur.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_info"><strong>D3D11_COUNTER_INFO</strong></a><br/></td>
<td>Informations sur les capacités des compteurs de performances de la carte vidéo.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc"><strong>D3D11_DEPTH_STENCIL_DESC</strong></a><br/></td>
<td>Décrit l’état du gabarit de profondeur.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc"><strong>D3D11_DEPTH_STENCILOP_DESC</strong></a><br/></td>
<td>Opérations de stencil qui peuvent être effectuées en fonction des résultats du test de stencil.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_indexed_instanced_indirect_args"><strong>D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS</strong></a><br/></td>
<td>Arguments pour le dessin d’instances indexées indirectes. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_instanced_indirect_args"><strong>D3D11_DRAW_INSTANCED_INDIRECT_ARGS</strong></a><br/></td>
<td>Arguments pour Draw indirectd instancié. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info"><strong>D3D11_FEATURE_DATA_ARCHITECTURE_INFO</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette structure est prise en charge par le runtime Direct3D 11,1, disponible sur les systèmes d’exploitation Windows 8 et versions ultérieures.
</blockquote>
<br/> Décrit les informations sur l’architecture de l’adaptateur Direct3D 11,1.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette structure est prise en charge par le runtime Direct3D 11,1, disponible sur les systèmes d’exploitation Windows 8 et versions ultérieures.
</blockquote>
<br/> Décrit les options des fonctionnalités de Direct3D 9 dans le pilote graphique actuel.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options1"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS1</strong></a><br/></td>
<td>Décrit les options des fonctionnalités de Direct3D 9 dans le pilote graphique actuel.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support"><strong>D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette structure est prise en charge par le runtime Direct3D 11,1, disponible sur les systèmes d’exploitation Windows 8 et versions ultérieures.
</blockquote>
<br/> Décrit la prise en charge des ombres Direct3D 9 dans le pilote Graphics actuel. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support"><strong>D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT</strong></a><br/></td>
<td>Indique si l’instanciation simple est prise en charge.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options"><strong>D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS</strong></a><br/></td>
<td>Décrit le nuanceur de calcul et la prise en charge des mémoires tampons brutes et structurées dans le pilote graphique actuel.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette structure est prise en charge par le runtime Direct3D 11,1, disponible sur les systèmes d’exploitation Windows 8 et versions ultérieures.
</blockquote>
<br/> Décrit les options de fonctionnalité Direct3D 11,1 dans le pilote Graphics actuel.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS1</strong></a><br/></td>
<td>Décrit les options de fonctionnalité Direct3D 11,2 dans le pilote Graphics actuel.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS2</strong></a><br/></td>
<td>Décrit les options de fonctionnalité Direct3D 11,3 dans le pilote Graphics actuel.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS3</strong></a><br/></td>
<td>Décrit les options de fonctionnalité Direct3D 11,3 dans le pilote Graphics actuel.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS4</strong></a><br/></td>
<td>Décrit les options de fonctionnalité Direct3D 11,4 dans le pilote Graphics actuel.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options5"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS5</strong></a><br/></td>
<td>Décrit le niveau de prise en charge des ressources partagées dans le pilote graphique actuel.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_doubles"><strong>D3D11_FEATURE_DATA_DOUBLES</strong></a><br/></td>
<td>Décrit la prise en charge des types de données double dans le pilote Graphics actuel.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT</strong></a><br/></td>
<td>Décrit les ressources prises en charge par le pilote Graphics actuel pour un format donné.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a><br/></td>
<td>Décrit les options de ressources non ordonnées prises en charge par le pilote Graphics actuel pour un format donné.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_gpu_virtual_address_support"><strong>D3D11_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</strong></a><br/></td>
<td>Décrit la prise en charge des adresses virtuelles du GPU des données de fonctionnalités, y compris les bits d’adresse maximaux par ressource et par processus. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support"><strong>D3D11_FEATURE_DATA_MARKER_SUPPORT</strong></a><br/></td>
<td>Indique si une technique de profilage GPU est prise en charge.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_shader_cache"><strong>D3D11_FEATURE_DATA_SHADER_CACHE</strong></a><br/></td>
<td>Décrit le niveau de mise en cache du nuanceur pris en charge dans le pilote graphique actuel.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support"><strong>D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette structure est prise en charge par le runtime Direct3D 11,1, disponible sur les systèmes d’exploitation Windows 8 et versions ultérieures.
</blockquote>
<br/> Décrit les options de prise en charge de la précision pour les nuanceurs dans le pilote graphique actuel.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_threading"><strong>D3D11_FEATURE_DATA_THREADING</strong></a><br/></td>
<td>Décrit les fonctionnalités de Multi-Threading prises en charge par le pilote graphique actuel.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_input_element_desc"><strong>D3D11_INPUT_ELEMENT_DESC</strong></a><br/></td>
<td>Description d’un élément unique pour l’étape assembleur d’entrée.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics"><strong>D3D11_QUERY_DATA_PIPELINE_STATISTICS</strong></a><br/></td>
<td>Interroger les informations sur l’activité de pipeline graphique entre les appels à <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ID3D11DeviceContext :: Begin</strong></a> et <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ID3D11DeviceContext :: end</strong></a>.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_so_statistics"><strong>D3D11_QUERY_DATA_SO_STATISTICS</strong></a><br/></td>
<td>Interroger les informations sur la quantité de données transmises aux mémoires tampons de flux de sortie entre <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ID3D11DeviceContext :: Begin</strong></a> et <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ID3D11DeviceContext :: end</strong></a>.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_timestamp_disjoint"><strong>D3D11_QUERY_DATA_TIMESTAMP_DISJOINT</strong></a><br/></td>
<td>Demander des informations sur la fiabilité d’une requête d’horodatage.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_desc"><strong>D3D11_QUERY_DESC</strong></a><br/></td>
<td>Décrit une requête.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_query_desc1"><strong>D3D11_QUERY_DESC1</strong></a><br/></td>
<td>Décrit une requête.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_rasterizer_desc"><strong>D3D11_RASTERIZER_DESC</strong></a><br/></td>
<td>Décrit l’état du rastériseur.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1"><strong>D3D11_RASTERIZER_DESC1</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette structure est prise en charge par le runtime Direct3D 11,1, disponible sur les systèmes d’exploitation Windows 8 et versions ultérieures.
</blockquote>
<br/> Décrit l’état du rastériseur.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2"><strong>D3D11_RASTERIZER_DESC2</strong></a><br/></td>
<td>Décrit l’état du rastériseur.<br/></td>
</tr>
<tr>
<td><a href="d3d11-rect.md"><strong>D3D11_RECT</strong></a><br/></td>
<td>D3D11_RECT est déclaré comme suit :<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_render_target_blend_desc"><strong>D3D11_RENDER_TARGET_BLEND_DESC</strong></a><br/></td>
<td>Décrit l’état de fusion d’une cible de rendu.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1"><strong>D3D11_RENDER_TARGET_BLEND_DESC1</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette structure est prise en charge par le runtime Direct3D 11,1, disponible sur les systèmes d’exploitation Windows 8 et versions ultérieures.
</blockquote>
<br/> Décrit l’état de fusion d’une cible de rendu.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc"><strong>D3D11_SAMPLER_DESC</strong></a><br/></td>
<td>Décrit un état de l’échantillonneur.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_so_declaration_entry"><strong>D3D11_SO_DECLARATION_ENTRY</strong></a><br/></td>
<td>Description d’un élément vertex dans une mémoire tampon de vertex dans un emplacement de sortie.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_viewport"><strong>D3D11_VIEWPORT</strong></a><br/></td>
<td>Définit les dimensions d’une fenêtre d’affichage.<br/></td>
</tr>
</tbody>
</table>

En outre, il existe une structure de rectangles 2D définie dans D3D11. h.

```cpp
typedef RECT D3D11_RECT;
```

Pour obtenir de la documentation, consultez [Rect](/previous-versions/dd162897%28v%3dvs.85%29) dans [Windows GDI](../gdi/windows-gdi.md).

## <a name="related-topics"></a>Rubriques connexes

[Référence principale](d3d11-graphics-reference-d3d11-core.md)