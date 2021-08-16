---
title: Gestionnaire de fenêtrage
description: Gestionnaire de fenêtrage
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b99585a75bf2b25b086f09a17a0d8d93391b1f94f5018c5d4f83f90937fde620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896877"
---
# <a name="the-desktop-window-manager"></a>Gestionnaire de fenêtrage

avant Windows Vista, un programme Windows dessinerait directement à l’écran. En d’autres termes, le programme écrit directement dans la mémoire tampon indiquée par la carte vidéo. Cette approche peut provoquer des artefacts visuels si une fenêtre ne se repeint pas correctement. Par exemple, si l’utilisateur fait glisser une fenêtre sur une autre fenêtre, et que la fenêtre située en dessous ne se redessine pas suffisamment rapidement, la fenêtre supérieure peut sortir d’une piste :

![capture d’écran qui montre les artefacts de redessin.](images/graphics04.png)

La trace est due au fait que Windows peigne à la même zone de mémoire. Lorsque vous faites glisser la fenêtre de niveau supérieur, la fenêtre située en dessous doit être redessinée. Si le redessin est trop lent, cela provoque l’affichage des artefacts dans l’image précédente.

Windows Vista a modifié fondamentalement la manière dont les fenêtres sont dessinées, en introduisant le Gestionnaire de fenêtrage (DWM). Lorsque le DWM est activé, une fenêtre ne dessine plus directement dans la mémoire tampon d’affichage. Au lieu de cela, chaque fenêtre dessine dans une mémoire tampon hors écran, également appelée *surface hors écran*. Le DWM compose ensuite ces surfaces à l’écran.

![diagramme qui montre comment le DWM composite le bureau.](images/graphics05.png)

Le DWM offre plusieurs avantages par rapport à l’ancienne architecture graphique.

-   Moins de messages de redessin. Quand une fenêtre est obstruée par une autre fenêtre, la fenêtre masquée n’a pas besoin de se repeindre.
-   Des artefacts réduits. Auparavant, le fait de faire glisser une fenêtre pouvait créer des artefacts visuels, comme décrit.
-   Effets visuels. Étant donné que le DWM est en mesure de comcréer l’écran, il peut restituer des zones translucides et floues de la fenêtre.
-   Mise à l’échelle automatique pour la haute résolution. Même si la mise à l’échelle n’est pas la méthode idéale pour gérer les résolutions élevées, il s’agit d’un secours viable pour les applications plus anciennes qui n’ont pas été conçues pour des paramètres haute résolution. (Nous allons revenir à cette rubrique plus tard, dans la section [dpi et Device-Independent pixels](dpi-and-device-independent-pixels.md).)
-   Autres affichages. Le DWM peut utiliser les surfaces hors écran de différentes façons intéressantes. par exemple, le DWM est la technologie derrière Windows rotation 3d, les miniatures et les transitions animées.

Notez, cependant, qu’il n’est pas garanti que le DWM soit activé. La carte graphique ne prend peut-être pas en charge la configuration système requise pour DWM et les utilisateurs peuvent désactiver le DWM via le panneau de configuration **Propriétés système** . Cela signifie que votre programme ne doit pas reposer sur le comportement de redessin du DWM. Testez votre programme avec DWM désactivé pour vous assurer qu’il se repeint correctement.

## <a name="next"></a>Suivant

[Mode de conservation et mode immédiat](retained-mode-versus-immediate-mode.md)

 

 




