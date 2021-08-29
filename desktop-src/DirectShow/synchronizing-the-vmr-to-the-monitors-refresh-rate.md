---
description: Synchronisation de VMR avec la fréquence d’actualisation du moniteur
ms.assetid: 73e73821-fb08-488a-956e-ef33f6651a26
title: Synchronisation de VMR avec la fréquence d’actualisation du moniteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4fa5055435d3adf737a3cdc253a3a43b041e5e849ac9c2b793ca37cedc78c0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072333"
---
# <a name="synchronizing-the-vmr-to-the-monitors-refresh-rate"></a>Synchronisation de VMR avec la fréquence d’actualisation du moniteur

Dans de rares scénarios, vous souhaiterez peut-être synchroniser précisément le rendu vidéo avec la fréquence d’actualisation du moniteur, afin qu’un juste nouveau Frame soit présenté chaque fois que l’analyse est actualisée. La méthode la plus fiable consiste à créer un Allocator-Presenter personnalisé qui utilise une opération de retournement au lieu d’une opération blit pour écrire les bits vidéo dans la surface principale. « Flip » est appelé chaque fois que l’analyse est actualisée. par conséquent, si votre flux vidéo ne contient pas de datage, VMR est rendu aussi rapide que possible à la surface principale, mais la surface bloque le flux jusqu’à ce que l’opération de retournement soit terminée. Cela signifie que, tant que le processeur n’est pas surchargé, le frame suivant est toujours en attente dans la surface principale chaque fois que l’analyse est actualisée. toutefois, si un autre processus nécessitant beaucoup de ressources processeur est en cours d’exécution, il risque de priver votre DirectShow thread de diffusion en continu afin qu’il ne puisse pas remettre des images vidéo suffisamment rapidement à la surface principale.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mode de lecture non rendu VMR (Allocator personnalisé-présentateur)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



