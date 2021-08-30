---
title: Principales énumérations
description: Les énumérations suivantes sont déclarées dans d3d12. h.
ms.assetid: 76E76C85-128E-4F0E-9711-C72C4CF6C835
ms.localizationpriority: low
ms.topic: article
ms.date: 09/19/2019
ms.openlocfilehash: b7991584cb72c147c65166622099b9d113d5f22f
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812926"
---
# <a name="core-enumerations"></a>Principales énumérations

Les énumérations suivantes sont déclarées dans d3d12. h.

## <a name="in-this-section"></a>Dans cette section

| Rubrique et description |
|-|
| [**D3D_ROOT_SIGNATURE_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version). Spécifie la version de la disposition de signature racine. |
| [**D3D_SHADER_MODEL**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model). Spécifie un modèle de nuanceur. |
| [**D3D12_AUTO_BREADCRUMB_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_auto_breadcrumb_op). Définit des constantes qui spécifient des opérations GPU de rendu/calcul. |
| [**D3D12_BACKGROUND_PROCESSING_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_background_processing_mode). Définit des constantes qui spécifient un niveau d’optimisation dynamique à appliquer au travail GPU qui est ensuite envoyé. |
| [**D3D12_BLEND**](/windows/win32/api/d3d12/ne-d3d12-d3d12_blend). Spécifie les facteurs de mélange, qui modulent les valeurs du nuanceur de pixels et de la cible de rendu. |
| [**D3D12_BLEND_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_blend_op). Spécifie les opérations de fusion RVB ou alpha. |
| [**D3D12_BUFFER_SRV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags). Identifie comment afficher une ressource de mémoire tampon. |
| [**D3D12_BUFFER_UAV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags). Identifie les options de vue d’accès non ordonnées pour une ressource de mémoire tampon. |
| [**D3D12_CLEAR_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_clear_flags). Spécifie les éléments à effacer de la vue du stencil de profondeur. |
| [**D3D12_COLOR_WRITE_ENABLE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_color_write_enable). Identifie les composants de chaque pixel d’une cible de rendu accessibles en écriture pendant la fusion. |
| [**D3D12_COMMAND_LIST_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_support_flags). Utilisé pour déterminer les genres de listes de commandes qui peuvent prendre en charge diverses opérations. |
| [**D3D12_COMMAND_LIST_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type). Spécifie le type d’une liste de commandes. |
| [**D3D12_COMMAND_QUEUE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_queue_flags). Spécifie les indicateurs à utiliser lors de la création d’une file d’attente de commandes. |
| [**D3D12_COMMAND_QUEUE_PRIORITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_queue_priority). Définit des niveaux de priorité pour une file d’attente de commandes. |
| [**D3D12_COMPARISON_FUNC**](/windows/win32/api/d3d12/ne-d3d12-d3d12_comparison_func). Spécifie les options de comparaison. |
| [**D3D12_CONSERVATIVE_RASTERIZATION_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode). Indique si la pixellisation conservatrice est activée ou désactivée. |
| [**D3D12_CONSERVATIVE_RASTERIZATION_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_tier). Identifie le niveau de niveau de pixellisation conservatrice. |
| [**D3D12_CPU_PAGE_PROPERTY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cpu_page_property). Spécifie les propriétés de la page de l’UC pour le tas. |
| [**D3D12_CROSS_NODE_SHARING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier). Spécifie le niveau de partage entre les nœuds d’un adaptateur, par exemple le niveau 1 émulé, le niveau 1 ou le niveau 2.  |
| [**D3D12_CULL_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cull_mode). Spécifie des triangles dans lesquels une direction particulière n’est pas dessinée. |
| [**D3D12_DEBUG_DEVICE_PARAMETER_TYPE**](/windows/win32/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type). Spécifie le type de données de la mémoire vers laquelle pointe le paramètre *pData* de [**ID3D12DebugDevice1 :: SetDebugParameter**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter) et [**ID3D12DebugDevice1 :: GetDebugParameter**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter). |
| [**D3D12_DEPTH_WRITE_MASK**](/windows/win32/api/d3d12/ne-d3d12-d3d12_depth_write_mask). Identifie la partie d’une mémoire tampon de stencil de profondeur pour l’écriture des données de profondeur. |
| [**D3D12_DESCRIPTOR_HEAP_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags). Spécifie des options pour un segment de mémoire. |
| [**D3D12_DESCRIPTOR_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type). Spécifie un type de tas de descripteur.  |
| [**D3D12_DESCRIPTOR_RANGE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags). Spécifie la volatilité des deux descripteurs et des données qu’ils référencent dans une description de signature racine 1,1, qui peut activer certaines optimisations du pilote. |
| [**D3D12_DESCRIPTOR_RANGE_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_type). Spécifie une plage de sorte que, par exemple, si une partie d’une table de descripteurs a des vues de ressources de nuanceur 100 (SRVs), cette plage peut être déclarée dans une entrée au lieu de 100.  |
| [**D3D12_DRED_ALLOCATION_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_allocation_type). Définit des constantes qui spécifient des opérations GPU de rendu/calcul. |
| [**D3D12_DRED_ENABLEMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_enablement). Définit des constantes (utilisées par l' [interface ID3D12DeviceRemovedExtendedDataSettings](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings)) qui spécifient la façon dont les fonctionnalités de données étendues supprimées (ordinateur) sont activées. |
| [**D3D12_DRED_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_flags). Définit des constantes utilisées dans la [structure D3D12_DEVICE_REMOVED_EXTENDED_DATA](/windows/win32/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data) pour spécifier des indicateurs de contrôle pour le runtime Direct3D. |
| [**D3D12_DRED_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_version). Définit des constantes qui spécifient une version des données étendues supprimées (ordinateur) de l’appareil, tel qu’il est utilisé par la [structure D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_device_removed_extended_data). |
| [**D3D12_DSV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dsv_dimension). Spécifie comment accéder à une ressource utilisée dans une vue de stencil de profondeur. |
| [**D3D12_DSV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dsv_flags). Spécifie les options d’affichage du stencil de profondeur. |
| [**D3D12_FEATURE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature). Options de fonctionnalité Direct3D 12 qui sont prises en charge par le pilote Graphics actuel.  |
| [**D3D12_FENCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags). Spécifie les options de clôture.  |
| [**D3D12_FILL_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fill_mode). Spécifie le mode de remplissage à utiliser lors du rendu des triangles. |
| [**D3D12_FILTER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter). Spécifie les options de filtrage lors de l’échantillonnage de texture. |
| [**D3D12_FILTER_REDUCTION_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter_reduction_type). Spécifie le type de réduction du filtre.  |
| [**D3D12_FILTER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter_type). Spécifie le type de filtres d’agrandissement ou de réduction de l’échantillonneur.  |
| [**D3D12_FORMAT_SUPPORT1**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support1). Spécifie les ressources qui sont prises en charge pour un format fourni. |
| [**D3D12_FORMAT_SUPPORT2**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support2). Spécifie les options de ressources non ordonnées prises en charge pour un format fourni. |
| [**D3D12_GRAPHICS_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_graphics_states). Définit des indicateurs qui spécifient des États associés à une liste de commandes Graphics. Les valeurs peuvent être assorties d’une opération or au niveau du bit. |
| [**D3D12_HEAP_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags). Spécifie les options du tas, par exemple si le tas peut contenir des textures et si les ressources sont partagées entre les adaptateurs.  |
| [**D3D12_HEAP_SERIALIZATION_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_serialization_tier). Définit des constantes qui spécifient la prise en charge de la sérialisation du tas. |
| [**D3D12_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type). Spécifie le type de segment de mémoire. Lorsque résident, les tas résident dans un pool de mémoire physique particulier avec certaines propriétés de cache de l’UC.  |
| [**D3D12_INDEX_BUFFER_STRIP_CUT_VALUE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value). Lors de l’utilisation de la topologie de la suppression de la bande de triangle, les positions de vertex sont interprétées comme des sommets d’une bande triangulaire continue. Il existe une valeur d’index spéciale qui représente le souhait d’avoir une discontinuité dans la bande, la valeur d’index de coupe. Cette énumération répertorie les valeurs de coupe prises en charge.  |
| [**D3D12_INDIRECT_ARGUMENT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_indirect_argument_type). Spécifie le type du paramètre indirect.  |
| [**D3D12_INPUT_CLASSIFICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_input_classification). Identifie le type de données contenues dans un emplacement d’entrée. |
| [**D3D12_LIFETIME_STATE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_lifetime_state). Définit des constantes qui spécifient l’état de durée de vie d’un objet faisant l’objet d’un suivi de durée de vie. |
| [**D3D12_LOGIC_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_logic_op). Spécifie les opérations logiques à configurer pour une cible de rendu. |
| [**D3D12_MEASUREMENTS_ACTION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_measurements_action). Définit les constantes qui spécifient ce qui doit être fait avec les résultats de l’instrumentation de la charge de travail antérieure. |
| [**D3D12_MEMORY_POOL**](/windows/win32/api/d3d12/ne-d3d12-d3d12_memory_pool). Spécifie le pool de mémoire pour le tas. |
| [**D3D12_MESH_SHADER_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_mesh_shader_tier). Définit des constantes qui spécifient la prise en charge des nuanceurs de maillage et d’amplification. |
| [**D3D12_META_COMMAND_PARAMETER_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_flags). Définit des constantes qui spécifient les indicateurs d’un paramètre pour une commande méta. Les valeurs peuvent être assorties d’une opération or au niveau du bit. |
| [**D3D12_META_COMMAND_PARAMETER_STAGE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_stage). Définit des constantes qui spécifient l’étape d’un paramètre à une commande méta. |
| [**D3D12_META_COMMAND_PARAMETER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_type). Définit des constantes qui spécifient le type de données d’un paramètre pour une commande meta. |
| [**D3D12_MULTIPLE_FENCE_WAIT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multiple_fence_wait_flags). Spécifie plusieurs indicateurs d’attente pour plusieurs délimiteurs. |
| [**D3D12_MULTISAMPLE_QUALITY_LEVELS_FLAG**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags). Spécifie les options de détermination des niveaux de qualité.  |
| [**D3D12_PIPELINE_STATE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags). Indicateurs pour contrôler l’état du pipeline.  |
| [**D3D12_PIPELINE_STATE_SUBOBJECT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type). Spécifie le type d’un sous-objet dans une description du flux d’État du pipeline. |
| [**D3D12_PREDICATION_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_predication_op). Spécifie l’opération de prédicat à appliquer.  |
| [**D3D12_PRIMITIVE_TOPOLOGY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type). Spécifie comment le pipeline interprète les primitives Geometry ou d’entrée du nuanceur de coque. |
| [**D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_programmable_sample_positions_tier). Spécifie le niveau de prise en charge des positions d’échantillonnage programmable offertes par l’adaptateur. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_resource_session_flags). Définit des constantes qui spécifient des indicateurs de session de ressources protégées. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_resource_session_support_flags). Définit des constantes qui spécifient la prise en charge des sessions de ressources protégées. |
| [**D3D12_PROTECTED_SESSION_STATUS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_session_status). Définit des constantes qui spécifient l’état de session protégée. |
| [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type). Spécifie le type de segment de mémoire de requête à créer. |
| [**D3D12_QUERY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type). Spécifie le type de requête. |
| [**D3D12_RAY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_ray_flags). Indicateurs passés à la fonction [**TraceRay**](./traceray-function.md) pour remplacer la transparence, l’élimination et le comportement précoce. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BUILD_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_build_flags). Spécifie des indicateurs pour la génération d’une structure d’accélération Raytracing. Utilisez une valeur de cette énumération avec la structure [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) qui fournit l’entrée à l’opération de génération de la structure d’accélération. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_copy_mode). Spécifie le type d’opération de copie effectuée lors de l’appel de [**CopyRaytracingAccelerationStructure**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-copyraytracingaccelerationstructure). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_type). Spécifie le type des informations de génération de la structure d’accélération qui peuvent être récupérées avec les appels à [**EmitRaytracingAccelerationStructurePostbuildInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo) et [**BuildRaytracingAccelerationStructure**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_type). Spécifie le type d’une structure d’accélération Raytracing. |
| [**D3D12_RAYTRACING_GEOMETRY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags). Spécifie des indicateurs pour la géométrie Raytracing dans une structure [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc) . |
| [**D3D12_RAYTRACING_GEOMETRY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_type). Spécifie le type de géométrie utilisé pour Raytracing. Utilisez une valeur de cette énumération pour spécifier le type Geometry dans un [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc). |
| [**D3D12_RAYTRACING_INSTANCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_instance_flags). Indicateurs pour une instance de structure d’accélération Raytracing. Ces indicateurs peuvent être utilisés pour remplacer des [**D3D12_RAYTRACING_GEOMETRY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags) pour des instances individuelles. |
| [**D3D12_RAYTRACING_PIPELINE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_pipeline_flags). Définit des constantes qui spécifient des indicateurs de configuration pour un pipeline Raytracing. |
| [**D3D12_RAYTRACING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_tier). Spécifie le niveau de prise en charge du suivi de rayon sur le périphérique graphique. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_beginning_access_type). Spécifie le type d’accès qu’une application reçoit aux ressources spécifiées lors de la transition dans une passe de rendu. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_ending_access_type). Spécifie le type d’accès qu’une application reçoit aux ressources spécifiées à la transition en dehors d’une passe de rendu. |
| [**D3D12_RENDER_PASS_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_flags). Spécifie la nature de la passe de rendu ; par exemple, s’il s’agit d’une réussite de l’interruption ou de la reprise d’un rendez-vous. |
| [**D3D12_RESIDENCY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_residency_flags). Utilisé avec la fonction EnqueueMakeResident pour choisir le mode de fonctionnement des opérations de résidence lorsque le budget de mémoire est dépassé. |
| [**D3D12_RESIDENCY_PRIORITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_residency_priority). Spécifie des compartiments de priorité de délégation de site utiles pour établir rapidement un schéma de priorité d’application. |
| [**D3D12_RESOLVE_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resolve_mode). Spécifie une opération de résolution. |
| [**D3D12_RESOURCE_BARRIER_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags). Indicateurs permettant de définir les barrières des ressources fractionnées.  |
| [**D3D12_RESOURCE_BARRIER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_type). Spécifie un type de cloisonnement des ressources (transition dans l’utilisation des ressources). |
| [**D3D12_RESOURCE_BINDING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_binding_tier). Identifie le niveau de la liaison de ressource en cours d’utilisation.  |
| [**D3D12_RESOURCE_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension). Identifie le type de ressource utilisé. |
| [**D3D12_RESOURCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_flags). Spécifie les options d’utilisation des ressources.  |
| [**D3D12_RESOURCE_HEAP_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_heap_tier). Spécifie le niveau de tas de ressources pris en charge par le matériel et le pilote.  |
| [**D3D12_RESOURCE_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states). Spécifie l’état d’une ressource en ce qui concerne la façon dont la ressource est utilisée.  |
| [**D3D12_ROOT_DESCRIPTOR_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags). Spécifie la volatilité des données référencées par les descripteurs dans une description de signature racine 1,1, qui peut activer certaines optimisations du pilote. |
| [**D3D12_ROOT_PARAMETER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_parameter_type). Spécifie le type d’emplacement de signature racine.  |
| [**D3D12_ROOT_SIGNATURE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_signature_flags). Spécifie des options pour la disposition de signature racine.  |
| [**D3D12_RTV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_rtv_dimension). Identifie le type de ressource à afficher en tant que cible de rendu. |
| [**D3D12_SAMPLER_FEEDBACK_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_sampler_feedback_tier). Définit les constantes qui spécifient la prise en charge des commentaires de l’échantillonneur. |
| [**D3D12_SHADER_CACHE_CONTROL_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_cache_control_flags). Définit des constantes qui spécifient les options de contrôle du cache du nuanceur. |
| [**D3D12_SHADER_CACHE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_cache_flags). Définit des constantes qui spécifient des indicateurs de cache de nuanceur. |
| [**D3D12_SHADER_CACHE_KIND_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_cache_kind_flags). Définit des constantes qui spécifient un type de cache de nuanceur. |
| [**D3D12_SHADER_CACHE_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_cache_mode). Définit des constantes qui spécifient le mode du cache du nuanceur. |
| [**D3D12_SHADER_CACHE_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_cache_support_flags). Décrit le niveau de prise en charge de la mise en cache du nuanceur dans le pilote graphique actuel. |
| [**D3D12_SHADER_COMPONENT_MAPPING**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_component_mapping). Spécifie la façon dont la mémoire est routée par une vue de ressource de nuanceur (SRV).  |
| [**D3D12_SHADER_MIN_PRECISION_SUPPORT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_min_precision_support). Décrit les options de prise en charge de la précision minimale pour les nuanceurs dans le pilote graphique actuel.  |
| [**D3D12_SHADER_VISIBILITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_visibility). Spécifie les nuanceurs qui peuvent accéder au contenu d’un emplacement de signature racine donné. |
| [**D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shared_resource_compatibility_tier). Définit des constantes qui spécifient un niveau de prise en charge du partage inter-API. |
| [**D3D12_SRV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_srv_dimension). Identifie le type de ressource qui sera affiché en tant que ressource de nuanceur. |
| [**D3D12_STATIC_BORDER_COLOR**](/windows/win32/api/d3d12/ne-d3d12-d3d12_static_border_color). Spécifie la couleur de la bordure d’un échantillonneur statique.  |
| [**D3D12_STENCIL_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_stencil_op). Identifie les opérations de stencil qui peuvent être effectuées pendant le test du stencil de profondeur. |
| [**D3D12_TEXTURE_ADDRESS_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_address_mode). Identifie une technique pour la résolution des coordonnées de texture qui se trouvent en dehors des limites d’une texture.  |
| [**D3D12_TEXTURE_COPY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_copy_type). Spécifie le type de copie de texture à effectuer. |
| [**D3D12_TEXTURE_LAYOUT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_layout). Spécifie les options de mise en page de texture.  |
| [**D3D12_TILE_COPY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_copy_flags). Spécifie comment copier une vignette.  |
| [**D3D12_TILE_MAPPING_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_mapping_flags). Spécifie comment effectuer une opération de mappage de mosaïque.  |
| [**D3D12_TILE_RANGE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_range_flags). Spécifie une plage de mappages de mosaïques.  |
| [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier). Identifie le niveau de niveau auquel les ressources en mosaïques sont prises en charge.  |
| [**D3D12_UAV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_uav_dimension). Identifie les options de vue d’accès non ordonnées. |
| [**D3D12_VIEW_INSTANCING_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_view_instancing_flags). Spécifie des options pour l’instanciation d’affichage. |
| [**D3D12_VIEW_INSTANCING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_view_instancing_tier). Indique le niveau de niveau auquel l’instanciation de vue est prise en charge. |
| [**D3D12_WAVE_MMA_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_wave_mma_tier). Définit des constantes qui spécifient un niveau de prise en charge pour les opérations WaveMMA (wave_matrix). |
| [**D3D12_WRITEBUFFERIMMEDIATE_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_writebufferimmediate_mode). Spécifie le mode utilisé par une opération **WriteBufferImmediate** . |

## <a name="related-topics"></a>Rubriques connexes

* [Référence de base](direct3d-12-core-reference.md)
* [Informations de référence sur Direct3D 12](direct3d-12-reference.md)
