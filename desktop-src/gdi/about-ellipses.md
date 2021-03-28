---
description: Une ellipse est une courbe fermée définie par deux points fixes (F1 et F2) de telle sorte que la somme des distances (D1 + D2) à partir de n’importe quel point de la courbe vers les deux points fixes est constante.
ms.assetid: c4aab4cf-9575-4817-b51f-aed4e3c27d2f
title: À propos des ellipses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c6b2774da9886e25d3e1dcca7c701b034e7b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560008"
---
# <a name="about-ellipses"></a>À propos des ellipses

Une ellipse est une courbe fermée définie par deux points fixes (F1 et F2) de telle sorte que la somme des distances (D1 + D2) à partir de n’importe quel point de la courbe vers les deux points fixes est constante. L’illustration suivante montre une ellipse dessinée à l’aide de la fonction [**ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse) .

![Illustration montrant une ellipse, deux points fixes, deux distances et un rectangle englobant](images/csfsh-01.png)

Lors de l’appel de [**ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse), une application fournit les coordonnées des angles supérieur gauche et inférieur droit du rectangle englobant de l’ellipse. Un *rectangle englobant* est le plus petit rectangle entourant complètement l’ellipse. Lorsque le système dessine l’ellipse, elle exclut les côtés droit et inférieur si aucune transformation universelle n’est définie. Par conséquent, pour tout rectangle mesurant x unités en largeur par unités y, l’ellipse associée mesure x1 unités en largeur par unités Y1 de haut. Si l’application définit une transformation universelle en appelant la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) ou [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) , le système comprend les côtés droit et inférieur.

 

 



