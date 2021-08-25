---
title: Niveaux de fonctionnalités des ressources en mosaïque
description: Direct3D 11,2 expose la prise en charge des ressources en mosaïque dans deux niveaux avec les \_ valeurs de niveau de ressources en mosaïque d3d11 \_ \_ .
ms.assetid: E6A6565B-079B-47DB-A80C-CA5B5413BA32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1b76c1d90cc48210f02983817b317eb830224b8f87bb8b4904ee3e11d6cdd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894379"
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

 

 





