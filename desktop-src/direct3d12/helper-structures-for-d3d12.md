---
title: Structures d’assistance pour Direct3D 12
description: Ces structures d’assistance permettent d’initialiser un grand nombre des structures Direct3D 12. Elles sont déclarées dans `d3dx12.h` .
ms.assetid: 822CACCE-4A45-4104-91BD-4968A657662E
keywords:
- Structures d’assistance
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 07/28/2021
ms.openlocfilehash: 16dfa0349a815a07db810d67c21747cb767f7c39
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812368"
---
# <a name="helper-structures-for-direct3d-12"></a>Structures d’assistance pour Direct3D 12

Ces structures d’assistance permettent d’initialiser un grand nombre des structures Direct3D 12. Elles sont déclarées dans `d3dx12.h` .

`d3dx12.h` est disponible séparément des en-têtes Direct3D 12. Vous pouvez télécharger `d3dx12.h` à partir de [la bibliothèque d’assistance D3D12](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h).

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [**CD3DX12_BLEND_DESC**](cd3dx12-blend-desc.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_BLEND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_blend_desc) . |
| [**CD3DX12_BOX**](cd3dx12-box.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_BOX**](/windows/win32/api/d3d12/ns-d3d12-d3d12_box) . |
| [**CD3DX12_CLEAR_VALUE**](cd3dx12-clear-value.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_CLEAR_VALUE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_clear_value) . |
| [**CD3DX12_CPU_DESCRIPTOR_HANDLE**](cd3dx12-cpu-descriptor-handle.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_CPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) . |
| [**CD3DX12_DEFAULT**](cd3dx12-default.md) | Passe **D3D12_DEFAULT** dans un constructeur pour chaque structure d’assistance. Cette structure est simplement utilisée comme un mécanisme pour définir des paramètres par défaut sur les autres structures d’assistance. |
| [**CD3DX12_DEPTH_STENCIL_DESC**](cd3dx12-depth-stencil-desc.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_DEPTH_STENCIL_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) . |
| [**CD3DX12_DEPTH_STENCIL_DESC1**](cd3dx12-depth-stencil-desc1.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_DEPTH_STENCIL_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) . |
| [**CD3DX12_DESCRIPTOR_RANGE**](cd3dx12-descriptor-range.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_DESCRIPTOR_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range) . |
| [**CD3DX12_DESCRIPTOR_RANGE1**](cd3dx12-descriptor-range1.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_DESCRIPTOR_RANGE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range1) . |
| [**CD3DX12_DXIL_LIBRARY_SUBOBJECT**](cd3dx12-dxil-library-subobject.md) | Classe d’assistance pour la création d’un sous-objet d’état de la bibliothèque DXIL. |
| [**CD3DX12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION**](cd3dx12-dxil-subobject-to-exports-association.md) | Classe d’assistance pour la création d’un sous-objet d’état d’association DXIL-SubObject-to-exports. |
| [**CD3DX12_EXISTING_COLLECTION_SUBOBJECT**](cd3dx12-existing-collection-subobject.md) | Classe d’assistance pour la création d’un sous-objet d’état de collection existant. |
| [**CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT**](cd3dx12-global-root-signature-subobject.md) | Classe d’assistance pour la création d’un état de signature racine globale suboject. |
| [**CD3DX12_GPU_DESCRIPTOR_HANDLE**](cd3dx12-gpu-descriptor-handle.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_GPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) . |
| [**CD3DX12_HEAP_DESC**](cd3dx12-heap-desc.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_desc) . |
| [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_HEAP_PROPERTIES**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties) . |
| [**CD3DX12_HIT_GROUP_SUBOBJECT**](cd3dx12-hit-group-subobject.md) | Classe d’assistance pour la création d’un sous-objet d’état de groupe d’accès. |
| [**CD3DX12_NODE_MASK_SUBOBJECT**](cd3dx12-node-mask-subobject.md) | Classe d’assistance pour la création d’un sous-objet State qui identifie les nœuds GPU auxquels s’applique l’objet d’État. |
| [**CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT**](cd3dx12-local-root-signature-subobject.md) | Classe d’assistance pour la création d’un état de signature racine locale suboject. |
| [**CD3DX12_PACKED_MIP_INFO**](cd3dx12-packed-mip-info.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_PACKED_MIP_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_packed_mip_info) . |
| [**CD3DX12_PIPELINE_STATE_STREAM**](cd3dx12-pipeline-state-stream.md) | Structure d’assistance pour la création et l’utilisation des graphiques et des États de pipeline de calcul via une interface combinée. Consultez [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) et [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc). |
| [**CD3DX12_PIPELINE_STATE_STREAM1**](cd3dx12-pipeline-state-stream1.md) | Structure d’assistance pour la création et l’utilisation des graphiques et des États de pipeline de calcul via une interface combinée. Consultez [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) et [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc). |
| [**CD3DX12_PIPELINE_STATE_STREAM2**](cd3dx12-pipeline-state-stream2.md) | Structure d’assistance pour la création et l’utilisation des graphiques et des États de pipeline de calcul via une interface combinée. |
| [**CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC**](cd3dx12-pipeline-state-stream-blend-desc.md) | Structure d’assistance utilisée pour décrire une description de Blend comme un objet unique approprié pour une description de flux. |
| [**CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO**](cd3dx12-pipeline-state-stream-cached-pso.md) | Structure d’assistance utilisée pour décrire un PSO mis en cache comme un objet unique approprié pour une description de flux. |
| [**CD3DX12_PIPELINE_STATE_STREAM_CS**](cd3dx12-pipeline-state-stream-cs.md) | Structure d’assistance utilisée pour décrire un nuanceur de calcul sous la forme d’un objet unique approprié pour une description de flux. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL**](cd3dx12-pipeline-state-stream-depth-stencil.md) | Structure d’assistance utilisée pour décrire une description de stencil de profondeur comme un objet unique approprié pour une description de flux. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md) | Structure d’assistance utilisée pour décrire une description de stencil de profondeur comme un objet unique approprié pour une description de flux. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT**](cd3dx12-pipeline-state-stream-depth-stencil-format.md) | Structure d’assistance utilisée pour décrire le format de stencil de profondeur comme un objet unique approprié pour une description de flux. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DS**](cd3dx12-pipeline-state-stream-ds.md) | Structure d’assistance utilisée pour décrire un nuanceur de domaine en tant qu’objet unique approprié pour une description de flux. |
| [**CD3DX12_PIPELINE_STATE_STREAM_FLAGS**](cd3dx12-pipeline-state-stream-flags.md) | Structure d’assistance utilisée pour décrire les indicateurs d’état de pipeline sous la forme d’un objet unique approprié pour une description de flux. |
| [**CD3DX12_PIPELINE_STATE_STREAM_GS**](cd3dx12-pipeline-state-stream-gs.md) | Structure d’assistance utilisée pour décrire un nuanceur Geometry en tant qu’objet unique approprié pour une description de flux. |
| [**CD3DX12_PIPELINE_STATE_STREAM_HS**](cd3dx12-pipeline-state-stream-hs.md) | Structure d’assistance utilisée pour décrire un nuanceur de coque comme un objet unique approprié pour une description de flux. |
| [**CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE**](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md) | Structure d’assistance utilisée pour décrire la valeur de coupe de la bande de mémoire tampon d’index comme un objet unique approprié pour une description de flux. |
| [**CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT**](cd3dx12-pipeline-state-stream-input-layout.md) | Structure d’assistance utilisée pour décrire une disposition d’entrée sous la forme d’un objet unique approprié pour une description de flux de données. |
| [**CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK**](cd3dx12-pipeline-state-stream-node-mask.md) | Structure d’assistance utilisée pour décrire un masque de nœud comme un objet unique approprié pour une description de flux. |
| [**CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER**](cd3dx12-pipeline-state-stream-parse-helper.md) | Génère un objet CD3DX12_PIPELINE_STATE_STREAM interne à partir des détails des sous-objets passés dans les fonctions membres correspondantes. Ce struct implémente l’interface [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) . |
| [**CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY**](cd3dx12-pipeline-state-stream-primitive-topology.md) | Structure d’assistance utilisée pour décrire la topologie primitive comme un objet unique approprié pour une description de flux. |
| [**CD3DX12_PIPELINE_STATE_STREAM_PS**](cd3dx12-pipeline-state-stream-ps.md) | Structure d’assistance utilisée pour décrire un nuanceur de pixels comme un objet unique approprié pour une description de flux. |
| [**CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER**](cd3dx12-pipeline-state-stream-rasterizer.md) | Structure d’assistance utilisée pour décrire une description de rastériseur comme un objet unique approprié pour une description de flux. |
| [**CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS**](cd3dx12-pipeline-state-stream-render-target-formats.md) | Structure d’assistance utilisée pour décrire les formats de cible de rendu sous la forme d’un objet unique approprié pour une description de flux. |
| [**CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE**](cd3dx12-pipeline-state-stream-root-signature.md) | Structure d’assistance utilisée pour décrire la signature racine comme un objet unique approprié pour une description de flux. |
| [**CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER**](cd3dx12-pipeline-state-stream-sample-desc.md) | Structure d’assistance utilisée pour décrire une description d’exemple comme un objet unique approprié pour une description de flux. |
| [**CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK**](cd3dx12-pipeline-state-stream-sample-mask.md) | Structure d’assistance utilisée pour décrire un exemple de masque comme un objet unique approprié pour une description de flux. |
| [**CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT**](cd3dx12-pipeline-state-stream-stream-output.md) | Structure d’assistance utilisée pour décrire la description de la sortie de flux comme un objet unique approprié pour une description de flux. |
| [**CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) | Structure d’assistance basée sur un modèle utilisée pour encapsuler le type de sous-objet et les paires de données de sous-objet en tant qu’objet unique approprié pour une description de flux. |
| [**CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING**](cd3dx12-pipeline-state-stream-view-instancing.md) | Structure d’assistance utilisée pour encapsuler une structure [CD3DX12_VIEW_INSTANCING_DESC](cd3dx12-view-instancing-desc.md) . Permet aux nuanceurs de s’afficher dans plusieurs vues avec un seul appel de dessin ; utile pour la vision stéréo ou la génération de carte cubique. |
| [**CD3DX12_PIPELINE_STATE_STREAM_VS**](cd3dx12-pipeline-state-stream-vs.md) | Structure d’assistance utilisée pour décrire un nuanceur de sommets en tant qu’objet unique approprié pour une description de flux. |
| [**CD3DX12_RANGE**](cd3dx12-range.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range) . |
| [**CD3DX12_RANGE_UINT64**](cd3dx12-range-uint64.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range_uint64) . |
| [**CD3DX12_RASTERIZER_DESC**](cd3dx12-rasterizer-desc.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_RASTERIZER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) . |
| [**CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT**](cd3dx12-raytracing-pipeline-config-subobject.md) | Classe d’assistance pour la création d’un sous-objet d’état de configuration du pipeline Raytracing. |
| [**CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT**](cd3dx12-raytracing-pipeline-config1-subobject.md) | Classe d’assistance pour la création d’un sous-objet d’état de configuration du pipeline Raytracing, avec des indicateurs. |
| [**CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT**](cd3dx12-raytracing-shader-config-subobject.md) | Classe d’assistance pour la création d’un sous-objet d’état de configuration du nuanceur Raytracing. |
| [**CD3DX12_RECT**](cd3dx12-rect.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_RECT**](d3d12-rect.md) . |
| [**CD3DX12_RESOURCE_ALLOCATION_INFO**](cd3dx12-resource-allocation-info.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_RESOURCE_ALLOCATION_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) . |
| [**CD3DX12_RESOURCE_BARRIER**](cd3dx12-resource-barrier.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_RESOURCE_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_barrier) . |
| [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_RESOURCE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc) . |
| [**CD3DX12_RESOURCE_DESC1**](cd3dx12-resource-desc1.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_RESOURCE_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1) . |
| [**CD3DX12_ROOT_CONSTANTS**](cd3dx12-root-constants.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_ROOT_CONSTANTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_constants) . |
| [**CD3DX12_ROOT_DESCRIPTOR**](cd3dx12-root-descriptor.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_ROOT_DESCRIPTOR**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor) . |
| [**CD3DX12_ROOT_DESCRIPTOR1**](cd3dx12-root-descriptor1.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_ROOT_DESCRIPTOR1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor1) . |
| [**CD3DX12_ROOT_DESCRIPTOR_TABLE**](cd3dx12-root-descriptor-table.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_ROOT_DESCRIPTOR_TABLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) . |
| [**CD3DX12_ROOT_DESCRIPTOR_TABLE1**](cd3dx12-root-descriptor-table1.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_ROOT_DESCRIPTOR_TABLE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) . |
| [**CD3DX12_ROOT_PARAMETER**](cd3dx12-root-parameter.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_ROOT_PARAMETER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter) . |
| [**CD3DX12_ROOT_PARAMETER1**](cd3dx12-root-parameter1.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_ROOT_PARAMETER1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter1) . |
| [**CD3DX12_ROOT_SIGNATURE_DESC**](cd3dx12-root-signature-desc.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc) . |
| [**CD3DX12_RT_FORMAT_ARRAY**](cd3dx12-rt-format-array.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_RT_FORMAT_ARRAY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rt_format_array) . |
| [**CD3DX12_SHADER_BYTECODE**](cd3dx12-shader-bytecode.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_SHADER_BYTECODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode) . |
| [**CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT**](cd3dx12-state-object-config-subobject.md) | Classe d’assistance pour la création d’un sous-objet qui définit les propriétés générales d’un objet d’État. |
| [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) | Classe centrale des applications auxiliaires de création d’objets d’État D3DX12, qui sont des classes d’assistance pour la création d’objets d’État à partir d’un ensemble arbitraire de sous-objets. |
| [**CD3DX12_STATIC_SAMPLER_DESC**](cd3dx12-static-sampler-desc.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_STATIC_SAMPLER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) . |
| [**CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT**](cd3dx12-subobject-to-exports-association-subobject.md) | Classe d’assistance pour la création d’un sous-objet d’état d’association de sous-objet à exporter. |
| [**CD3DX12_SUBRESOURCE_FOOTPRINT**](cd3dx12-subresource-footprint.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_SUBRESOURCE_FOOTPRINT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_footprint) . |
| [**CD3DX12_SUBRESOURCE_RANGE_UINT64**](cd3dx12-subresource-range-uint64.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_SUBRESOURCE_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) . |
| [**CD3DX12_SUBRESOURCE_TILING**](cd3dx12-subresource-tiling.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_SUBRESOURCE_TILING**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_tiling) . |
| [**CD3DX12_TEXTURE_COPY_LOCATION**](cd3dx12-texture-copy-location.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_TEXTURE_COPY_LOCATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texture_copy_location) . |
| [**CD3DX12_TILE_REGION_SIZE**](cd3dx12-tile-region-size.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_TILE_REGION_SIZE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_region_size) . |
| [**CD3DX12_TILE_SHAPE**](cd3dx12-tile-shape.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_TILE_SHAPE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_shape) . |
| [**CD3DX12_TILED_RESOURCE_COORDINATE**](cd3dx12-tiled-resource-coordinate.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) . |
| [**CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC**](cd3dx12-versioned-root-signature-desc.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_VERSIONED_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) . |
| [**CD3DX12_VIEW_INSTANCING_DESC**](cd3dx12-view-instancing-desc.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc) . |
| [**CD3DX12_VIEWPORT**](cd3dx12-viewport.md) | Structure d’assistance pour faciliter l’initialisation d’une structure [**D3D12_VIEWPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport) . |
| [**D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**](d3dx12-mesh-shader-pipeline-state-desc.md) | Pour les [nuanceurs de maillage/amplifications](https://microsoft.github.io/DirectX-Specs/d3d/MeshShader.html), vous pouvez utiliser les données d’un [EffectPipelineStateDescription](https://github.com/Microsoft/DirectXTK12/wiki/EffectPipelineStateDescription), avec **D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**, pour fournir tout l’État. |

## <a name="related-topics"></a>Rubriques connexes

* [Structures et fonctions d’assistance pour D3D12](helper-structures-and-functions-for-d3d12.md)
* [Informations de référence sur Direct3D 12](direct3d-12-reference.md)
