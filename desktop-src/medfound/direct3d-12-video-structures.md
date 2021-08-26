---
description: Cette section contient des informations de référence sur les structures de l’API vidéo Microsoft Direct3D 12.
ms.assetid: ''
title: Structures vidéo Direct3D 12
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: 945bb3f32a72cab437939e45a0b9691cbde70ef32acf7b08afd2580ff4a4259b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958749"
---
# <a name="direct3d-12-video-structures"></a>Structures vidéo Direct3D 12

Cette section contient des informations de référence sur les structures de l’API vidéo Microsoft Direct3D 12.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique                                                                                | Description                                                                                              |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support)  | Récupère la liste des profils pris en charge.|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_formats)  | Récupère la liste des formats pris en charge.|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_HISTOGRAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_histogram)  | Fournit des données pour les appels à ID3D12VideoDevice :: CheckFeatureSupport lorsque la fonctionnalité spécifiée est D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM.|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles)  | Récupère la liste des profils pris en charge.|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_support)  | Récupère les informations de prise en charge pour le décodage vidéo.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_COUNT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_count)  | Récupère le nombre de commandes d’extension vidéo.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETER_COUNT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_parameter_count)  | Récupère le nombre de paramètres pris en charge pour l’étape de paramètre spécifiée.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETERS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_parameters)  | Récupère la liste des paramètres de commande d’extension vidéo pour l’étape de paramètre spécifiée.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_SIZE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_size)  | Vérifie la taille d’allocation d’une commande d’extension vidéo.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_support)  | Récupère la prise en charge des commandes d’extension vidéo à l’aide de structures d’entrée et de sortie définies par la commande.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMANDS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_commands)  | Récupère la liste des commandes d’extension vidéo à partir du pilote.|
| [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator)  | Fournit des données pour les appels à ID3D12VideoDevice :: CheckFeatureSupport lorsque la fonctionnalité spécifiée est D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR. Récupère les fonctionnalités d’estimation de mouvement pour un encodeur vidéo.|
| [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR_PROTECTED_RESOURCES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator_protected_resources)  | Fournit des données pour les appels à ID3D12VideoDevice :: CheckFeatureSupport lorsque la fonctionnalité spécifiée est D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR_PROTECTED_RESOURCES. Récupère la prise en charge des ressources protégées pour l’estimation de mouvement vidéo.|
| [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR_SIZE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator_size)  | Décrit la taille d’allocation d’un tas d’estimateur de mouvement vidéo.|
| [D3D12_FEATURE_DATA_VIDEO_PROCESS_MAX_INPUT_STREAMS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_process_max_input_streams)  | Récupère le nombre maximal de flux d’entrée activés pris en charge par le processeur vidéo.|
| [D3D12_FEATURE_DATA_VIDEO_PROCESS_REFERENCE_INFO](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_process_reference_info)  | Récupère le nombre de frames de référence passés et futurs requis pour le mode d’entrelacement, le filtre, la conversion de taux ou les fonctionnalités de traitement automatique spécifiés.|
| [D3D12_FEATURE_DATA_VIDEO_PROCESS_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_process_support)  | Fournit des données pour les appels à ID3D12VideoDevice :: CheckFeatureSupport lorsque la fonctionnalité spécifiée est D3D12_FEATURE_VIDEO_PROCESS_SUPPORT.|
| [D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_query_data_video_decode_statistics)  | Représente des données pour une requête de statistiques de décodage de vidéo appelée par l’appel de ID3D12VideoDecodeCommandList :: EndQuery.|
| [D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_INPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_resolve_video_motion_vector_heap_input)  | Fournit des données d’entrée pour les appels à ID3D12VideoEncodeCommandList :: ResolveMotionVectorHeap.|
| [D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_OUTPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_resolve_video_motion_vector_heap_output)  | Reçoit les données de sortie des appels à ID3D12VideoEncodeCommandList :: ResolveMotionVectorHeap.|
| [D3D12_RESOURCE_COORDINATE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_resource_coordinate)  | Décrit les coordonnées d’une ressource.|
| [D3D12_VIDEO_DECODER_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_desc)  | Décrit un ID3D12VideoDecoder.|
| [D3D12_VIDEO_DECODER_HEAP_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_heap_desc)  | Décrit un ID3D12VideoDecoderHeap.|
| [D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_compressed_bitstream)  | Représente un flux binaire compressé à partir duquel la vidéo est décodée.|
| [D3D12_VIDEO_DECODE_CONFIGURATION](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_configuration)  | Décrit la configuration d’un décodeur vidéo.|
| [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments)  | Spécifie les paramètres pour la conversion de sortie de décodage.|
| [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS1](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments1)  | Spécifie les paramètres pour la conversion de sortie de décodage.|
| [D3D12_VIDEO_DECODE_FRAME_ARGUMENT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_frame_argument)  | Représente les paramètres de décodage d’un frame.|
| [D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_input_stream_arguments)  | Spécifie les paramètres pour le flux d’entrée pour une opération de décodage vidéo.|
| [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram)  | Représente la mémoire tampon de sortie de l’histogramme pour un composant unique.|
| [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments)  | Spécifie les paramètres du flux de sortie pour une opération de décodage vidéo.|
| [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1)  | Spécifie les paramètres du flux de sortie pour une opération de décodage vidéo.|
| [D3D12_VIDEO_DECODE_REFERENCE_FRAMES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_reference_frames)  | Contient la liste des frames de référence pour l’opération de décodage en cours.|
| [D3D12_VIDEO_DECODE_SUB_SAMPLE_MAPPING_BLOCK](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_sub_sample_mapping_block)  | Définit le mappage d’octets de chiffrement des sous-exemples pour le décodage vidéo.|
| [D3D12_VIDEO_EXTENSION_COMMAND_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_extension_command_desc)  | Décrit une commande d’extension vidéo.|
| [D3D12_VIDEO_EXTENSION_COMMAND_INFO](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_extension_command_info)  | Décrit une commande d’extension vidéo.|
| [D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_INFO](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_extension_command_parameter_info)  | Décrit un paramètre de commande d’extension vidéo.|
| [D3D12_VIDEO_FORMAT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_format)  | Définit la combinaison d’un format de pixel et d’un espace de couleurs pour une description de contenu de ressource.|
| [D3D12_VIDEO_MOTION_ESTIMATOR_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_desc)  | Décrit un ID3D12VideoMotionEstimator. Transmettez cette structure dans ID3D12VideoDevice1 :: CreateVideoMotionEstimator pour créer une instance de ID3D12VideoMotionEstimator.|
| [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input)  | Fournit des données d’entrée pour les appels à ID3D12VideoEncodeCommandList :: EstimateMotion.|
| [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output)  | Reçoit les données de sortie des appels à ID3D12VideoEncodeCommandList :: EstimateMotion.|
| [D3D12_VIDEO_MOTION_VECTOR_HEAP_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_vector_heap_desc)  | Décrit un ID3D12VideoMotionEstimatorHeap. Transmettez cette structure dans ID3D12VideoDevice1 :: CreateVideoMotionEstimatorHeap pour créer une instance de ID3D12VideoMotionEstimatorHeap.|
| [D3D12_VIDEO_PROCESS_ALPHA_BLENDING](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_alpha_blending)  | Spécifie les paramètres de fusion alpha pour le traitement vidéo.|
| [D3D12_VIDEO_PROCESS_FILTER_RANGE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_filter_range)  | Définit la plage de valeurs prises en charge pour un filtre d’image.|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream)  | Contient des informations d’entrée pour la fonctionnalité de mélange du processeur vidéo.|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments)  | Spécifie les arguments de flux d’entrée pour un flux d’entrée transmis à ID3D12VideoCommandList ::P rocessFrames.|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc)  | Spécifie les paramètres pour le flux d’entrée pour une opération de traitement vidéo.|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM_RATE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_rate)  | Fournit des informations sur la vitesse du flux de données.|
| [D3D12_VIDEO_PROCESS_LUMA_KEY](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_luma_key)  | Spécifie les paramètres utilisés pour la gestion des luminances.|
| [D3D12_VIDEO_PROCESS_OUTPUT_STREAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream)  | Représente le flux de sortie pour les commandes de traitement vidéo.|
| [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments)  | Spécifie les arguments de flux de sortie pour la sortie passée à ID3D12VideoCommandList ::P rocessFrames.|
| [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc)  | Spécifie les arguments de flux de sortie pour la sortie passée à ID3D12VideoProcessCommandList ::P rocessFrames.|
| [D3D12_VIDEO_PROCESS_REFERENCE_SET](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_reference_set)  | Contient les frames de référence nécessaires pour effectuer le traitement vidéo.|
| [D3D12_VIDEO_PROCESS_TRANSFORM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_transform)  | Spécifie les paramètres de transformation pour le traitement vidéo.|
| [D3D12_VIDEO_SAMPLE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_sample)  | Décrit la largeur, la hauteur, le format et l’espace colorimétrique d’une mémoire tampon d’image.|
| [D3D12_VIDEO_SCALE_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_scale_support)  | Décrit la plage de tailles de sortie prise en charge pour un scaler vidéo.|
| [D3D12_VIDEO_SIZE_RANGE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_size_range)  | Décrit la plage de tailles prises en charge pour un Video scaler.|



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API vidéo Direct3D 12](direct3d-12-video-apis.md)
</dt> </dl>

 

 



