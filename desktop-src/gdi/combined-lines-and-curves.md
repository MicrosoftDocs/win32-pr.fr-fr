---
description: En plus de dessiner des lignes ou des courbes, les applications peuvent dessiner des combinaisons de sortie de ligne et de courbe en appelant une fonction unique. Par exemple, une application peut dessiner le contour d’un graphique en secteurs en appelant la fonction AngleArc.
ms.assetid: 0abcc20c-ba89-4eb4-bbd1-7ea27d367fb8
title: Lignes et courbes combinées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ee6aaa3e7a1be580e36c01fb44c81296e894d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972739"
---
# <a name="combined-lines-and-curves"></a>Lignes et courbes combinées

En plus de dessiner des lignes ou des courbes, les applications peuvent dessiner des combinaisons de sortie de ligne et de courbe en appelant une fonction unique. Par exemple, une application peut dessiner le contour d’un graphique en secteurs en appelant la fonction [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) .

La fonction [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) dessine un arc le long du périmètre d’un cercle et dessine une ligne reliant le point de départ de l’arc au centre du cercle. Outre l’utilisation de la fonction **AngleArc** , une application peut également combiner une sortie de courbe et de courbe irrégulière à l’aide de la fonction [**polydraw**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw) .

 

 



