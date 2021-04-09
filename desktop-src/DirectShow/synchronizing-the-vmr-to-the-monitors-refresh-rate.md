---
description: Synchronisation de VMR avec la fréquence d’actualisation du moniteur
ms.assetid: 73e73821-fb08-488a-956e-ef33f6651a26
title: Synchronisation de VMR avec la fréquence d’actualisation du moniteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a9550e96e6a2e35c196048d38dd5b6e5b536d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210458"
---
# <a name="synchronizing-the-vmr-to-the-monitors-refresh-rate"></a>Synchronisation de VMR avec la fréquence d’actualisation du moniteur

Dans de rares scénarios, vous souhaiterez peut-être synchroniser précisément le rendu vidéo avec la fréquence d’actualisation du moniteur, afin qu’un juste nouveau Frame soit présenté chaque fois que l’analyse est actualisée. La méthode la plus fiable consiste à créer un Allocator-Presenter personnalisé qui utilise une opération de retournement au lieu d’une opération blit pour écrire les bits vidéo dans la surface principale. « Flip » est appelé chaque fois que l’analyse est actualisée. par conséquent, si votre flux vidéo ne contient pas de datage, VMR est rendu aussi rapide que possible à la surface principale, mais la surface bloque le flux jusqu’à ce que l’opération de retournement soit terminée. Cela signifie que, tant que le processeur n’est pas surchargé, le frame suivant est toujours en attente dans la surface principale chaque fois que l’analyse est actualisée. Toutefois, si un autre processus nécessitant beaucoup de ressources processeur est en cours d’exécution, il risque de priver votre thread de diffusion en continu DirectShow afin qu’il ne puisse pas remettre des images vidéo suffisamment rapidement à la surface principale.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mode de lecture non rendu VMR (Allocator personnalisé-présentateur)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



