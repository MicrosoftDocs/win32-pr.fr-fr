---
title: Utilisation des palettes
description: Utilisation des palettes
ms.assetid: 0ad0d78b-4c2c-499c-ad5e-8324b59e89fc
keywords:
- Message WM_CAP_PAL_PASTE
- capPalettePaste macro)
- Message WM_CAP_PAL_OPEN
- capPaletteOpen macro)
- Message WM_CAP_PAL_AUTOCREATE
- capPaletteAuto macro)
- Message WM_CAP_PAL_MANUALCREATE
- capPaletteManual macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09cbbe3ffc8ea21d1ecf8545f036f5ba6dfb927
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510193"
---
# <a name="working-with-palettes"></a>Utilisation des palettes

Au départ, si le format de capture vidéo nécessite une palette, la fenêtre de capture utilise la palette fournie par le pilote de capture. Cette palette peut comporter des valeurs de nuances de gris pour la reproduction en noir et blanc, ou une large sélection de valeurs de couleur. Vous pouvez récupérer une palette existante pour remplacer la palette par défaut à l’aide du message [**WM \_ capuchon \_ PAL \_ Paste**](wm-cap-pal-paste.md) ou [**WM \_ Cap \_ PAL \_ Open**](wm-cap-pal-open.md) (ou de la macro [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) ou [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) ). Vous pouvez également créer une palette personnalisée pour remplacer la palette par défaut à l’aide du [**message WM \_ Cap \_ PAL \_ AutoCreate**](wm-cap-pal-autocreate.md) ou [**WM \_ Cap \_ PAL \_ MANUALCREATE**](wm-cap-pal-manualcreate.md) (ou la macro [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) ou [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) ). Une fois que vous avez remplacé la palette par défaut, la fenêtre de capture et le pilote utilisent la palette de remplacement jusqu’à ce que vous ayez créé ou ouvert une autre palette.

Le \_ message WM Cap \_ PAL \_ AutoCreate ou WM \_ Cap \_ PAL \_ MANUALCREATE crée une palette optimisée basée sur l’entrée vidéo actuelle. Cette palette personnalisée donne à une séquence vidéo la meilleure fidélité des couleurs, car elle est basée sur les couleurs qui existent dans la séquence. La fenêtre de capture crée un histogramme à trois dimensions des couleurs qu’il échantillonne. Elle réduit le nombre de couleurs en examinant l’erreur absolue entre les couleurs adjacentes et en consolidant celles qui ont la plus petite valeur d’erreur.

Lors de l’envoi de la \_ création automatique de WM Cap \_ PAL \_ , vous devez spécifier le nombre d’images pour AVICap à échantillonner et spécifier la taille de la palette de couleurs. Lorsque vous spécifiez le nombre de frames, incluez suffisamment d’images pour vous assurer que toutes les couleurs de la séquence sont échantillonnées.

Vous pouvez échantillonner le frame en cours à l’aide de WM \_ Cap \_ PAL \_ MANUALCREATE. En utilisant ce message avec plusieurs frames sélectionnés manuellement, vous pouvez créer une palette qui contient les couleurs que vous souhaitez voir apparaître dans la palette.

Une palette peut contenir jusqu’à 256 couleurs. Si vous fusionnez des palettes ou si la séquence vidéo doit être affichée simultanément avec d’autres vidéos ou images, vous devez utiliser une plus petite sélection de couleurs pour que les couleurs de chaque image ou clip vidéo puissent coexister.

Pour enregistrer une nouvelle palette, utilisez le message [**WM \_ Cap \_ PAL \_ Save**](wm-cap-pal-save.md) (ou la macro [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) ) et récupérez-la ultérieurement à l’aide du message [**WM \_ Cap \_ PAL \_ Open**](wm-cap-pal-open.md) . Vous pouvez enregistrer une palette pour le traitement postérieur de la palette ou pour une utilisation dans une autre application.

Vous pouvez coller une palette du presse-papiers dans la fenêtre de capture à l’aide du message [**WM \_ Cap \_ PAL \_ Paste**](wm-cap-pal-paste.md) . La fenêtre de capture transmet la palette au pilote de capture. D’autres applications peuvent copier des palettes dans le presse-papiers. Vous pouvez également copier une palette dans le presse-papiers à l’aide du message [**WM \_ Cap \_ Edit \_ Copy**](wm-cap-edit-copy.md) (ou de la macro [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) ). Ce message copie la mémoire tampon de l’image vidéo, y compris la palette, dans le presse-papiers.

 

 




