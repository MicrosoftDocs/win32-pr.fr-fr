---
title: Gestionnaire de fenêtres du Bureau
description: la fonctionnalité de composition du bureau, introduite dans Windows Vista, a modifié fondamentalement la manière dont les applications affichent les pixels à l’écran.
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
ms.openlocfilehash: a8259be171f225cc955546314febdff5395a47318499b830ee855bc8b985b025
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456039"
---
# <a name="desktop-window-manager"></a>Gestionnaire de fenêtres du Bureau

la fonctionnalité de composition du bureau, introduite dans Windows Vista, a modifié fondamentalement la manière dont les applications affichent les pixels à l’écran. Lorsque la composition du Bureau est activée, les fenêtres individuelles ne dessinent plus directement sur l’écran ou l’appareil d’affichage principal comme c’était le cas dans les versions précédentes de Windows. Au lieu de cela, leur dessin est redirigé vers des surfaces hors écran dans la mémoire vidéo, qui sont ensuite rendues dans une image de bureau et présentées à l’écran.

La composition du Bureau est effectuée par le Gestionnaire de fenêtrage (DWM). grâce à la composition du poste de travail, DWM active les effets visuels sur le bureau, ainsi que diverses fonctionnalités telles que les cadres de fenêtres en verre, les animations de transition de fenêtre 3d, les Windows Flip et Windows Flip3D, ainsi que la prise en charge de la haute résolution.

le Gestionnaire de fenêtrage s’exécute en tant que service Windows. Vous pouvez l’activer et le désactiver à l’aide de l’élément outils d’administration du panneau de configuration, sous services, comme gestionnaire de sessions Gestionnaire de fenêtrage.

La plupart des fonctionnalités DWM peuvent être contrôlées ou accessibles par une application via les API DWM. La documentation suivante décrit les fonctionnalités et les exigences des API DWM.

-   [Vues d’ensemble de DWM](desktop-window-manager-overviews.md)
-   [Exemple de code DWM](dwm-samples.md)
-   [Référence DWM](reference.md)

 

 




