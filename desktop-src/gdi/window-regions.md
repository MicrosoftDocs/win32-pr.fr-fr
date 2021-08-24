---
description: En plus de la région de mise à jour, chaque fenêtre possède une zone visible qui définit la partie de la fenêtre visible par l’utilisateur.
ms.assetid: 9d8beba1-93c0-437d-a138-76880a40bc79
title: Régions de fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac3f751303d8a971d010ea7dabf7604c24db892f88d9a4029f0189d303cf5a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727409"
---
# <a name="window-regions"></a>Régions de fenêtre

En plus de la région de mise à jour, chaque fenêtre possède une *zone visible* qui définit la partie de la fenêtre visible par l’utilisateur. Le système modifie la zone visible pour la fenêtre chaque fois que la fenêtre change de taille ou lorsqu’une autre fenêtre est déplacée de telle sorte qu’elle masque ou expose une partie de la fenêtre. Les applications ne peuvent pas modifier directement la région visible, mais le système utilise automatiquement la région visible pour créer la zone de découpage pour tout contexte de périphérique d’affichage récupéré pour la fenêtre.

La *zone de découpage* détermine où le système autorise le dessin. Lorsque l’application récupère un contexte de périphérique d’affichage à l’aide de la fonction [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)ou [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) , le système définit la zone de découpage pour le contexte de périphérique sur l’intersection de la région visible et de la région de mise à jour. Les applications peuvent modifier la zone de découpage à l’aide de fonctions telles que [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn), [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) et [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn), afin de limiter davantage le dessin à une partie particulière de la zone de mise à jour.

Les \_ styles WS CLIPCHILDREN et WS \_ CLIPSIBLINGS spécifient plus en détail la façon dont le système calcule la région visible pour une fenêtre. Si une fenêtre possède un ou plusieurs de ces styles, la zone visible exclut les fenêtres enfants ou sœurs (Windows ayant la même fenêtre parente). Par conséquent, le dessin qui pourrait entraîner une intrusion dans ces fenêtres sera toujours coupé.

 

 



