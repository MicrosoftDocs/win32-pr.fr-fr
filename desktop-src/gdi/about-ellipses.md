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
# <a name="about-ellipses"></a><span data-ttu-id="9cd94-103">À propos des ellipses</span><span class="sxs-lookup"><span data-stu-id="9cd94-103">About Ellipses</span></span>

<span data-ttu-id="9cd94-104">Une ellipse est une courbe fermée définie par deux points fixes (F1 et F2) de telle sorte que la somme des distances (D1 + D2) à partir de n’importe quel point de la courbe vers les deux points fixes est constante.</span><span class="sxs-lookup"><span data-stu-id="9cd94-104">An ellipse is a closed curve defined by two fixed points (f1 and f2 ) such that the sum of the distances (d1 +d2 ) from any point on the curve to the two fixed points is constant.</span></span> <span data-ttu-id="9cd94-105">L’illustration suivante montre une ellipse dessinée à l’aide de la fonction [**ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse) .</span><span class="sxs-lookup"><span data-stu-id="9cd94-105">The following illustration shows an ellipse drawn by using the [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse) function.</span></span>

![Illustration montrant une ellipse, deux points fixes, deux distances et un rectangle englobant](images/csfsh-01.png)

<span data-ttu-id="9cd94-107">Lors de l’appel de [**ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse), une application fournit les coordonnées des angles supérieur gauche et inférieur droit du rectangle englobant de l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="9cd94-107">When calling [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse), an application supplies the coordinates of the upper-left and lower-right corners of the ellipse's bounding rectangle.</span></span> <span data-ttu-id="9cd94-108">Un *rectangle englobant* est le plus petit rectangle entourant complètement l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="9cd94-108">A *bounding rectangle* is the smallest rectangle completely surrounding the ellipse.</span></span> <span data-ttu-id="9cd94-109">Lorsque le système dessine l’ellipse, elle exclut les côtés droit et inférieur si aucune transformation universelle n’est définie.</span><span class="sxs-lookup"><span data-stu-id="9cd94-109">When the system draws the ellipse, it excludes the right and lower sides if no world transformations are set.</span></span> <span data-ttu-id="9cd94-110">Par conséquent, pour tout rectangle mesurant x unités en largeur par unités y, l’ellipse associée mesure x1 unités en largeur par unités Y1 de haut.</span><span class="sxs-lookup"><span data-stu-id="9cd94-110">Therefore, for any rectangle measuring x units wide by y units high, the associated ellipse measures x1 units wide by y1 units high.</span></span> <span data-ttu-id="9cd94-111">Si l’application définit une transformation universelle en appelant la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) ou [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) , le système comprend les côtés droit et inférieur.</span><span class="sxs-lookup"><span data-stu-id="9cd94-111">If the application sets a world transformation by calling the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) or [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) function, the system includes the right and lower sides.</span></span>

 

 



