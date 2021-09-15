---
description: Cette section contient des informations de référence sur les structures de l’API vidéo Microsoft Direct3D 12.
ms.assetid: ''
title: Structures vidéo Direct3D 12
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: dd73ba1cf374dade90963513ddbc92317cd3b05c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525785"
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
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_CODEC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_codec)  | Récupère une valeur indiquant si le codec spécifié est pris en charge pour l’encodage vidéo.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_codec_configuration_support)  | Récupère une valeur indiquant si les paramètres de prise en charge de la configuration du codec spécifiés sont pris en charge pour 
la configuration d’encodage HEVC fournie ou récupère la configuration prise en charge pour l’encodage H. 264.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_codec_picture_control_support)  | Récupère la prise en charge du contrôle d’image pour le codec et le profil spécifiés.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_frame_subregion_layout_mode)  | Récupère une valeur indiquant si le mode de disposition de la sous-région du frame spécifié est pris en charge pour le spécifié. 
code, profil et niveau.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_HEAP_SIZE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_heap_size)  | Récupère une valeur indiquant si le codec spécifié est pris en charge pour l’encodage vidéo ainsi que le N0 et 
Tailles L1 de l’objet de segment de mémoire.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_INPUT_FORMAT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_input_format)  | Récupère une valeur indiquant si le codec, le profil et le format spécifiés sont pris en charge pour l’encodage vidéo.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_INTRA_REFRESH_MODE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_intra_refresh_mode)  | Récupère une valeur indiquant si le mode d’actualisation intra spécifié est pris en charge pour le codec spécifié. 
Profile et Level.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_OUTPUT_RESOLUTION](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_output_resolution)  | Récupère la liste des résolutions prises en charge pour le codec spécifié.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_OUTPUT_RESOLUTION_RATIOS_COUNT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_output_resolution_ratios_count)  | |
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_PROFILE_LEVEL](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_profile_level)  | Récupère une valeur indiquant si le profil spécifié est pris en charge pour l’encodage vidéo.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_RATE_CONTROL_MODE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_rate_control_mode)  | Récupère une valeur indiquant si le mode de contrôle de la fréquence spécifié est pris en charge pour l’encodage vidéo avec l' 
Codec spécifié|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_LIMITS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_resolution_support_limits)  | Représente les limites de prise en charge de la résolution de l’encodeur vidéo pour un D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT 
arborescence.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_resource_requirements)  | Récupère des valeurs indiquant les besoins en ressources pour l’encodage vidéo avec l’encodage spécifié 
.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_support)  | Récupère des valeurs indiquant la prise en charge des fonctionnalités d’encodage vidéo spécifiées et des valeurs de configuration.|
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
| [D3D12_VIDEO_ENCODE_REFERENCE_FRAMES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encode_reference_frames)  | Représente les images de référence reconstruites pour une opération d’encodage.|
| [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_codec_configuration)  | Représente une structure de configuration de codec pour l’encodage vidéo.|
| [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_codec_configuration_h264)  | Représente la configuration du codec pour l’encodage H. 264.|
| [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_codec_configuration_hevc)  | Représente la configuration du codec pour l’encodage HEVC.|
| [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_codec_configuration_support)  | Représente une structure de prise en charge de la configuration du codec pour l’encodage vidéo.|
| [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_H264](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_codec_configuration_support_h264)  | Représente la prise en charge de la configuration du codec d’encodeur pour H. 264.|
| [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_codec_configuration_support_hevc)  | Représente la prise en charge de la configuration du codec d’encodeur pour le codage HEVC.|
| [D3D12_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_codec_picture_control_support)  | Représente la structure de prise en charge du contrôle d’image pour plusieurs codecs.|
| [D3D12_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT_H264](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_codec_picture_control_support_h264)  | Représente les paramètres de prise en charge du contrôle d’image pour l’encodage vidéo H. 264.|
| [D3D12_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT_HEVC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_codec_picture_control_support_hevc)  | Représente les paramètres de prise en charge du contrôle d’image pour l’encodage vidéo HEVC.|
| [D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_compressed_bitstream)  | Encapsule la sortie de flux binaire compressée pour l’opération d’encodage.|
| [D3D12_VIDEO_ENCODER_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_desc)  | Décrit un ID3D12VideoEncoder.|
| [D3D12_VIDEO_ENCODER_ENCODE_OPERATION_METADATA_BUFFER](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_encode_operation_metadata_buffer)  | Représente une mémoire tampon qui contient les métadonnées relatives à une opération ID3D12VideoEncodeCommandList2 :: EncodeFrame.|
| [D3D12_VIDEO_ENCODER_ENCODEFRAME_INPUT_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_encodeframe_input_arguments)  | Représente les arguments d’entrée de ID3D12VideoEncodeCommandList2 :: EncodeFrame.|
| [D3D12_VIDEO_ENCODER_ENCODEFRAME_OUTPUT_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_encodeframe_output_arguments)  | Représente les arguments de sortie de ID3D12VideoEncodeCommandList2 :: EncodeFrame.|
| [D3D12_VIDEO_ENCODER_FRAME_SUBREGION_METADATA](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_frame_subregion_metadata)  | Représente les métadonnées de la sous-région de l’encodeur vidéo.|
| [D3D12_VIDEO_ENCODER_HEAP_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_heap_desc)  | Décrit un ID3D12VideoEncoderHeap.|
| [D3D12_VIDEO_ENCODER_INTRA_REFRESH](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_intra_refresh)  | Représente les paramètres d’actualisation intra-vidéo pour l’encodage vidéo.|
| [D3D12_VIDEO_ENCODER_LEVEL_SETTING](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_level_setting)  | Représente un paramètre de niveau d’encodeur vidéo.|
| [D3D12_VIDEO_ENCODER_LEVEL_TIER_CONSTRAINTS_HEVC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_level_tier_constraints_hevc)  | Associe un niveau et un niveau pour la configuration du paramètre de niveau HEVC (High EFFICACITE Video Coding).|
| [D3D12_VIDEO_ENCODER_OUTPUT_METADATA](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_output_metadata)  | Représente les métadonnées relatives à une opération ID3D12VideoEncodeCommandList2 :: EncodeFrame.|
| [D3D12_VIDEO_ENCODER_OUTPUT_METADATA_STATISTICS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_output_metadata_statistics)  | Représente les statistiques d’encodage relatives à une opération ID3D12VideoEncodeCommandList2 :: EncodeFrame.|
| [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_control_codec_data)  | Représente les éléments de contrôle au niveau de l’image pour la commande EncodeFrame associée pour plusieurs codecs.|
| [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_control_codec_data_h264)  | Représente les éléments de contrôle au niveau de l’image pour la commande EncodeFrame associée pour l’encodage H. 264.|
| [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_REFERENCE_PICTURE_LIST_MODIFICATION_OPERATION](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_control_codec_data_h264_reference_picture_list_modification_operation)  | Représente une opération de modification de la liste d’images pour l’encodage vidéo H264 –.|
| [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_REFERENCE_PICTURE_MARKING_OPERATION](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_control_codec_data_h264_reference_picture_marking_operation)  | Décrit les modifications apportées aux images de référence en tant qu’opérations de mémoire sous forme de tuple d’une opération identificateur du 
et les paramètres associés nécessaires à l’opération.|
| [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_HEVC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_control_codec_data_hevc)  | Représente les éléments de contrôle au niveau de l’image pour la commande EncodeFrame associée pour l’encodage HEVC.|
| [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_control_desc)  | 06/30/2021|
| [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_SUBREGIONS_LAYOUT_DATA](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_control_subregions_layout_data)  | Définit des sous-régions de contrôle d’image comme tranches pour plusieurs codecs.|
| [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_SUBREGIONS_LAYOUT_DATA_SLICES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_control_subregions_layout_data_slices)  | Définit des sous-régions en tant que tranches pour les codecs qui prennent en charge ce mode de partitionnement.|
| [D3D12_VIDEO_ENCODER_PICTURE_RESOLUTION_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_resolution_desc)  | Définit une résolution d’image de l’encodeur vidéo.|
| [D3D12_VIDEO_ENCODER_PICTURE_RESOLUTION_RATIO_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_resolution_ratio_desc)  | Définit un rapport de résolution comme une fraction Irreducible.|
| [D3D12_VIDEO_ENCODER_PROFILE_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_profile_desc)  | Décrit un profil d’encodeur.|
| [D3D12_VIDEO_ENCODER_RATE_CONTROL](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_rate_control)  | Représente une configuration de contrôle du taux de l’encodeur vidéo.|
| [D3D12_VIDEO_ENCODER_RATE_CONTROL_CBR](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_rate_control_cbr)  | Représente une définition de structure de contrôle de taux pour le mode de débit binaire constant.|
| [D3D12_VIDEO_ENCODER_RATE_CONTROL_CONFIGURATION_PARAMS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_rate_control_configuration_params)  | Représente les définitions de structure de contrôle du taux d’encodeur vidéo pour un D3D12_VIDEO_ENCODER_RATE_CONTROL 
arborescence.|
| [D3D12_VIDEO_ENCODER_RATE_CONTROL_CQP](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_rate_control_cqp)  | Représente une définition de structure de contrôle de taux pour le mode de paramètre de quantification constante.|
| [D3D12_VIDEO_ENCODER_RATE_CONTROL_QVBR](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_rate_control_qvbr)  | Représente une définition de structure de contrôle de taux pour une cible de qualité constante avec un débit restreint.|
| [D3D12_VIDEO_ENCODER_RATE_CONTROL_VBR](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_rate_control_vbr)  | Représente une définition de structure de contrôle de taux pour le mode de débit binaire variable.|
| [D3D12_VIDEO_ENCODER_RECONSTRUCTED_PICTURE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_reconstructed_picture)  | Représente l’image reconstruite générée à partir de la trame d’entrée passée à l’opération d’encodage.|
| [D3D12_VIDEO_ENCODER_REFERENCE_PICTURE_DESCRIPTOR_H264](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_reference_picture_descriptor_h264)  | Représente un descripteur d’image de référence pour l’encodage vidéo H. 264.|
| [D3D12_VIDEO_ENCODER_REFERENCE_PICTURE_DESCRIPTOR_HEVC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_reference_picture_descriptor_hevc)  | Représente un descripteur d’image de référence pour l’encodage vidéo HEVC.|
| [D3D12_VIDEO_ENCODER_RESOLVE_METADATA_INPUT_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_resolve_metadata_input_arguments)  | Représente des arguments d’entrée pour un appel à ID3D12VideoEncodeCommandList2 :: ResolveEncoderOutputMetadata.|
| [D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_resolve_metadata_output_arguments)  | Représente les arguments de sortie d’un appel à ID3D12VideoEncodeCommandList2 :: ResolveEncoderOutputMetadata.|
| [D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_sequence_control_desc)  | |
| [D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_sequence_gop_structure)  | Représente la structure GOP pour plusieurs codecs vidéo.|
| [D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE_H264](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_sequence_gop_structure_h264)  | Représente la structure GOP pour l’encodage vidéo H. 264.|
| [D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE_HEVC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_sequence_gop_structure_hevc)  | Représente la structure GOP pour l’encodage vidéo HEVC.|
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

 

 



