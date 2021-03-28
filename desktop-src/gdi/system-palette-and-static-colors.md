---
description: En règle générale, les entrées de la palette système que le système réserve pour les couleurs statiques ne peuvent pas être modifiées.
ms.assetid: be258151-36cc-42ba-8005-ff9d8e59b894
title: Palette système et couleurs statiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 537bdc87fecdd055334b83a56b0a53f9999be94c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973083"
---
# <a name="system-palette-and-static-colors"></a>Palette système et couleurs statiques

En règle générale, les entrées de la palette système que le système réserve pour les couleurs statiques ne peuvent pas être modifiées. Une application peut remplacer ce comportement par défaut à l’aide de la fonction [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) pour réduire le nombre d’entrées de couleur statique et, par conséquent, augmenter le nombre d’entrées de palette système inutilisées. Toutefois, étant donné que la modification des couleurs statiques peut avoir un effet immédiat et spectaculaire sur toutes les fenêtres à l’écran, une application ne doit pas appeler **SetSystemPaletteUse**, sauf si elle a une fenêtre agrandie et le focus d’entrée.

Quand une application appelle [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) avec la \_ valeur nostatique SYSPAL, le système libère toutes les entrées sauf deux des entrées réservées, ce qui permet à ces entrées de recevoir de nouvelles valeurs de couleur lorsque l’application réalise par la suite sa palette logique. Les deux autres entrées de couleur statiques restent réservées et sont définies en blanc et noir. Une application peut restaurer les entrées réservées en appelant **SetSystemPaletteUse** avec la \_ valeur statique SYSPAL. Il peut découvrir l’utilisation actuelle de la palette système à l’aide de la fonction [**GetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteuse) .

En outre, après avoir défini l’utilisation de la palette système sur SYSPAL \_ Nostatic, l’application doit immédiatement réaliser sa palette logique, appeler la fonction [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) pour enregistrer les paramètres de couleur système actuels, appeler la fonction [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) pour définir les couleurs système sur des valeurs raisonnables en utilisant le noir et le blanc, et enfin envoyer le message [**WM \_ SYSCOLORCHANGE**](wm-syscolorchange.md) à d’autres fenêtres de niveau supérieur pour les autoriser Quand vous définissez des couleurs système en noir et blanc, l’application doit s’assurer que les éléments adjacents ou qui se chevauchent, tels que les cadres de fenêtre et les bordures, sont respectivement en noir et blanc.

Avant que l’application perde le focus d’entrée, ferme sa fenêtre ou se termine, elle doit immédiatement appeler [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) avec la \_ valeur statique SYSPAL, réaliser sa palette logique, restaurer les couleurs système à leurs valeurs précédentes et envoyer le message [**WM \_ SYSCOLORCHANGE**](wm-syscolorchange.md) . Le système envoie un message de [**\_ peinture WM**](wm-paint.md) à toute fenêtre affectée par une modification de couleur système. Les applications qui ont des pinceaux utilisant les couleurs système existantes doivent supprimer ces pinceaux et les recréer à l’aide des nouvelles couleurs système.

 

 
