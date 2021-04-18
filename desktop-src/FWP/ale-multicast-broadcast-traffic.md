---
title: Trafic de diffusion/multidiffusion ALE
description: Tout le trafic de multidiffusion et de diffusion entrant au niveau des couches d’application de la couche application (ALE) est mappé à un flux ALE global.
ms.assetid: b10b9758-8fce-4256-a25d-917e01336456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30b56a6e2a27a209baf66d34948b704ae321644
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309894"
---
# <a name="ale-multicastbroadcast-traffic"></a>Trafic de diffusion/multidiffusion ALE

Tout le trafic de multidiffusion et de diffusion entrant au niveau des couches d’application de la couche application (ALE) est mappé à un [flux ALE](ale-stateful-filtering.md)global. Le trafic de réponse pour les paquets de multidiffusion et de diffusion entrants est classé au niveau de la couche [**FWPM d' \_ authentification ALE de couche \_ ALE \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) , et des flux ALE distincts sont créés pour chaque réponse.

Le trafic de multidiffusion et de diffusion en sortie sur les couches ALE crée un flux ALE de 4 secondes. Par défaut, l’autorisation d’un paquet de multidiffusion ou de diffusion ALE de diffusion en sortie autorise le trafic entrant, qu’il s’agisse de monodiffusion, de multidiffusion ou de diffusion, depuis n’importe quelle adresse distante jusqu’à 4 secondes. Ce flux ALE peut uniquement être actualisé ou maintenu actif par le trafic sortant suivant qui correspond au flux ALE.

> [!Note]  
> La durée de vie de 4 secondes est spécifiée par les options Set d’appel FWPM de l' [**\_ \_ option Set Connect de la \_ \_ \_ \_ couche \_ V {4 \| 6}**](built-in-callout-identifiers.md)de la légende intégrée. Pour modifier la durée de vie par défaut de 4 secondes, ajoutez un filtre qui fait référence aux options de l' **ensemble de légendes FWPM appel de \_ \_ \_ \_ \_ \_ couche \_ V {4 \| 6}** . Pour plus d’informations, consultez [Personnalisation du fluide ALE](ale-flow-customization.md) .

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Application de la couche application (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Couches ALE](ale-layers.md)
</dt> <dt>

[Filtrage avec état ALE](ale-stateful-filtering.md)
</dt> <dt>

[Réautorisation ALE](ale-re-authorization.md)
</dt> <dt>

[Personnalisation du fluide ALE](ale-flow-customization.md)
</dt> </dl>

 

 




