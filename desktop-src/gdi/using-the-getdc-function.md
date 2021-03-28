---
description: Vous utilisez la fonction GetDC pour effectuer un dessin qui doit se produire instantanément plutôt qu’en cas de traitement d’un \_ message de peinture WM.
ms.assetid: 75525e26-72f5-4a58-a663-0bbdc2034759
title: Utilisation de la fonction GetDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c018228eccbce7b487444341481165e24214b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973059"
---
# <a name="using-the-getdc-function"></a><span data-ttu-id="46407-103">Utilisation de la fonction GetDC</span><span class="sxs-lookup"><span data-stu-id="46407-103">Using the GetDC Function</span></span>

<span data-ttu-id="46407-104">Vous utilisez la fonction [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) pour effectuer un dessin qui doit se produire instantanément plutôt qu’en cas de traitement d’un message de [**\_ peinture WM**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="46407-104">You use the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function to carry out drawing that must occur instantly rather than when a [**WM\_PAINT**](wm-paint.md) message is processing.</span></span> <span data-ttu-id="46407-105">Ce dessin est généralement en réponse à une action de l’utilisateur, par exemple en effectuant une sélection ou un dessin avec la souris.</span><span class="sxs-lookup"><span data-stu-id="46407-105">Such drawing is usually in response to an action by the user, such as making a selection or drawing with the mouse.</span></span> <span data-ttu-id="46407-106">Dans ce cas, l’utilisateur doit recevoir des commentaires instantanés et ne doit pas être contraint d’arrêter la sélection ou le dessin afin que l’application affiche le résultat.</span><span class="sxs-lookup"><span data-stu-id="46407-106">In such cases, the user should receive instant feedback and must not be forced to stop selecting or drawing in order for the application to display the result.</span></span> <span data-ttu-id="46407-107">Les sections suivantes montrent comment utiliser GetDC pour dessiner dans une fenêtre :</span><span class="sxs-lookup"><span data-stu-id="46407-107">The following sections show how to use GetDC to draw in a window:</span></span>

-   [<span data-ttu-id="46407-108">Dessin avec la souris</span><span class="sxs-lookup"><span data-stu-id="46407-108">Drawing with the Mouse</span></span>](drawing-with-the-mouse.md)
-   [<span data-ttu-id="46407-109">Dessin à des intervalles chronométrés</span><span class="sxs-lookup"><span data-stu-id="46407-109">Drawing at Timed Intervals</span></span>](drawing-at-timed-intervals.md)

 

 



