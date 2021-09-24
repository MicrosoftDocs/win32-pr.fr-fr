---
title: Structures principales (Direct3D 12 Graphics)
description: Les structures suivantes sont déclarées dans d3d12. h.
ms.assetid: 7FE8796A-98D1-4333-8755-2A47567460B3
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 7f656a9c8a69a0b684f411729f51d9eef37daad3
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520811"
---
# <a name="core-structures"></a>Structures de base

Les structures suivantes sont déclarées dans d3d12. h.

## <a name="in-this-section"></a>Dans cette section

| Rubrique et description |
|-|
| [**D3D12_AUTO_BREADCRUMB_NODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_auto_breadcrumb_node). Représente les données de la navigation automatique ordinateur (Device removed Extended Data) en tant que nœud dans une liste liée. |
| [**D3D12_BLEND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_blend_desc). Décrit l’état de fusion. |
| [**D3D12_BOX**](/windows/win32/api/d3d12/ns-d3d12-d3d12_box). Décrit une zone 3D. |
| [**D3D12_BUFFER_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_buffer_rtv). Décrit les éléments d’une ressource de mémoire tampon à utiliser dans une vue de cible de rendu. |
| [**D3D12_BUFFER_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_buffer_srv). Décrit les éléments d’une ressource de mémoire tampon à utiliser dans un affichage des ressources de nuanceur. |
| [**D3D12_BUFFER_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_buffer_uav). Décrit les éléments d’une mémoire tampon à utiliser dans un affichage d’accès non ordonné. |
| [**D3D12_CACHED_PIPELINE_STATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state). Stocke un état de pipeline. |
| [**D3D12_CLEAR_VALUE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_clear_value). Décrit une valeur utilisée pour optimiser les opérations Clear pour une ressource particulière. |
| [**D3D12_COMMAND_QUEUE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc). Décrit une file d’attente de commandes. |
| [**D3D12_COMMAND_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc). Décrit les arguments (paramètres) d’une signature de commande. |
| [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc). Décrit un objet d’état de pipeline de calcul. |
| [**D3D12_CONSTANT_BUFFER_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc). Décrit une mémoire tampon constante à afficher. |
| [**D3D12_CPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle). Décrit un handle de descripteur de processeur. |
| [**D3D12_DEPTH_STENCIL_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc). Décrit l’état du gabarit de profondeur. |
| [**D3D12_DEPTH_STENCIL_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1). Décrit l’état du gabarit de profondeur. |
| [**D3D12_DEPTH_STENCIL_VALUE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_value). Spécifie une valeur de gabarit et de profondeur. |
| [**D3D12_DEPTH_STENCIL_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc). Décrit les sous-ressources d’une texture qui sont accessibles à partir d’une vue de stencil de profondeur. |
| [**D3D12_DEPTH_STENCILOP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencilop_desc). Décrit les opérations de stencil qui peuvent être effectuées en fonction des résultats du test de stencil. |
| [**D3D12_DESCRIPTOR_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc). Décrit le tas du descripteur. |
| [**D3D12_DESCRIPTOR_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range). Décrit une plage de descripteurs. |
| [**D3D12_DESCRIPTOR_RANGE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range1). Décrit une plage de descripteurs, avec des indicateurs pour déterminer leur volatilité. |
| [**D3D12_DEVICE_REMOVED_EXTENDED_DATA**](/windows/win32/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data). Représente des données ordinateur (Device removed Extended Data) version 1,0. |
| [**D3D12_DEVICE_REMOVED_EXTENDED_DATA1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data1). Représente les données de suppression d’appareils ordinateur (Device removed Extended Data) version 1,1, afin que les débogueurs et les extensions de débogueur puissent accéder aux données ordinateur. |
| [**D3D12_DISCARD_REGION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_discard_region). Décrit les détails de l’opération de suppression de ressource. |
| [**D3D12_DISPATCH_ARGUMENTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dispatch_arguments). Décrit les paramètres de dispatch, à utiliser par le nuanceur de calcul. |
| [**D3D12_DRAW_ARGUMENTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_draw_arguments). Décrit les paramètres pour les instances de dessin. |
| [**D3D12_DRAW_INDEXED_ARGUMENTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_draw_indexed_arguments). Décrit les paramètres pour le dessin d’instances indexées. |
| [**D3D12_DRED_ALLOCATION_NODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dred_allocation_node). Décrit, sous la forme d’un nœud dans une liste liée, les données relatives à une allocation suivie par l’appareil, les données étendues ont été supprimées (ordinateur). |
| [**D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dred_auto_breadcrumbs_output). Contient un pointeur vers le début d’une liste liée d’objets [D3D12_AUTO_BREADCRUMB_NODE](/windows/win32/api/d3d12/ns-d3d12-d3d12_auto_breadcrumb_node) . La liste représente l’état de la navigation automatique avant la suppression de l’appareil. |
| [**D3D12_DRED_PAGE_FAULT_OUTPUT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dred_page_fault_output). Décrit les données d’allocation associées à une erreur de page GPU sur une adresse virtuelle donnée (VA). |
| [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture). Fournissez des détails sur l’architecture de l’adaptateur, en aidant les applications à optimiser les performances de certaines propriétés de l’adaptateur. |
| [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1). Fournissez des détails sur l’architecture de l’adaptateur, en aidant les applications à optimiser les performances de certaines propriétés de l’adaptateur. |
| [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority). Détaille la prise en charge de l’adaptateur pour la hiérarchisation des différents types de file d’attente de commandes. |
| [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node). Indique le niveau de prise en charge pour le partage des ressources entre les différents adaptateurs. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options). Décrit les options des fonctionnalités Direct3D 12 dans le pilote Graphics actuel. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1). Décrit le niveau de prise en charge des opérations HLSL 6,0 Wave. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2). Détaille la prise en charge par l’adaptateur de certaines fonctionnalités facultatives de Direct3D 12. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3). Permet d’indiquer le niveau de prise en charge fourni par l’adaptateur pour les fonctionnalités facultatives de Direct3D 12. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4). Indique le niveau de prise en charge des textures MSAA, du partage inter-API et des opérations de nuanceur 16 bits natifs. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5). Indique le niveau de prise en charge que l’adaptateur fournit pour les ressources en mosaïque des passes de rendu, de traçage de rayon et de vue de la ressource de nuanceur 3. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6). Indique le niveau de prise en charge fourni par l’adaptateur pour l’ombrage à taux variable (VRS) et indique si le traitement en arrière-plan est pris en charge ou non. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS7**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options7). Indique le niveau de prise en charge fourni par l’adaptateur pour les nuanceurs de maillage et d’amplification, et pour les commentaires de l’échantillonneur. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS8**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options8). Indique si les textures compressées par blocs non alignées sont prises en charge. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS9**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options9). Indique si la prise en charge existe ou non pour les nuanceurs de maille, les valeurs de *SV_RenderTargetArrayIndex* qui sont supérieures ou égales à 8, les exemples d’opérations de texture de type entier 64 bits atomiques, dérivés et dérivés dépendants, ainsi que le niveau de prise en charge pour les opérations WaveMMA (wave_matrix). |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS10**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options10). Indique si le combinateur de somme peut être utilisé, et si *SV_ShadingRate* peut être défini à partir d’un nuanceur de maille. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS11**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options11). Indique si les nombres entiers 64 bits atomiques sur les ressources des tas de descripteur sont pris en charge. |
| [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps). Utilisé pour determinine si l’adaptateur prend en charge la création de tas à partir de la mémoire système existante. Ces segments de mémoire ne sont pas destinés à un usage général, mais sont utiles à des fins de diagnostic, car ils sont assurés de persister même après l’erreur de l’adaptateur ou un événement de suppression de l’appareil. |
| [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels). Décrit les informations sur les [niveaux de fonctionnalité](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) pris en charge par le pilote graphique actuel. |
| [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_format_info). Décrit le format de données DXGI. |
| [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_format_support). Décrit les ressources prises en charge par le pilote Graphics actuel pour un format donné. |
| [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support). Détaille les limitations de l’espace d’adressage virtuel du GPU de l’adaptateur, y compris les bits d’adresse maximaux par ressource et par processus. |
| [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels). Décrit les niveaux de qualité de l’image pour un format et un nombre d’échantillons donnés. |
| [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support). Indique le niveau de prise en charge des sessions de ressources protégées. |
| [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_TYPE_COUNT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_type_count). Indique le nombre de types de session de ressources protégées. |
| [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_TYPES**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_types). Indique une liste de types de session de ressources protégées. |
| [**D3D12_FEATURE_DATA_QUERY_META_COMMAND**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_query_meta_command). Indique le niveau de prise en charge fourni par l’adaptateur pour les commandes de commande. |
| [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature). Transmettez cette structure à [**CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) pour vérifier la prise en charge de la version de signature racine. |
| [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_serialization). Indique le niveau de prise en charge pour la sérialisation du tas. |
| [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache). Décrit le niveau de mise en cache du nuanceur pris en charge dans le pilote graphique actuel. |
| [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model). Contient le modèle de nuanceur pris en charge. |
| [**D3D12_GPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle). Décrit un handle de descripteur GPU. |
| [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc). Décrit un objet d’état de pipeline Graphics. |
| [**D3D12_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_desc). Décrit un segment de mémoire. |
| [**D3D12_HEAP_PROPERTIES**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties). Décrit les propriétés du tas. |
| [**D3D12_INDEX_BUFFER_VIEW**](/windows/win32/api/d3d12/ns-d3d12-d3d12_index_buffer_view). Décrit la mémoire tampon d’index à afficher. |
| [**D3D12_INDIRECT_ARGUMENT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc). Décrit un argument indirect (un paramètre indirect) à utiliser avec une signature de commande. |
| [**D3D12_INPUT_ELEMENT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc). Décrit un élément unique pour l’étape d’assembleur d’entrée du pipeline Graphics. |
| [**D3D12_INPUT_LAYOUT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_layout_desc). Décrit les données de mémoire tampon d’entrée pour l’étape assembleur d’entrée. |
| [**D3D12_MEMCPY_DEST**](/windows/win32/api/d3d12/ns-d3d12-d3d12_memcpy_dest). Décrit la destination d’une opération de copie de mémoire. |
| [**D3D12_META_COMMAND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_meta_command_desc). Décrit une commande meta. |
| [**D3D12_META_COMMAND_PARAMETER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_meta_command_parameter_desc). Décrit un paramètre pour une commande meta. |
| [**D3D12_PACKED_MIP_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_packed_mip_info). Décrit la structure de vignette d’une ressource en mosaïque avec des mipmaps. |
| [**D3D12_PIPELINE_STATE_STREAM_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc). Décrit un flux d’état de pipeline. |
| [**D3D12_PLACED_SUBRESOURCE_FOOTPRINT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint). Décrit l’encombrement d’une sous-ressource placée, y compris le décalage et le D3D12_SUBRESOURCE_FOOTPRINT. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_protected_resource_session_desc). Décrit les indicateurs pour une session de ressources protégée, par adaptateur. |
| [**D3D12_QUERY_DATA_PIPELINE_STATISTICS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_data_pipeline_statistics). Interroger les informations sur l’activité de pipeline graphique entre les appels à [**BeginQuery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) et [**EndQuery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery). |
| [**D3D12_QUERY_DATA_SO_STATISTICS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_data_so_statistics). Décrit les données de requête pour la sortie de flux. |
| [**D3D12_QUERY_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc). Décrit l’objectif d’un segment de mémoire de requête. Un segment de mémoire de requête contient un tableau de requêtes individuelles. |
| [**D3D12_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range). Décrit une plage de mémoire. |
| [**D3D12_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range_uint64). Décrit une plage de mémoire dans un espace d’adressage 64 bits. |
| [**D3D12_RASTERIZER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rasterizer_desc). Décrit l’état du rastériseur. |
| [**D3D12_RAYTRACING_AABB**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_aabb). Représente un cadre englobant aligné sur l’axe (AABB) utilisé comme Geometry Raytracing. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_COMPACTED_SIZE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_compacted_size_desc). Décrit l’espace requis pour la structure d’accélération après compactage. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_CURRENT_SIZE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_current_size_desc). Décrit l’espace actuellement utilisé par une structure d’accélération. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_desc). Description des informations postérieures à la génération à générer à partir d’une structure d’accélération. Utilisez cette structure dans les appels à [**EmitRaytracingAccelerationStructurePostbuildInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo) et [**BuildRaytracingAccelerationStructure**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_serialization_desc). Décrit la taille et la disposition de la structure et de l’en-tête d’accélération sérialisée |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TOOLS_VISUALIZATION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_tools_visualization_desc). Décrit l’espace requis pour le décodage d’une structure d’accélération dans un format qui peut être visualisé par les outils. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_prebuild_info). Représente les informations de prégénération relatives à une structure d’accélération Raytracing. Obtient une instance de ce structure en appelant [**GetRaytracingAccelerationStructurePrebuildInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-getraytracingaccelerationstructureprebuildinfo). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_srv). Structure de vue de ressource de nuanceur (SRV) pour le stockage d’une structure d’accélération Raytracing. |
| [**D3D12_RAYTRACING_GEOMETRY_AABBS_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_aabbs_desc). Décrit un ensemble de zones englobantes alignées sur l’axe qui sont utilisées dans la structure [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) pour fournir des données d’entrée à une opération de génération de structure d’accélération RAYTRACING. |
| [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc). Décrit un ensemble de géométrie qui est utilisé dans la structure [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) pour fournir des données d’entrée à une opération de génération de structure d’accélération RAYTRACING. |
| [**D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_triangles_desc). Décrit un ensemble de triangles utilisé comme Geometry Raytracing. La géométrie vers laquelle pointe ce struct est toujours sous forme de liste de triangles, indexée ou non indexée. Les bandes de triangle ne sont pas prises en charge. |
| [**D3D12_RAYTRACING_INSTANCE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_instance_desc). Décrit une instance d’une structure d’accélération Raytracing utilisée dans la mémoire du GPU pendant le processus de génération de la structure d’accélération. |
| [**D3D12_RAYTRACING_PIPELINE_CONFIG**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config). Sous-objet état qui représente une configuration de pipeline Raytracing. |
| [**D3D12_RAYTRACING_PIPELINE_CONFIG1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config1). Sous-objet état qui représente une configuration de pipeline Raytracing, avec des indicateurs. |
| [**D3D12_RAYTRACING_SHADER_CONFIG**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config). Sous-objet état qui représente une configuration de nuanceur. |
| [**D3D12_RECT**](d3d12-rect.md). D3D12_RECT est déclarée en tant que RECT. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access). Décrit l’accès aux ressources demandées par une application lors de la transition dans une passe de rendu. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS_CLEAR_PARAMETERS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access_clear_parameters). Décrit la valeur claire à laquelle les ressources doivent être effacées au début d’une passe de rendu. |
| [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc). Décrit une liaison (fixée pour la durée de la passe de rendu) à une vue de stencil de profondeur (DSV), ainsi que ses caractéristiques d’accès de début et de fin. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access). Décrit l’accès aux ressources demandées par une application à la transition en dehors d’une passe de rendu. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_parameters). Décrit une ressource à résoudre à la fin d’une passe de rendu. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_subresource_parameters). Décrit les sous-ressources impliquées dans la résolution à la fin d’une passe de rendu. |
| [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc). Décrit les liaisons (fixes pour la durée de la passe de rendu) à une ou plusieurs vues de la cible de rendu (RTVs), ainsi que leurs caractéristiques d’accès de début et de fin. |
| [**D3D12_RENDER_TARGET_BLEND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_target_blend_desc). Décrit l’état de fusion d’une cible de rendu. |
| [**D3D12_RENDER_TARGET_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_target_view_desc). Décrit les sous-ressources d’une ressource qui sont accessibles à l’aide d’une vue de cible de rendu. |
| [**D3D12_RESOURCE_ALIASING_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier). Décrit la transition entre les utilisations de deux ressources différentes qui ont des mappages dans le même tas. |
| [**D3D12_RESOURCE_ALLOCATION_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info). Décrit les paramètres nécessaires pour allouer des ressources. |
| [**D3D12_RESOURCE_ALLOCATION_INFO1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info1). Décrit les paramètres nécessaires pour allouer des ressources, y compris l’offset. |
| [**D3D12_RESOURCE_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_barrier). Décrit une barrière de ressources (transition dans l’utilisation des ressources). |
| [**D3D12_RESOURCE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc). Décrit une ressource, telle qu’une texture. Cette structure est largement utilisée. |
| [**D3D12_RESOURCE_TRANSITION_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier). Décrit la transition des sous-ressources entre différentes utilisations. |
| [**D3D12_RESOURCE_UAV_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier). Représente une ressource dans laquelle tous les accès UAV doivent se terminer avant que des accès futurs UAV puissent commencer. |
| [**D3D12_ROOT_CONSTANTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_constants). Décrit les constantes inline dans la signature racine qui apparaissent dans les nuanceurs comme une seule mémoire tampon constante. |
| [**D3D12_ROOT_DESCRIPTOR**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor). Décrit les descripteurs inline dans la version 1,0 de la signature racine qui s’affichent dans les nuanceurs. |
| [**D3D12_ROOT_DESCRIPTOR1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor1). Décrit les descripteurs inline dans la version 1,1 de la signature racine qui s’affichent dans les nuanceurs. |
| [**D3D12_ROOT_DESCRIPTOR_TABLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table). Décrit la disposition de signature racine 1,0 d’une table de descripteurs sous la forme d’une collection de plages de descripteur qui apparaissent une après l’autre dans un tas de descripteur. |
| [**D3D12_ROOT_DESCRIPTOR_TABLE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1). Décrit la disposition de signature racine 1,1 d’une table de descripteurs sous la forme d’une collection de plages de descripteur qui apparaissent une après l’autre dans un tas de descripteur. |
| [**D3D12_ROOT_PARAMETER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter). Décrit l’emplacement d’une signature racine version 1,0. |
| [**D3D12_ROOT_PARAMETER1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter1). Décrit l’emplacement d’une signature racine version 1,1. |
| [**D3D12_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc). Décrit la disposition d’une signature racine version 1,0. |
| [**D3D12_ROOT_SIGNATURE_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc1). Décrit la disposition d’une signature racine version 1,1. |
| [**D3D12_RT_FORMAT_ARRAY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rt_format_array). Encapsule un tableau de formats de cibles de rendu. |
| [**D3D12_SAMPLE_POSITION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_sample_position). Décrit une position d’échantillon de sous-pixel à utiliser avec des positions d’échantillonnage programmables. |
| [**D3D12_SAMPLER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_sampler_desc). Décrit un état de l’échantillonneur. |
| [**D3D12_SHADER_BYTECODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode). Décrit les données de nuanceur. |
| [**D3D12_SHADER_CACHE_SESSION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_cache_session_desc). Décrit une session de cache de nuanceur. |
| [**D3D12_SHADER_RESOURCE_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc). Décrit un affichage des ressources de nuanceur. |
| [**D3D12_SO_DECLARATION_ENTRY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_so_declaration_entry). Décrit un élément vertex dans une mémoire tampon de vertex dans un emplacement de sortie. |
| [**D3D12_STATIC_SAMPLER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_static_sampler_desc). Décrit un échantillonneur statique. |
| [**D3D12_STREAM_OUTPUT_BUFFER_VIEW**](/windows/win32/api/d3d12/ns-d3d12-d3d12_stream_output_buffer_view). Décrit une mémoire tampon de sortie de flux. |
| [**D3D12_STREAM_OUTPUT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_stream_output_desc). Décrit une mémoire tampon de sortie de diffusion en continu. |
| [**D3D12_SUBRESOURCE_DATA**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_data). Décrit les données de sous-ressource. |
| [**D3D12_SUBRESOURCE_FOOTPRINT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_footprint). Décrit le format, la largeur, la hauteur, la profondeur et l’espacement des lignes de la sous-ressource dans la ressource parente. |
| [**D3D12_SUBRESOURCE_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_info). Décrit les données de sous-ressource. |
| [**D3D12_SUBRESOURCE_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64). Décrit une plage de mémoire de sous-ressources. |
| [**D3D12_SUBRESOURCE_TILING**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_tiling). Décrit un volume de sous-ressources en mosaïque. |
| [**D3D12_TEX1D_ARRAY_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv). Décrit les sous-ressources d’un tableau de textures 1D à utiliser dans une vue de stencil de profondeur. |
| [**D3D12_TEX1D_ARRAY_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv). Décrit les sous-ressources d’un tableau de textures 1D à utiliser dans une vue de cible de rendu. |
| [**D3D12_TEX1D_ARRAY_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv). Décrit les sous-ressources d’un tableau de textures 1D à utiliser dans un affichage des ressources de nuanceur. |
| [**D3D12_TEX1D_ARRAY_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav). Décrit un tableau de ressources de texture 1D avec accès non ordonné. |
| [**D3D12_TEX1D_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_dsv). Décrit la sous-ressource d’une texture 1D qui est accessible à une vue de stencil de profondeur. |
| [**D3D12_TEX1D_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_rtv). Décrit la sous-ressource d’une texture 1D à utiliser dans une vue de cible de rendu. |
| [**D3D12_TEX1D_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_srv). Spécifie la sous-ressource d’une texture 1D à utiliser dans un affichage des ressources de nuanceur. |
| [**D3D12_TEX1D_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_uav). Décrit une ressource de texture 1D avec accès non ordonné. |
| [**D3D12_TEX2D_ARRAY_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv). Décrit les sous-ressources d’un tableau de textures 2D qui sont accessibles à une vue de stencil de profondeur. |
| [**D3D12_TEX2D_ARRAY_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv). Décrit les sous-ressources d’un tableau de textures 2D à utiliser dans une vue de cible de rendu. |
| [**D3D12_TEX2D_ARRAY_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv). Décrit les sous-ressources d’un tableau de textures 2D à utiliser dans un affichage des ressources de nuanceur. |
| [**D3D12_TEX2D_ARRAY_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav). Décrit un tableau de ressources de texture 2D avec accès non ordonné. |
| [**D3D12_TEX2D_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_dsv). Décrit la sous-ressource d’une texture 2D qui est accessible à une vue de stencil de profondeur. |
| [**D3D12_TEX2D_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_rtv). Décrit la sous-ressource d’une texture 2D à utiliser dans une vue de cible de rendu. |
| [**D3D12_TEX2D_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_srv). Décrit la sous-ressource d’une texture 2D à utiliser dans un affichage des ressources de nuanceur. |
| [**D3D12_TEX2D_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_uav). Décrit une ressource de texture 2D avec accès non ordonné. |
| [**D3D12_TEX2DMS_ARRAY_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv). Décrit les sous-ressources d’un tableau de textures 2D à échantillonnage multiple pour une vue de stencil de profondeur. |
| [**D3D12_TEX2DMS_ARRAY_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv). Décrit les sous-ressources d’un tableau de textures 2D à échantillonnage multiple à utiliser dans une vue de cible de rendu. |
| [**D3D12_TEX2DMS_ARRAY_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv). Décrit les sous-ressources d’un tableau de textures 2D à échantillonnage multiple à utiliser dans un affichage des ressources de nuanceur. |
| [**D3D12_TEX2DMS_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_dsv). Décrit la sous-ressource d’une texture 2D échantillonnée multiple qui est accessible à une vue de stencil de profondeur. |
| [**D3D12_TEX2DMS_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_rtv). Décrit la sous-ressource d’une texture 2D échantillonnée multiple à utiliser dans une vue de cible de rendu. |
| [**D3D12_TEX2DMS_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_srv). Décrit les sous-ressources d’une texture 2D à échantillonnage multiple à utiliser dans un affichage des ressources de nuanceur. |
| [**D3D12_TEX3D_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex3d_rtv). Décrit les sous-ressources d’une texture 3D à utiliser dans une vue de cible de rendu. |
| [**D3D12_TEX3D_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex3d_srv). Décrit les sous-ressources d’une texture 3D à utiliser dans un affichage des ressources de nuanceur. |
| [**D3D12_TEX3D_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex3d_uav). Décrit une ressource de texture 3D avec accès non ordonné. |
| [**D3D12_TEXCUBE_ARRAY_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texcube_array_srv). Décrit les sous-ressources d’un tableau de textures de cube à utiliser dans un affichage des ressources de nuanceur. |
| [**D3D12_TEXCUBE_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texcube_srv). Décrit la sous-ressource d’une texture de cube à utiliser dans un affichage des ressources de nuanceur. |
| [**D3D12_TEXTURE_COPY_LOCATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texture_copy_location). Décrit une partie d’une texture à des fins de copie de texture. |
| [**D3D12_TILE_REGION_SIZE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_region_size). Décrit la taille d’une région en mosaïque. |
| [**D3D12_TILE_SHAPE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_shape). Décrit la forme d’une vignette en spécifiant ses dimensions. |
| [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate). Décrit les coordonnées d’une ressource en mosaïque. |
| [**D3D12_UNORDERED_ACCESS_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc). Décrit les sous-ressources d’une ressource qui sont accessibles à l’aide d’un affichage d’accès non ordonné. |
| [**D3D12_VERTEX_BUFFER_VIEW**](/windows/win32/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view). Décrit une vue de mémoire tampon de vertex. |
| [**D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_device_removed_extended_data). Représente des données de données étendues supprimées (ordinateur) de l’appareil avec version, afin que les débogueurs et les extensions de débogueur puissent accéder aux données ordinateur. |
| [**D3D12_VERSIONED_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc). Contient une version d’une description de signature racine et est conçu pour être utilisé avec les fonctions de sérialisation/désérialisation. |
| [**D3D12_VIEW_INSTANCE_LOCATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instance_location). Spécifie la fenêtre d’affichage/le stencil et la cible de rendu associés à une instance de vue. |
| [**D3D12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc). Spécifie les paramètres utilisés pendant la configuration de l’instanciation de vues. |
| [**D3D12_VIEWPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport). Décrit les dimensions d’une fenêtre d’affichage. |
| [**D3D12_WRITEBUFFERIMMEDIATE_PARAMETER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_writebufferimmediate_parameter). Spécifie la valeur immédiate et l’adresse de destination écrites à l’aide de [**ID3D12CommandList2 :: WriteBufferImmediate**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2). |

## <a name="related-topics"></a>Rubriques connexes

* [Référence principale](direct3d-12-core-reference.md)
* [Référence de Direct3D 12](direct3d-12-reference.md)
