---
title: Niveaux de fonctionnalités des ressources en mosaïque
description: Direct3D 11,2 expose la prise en charge des ressources en mosaïque dans deux niveaux avec les \_ valeurs de niveau de ressources en mosaïque d3d11 \_ \_ .
ms.assetid: E6A6565B-079B-47DB-A80C-CA5B5413BA32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2282cde1dfc8c4249672d18e303a4529338d4fbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939718"
---
# <a name="tiled-resources-features-tiers"></a>Niveaux de fonctionnalités des ressources en mosaïque

Direct3D 11,2 expose la prise en charge des ressources en mosaïque dans deux niveaux avec les valeurs de [**\_ niveau de \_ ressources \_ en mosaïque d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) .

Pour déterminer si le matériel et les pilotes prennent en charge les ressources en mosaïque et au niveau du niveau, transmettez la [**d3d11 \_ fonctionnalité \_ d3d11 \_ options1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) à la valeur du paramètre *Feature* de [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). En outre, transmettez un pointeur vers la structure de données de la [**\_ fonctionnalité d3d11 \_ \_ d3d11 \_ options1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) vers le paramètre *pFeatureSupportData* , puis transmettez la taille de la de données de la **\_ fonctionnalité \_ \_ \_** d3d11 à la structure d3d11 au paramètre *options1* . **CheckFeatureSupport** retourne le niveau de couche sous la forme d’une valeur de [**niveau de \_ \_ ressources \_ en mosaïque d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) dans le membre **TiledResourcesTier** des données de la **\_ fonctionnalité d3d11 \_ \_ d3d11 \_ options1**.

Cette section décrit ces deux niveaux.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                           | Description                                       |
|---------------------------------|---------------------------------------------------|
| [Niveau 1](tier-1.md)<br/> | Cette section décrit la prise en charge de niveau 1.<br/> |
| [Niveau 2](tier-2.md)<br/> | Cette section décrit le support de niveau 2.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources en mosaïque](tiled-resources.md)
</dt> </dl>

 

 





