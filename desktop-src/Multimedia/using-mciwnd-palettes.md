---
title: Utilisation des palettes MCIWnd
description: Utilisation des palettes MCIWnd
ms.assetid: 2b99ca57-f321-4286-8ebf-ae3344d8d2c9
keywords:
- MCIWndGetPalette macro)
- MCIWndSetPalette macro)
- MCIWndRealize macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970e0e33c9dd03c7f1133576f371b713f7174df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194952"
---
# <a name="using-mciwnd-palettes"></a>Utilisation des palettes MCIWnd

La diffusion de clips vidéo avec une profondeur de couleur de 8 bits (capacité de 256) nécessite une palette pour définir les couleurs à utiliser. Parfois, la palette incluse avec un clip vidéo n’est pas la palette la plus appropriée à utiliser lors de la lecture. Dans ce cas, MCIWnd offre trois moyens de gérer les palettes pour la lecture :

-   Récupérez un handle vers la palette associée à une fenêtre MCIWnd à l’aide de la macro [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) . La palette n’est pas nécessairement associée exclusivement à la fenêtre MCIWnd. D’autres applications peuvent accéder au handle de palette, et même l’invalider. Par conséquent, votre application doit anticiper l’utilisation globale de la palette et, lorsque vous avez terminé avec la palette, ne doit pas la libérer.
-   Spécifiez une nouvelle palette à utiliser avec le clip vidéo associé à une fenêtre MCIWnd à l’aide de la macro [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) .
-   Réalisez la palette associée à une fenêtre MCIWnd dans la palette système à l’aide de la macro [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) . Cette macro appelle la fonction [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) avec la palette associée à la fenêtre MCIWnd. Si les gestionnaires de messages de votre application pour [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) et [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) appellent uniquement **RealizePalette** ou **MCIWndRealize**, vous devez transférer ces messages à MCIWnd si vous ne les gérez pas vous-même.

> [!Note]  
> Quand un clip vidéo avec une profondeur de couleur de 8 bits est chargé dans la fenêtre MCIWnd, la palette incluse avec ce clip remplace la palette associée à la fenêtre MCIWnd.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Améliorations de la lecture](playback-enhancements.md)
</dt> </dl>

 

 