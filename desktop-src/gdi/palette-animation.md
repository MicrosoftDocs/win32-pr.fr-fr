---
description: L’animation de la palette est une technique qui permet de simuler le mouvement en modifiant rapidement les couleurs des entrées sélectionnées dans une palette de couleurs.
ms.assetid: fc5b8061-fd4f-4751-883d-877fa32cdfcc
title: Animation de la palette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ea2d557ddd071a8f8e993f3a797fb42c2f4fef9abc68fc13737cded96a18fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965589"
---
# <a name="palette-animation"></a>Animation de la palette

L’animation de la palette est une technique qui permet de simuler le mouvement en modifiant rapidement les couleurs des entrées sélectionnées dans une palette de couleurs. Une application peut effectuer une animation de palette en créant une palette logique qui contient des entrées « réservées », puis en utilisant la fonction [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) pour modifier les couleurs dans ces entrées réservées.

Une application crée une entrée réservée dans une palette logique en définissant le membre **peFlags** de la structure [**PaletteEntry**](/previous-versions//dd162769(v=vs.85)) sur l' \_ indicateur réservé PC. Une fois cette palette logique sélectionnée et réalisée, l’application peut appeler la fonction [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) pour modifier une ou plusieurs entrées réservées. Si la palette donnée est associée à la fenêtre active, le système met immédiatement à jour les couleurs sur l’écran.

 

 
