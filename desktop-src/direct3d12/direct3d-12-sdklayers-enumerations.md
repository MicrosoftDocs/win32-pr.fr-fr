---
title: Énumérations de couche de débogage
description: Les énumérations suivantes sont déclarées dans d3d12sdklayers. h.
ms.assetid: 6E76C857-128E-4F0E-9711-72C4CF6C835C
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108e8bce1627c37cd0c6f9ffbacfeb1bea991bb0fca97adda116a3c8f0e1b9fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069639"
---
# <a name="debug-layer-enumerations"></a>Énumérations de couche de débogage

Les énumérations suivantes sont déclarées dans d3d12sdklayers. h.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                                                      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Type de \_ \_ paramètre de liste de commandes de débogage D3D12 \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)<br/>                                 | Indique le type de paramètre de débogage utilisé par [**ID3D12DebugCommandList1 :: SetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist1-setdebugparameter) et [**ID3D12DebugCommandList1 :: GetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist1-getdebugparameter).<br/>                                                                                                                                                                                                      |
| [**TYPE de paramètre de l' \_ appareil de débogage D3D12 \_ \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)<br/>                                              | Spécifie le type de données de la mémoire vers laquelle pointe le paramètre *pData* de [**ID3D12DebugDevice1 :: SetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter) et [**ID3D12DebugDevice1 :: GetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-getdebugparameter).<br/>                                                                                                                                                                                        |
| [**\_Fonctionnalité de débogage D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_feature)<br/>                                                                            | Indicateurs pour les fonctionnalités facultatives de la couche de débogage D3D12.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**\_Indicateurs de \_ validation basés sur GPU \_ D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_flags)<br/>                                                | Décrit le niveau de validation basée sur le GPU à exécuter au moment de l’exécution.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**Indicateurs de création de l' \_ \_ \_ État du \_ pipeline de validation \_ basé \_ sur \_ GPU D3D12**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)<br/> | Spécifie comment GPU-Based validation gère les États de pipeline corrigés pendant [**ID3D12Device :: CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) et [**ID3D12Device :: CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate).<br/>                                                                                                                                                                             |
| [**\_Mode de \_ \_ Correction du \_ nuanceur de validation basé \_ sur GPU D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)<br/>                      | Spécifie le type de mise à jour corrective de nuanceur utilisé par GPU-Based validation au niveau de l’appareil ou de la liste de commandes.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**\_Catégorie de message D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_category)<br/>                                                                      | Spécifie les catégories de messages de débogage. Cela permet d’identifier la catégorie d’un message lors de l’extraction d’un message avec [**ID3D12InfoQueue :: GetMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmessage) et lors de l’ajout d’un message avec [**ID3D12InfoQueue :: AddMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addmessage). Lors de la création d’un filtre de file d’attente d’informations, ces valeurs peuvent être utilisées pour autoriser ou refuser les catégories de messages à traverser les filtres de stockage et de récupération. <br/> |
| [**\_ID de message D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_id)<br/>                                                                                  | Spécifie les ID de message de débogage pour la configuration d’un filtre de file d’attente d’informations (consultez [**D3D12 \_ info \_ Queue \_ Filter**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter)). Utilisez ces messages pour autoriser ou refuser les catégories de message à traverser les filtres de stockage et de récupération. Ces ID sont utilisés par des méthodes telles que [**ID3D12InfoQueue :: GetMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmessage) ou [**ID3D12InfoQueue :: AddMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addmessage). <br/>                        |
| [**\_Gravité du message D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_severity)<br/>                                                                      | Déboguez les niveaux de gravité des messages pour une file d’attente d’informations.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| [**\_Indicateurs D3D12 RLDO \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_rldo_flags)<br/>                                                                                  | Spécifie des options pour la quantité d’informations à signaler sur la durée de vie d’un objet de périphérique actif. <br/>                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de l’environnement de programmation Direct3D 12](directx-12-programming-environment-set-up.md)
</dt> <dt>

[Référence de la couche de débogage](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[Référence de Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 





