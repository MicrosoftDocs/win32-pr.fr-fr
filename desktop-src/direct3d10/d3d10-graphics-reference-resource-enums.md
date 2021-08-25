---
description: Les énumérations suivantes sont utilisées pour spécifier des informations sur la façon dont les ressources sont créées et accessibles pendant le rendu.
ms.assetid: c986b22c-2960-4571-98bc-028c9f41ec65
title: Énumérations de ressources (graphiques Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc82ac605c8ab4dd6ead6ea392dc30db67cd777642dbaab0b9f57520353a467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989558"
---
# <a name="resource-enumerations-direct3d-10-graphics"></a>Énumérations de ressources (graphiques Direct3D 10)

Les énumérations suivantes sont utilisées pour spécifier des informations sur la façon dont les ressources sont créées et accessibles pendant le rendu.



| Énumération                                                     | Description                                                                                                               |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**\_Indicateur de liaison D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)                    | Identifie la manière dont une ressource sera utilisée par le pipeline et détermine la ou les étapes de pipeline auxquelles une ressource peut être liée. |
| [**\_Indicateur d' \_ accès au processeur D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag)       | Spécifie les types d’accès de l’UC autorisés pour une ressource.                                                                 |
| [**\_Dimension DSV \_ D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_dsv_dimension)            | Spécifie comment accéder à une ressource qui est utilisée dans une vue de stencil de profondeur.                                                  |
| [**Carte de D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_map)                                 | Identifie une ressource à mapper pour la lecture et l’écriture par l’UC.                                                    |
| [**\_Indicateur de carte de D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_map_flag)                      | Spécifie la façon dont l’UC doit répondre à toutes les méthodes cartographiques lorsque le GPU n’est pas encore terminé avec la ressource.               |
| [**\_Dimension de ressource D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)  | Identifie le type de ressource en cours d’utilisation.                                                                           |
| [**\_ \_ Indicateur div de la ressource D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag) | Identifie les options de création de ressources moins courantes.                                                                         |
| [**\_Dimension D3D10 RTV \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_rtv_dimension)            | Spécifie comment accéder à une ressource utilisée dans une vue de cible de rendu.                                                          |
| [**Utilisation de D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)                             | Identifie la manière dont une ressource est supposée être lue et écrite par l’UC et/ou le GPU.                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de ressource](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 



