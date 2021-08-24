---
description: la gestion des couleurs de l’image Microsoft (ICM) garantit qu’une Image de couleur, un objet graphique ou un objet texte est rendu aussi fidèlement que possible à son intention d’origine sur n’importe quel appareil, en dépit des différences entre les technologies d’imagerie et les fonctionnalités de couleur entre les appareils.
ms.assetid: 7b3cb9a4-ffd2-4867-85bd-0e663fdde6e3
title: ICM-Enabled les fonctions bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38341851eb9ba2aed25cc93afbf7b869909430a30ecb626bf3a452883fdea97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831969"
---
# <a name="icm-enabled-bitmap-functions"></a>ICM-Enabled les fonctions bitmap

la gestion des couleurs de l’image Microsoft (ICM) garantit qu’une Image de couleur, un objet graphique ou un objet texte est rendu aussi fidèlement que possible à son intention d’origine sur n’importe quel appareil, en dépit des différences entre les technologies d’imagerie et les fonctionnalités de couleur entre les appareils. que vous scanniez une image ou un autre graphique sur un scanneur de couleurs, que vous la téléchargeiez sur Internet, que vous la visualisiez ou la modifiiez à l’écran, que vous l’imprimiez sur papier, film ou autre média, ICM 2,0 vous aide à maintenir la cohérence et la précision des couleurs. pour plus d’informations sur la ICM, consultez [Windows système de couleurs](/previous-versions//dd372446(v=vs.85)).

Il existe différentes fonctions dans l’interface GDI (Graphics Device Interface) qui utilisent ou opèrent sur les données de couleur. Les fonctions bitmap suivantes sont activées pour une utilisation avec ICM :

-   [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)
-   [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)
-   [**CreateDIBSection**](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)
-   [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)
-   [**SetDIBColorTable**](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)
-   [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)
-   [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)
-   [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)
-   [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)

 

 
