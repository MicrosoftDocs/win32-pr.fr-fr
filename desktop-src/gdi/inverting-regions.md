---
description: Une application inverse les couleurs qui apparaissent dans une région en appelant la fonction InvertRgn.
ms.assetid: bcd9fe61-0f92-41bc-b953-a66e01e43a75
title: Inverser les régions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e3c4b4d01f9ed8f09e819d59bf3268a1ccae4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991200"
---
# <a name="inverting-regions"></a><span data-ttu-id="99199-103">Inverser les régions</span><span class="sxs-lookup"><span data-stu-id="99199-103">Inverting Regions</span></span>

<span data-ttu-id="99199-104">Une application inverse les couleurs qui apparaissent dans une région en appelant la fonction [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) .</span><span class="sxs-lookup"><span data-stu-id="99199-104">An application inverts the colors that appear within a region by calling the [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) function.</span></span> <span data-ttu-id="99199-105">Sur les écrans monochrome, **InvertRgn** fait en sorte que les pixels blancs sont noirs et noirs.</span><span class="sxs-lookup"><span data-stu-id="99199-105">On monochrome displays, **InvertRgn** makes white pixels black and black pixels white.</span></span> <span data-ttu-id="99199-106">Sur les écrans de couleur, cette inversion dépend du type de technologie utilisée pour générer les couleurs de l’écran.</span><span class="sxs-lookup"><span data-stu-id="99199-106">On color screens, this inversion is dependent on the type of technology used to generate the colors for the screen.</span></span>

 

 



