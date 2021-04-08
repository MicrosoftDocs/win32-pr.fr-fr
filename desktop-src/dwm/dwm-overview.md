---
title: Gestionnaire de fenêtres du Bureau
description: La fonctionnalité de composition du bureau, introduite dans Windows Vista, a modifié fondamentalement la manière dont les applications affichent les pixels à l’écran.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_overview.htm
keywords:
- Gestionnaire de fenêtrage (DWM), à propos de
- DWM (Gestionnaire de fenêtrage), à propos de
- Gestionnaire de fenêtrage (DWM), composition
- DWM (Gestionnaire de fenêtrage), composition
- composition du Bureau
- composition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8578001aebf1c73e6d400ffae383674a8432c399
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673661"
---
# <a name="desktop-window-manager"></a>Gestionnaire de fenêtres du Bureau

La fonctionnalité de composition du bureau, introduite dans Windows Vista, a modifié fondamentalement la manière dont les applications affichent les pixels à l’écran. Lorsque la composition du Bureau est activée, les fenêtres individuelles ne dessinent plus directement sur l’écran ou l’appareil d’affichage principal comme c’était le cas dans les versions précédentes de Windows. Au lieu de cela, leur dessin est redirigé vers des surfaces hors écran dans la mémoire vidéo, qui sont ensuite rendues dans une image de bureau et présentées à l’écran.

La composition du Bureau est effectuée par le Gestionnaire de fenêtrage (DWM). Grâce à la composition du bureau, DWM active les effets visuels sur le bureau, ainsi que diverses fonctionnalités telles que les cadres de fenêtres en verre, les animations de transition de fenêtre 3D, Windows Flip et Windows Flip3D et la haute résolution.

Le Gestionnaire de fenêtrage s’exécute en tant que service Windows. Vous pouvez l’activer et le désactiver à l’aide de l’élément outils d’administration du panneau de configuration, sous services, comme gestionnaire de sessions Gestionnaire de fenêtrage.

La plupart des fonctionnalités DWM peuvent être contrôlées ou accessibles par une application via les API DWM. La documentation suivante décrit les fonctionnalités et les exigences des API DWM.

-   [Vues d’ensemble de DWM](desktop-window-manager-overviews.md)
-   [Exemple de code DWM](dwm-samples.md)
-   [Référence DWM](reference.md)

 

 




