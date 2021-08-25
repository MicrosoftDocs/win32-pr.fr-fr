---
description: 'Cette section contient des informations sur les énumérations principales suivantes :'
ms.assetid: 3d1541bf-75d8-459d-a912-4068e9a0a9e4
title: Énumérations de base Direct3D 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e96a0426a50ad3e8d643f8b4e7e1ab0d7a2034bbaa925a09fcb7d4e5f96640f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858599"
---
# <a name="direct3d-10-core-enumerations"></a>Énumérations de base Direct3D 10

Cette section contient des informations sur les énumérations principales suivantes :



| Énumération                                                               | Description                                                                                                                                         |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ Indicateur GetData Async \_ D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_async_getdata_flag)           | Indicateurs facultatifs qui contrôlent ce qui se produit lorsque les données sont récupérées en appelant [**ID3D10Asynchronous :: GetData**](/windows/desktop/api/D3D10/nf-d3d10-id3d10asynchronous-getdata).       |
| [**D3D10 \_ Blend**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_blend)                                       | Options de fusion.                                                                                                                                      |
| [**D3D10 \_ Blend \_ op**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_blend_op)                                | Opérations de fusion entre les pixels source et de destination.                                                                                          |
| [**\_Indicateur d’effacement D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_clear_flag)                            | Spécifie les parties du stencil de profondeur à effacer.                                                                                                |
| [**Activation de l' \_ écriture de couleurs D3D10 \_ \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_color_write_enable)           | Masques d’écriture de couleurs.                                                                                                                                |
| [**D3D10 de comparaison de la fonction \_ \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_comparison_func)                  | Fonctions de comparaison.                                                                                                                               |
| [**\_Compteur D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_counter)                                   | Types de compteurs de performances.                                                                                                                      |
| [**\_Type de compteur D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_counter_type)                        | Type de données d’un compteur.                                                                                                                             |
| [**D3D10 \_ créer \_ un \_ indicateur d’appareil**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)           | Indicateurs de création de l’appareil.                                                                                                                              |
| [**\_Mode d’élimination D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode)                              | Modes d’élimination du rastériseur.                                                                                                                              |
| [**\_Masque d' \_ écriture de profondeur D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_depth_write_mask)               | Détermine quelle partie du stencil de profondeur est accessible en écriture.                                                                                          |
| [**TYPES d’état de l' \_ appareil D3D10 \_ \_**](/windows/desktop/api/D3D10Effect/ne-d3d10effect-d3d10_device_state_types)           | Utilisé dans les appels de fonction d' [**interface ID3D10StateBlock**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10stateblock) .                                                                      |
| [**\_Type de pilote D3D10 \_**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)                          | Type de pilote de périphérique.                                                                                                                              |
| [**D3D10 \_ fonctionnalité de \_ niveau1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)                    | Version de l’accélération matérielle.                                                                                                               |
| [**\_Mode de remplissage D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode)                              | Modes de remplissage de rastériseur.                                                                                                                              |
| [**\_Filtre D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_filter)                                     | Types de filtres d’échantillonnage.                                                                                                                           |
| [**\_Type de filtre D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_filter_type)                          | Types de filtres d’échantillonnage de texture.                                                                                                                  |
| [**\_ \_ Prise en charge du format D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_format_support)                    | Les ressources prises en charge pour un format donné et un appareil donné. Consultez [**ID3D10Device :: CheckFormatSupport**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-checkformatsupport). |
| [**\_Classification d’entrée D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_input_classification)        | Types de données d’entrée.                                                                                                                                |
| [**\_Catégorie de message D3D10 \_**](/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_category)                | Catégories de messages de débogage.                                                                                                                       |
| [**\_ID de message D3D10 \_**](/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_id)                            | ID unique d’un message de débogage.                                                                                                                        |
| [**\_Gravité du message D3D10 \_**](/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_severity)                | Gravité d’un message de débogage.                                                                                                                        |
| [**\_Topologie primitive \_ D3D10**](/previous-versions/windows/desktop/legacy/bb205334(v=vs.85))            | Types de topologie primitive ou mode de réorganisation des données d’une primitive.                                                                              |
| [**\_Requête D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_query)                                       | Types de requêtes.                                                                                                                                   |
| [**\_ \_ Indicateur div de la requête D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_query_misc_flag)                 | Indicateurs qui décrivent le comportement des requêtes divers.                                                                                                   |
| [**\_Indicateur de déclenchement D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_raise_flag)                            | Indicateurs qui indiquent comment gérer les erreurs internes du pilote.                                                                                           |
| [**\_Type de \_ composant \_ Register D3D10**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_register_component_type) | Types de composant de Registre, généralement utilisés dans la [**\_ Description du \_ paramètre \_ de signature D3D10**](/windows/desktop/api/D3D10Shader/ns-d3d10shader-d3d10_signature_parameter_desc).                          |
| [**TYPE de retour de la \_ ressource D3D10 \_ \_**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_resource_return_type)       | Type de retour d’une ressource. Consultez [**la \_ \_ liaison d’entrée de nuanceur D3D10 \_ \_ desc**](/windows/desktop/api/D3D10Shader/ns-d3d10shader-d3d10_shader_input_bind_desc).                                        |
| [**D3D10 \_ stencil \_ op**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_stencil_op)                            | Opérations de stencil.                                                                                                                                 |
| [**MODE d’adresse de la \_ texture D3D10 \_ \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_texture_address_mode)       | Actions à effectuer quand une coordonnée de texture est en dehors des limites d’une texture.                                                             |
| [**\_Visage D3D10 TEXTURECUBE \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_texturecube_face)                | Différentes faces d’une texture de cube.                                                                                                              |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence principale](d3d10-graphics-reference-d3d10-core.md)
</dt> </dl>

 

 
