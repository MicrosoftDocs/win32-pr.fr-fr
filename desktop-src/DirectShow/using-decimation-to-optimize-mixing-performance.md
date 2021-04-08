---
description: Utilisation de la décimalisation pour optimiser les performances de mixage
ms.assetid: 94d4ce86-9d60-4fd4-ab01-851dc073680b
title: Utilisation de la décimalisation pour optimiser les performances de mixage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e9e4ddfe3bbba3eb5eeab91b7cf0e8b9cbfa03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866458"
---
# <a name="using-decimation-to-optimize-mixing-performance"></a>Utilisation de la décimalisation pour optimiser les performances de mixage

> [!IMPORTANT]
> L’optimisation décrite dans cette section dépend fortement du matériel sous-jacent. À moins que vous ne puissiez garantir le type de matériel graphique qui sera utilisé avec l’application, cela peut sérieusement nuire à l’apparence de l’image vidéo.

 

La HDTV requiert beaucoup de puissance de traitement, qui, sur les systèmes les plus récents, est fournie principalement par la carte graphique. Toutefois, même si la carte graphique et le décodeur peuvent prendre en charge des résolutions de 1920 x 1080, il se peut que l’analyse de l’utilisateur ne soit pas toujours définie sur cette résolution. Dans ce cas, la puce graphique est requise pour créer une image 1920 x 1080, puis réduire la résolution avant de l’envoyer à la mémoire tampon de trame.

Étant donné qu’il s’agit d’un gaspillage de la puissance de traitement, VMR offre un moyen de décimer (réduire) l’image au moment où elle est rendue sur la surface DirectDraw. Cela élimine la copie de mémoire supplémentaire requise si l’image doit être redimensionnée après son rendu.

**VMR-7 :** Pour activer la décimalisation, appelez [**IVMRMixerControl :: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) avec l' \_ indicateur DecimateOutput MixerPref.

**VMR-9 :** Pour activer la décimalisation, appelez [**IVMRMixerControl9 :: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) avec l' \_ indicateur DecimateOutput MixerPref9.

La méthode **SetMixingPrefs** doit être appelée avant que VMR soit connecté. Les indicateurs de préférence de mixage ne peuvent pas être modifiés une fois que le graphique est en cours d’exécution.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du mode de mixage VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



