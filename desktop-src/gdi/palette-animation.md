---
description: L’animation de la palette est une technique qui permet de simuler le mouvement en modifiant rapidement les couleurs des entrées sélectionnées dans une palette de couleurs.
ms.assetid: fc5b8061-fd4f-4751-883d-877fa32cdfcc
title: Animation de la palette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9761e99033e7a01fa875fce7c41e5a35cf40ab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754340"
---
# <a name="palette-animation"></a><span data-ttu-id="6c135-103">Animation de la palette</span><span class="sxs-lookup"><span data-stu-id="6c135-103">Palette Animation</span></span>

<span data-ttu-id="6c135-104">L’animation de la palette est une technique qui permet de simuler le mouvement en modifiant rapidement les couleurs des entrées sélectionnées dans une palette de couleurs.</span><span class="sxs-lookup"><span data-stu-id="6c135-104">Palette animation is a technique to simulate motion by rapidly changing the colors of selected entries in a color palette.</span></span> <span data-ttu-id="6c135-105">Une application peut effectuer une animation de palette en créant une palette logique qui contient des entrées « réservées », puis en utilisant la fonction [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) pour modifier les couleurs dans ces entrées réservées.</span><span class="sxs-lookup"><span data-stu-id="6c135-105">An application can carry out palette animation by creating a logical palette that contains "reserved" entries and then using the [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) function to change colors in those reserved entries.</span></span>

<span data-ttu-id="6c135-106">Une application crée une entrée réservée dans une palette logique en définissant le membre **peFlags** de la structure [**PaletteEntry**](/previous-versions//dd162769(v=vs.85)) sur l' \_ indicateur réservé PC.</span><span class="sxs-lookup"><span data-stu-id="6c135-106">An application creates a reserved entry in a logical palette by setting the **peFlags** member of the [**PALETTEENTRY**](/previous-versions//dd162769(v=vs.85)) structure to the PC\_RESERVED flag.</span></span> <span data-ttu-id="6c135-107">Une fois cette palette logique sélectionnée et réalisée, l’application peut appeler la fonction [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) pour modifier une ou plusieurs entrées réservées.</span><span class="sxs-lookup"><span data-stu-id="6c135-107">Once this logical palette is selected and realized, the application can call the [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) function to change one or more reserved entries.</span></span> <span data-ttu-id="6c135-108">Si la palette donnée est associée à la fenêtre active, le système met immédiatement à jour les couleurs sur l’écran.</span><span class="sxs-lookup"><span data-stu-id="6c135-108">If the given palette is associated with the active window, the system updates the colors on the screen immediately.</span></span>

 

 
