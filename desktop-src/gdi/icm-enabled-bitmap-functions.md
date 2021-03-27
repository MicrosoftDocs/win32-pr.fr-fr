---
description: La gestion des couleurs ICM (Microsoft Image Color Management) garantit qu’une image de couleur, un objet graphique ou un objet texte est rendu aussi fidèlement que possible à son intention d’origine sur n’importe quel appareil, en dépit des différences entre les technologies d’imagerie et les capacités de couleur entre les appareils.
ms.assetid: 7b3cb9a4-ffd2-4867-85bd-0e663fdde6e3
title: ICM-Enabled les fonctions bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b89dac569aafad1ef94b066bc97f588bac62c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863638"
---
# <a name="icm-enabled-bitmap-functions"></a>ICM-Enabled les fonctions bitmap

La gestion des couleurs ICM (Microsoft Image Color Management) garantit qu’une image de couleur, un objet graphique ou un objet texte est rendu aussi fidèlement que possible à son intention d’origine sur n’importe quel appareil, en dépit des différences entre les technologies d’imagerie et les capacités de couleur entre les appareils. Que vous scanniez une image ou un autre graphique sur un scanneur de couleurs, que vous la téléchargeiez sur Internet, que vous la visualisiez ou la modifiiez à l’écran, ou que vous l’imprimiez sur papier, film ou autre média, ICM 2,0 vous aide à maintenir la cohérence et la précision des couleurs. Pour plus d’informations sur ICM, consultez [système de couleurs Windows](/previous-versions//dd372446(v=vs.85)).

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

 

 
