---
description: En plus de dessiner des lignes ou des courbes, les applications peuvent dessiner des combinaisons de sortie de ligne et de courbe en appelant une fonction unique. Par exemple, une application peut dessiner le contour d’un graphique en secteurs en appelant la fonction AngleArc.
ms.assetid: 0abcc20c-ba89-4eb4-bbd1-7ea27d367fb8
title: Lignes et courbes combinées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1939b863bfacf2176f15c950b48c8b7c91cc43e7b6b4d4c58ac08e1760c4cee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105718"
---
# <a name="combined-lines-and-curves"></a>Lignes et courbes combinées

En plus de dessiner des lignes ou des courbes, les applications peuvent dessiner des combinaisons de sortie de ligne et de courbe en appelant une fonction unique. Par exemple, une application peut dessiner le contour d’un graphique en secteurs en appelant la fonction [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) .

La fonction [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) dessine un arc le long du périmètre d’un cercle et dessine une ligne reliant le point de départ de l’arc au centre du cercle. Outre l’utilisation de la fonction **AngleArc** , une application peut également combiner une sortie de courbe et de courbe irrégulière à l’aide de la fonction [**polydraw**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw) .

 

 



