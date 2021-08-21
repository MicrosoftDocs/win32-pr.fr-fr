---
description: Attributs EVR
ms.assetid: 33f9bb09-625f-4bbb-a884-70c6bba3700b
title: Attributs EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b5af186a909dc672876eb12846e842360ccabfd3f2cc1de8f203d3e40d94ce7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974538"
---
# <a name="evr-attributes"></a>Attributs EVR

Les attributs suivants peuvent être utilisés pour configurer le convertisseur vidéo amélioré (EVR).



| Attribut                                                                                                         | Description                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [EVRConfig \_ AllowBatching](evrconfig-allowbatching.md)                                                           | Permet à EVR de traiter par lots les appels à la méthode Microsoft Direct3D **IDirect3DDevice9 ::P** renouvely.                            |
| [EVRConfig \_ AllowDropToBob](evrconfig-allowdroptobob.md)                                                         | Permet à l’EVR d’améliorer les performances à l’aide de l’entrelacement Bob.                                                        |
| [EVRConfig \_ AllowDropToHalfInterlace](evrconfig-allowdroptohalfinterlace.md)                                     | Permet à l’EVR d’améliorer les performances en ignorant le deuxième champ de chaque trame entrelacée.                            |
| [EVRConfig \_ AllowDropToThrottle](evrconfig-allowdroptothrottle.md)                                               | Autorise le EVR à limiter sa sortie pour qu’il corresponde à la bande passante GPU.                                                               |
| [EVRConfig \_ AllowScaling](evrconfig-allowscaling.md)                                                             | Permet au EVR de mélanger la vidéo dans un rectangle qui est plus petit que le rectangle de sortie, puis de mettre à l’échelle le résultat. |
| [EVRConfig \_ ForceBatching](evrconfig-forcebatching.md)                                                           | Force EVR à appeler par lots la méthode **IDirect3D9Device ::P** renouvely.                                               |
| [EVRConfig \_ ForceBob](evrconfig-forcebob.md)                                                                     | Force le EVR à utiliser la désentrelacement Bob.                                                                                 |
| [EVRConfig \_ ForceHalfInterlace](evrconfig-forcehalfinterlace.md)                                                 | Force le EVR à ignorer le deuxième champ de chaque trame entrelacée.                                                       |
| [EVRConfig \_ ForceScaling](evrconfig-forcescaling.md)                                                             | Force le EVR à mélanger la vidéo dans un rectangle qui est plus petit que le rectangle de sortie, puis à mettre à l’échelle le résultat. |
| [EVRConfig \_ ForceThrottle](evrconfig-forcethrottle.md)                                                           | Force le EVR à limiter sa sortie pour qu’il corresponde à la bande passante GPU.                                                               |
| [**activer \_ le \_ \_ \_ MÉLANGEur vidéo \_ personnalisé MF activé**](mf-activate-custom-video-mixer-activate-attribute.md)         | Spécifie un objet d’activation qui crée un mélangeur vidéo personnalisé pour le convertisseur vidéo amélioré (EVR).                  |
| [**\_activer le \_ \_ CLSID du \_ MÉLANGEur vidéo personnalisé \_ MF**](mf-activate-custom-video-mixer-clsid-attribute.md)               | CLSID d’un mélangeur vidéo personnalisé pour EVR.                                                                               |
| [**\_activer les \_ \_ indicateurs du \_ MÉLANGEur vidéo personnalisé \_ MF**](mf-activate-custom-video-mixer-flags-attribute.md)               | Spécifie comment créer un mélangeur personnalisé pour le EVR.                                                                      |
| [**activer \_ le \_ \_ \_ PRÉSENTateur vidéo personnalisé \_ MF activer**](mf-activate-custom-video-presenter-activate-attribute.md) | Spécifie un objet d’activation qui crée un présentateur vidéo personnalisé pour le EVR.                                        |
| [**PP \_ activer \_ le \_ CLSID vidéo personnalisé \_ présentateur \_**](mf-activate-custom-video-presenter-clsid-attribute.md)       | CLSID d’un présentateur vidéo personnalisé pour EVR.                                                                           |
| [**\_activer les \_ \_ indicateurs de \_ PRÉSENTateur vidéo personnalisé \_ MF**](mf-activate-custom-video-presenter-flags-attribute.md)       | Spécifie comment créer un présentateur personnalisé pour le EVR.                                                                  |
| [**\_ \_ fenêtre vidéo d’activation MF \_**](mf-activate-video-window-attribute.md)                                         | Handle vers la fenêtre de découpage vidéo.                                                                                     |
| [**\_nombre d' \_ \_ échantillons requis As MF \_**](mf-sa-required-sample-count-attribute.md)                                  | Indique le nombre de mémoires tampons non compressées dont le récepteur multimédia EVR a besoin pour l’entrelacement.                         |
| [**\_rectangle de zoom vidéo \_**](video-zoom-rect-attribute.md)                                                            | Spécifie le rectangle de zoom pour le mélangeur EVR.                                                                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Convertisseur vidéo amélioré](enhanced-video-renderer.md)
</dt> </dl>

 

 



