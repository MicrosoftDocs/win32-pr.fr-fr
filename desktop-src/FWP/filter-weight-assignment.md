---
title: Affectation de poids de filtre
description: chaque filtre de la plateforme de filtrage Windows (WFP) est associé à un poids, qui est utilisé pendant l’arbitrage des filtres.
ms.assetid: c78854c2-9aa1-408f-82d6-4b9e52f38e84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9042b15da0df5f81c71a32deb923369a54243854e86aeaed1ba30c7fc8484193
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746869"
---
# <a name="filter-weight-assignment"></a>Affectation de poids de filtre

chaque filtre de la plateforme de filtrage Windows (WFP) est associé à un poids, qui est utilisé pendant l' [arbitrage des filtres](filter-arbitration.md).

Le poids de filtre utilisé par le moteur de filtrage de base (BFE) est de type [**fwp \_ UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type). Les appelants ont trois options lors de l’ajout de filtres.

-   Définissez le poids sur un [**fwp \_ UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type). BFE utilise le poids fourni tel quel.
-   Définissez le poids sur [**fwp \_ vide**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type). BFE génère automatiquement un poids dans la plage \[ 0, 2 ⁶ ⁰).
-   Définissez le poids sur un [**\_ UINT8 UINT8**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) dans la plage \[ 0, 15 \] . BFE utilise le poids fourni comme identificateur de plage de poids.

    BFE génère automatiquement les bits de poids faible 60 (exactement comme si le poids avait été défini sur [**fwp \_ vide**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)), puis utilise la valeur fournie pour définir les 4 bits de poids fort. Cela permet aux appelants de diviser manuellement l’espace de poids en 16 plages, tout en continuant à utiliser la pondération automatique au sein d’une plage.

> [!Note]  
> Lorsque deux ou plusieurs légendes sont inscrites sur la même sous-couche, des problèmes peuvent se produire lorsque le même poids est affecté aux filtres. Ce problème peut être évité en faisant en sorte que les légendes créent leur propre sous-couche à l’aide de [**FwpmSubLayerAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Identificateurs de poids de filtre**](filter-weight-identifiers.md)
</dt> </dl>

 

 




