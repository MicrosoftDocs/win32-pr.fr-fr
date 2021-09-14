---
description: Fonctionnalités de VMR
ms.assetid: a809045b-b60d-4092-bc4d-0e70e17d2913
title: Fonctionnalités de VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c4a5a34be9fb3b3bb08df18091b88fbe7d7432
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224468"
---
# <a name="features-of-the-vmr"></a>Fonctionnalités de VMR

Le convertisseur de mixage vidéo 7 (VMR-7) prend en charge les nouvelles fonctionnalités suivantes :

-   Mélange réel de plusieurs flux vidéo à l’aide des fonctionnalités de fusion alpha des périphériques matériels Direct3D.
-   La possibilité de brancher votre propre composant de composition pour implémenter des effets et des transitions entre plusieurs flux vidéo entrant VMR.
-   Rendu true sans fenêtre. Il n’est plus nécessaire de faire de la fenêtre de lecture vidéo un enfant de la fenêtre de l’application afin de contenir la lecture vidéo. Le nouveau mode de rendu sans fenêtre de VMR permet aux applications d’héberger facilement la lecture vidéo dans n’importe quelle fenêtre sans avoir à transférer les messages de fenêtre au convertisseur pour le traitement spécifique au convertisseur.
-   Nouveau mode de lecture non rendu dans lequel les applications peuvent fournir leur propre composant allocateur pour accéder à l’image vidéo décodée avant de l’afficher à l’écran.
-   Prise en charge améliorée des PC équipés de plusieurs moniteurs.
-   Prise en charge de la nouvelle architecture d’accélération vidéo DirectX de Microsoft.
-   Prise en charge de la lecture vidéo de haute qualité simultanément sur plusieurs fenêtres.
-   Prise en charge du mode exclusif DirectDraw
-   100% de compatibilité descendante avec les applications existantes.
-   Prise en charge du pas à pas et d’un moyen fiable de capturer l’image actuelle affichée.
-   La possibilité pour les applications de se mélanger facilement à l’aide d’alpha de leurs propres données d’image statiques (telles que les logos de canaux ou les composants d’interface utilisateur) avec la vidéo de façon sans scintillement.

VMR-9 prend en charge toutes les fonctionnalités mentionnées ci-dessus, ainsi que :

-   La possibilité de traiter les données vidéo directement avec les API Direct3D, telles que les nuanceurs de pixels.
-   Prise en charge améliorée du contenu vidéo entrelacé.
-   Prise en charge sur toutes les plateformes prises en charge par DirectX.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos du rendu de mixage vidéo](about-the-video-mixing-render.md)
</dt> </dl>

 

 



