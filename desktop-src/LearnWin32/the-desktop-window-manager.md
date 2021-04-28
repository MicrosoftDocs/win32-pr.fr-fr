---
title: Gestionnaire de fenêtrage
description: Gestionnaire de fenêtrage
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fca8550134ba0c1cdafe0bd5c349061ef900a9e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103897"
---
# <a name="the-desktop-window-manager"></a>Gestionnaire de fenêtrage

Avant Windows Vista, un programme Windows serait directement dessiné à l’écran. En d’autres termes, le programme écrit directement dans la mémoire tampon indiquée par la carte vidéo. Cette approche peut provoquer des artefacts visuels si une fenêtre ne se repeint pas correctement. Par exemple, si l’utilisateur fait glisser une fenêtre sur une autre fenêtre, et que la fenêtre située en dessous ne se redessine pas suffisamment rapidement, la fenêtre supérieure peut sortir d’une piste :

![capture d’écran qui montre les artefacts de redessin.](images/graphics04.png)

La trace est due au fait que Windows peigne à la même zone de mémoire. Lorsque vous faites glisser la fenêtre de niveau supérieur, la fenêtre située en dessous doit être redessinée. Si le redessin est trop lent, cela provoque l’affichage des artefacts dans l’image précédente.

Windows Vista a modifié fondamentalement la manière dont les fenêtres sont dessinées, en introduisant le Gestionnaire de fenêtrage (DWM). Lorsque le DWM est activé, une fenêtre ne dessine plus directement dans la mémoire tampon d’affichage. Au lieu de cela, chaque fenêtre dessine dans une mémoire tampon hors écran, également appelée *surface hors écran*. Le DWM compose ensuite ces surfaces à l’écran.

![diagramme qui montre comment le DWM composite le bureau.](images/graphics05.png)

Le DWM offre plusieurs avantages par rapport à l’ancienne architecture graphique.

-   Moins de messages de redessin. Quand une fenêtre est obstruée par une autre fenêtre, la fenêtre masquée n’a pas besoin de se repeindre.
-   Des artefacts réduits. Auparavant, le fait de faire glisser une fenêtre pouvait créer des artefacts visuels, comme décrit.
-   Effets visuels. Étant donné que le DWM est en mesure de comcréer l’écran, il peut restituer des zones translucides et floues de la fenêtre.
-   Mise à l’échelle automatique pour la haute résolution. Même si la mise à l’échelle n’est pas la méthode idéale pour gérer les résolutions élevées, il s’agit d’un secours viable pour les applications plus anciennes qui n’ont pas été conçues pour des paramètres haute résolution. (Nous allons revenir à cette rubrique plus tard, dans la section [dpi et Device-Independent pixels](dpi-and-device-independent-pixels.md).)
-   Autres affichages. Le DWM peut utiliser les surfaces hors écran de différentes façons intéressantes. Par exemple, le DWM est la technologie sous-jacente de Windows Flip 3D, des miniatures et des transitions animées.

Notez, cependant, qu’il n’est pas garanti que le DWM soit activé. La carte graphique ne prend peut-être pas en charge la configuration système requise pour DWM et les utilisateurs peuvent désactiver le DWM via le panneau de configuration **Propriétés système** . Cela signifie que votre programme ne doit pas reposer sur le comportement de redessin du DWM. Testez votre programme avec DWM désactivé pour vous assurer qu’il se repeint correctement.

## <a name="next"></a>Suivant

[Mode de conservation et mode immédiat](retained-mode-versus-immediate-mode.md)

 

 




