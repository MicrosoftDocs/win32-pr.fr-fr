---
description: La haute définition de Microsoft DirectX Video Acceleration (DXVA-HD) est une API pour le traitement vidéo accéléré par le matériel.
ms.assetid: 38ebec28-c4fc-4e72-ac87-1e41707d1908
title: DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f8694a28d8d5871112590c90bf166d1aa9246e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749253"
---
# <a name="dxva-hd"></a>DXVA-HD

La haute définition de Microsoft DirectX Video Acceleration (DXVA-HD) est une API pour le traitement vidéo accéléré par le matériel. DXVA-HD utilise le GPU pour exécuter des fonctions telles que l’entrelacement, la composition et la conversion de l’espace colorimétrique.

DXVA-HD est similaire au [traitement vidéo DXVA](dxva-video-processing.md) (DXVA-VP), mais offre des fonctionnalités améliorées et un modèle de traitement plus simple. En fournissant un modèle de composition plus flexible, DXVA-HD est conçu pour prendre en charge la prochaine génération de formats optiques HD et de normes de diffusion.

L’API DXVA-HD requiert un pilote d’affichage WDDM qui prend en charge l’interface DDI (Device Driver Interface) DXVA-HD ou un processeur logiciel de plug-in.

-   [Améliorations apportées à DXVA-VP](#improvements-over-dxva-vp)
-   [Rubriques connexes](#related-topics)

## <a name="improvements-over-dxva-vp"></a>Améliorations apportées à DXVA-VP

DXVA-HD étend l’ensemble des fonctionnalités fournies par DXVA-VP. Les améliorations sont les suivantes :

-   Mixage RGB et YUV. Tout flux peut avoir la valeur RVB ou YUV. Il n’existe plus de distinction entre le flux principal et les sous-flux.
-   Désentrelacement de plusieurs flux. Tout flux peut être progressif ou entrelacé. En outre, la cadence et la fréquence d’images peuvent varier d’un flux d’entrée à l’autre.
-   Couleurs d’arrière-plan RVB. Auparavant, seules les couleurs d’arrière-plan YUV étaient prises en charge.
-   Incrustation de luminance. Lorsque la incrustation de luminance est activée, les valeurs de luminance qui se trouvent dans une plage désignée deviennent transparentes.
-   Basculement dynamique entre les modes de désentrelacement.

DXVA-HD définit également certaines fonctionnalités avancées que les pilotes peuvent prendre en charge. Toutefois, les applications ne doivent pas supposer que tous les pilotes prendront en charge ces fonctionnalités. Les fonctionnalités avancées sont les suivantes :

-   Inverse telecine (par exemple, 60i à 24p).
-   Conversion de la fréquence des images (par exemple, 24p à 120P).
-   Modes de remplissage alphanumérique.
-   Réduction du bruit et filtrage d’amélioration des bords.
-   Mise à l’échelle non linéaire anamorphique.
-   YCbCr étendu (xvYCC).

Cette section contient les rubriques suivantes :

-   [Création d’un processeur vidéo DXVA-HD](creating-a-dxva-hd-video-processor.md)
-   [Vérification des formats DXVA-HD pris en charge](checking-supported-dxva-hd-formats.md)
-   [Création de surfaces vidéo DXVA-HD](creating-dxva-hd-video-surfaces.md)
-   [Définition des États DXVA-HD](setting-dxva-hd-states.md)
-   [Exécution du blit DXVA-HD](performing-the-dxva-hd-blit.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accélération vidéo DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[DXVA-HD, exemple](dxva-hd-sample.md)
</dt> </dl>

 

 



