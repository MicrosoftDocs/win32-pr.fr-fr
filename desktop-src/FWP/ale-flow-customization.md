---
title: Personnalisation du fluide ALE
description: Le filtrage réseau au niveau des couches de mise en œuvre de la couche application (ALE) de la plateforme de filtrage Windows (WFP) peut être personnalisé en ajoutant des filtres avec des options de classification spécifiques.
ms.assetid: 123af237-cf42-410b-8a2f-c011cb5f4f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9843a60719f424403139885f24f165c0dd936b
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104314366"
---
# <a name="ale-flow-customization"></a>Personnalisation du fluide ALE

Le filtrage réseau au niveau des couches de mise en œuvre de la couche application (ALE) de la plateforme de filtrage Windows (WFP) peut être personnalisé en ajoutant des filtres avec des options de classification spécifiques.

## <a name="multicastbroadcast-traffic"></a>Trafic de multidiffusion/diffusion

Pour bloquer le trafic entrant en fonction des États de multidiffusion ou de diffusion sortants, ajoutez un filtre qui autorise le trafic de multidiffusion et de diffusion en sortie et dont l’option d' [**\_ \_ \_ \_ État de multidiffusion option de classement fwp**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) a la **valeur d' \_ option fwp refuser l' \_ \_ \_ \_ État de multidiffusion**.

## <a name="remote-peers"></a>Homologues distants

Pour ajouter des paquets de réponse provenant de différents pairs au même fluide ALE, ajoutez un filtre dont l’option de [**\_ \_ \_ \_ \_ mappage de source libre de l’option de classement fwp**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) est définie sur la valeur d' **\_ option fwp activer le \_ \_ \_ \_ \_ mappage de source libre**.

Consultez [utilisation des options de classification pour l'](using-classify-options.md) exemple de code.

## <a name="ale-flow-lifetime"></a>Durée de vie du flot ALE

Pour modifier les valeurs du délai d’inactivité d’un fluide ALE, ajoutez un filtre avec l’option de durée de vie de l' [**\_ option de classification fwp \_ \_ \_ \_ Bcast**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) et/ou l’option de durée de vie **\_ \_ \_ \_ monodiffusion option de classement fwp** définie sur la valeur du délai d’inactivité souhaité.

Consultez [utilisation des options de classification](using-classify-options.md) pour obtenir un exemple de code.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Application de la couche application (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Couches ALE](ale-layers.md)
</dt> <dt>

[Filtrage avec état ALE](ale-stateful-filtering.md)
</dt> <dt>

[Trafic de diffusion/multidiffusion ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Réautorisation ALE](ale-re-authorization.md)
</dt> <dt>

[Utilisation des options de classification](using-classify-options.md)
</dt> </dl>

 

 




