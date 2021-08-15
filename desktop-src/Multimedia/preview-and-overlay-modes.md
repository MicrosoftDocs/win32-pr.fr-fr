---
title: Modes d’aperçu et de superposition
description: Modes d’aperçu et de superposition
ms.assetid: 11e7848f-efda-452c-a9c7-405e636a2ead
keywords:
- Message WM_CAP_SET_PREVIEW
- capPreview macro)
- Message WM_CAP_SET_PREVIEWRATE
- capPreviewRate macro)
- Message WM_CAP_SET_SCALE
- capPreviewScale macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9359b1380c5d6efe049bc4bea52a08a92f880af5d35558f4e65e21070f20c0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372368"
---
# <a name="preview-and-overlay-modes"></a>Modes d’aperçu et de superposition

Un pilote de capture peut implémenter deux méthodes pour afficher un flux vidéo entrant : le mode Aperçu et le mode superposition. Si un pilote de capture implémente les deux méthodes, l’utilisateur peut choisir la méthode à utiliser.

Le mode aperçu transfère les images numérisées du matériel de capture à la mémoire système, puis affiche les images numérisées dans la fenêtre de capture à l’aide des fonctions GDI (Graphics Device Interface). Les applications peuvent réduire le taux d’aperçu lorsque la fenêtre parente perd le focus et augmenter la vitesse d’aperçu lorsque la fenêtre parente obtient le focus. Cette action améliore la réactivité générale du système, car l’opération de préversion est gourmande en ressources processeur.

Trois messages permettent de contrôler l’opération d’aperçu.

-   Utilisez le message [**WM \_ Cap \_ Set \_ preview**](wm-cap-set-preview.md) pour activer ou désactiver le mode aperçu en envoyant (ou la macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) ) à une fenêtre de capture.
-   Utilisez le message [**WM \_ embout \_ Set \_ PREVIEWRATE**](wm-cap-set-previewrate.md) (ou la macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) ) pour définir la fréquence d’affichage des images en mode aperçu.
-   Utilisez le message de mise à l' [**\_ \_ \_ échelle WM Cap Set**](wm-cap-set-scale.md) (ou la macro [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) ) pour activer ou désactiver la mise à l’échelle de la vidéo d’aperçu.

Lorsque l’aperçu et la mise à l’échelle sont activés, l’image vidéo capturée est étirée sur les dimensions de la fenêtre de capture. L’activation du mode aperçu désactive automatiquement le mode superposition.

Le mode superposition est une fonction matérielle qui affiche le contenu de la mémoire tampon de capture sur le moniteur sans utiliser les ressources du processeur. Vous pouvez activer et désactiver le mode superposition en envoyant le message [**WM \_ Cap \_ Set \_ Overlay**](wm-cap-set-overlay.md) (ou la macro [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) ) à une fenêtre de capture. L’activation du mode superposition désactive automatiquement le mode aperçu.

Vous pouvez également définir la position de défilement de la trame vidéo dans la zone cliente de la fenêtre de capture pour le mode aperçu ou le mode superposition en envoyant le message de [**\_ \_ \_ défilement WM Cap Set**](wm-cap-set-scroll.md) (ou la macro [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) ) à une fenêtre de capture.

 

 




