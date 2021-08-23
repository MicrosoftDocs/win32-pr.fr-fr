---
description: Les modifications apportées à la palette système pour le périphérique d’affichage peuvent avoir des effets spectaculaires et parfois indésirables sur les couleurs utilisées dans Windows sur le bureau.
ms.assetid: 9c470b6f-c0d3-462e-9649-1f39b06bd543
title: Messages de palette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a82c5ae2727e9f687f5f7fb628279b7832e896991f703225beec075a6630133
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558439"
---
# <a name="palette-messages"></a>Messages de palette

Les modifications apportées à la palette système pour le périphérique d’affichage peuvent avoir des effets spectaculaires et parfois indésirables sur les couleurs utilisées dans Windows sur le bureau. Pour réduire l’impact de ces modifications, le système fournit un ensemble de messages qui permettent aux applications de gérer leurs palettes logiques tout en veillant à ce que les couleurs de la fenêtre active soient aussi proches que possible des couleurs prévues.

Le système envoie un message [**WM \_ QUERYNEWPALETTE**](wm-querynewpalette.md) à une fenêtre de niveau supérieur ou Overlapped juste avant d’activer la fenêtre. Ce message donne à une application la possibilité de sélectionner et de réaliser sa palette logique afin qu’elle reçoive le meilleur mappage possible des couleurs pour sa palette logique. Lorsque l’application reçoit le message, elle doit utiliser les fonctions [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette), [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject)et [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) pour sélectionner et réaliser la palette logique. Cela permet au système de mettre à jour les couleurs de la palette système de sorte que ses couleurs correspondent autant de couleurs que possible dans la palette logique.

Lorsqu’une application entraîne des modifications de la palette système suite à la réalisation de sa palette logique, le système envoie un message [**WM \_ PALETTECHANGED**](wm-palettechanged.md) à toutes les fenêtres superposées et de niveau supérieur. Ce message donne aux applications la possibilité de mettre à jour les couleurs des zones clientes de leurs fenêtres, en remplaçant les couleurs qui ont changé par des couleurs qui correspondent davantage aux couleurs prévues. Une application qui reçoit le **message WM \_ PALETTECHANGED** doit utiliser [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) et [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) pour réinitialiser les palettes logiques associées à toutes les fenêtres inactives, puis mettre à jour les couleurs dans la zone cliente pour chaque fenêtre inactive à l’aide de la fonction [**UpdateColors**](/windows/desktop/api/Wingdi/nf-wingdi-updatecolors) . Cette technique ne garantit pas le plus grand nombre de correspondances de couleurs exactes. Toutefois, cela permet de s’assurer que les couleurs de la palette logique sont mappées à des couleurs raisonnables dans la palette du système.

> [!Note]  
> Pour éviter de créer une boucle infinie, une application ne doit jamais se rendre compte de la palette de la fenêtre dont le descripteur correspond au descripteur passé dans le paramètre *wParam* du message [**WM \_ PALETTECHANGED**](wm-palettechanged.md) .

 

La fonction [**UpdateColors**](/windows/desktop/api/Wingdi/nf-wingdi-updatecolors) met généralement à jour une zone cliente d’une fenêtre inactive plus rapidement que le rafraîchissement de la zone. Toutefois, étant donné que **UpdateColors** effectue la traduction des couleurs en fonction de la couleur de chaque pixel avant la modification de la palette du système, chaque appel à cette fonction entraîne une perte de précision de la couleur. Cela signifie que **UpdateColors** ne peut pas être utilisé pour mettre à jour les couleurs quand la fenêtre devient active. Dans ce cas, l’application doit redessiner la zone cliente.

Le système peut envoyer le message [**WM \_ QUERYNEWPALETTE**](wm-querynewpalette.md) lorsque des modifications sont apportées à la palette logique. En outre, le système peut envoyer le message [**WM \_ PALETTEISCHANGING**](wm-paletteischanging.md) à toutes les fenêtres superposées et de niveau supérieur lorsque la palette du système va être modifiée.

 

 



