---
description: Cette section contient des informations sur les énumérations fournies par DXGI.
ms.assetid: c4574c89-dee2-4841-9318-5383cf417111
title: Énumérations DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9347fdf39f2cde6bb50e3ae4c65f2601c570e084516bf817c4dc66169a83925
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987139"
---
# <a name="dxgi-enumerations"></a>Énumérations DXGI

Cette section contient des informations sur les énumérations fournies par DXGI.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                         | Description                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_indicateur d’adaptateur dxgi \_**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_adapter_flag)<br/>                                          | Identifie le type d’adaptateur DXGI.<br/>                                                                                                                                   |
| [**\_Adaptateur dxgi \_ Indicateur3**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3)<br/>                                        | Identifie le type d’adaptateur DXGI.<br/>                                                                                                                                   |
| [**\_mode Alpha \_ dxgi**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)<br/>                                                       | Identifie la valeur alpha, le comportement de transparence, d’une surface.<br/>                                                                                                       |
| [**\_type d' \_ espace de couleurs dxgi \_**](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)<br/>                                          | Spécifie les types d’espace colorimétrique.<br/>                                                                                                                                           |
| [**\_ \_ granularité de préemption de calcul dxgi \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_compute_preemption_granularity)<br/>              | Identifie la granularité à laquelle l’unité de traitement graphique (GPU, Graphical Processing Unit) peut être préemptée pour effectuer sa tâche de calcul actuelle.<br/>                                      |
| [**\_indicateurs de débogage dxgi \_ RLO \_**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_debug_rlo_flags)<br/>                                            | Indicateurs utilisés avec [**ReportLiveObjects**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-idxgidebug-reportliveobjects) pour spécifier la quantité d’informations à signaler sur la durée de vie d’un objet. <br/>                         |
| [**\_fonctionnalité dxgi**](/windows/desktop/api/DXGI1_5/ne-dxgi1_5-dxgi_feature)<br/>                                                              | Spécifie une plage de fonctionnalités matérielles à utiliser lors de la vérification de la prise en charge des fonctionnalités.<br/>                                                                                  |
| [**\_format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)<br/>                                                       | Les formats de données de ressources, y compris les formats entièrement typés et sans type. Une liste de modificateurs au bas de la page décrit plus en détail chaque type de format. <br/>               |
| [**\_mode de \_ Présentation de frame dxgi \_**](/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_frame_presentation_mode)<br/>                            | Indique les options de présentation des frames à la chaîne de permutation. <br/>                                                                                                            |
| [**\_préférence dxgi GPU \_**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference)<br/>                                               | La préférence du GPU pour l’application à exécuter.<br/>                                                                                                                           |
| [**\_ \_ granularité de préemption des graphiques dxgi \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_graphics_preemption_granularity)<br/>            | Identifie la granularité à laquelle le GPU peut être devancé pour effectuer sa tâche de rendu graphique actuelle.<br/>                                                      |
| [**\_indicateurs de \_ \_ prise en \_ charge de la composition matérielle dxgi**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags)<br/>     | décrit les niveaux de composition matérielle pris en charge.<br/>                                                                                                          |
| [**\_type de \_ métadonnées HDR dxgi \_**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_hdr_metadata_type)<br/>                                        | Spécifie le type de métadonnées d’en-tête.<br/>                                                                                                                                    |
| [**catégorie de message de la \_ \_ file d’attente d’informations \_ dxgi \_**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_info_queue_message_category)<br/>                   | Valeurs qui spécifient des catégories de messages de débogage.<br/>                                                                                                                      |
| [**gravité du message de la \_ \_ file d’attente dxgi info \_ \_**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_info_queue_message_severity)<br/>                   | Valeurs qui spécifient les niveaux de gravité des messages de débogage pour une file d’attente d’informations.<br/>                                                                                            |
| [**\_groupe de \_ segments de mémoire dxgi \_**](/windows/desktop/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)<br/>                                  | Spécifie le groupe de segments de mémoire à utiliser.<br/>                                                                                                                             |
| [**\_rotation en mode dxgi \_**](/previous-versions/windows/desktop/legacy/bb173065(v=vs.85))<br/>                                        | Indicateurs qui indiquent comment les mémoires tampons d’arrière-plan doivent être pivotées pour s’adapter à la rotation physique d’une analyse.<br/>                                                                  |
| [**\_mise à \_ l’échelle du mode dxgi**](/previous-versions/windows/desktop/legacy/bb173066(v=vs.85))<br/>                                          | Indicateurs indiquant comment une image est étirée pour s’adapter à la résolution d’un moniteur donné.<br/>                                                                                        |
| [**\_commande numérisation en mode dxgi \_ \_**](/previous-versions/windows/desktop/legacy/bb173067(v=vs.85))<br/>                           | Indicateurs qui indiquent la méthode utilisée par raster pour créer une image sur une surface.<br/>                                                                                           |
| [**\_ \_ Indicateurs de superpositions dxgi Multiplans \_ YCbCr \_**](/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_multiplane_overlay_ycbcr_flags)<br/>             | Options pour l’espace colorimétrique de la chaîne d’échange.<br/>                                                                                                                                    |
| [**indicateurs de ressource de l' \_ offre dxgi \_ \_**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags)<br/>                                  | Spécifie des indicateurs pour la méthode [**OfferResources1**](/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) .<br/>                                                                                |
| [**priorité de la \_ ressource d’offre dxgi \_ \_**](/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_offer_resource_priority)<br/>                           | Identifie l’importance d’un contenu de ressource s quand vous appelez la méthode [**IDXGIDevice2 :: OfferResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources) pour offrir la ressource. <br/> |
| [**\_type de \_ \_ forme pointeur dxgi OUTDUPL \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_outdupl_pointer_shape_type)<br/>                     | Identifie le type de la forme du pointeur.<br/>                                                                                                                                  |
| [**\_indicateur de \_ \_ \_ prise en charge \_ de l’espace de couleurs de superposition dxgi**](/windows/desktop/api/DXGI1_4/ne-dxgi1_4-dxgi_overlay_color_space_support_flag)<br/>        | Spécifie la prise en charge de l’espace de couleurs de superposition.<br/>                                                                                                                             |
| [**\_indicateur de \_ support de recouvrement dxgi \_**](/windows/desktop/api/DXGI1_3/ne-dxgi1_3-dxgi_overlay_support_flag)<br/>                                  | Spécifie la prise en charge de la superposition à vérifier dans un appel à [**IDXGIOutput3 :: CheckOverlaySupport**](/windows/desktop/api/DXGI1_3/nf-dxgi1_3-idxgioutput3-checkoverlaysupport).<br/>                                     |
| [**DXGI \_ récupérer les \_ résultats des ressources \_**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_reclaim_resource_results)<br/>                          | Spécifie les indicateurs de résultat de la méthode [**ReclaimResources1**](/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) .<br/>                                                                     |
| [**\_résidence dxgi**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_residency)<br/>                                                 | Indicateurs spécifiant l’emplacement de mémoire d’une ressource.<br/>                                                                                                                    |
| [**\_mise à l’échelle dxgi**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_scaling)<br/>                                                              | Identifie le comportement de redimensionnement lorsque la taille de la mémoire tampon d’arrière-plan ne correspond pas à la taille de la sortie cible.<br/>                                                                     |
| [**\_indicateur de \_ \_ \_ \_ prise en charge \_ de l’espace de couleurs de la chaîne d’échange dxgi**](/windows/desktop/api/DXGI1_4/ne-dxgi1_4-dxgi_swap_chain_color_space_support_flag)<br/> | Spécifie la prise en charge de l’espace colorimétrique pour la chaîne de permutation.<br/>                                                                                                                      |
| [**\_indicateur de \_ chaîne d’échange dxgi \_**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag)<br/>                                   | Options de comportement de la chaîne d’échange.<br/>                                                                                                                                       |
| [**DXGI \_ l' \_ effet d’échange**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)<br/>                                                     | Options de gestion des pixels dans une surface d’affichage après l’appel de [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). <br/>                                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence DXGI](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

