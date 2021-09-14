---
title: Énumérations de ressources (graphiques Direct3D 11)
description: Les énumérations sont utilisées pour spécifier des informations sur la façon dont les ressources sont créées et accessibles pendant le rendu.
ms.assetid: b547819b-7006-40b5-84a4-adf198048051
keywords:
- énumérations, ressource Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6124fcbc93cb0069152dd20d3b4b3bf0f4be60d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918560"
---
# <a name="resource-enumerations-direct3d-11-graphics"></a>Énumérations de ressources (graphiques Direct3D 11)

Les énumérations sont utilisées pour spécifier des informations sur la façon dont les ressources sont créées et accessibles pendant le rendu.


## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                               | Description                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Indicateur de liaison d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)<br/>                                                             | Identifie comment lier une ressource au pipeline.<br/>                                                                                                                                 |
| [**\_ \_ Indicateur SRV d3d11 \_ BUFFEREX**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bufferex_srv_flag)<br/>                                            | Identifie comment afficher une ressource de mémoire tampon.<br/>                                                                                                                                          |
| [**\_Indicateur UAV de mémoire tampon d3d11 \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_buffer_uav_flag)<br/>                                                | Identifie les options de vue d’accès non ordonnées pour une ressource de mémoire tampon.<br/>                                                                                                                    |
| [**\_Indicateur de \_ niveau de \_ qualité à échantillons \_ multiples d3d11 \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag)<br/> | Identifie comment vérifier des niveaux de qualité d’échantillonnages différents.<br/>                                                                                                                                |
| [**\_Indicateur d' \_ accès au processeur d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)<br/>                                                | Spécifie les types d’accès de l’UC autorisés pour une ressource.<br/>                                                                                                                          |
| [**\_Dimension DSV \_ d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_dsv_dimension)<br/>                                                     | Spécifie comment accéder à une ressource utilisée dans une vue de stencil de profondeur.<br/>                                                                                                                   |
| [**\_Indicateur DSV \_ d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_dsv_flag)<br/>                                                               | Options de vue de stencil de profondeur.<br/>                                                                                                                                                        |
| [**Carte de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)<br/>                                                                          | Identifie une ressource accessible en lecture et en écriture par l’UC. Les applications peuvent combiner un ou plusieurs de ces indicateurs.<br/>                                                      |
| [**\_Indicateur de carte de d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map_flag)<br/>                                                               | Spécifie le mode de réponse de l’UC lorsqu’une application appelle la méthode [**ID3D11DeviceContext :: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) sur une ressource qui est utilisée par le GPU.<br/> |
| [**\_Dimension de ressource d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)<br/>                                           | Identifie le type de ressource utilisé.<br/>                                                                                                                                        |
| [**\_ \_ Indicateur div de la ressource d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)<br/>                                          | Identifie les options pour les ressources.<br/>                                                                                                                                                  |
| [**\_Dimension d3d11 RTV \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_rtv_dimension)<br/>                                                     | Ces indicateurs identifient le type de ressource qui sera affiché en tant que cible de rendu.<br/>                                                                                                  |
| [**\_Dimension SRV \_ d3d11**](/previous-versions/windows/desktop/legacy/ff476217(v=vs.85))<br/>                                                     | Ces indicateurs identifient le type de ressource qui sera affiché en tant que ressource de nuanceur.<br/>                                                                                                |
| [**Niveaux de qualité de l' \_ exemple d3d11 standard \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_standard_multisample_quality_levels)<br/>       | Spécifie un type de modèle à plusieurs échantillons.<br/>                                                                                                                                             |
| [**\_Disposition de texture d3d11 \_**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout)<br/>                                                   | Spécifie les options de mise en page de texture.<br/>                                                                                                                                                  |
| [**\_Indicateur de \_ copie de vignette d3d11 \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag)<br/>                                                 | Identifie comment copier une vignette.<br/>                                                                                                                                                     |
| [**\_Indicateur de \_ mappage de vignette d3d11 \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_mapping_flag)<br/>                                           | Identifie comment effectuer une opération de mappage de mosaïques.<br/>                                                                                                                                |
| [**\_Indicateur de plage de vignettes d3d11 \_ \_**](/windows/desktop/api/d3d11_2/ne-d3d11_2-d3d11_tile_range_flag)<br/>                                                | Spécifie une plage de mappages de vignettes à utiliser avec [**ID3D11DeviceContext2 :: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles).<br/>                                                      |
| [**\_Dimension d3d11 UAV \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_uav_dimension)<br/>                                                     | Options de vue d’accès non ordonnées.<br/>                                                                                                                                                     |
| [**Utilisation de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)<br/>                                                                      | Identifie l’utilisation des ressources attendue pendant le rendu. L’utilisation de indique directement si une ressource est accessible par l’UC et/ou par l’unité de traitement graphique (GPU).<br/>              |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de ressource](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

