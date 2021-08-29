---
description: Rubriques avancées sur la capture
ms.assetid: 407702b2-5f4f-424d-a3ec-b0473e1b0da3
title: Rubriques avancées sur la capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d80ba7615b0ad42bbfe62ae646a4cf7e58897cb678eae836b2b5329eda0e17c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690509"
---
# <a name="advanced-capture-topics"></a>Rubriques avancées sur la capture

Cette section décrit certains aspects avancés de la capture vidéo dans DirectShow. La plupart des problèmes décrits dans cette section sont gérés automatiquement par l’interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) . Toutefois, les informations fournies ici peuvent être utiles si vous devez dépanner une application de capture vidéo. Vous devez également lire cette section si votre application génère un graphique de capture personnalisé d’un certain type et que ICaptureGraphBuilder2 ne répond pas à vos besoins. Enfin, cette section contient des informations sur l’utilisation du filtre de mixage vidéo (VMR) dans une application de capture vidéo.

Il est possible de créer un graphique de capture vidéo entièrement à l’aide des méthodes [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) . Vous pouvez également combiner les deux interfaces, à l’aide de ICaptureGraphBuilder2 pour certaines tâches et IGraphBuilder pour d’autres.

Cette section contient les rubriques suivantes :

-   [Gestion des événements de redessin dans la capture vidéo](handling-repaint-events-in-video-capture.md)
-   [Utilisation des catégories de code confidentiel](working-with-pin-categories.md)
-   [Utilisation du filtre tee Smart](using-the-smart-tee-filter.md)
-   [utilisation de la superposition Mixer dans la Capture vidéo](using-the-overlay-mixer-in-video-capture.md)
-   [Broches de port vidéo](video-port-pins.md)
-   [Type de format VideoInfo2](videoinfo2-format-type.md)
-   [Création de filtres de Kernel-Mode](creating-kernel-mode-filters.md)
-   [Filtres de pilote de classe WDM](wdm-class-driver-filters.md)
-   [Utilisation de la capture WDDM dans DirectShow](using-wddm-capture-in-directshow.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Capture vidéo](video-capture.md)
</dt> </dl>

 

 



