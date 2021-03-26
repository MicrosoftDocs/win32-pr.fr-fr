---
description: Le système gère automatiquement le dessin dans un contexte de périphérique (DC) qui couvre plusieurs moniteurs, même lorsque les moniteurs ont des profondeurs de couleurs différentes.
ms.assetid: 2f03f612-293a-4a42-a13b-1e08e49d9e54
title: Peinture sur plusieurs moniteurs d’affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b6a3e3699000399c61e641137a951ed321fd9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754341"
---
# <a name="painting-on-multiple-display-monitors"></a><span data-ttu-id="979f8-103">Peinture sur plusieurs moniteurs d’affichage</span><span class="sxs-lookup"><span data-stu-id="979f8-103">Painting on Multiple Display Monitors</span></span>

<span data-ttu-id="979f8-104">Le système gère automatiquement le dessin dans un contexte de périphérique (DC) qui couvre plusieurs moniteurs, même lorsque les moniteurs ont des profondeurs de couleurs différentes.</span><span class="sxs-lookup"><span data-stu-id="979f8-104">The system automatically handles painting into a device context (DC) that spans more than one monitor, even when the monitors have different color depths.</span></span> <span data-ttu-id="979f8-105">En général, cela produit de bons résultats, mais il peut ne pas être optimal.</span><span class="sxs-lookup"><span data-stu-id="979f8-105">Usually this produces good results, but it may not be optimal.</span></span> <span data-ttu-id="979f8-106">Par exemple, une fenêtre sur deux moniteurs de palettes de couleurs très différentes peut avoir un rendu de couleur médiocre.</span><span class="sxs-lookup"><span data-stu-id="979f8-106">For example, a window on two monitors of vastly different color depths could have poor color rendition.</span></span> <span data-ttu-id="979f8-107">En outre, les analyses avec la même profondeur de couleur peuvent avoir un exemple de formatsfor de couleur différent, les couleurs peuvent être encodées avec différents nombres de bits ou se trouver à des emplacements différents dans la valeur de couleur d’un pixel.</span><span class="sxs-lookup"><span data-stu-id="979f8-107">Also, monitors with the same color depth may have different color formatsfor example, colors could be encoded with different numbers of bits, or be located in different places in a pixel's color value.</span></span>

<span data-ttu-id="979f8-108">Pour obtenir les meilleurs résultats pour chaque moniteur d’un contrôleur de domaine qui s’étend sur plusieurs affichages, appelez [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) pour énumérer les moniteurs qui croisent votre contrôleur de domaine et peignez la zone d’intersection dans chacune d’elles séparément en fonction des attributs d’affichage de cette analyse.</span><span class="sxs-lookup"><span data-stu-id="979f8-108">To get the best results for each of the monitors in a DC that spans more than one display, call [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) to enumerate the monitors that intersect your DC and paint the intersecting area in each of them separately according to the display attributes for that monitor.</span></span> <span data-ttu-id="979f8-109">Consultez l’exemple relatif à la [peinture sur un contrôleur de périphérique qui s’étend sur plusieurs affichages](painting-on-a-dc-that-spans-multiple-displays.md).</span><span class="sxs-lookup"><span data-stu-id="979f8-109">See the example in [Painting on a DC That Spans Multiple Displays](painting-on-a-dc-that-spans-multiple-displays.md).</span></span>

<span data-ttu-id="979f8-110">Si vous effectuez tout le dessin dans votre code **de \_ peinture WM** et si votre code de **\_ peinture WM** gère tous les différents modes vidéo, vous devez être en mesure de placer votre code de **\_ peinture WM** dans le **MonitorEnumProc** de [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) avec quelques modifications uniquement.</span><span class="sxs-lookup"><span data-stu-id="979f8-110">If you do all of your drawing in your **WM\_PAINT** code and if your **WM\_PAINT** code handles all of the various video modes, then you should be able to place your **WM\_PAINT** code in the **MonitorEnumProc** of [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) with only a few modifications.</span></span>

 

 



