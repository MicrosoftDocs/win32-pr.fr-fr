---
description: Les palettes de demi-teintes sont destinées à être utilisées chaque fois que le mode d’étirement d’un contexte de périphérique est défini sur des demi-TEINTes.
ms.assetid: ee171379-2ab3-4c38-8e86-ff80fa63a357
title: Palette de demi-teintes et réglage des couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3e6708aff92387b792424f07e9b82a1f6125ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528341"
---
# <a name="halftone-palette-and-color-adjustment"></a><span data-ttu-id="84950-103">Palette de demi-teintes et réglage des couleurs</span><span class="sxs-lookup"><span data-stu-id="84950-103">Halftone Palette and Color Adjustment</span></span>

<span data-ttu-id="84950-104">Les palettes de demi-teintes sont destinées à être utilisées chaque fois que le mode d’étirement d’un contexte de périphérique est défini sur des demi-TEINTes.</span><span class="sxs-lookup"><span data-stu-id="84950-104">Halftone palettes are intended to be used whenever the stretching mode of a device context is set to HALFTONE.</span></span> <span data-ttu-id="84950-105">Une application crée une palette de demi-teintes à l’aide de la fonction [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) .</span><span class="sxs-lookup"><span data-stu-id="84950-105">An application creates a halftone palette by using the [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) function.</span></span> <span data-ttu-id="84950-106">L’application doit sélectionner et rendre cette palette dans le contexte de l’appareil avant d’appeler la fonction [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) ou [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) .</span><span class="sxs-lookup"><span data-stu-id="84950-106">The application must select and realize this palette into the device context before calling the [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) or [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) function.</span></span>

<span data-ttu-id="84950-107">Le système ajuste automatiquement la couleur d’entrée des bitmaps sources chaque fois que les applications appellent les fonctions [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) et [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) et que le mode d’étirement d’un contexte de périphérique est défini sur des demi-teintes.</span><span class="sxs-lookup"><span data-stu-id="84950-107">The system automatically adjusts the input color of source bitmaps whenever applications call the [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) and [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) functions and the stretching mode of a device context is set to HALFTONE.</span></span> <span data-ttu-id="84950-108">Ces réglages de couleurs affectent certains attributs de l’image, tels que le contraste et la luminosité.</span><span class="sxs-lookup"><span data-stu-id="84950-108">These color adjustments affect certain attributes of the image, such as contrast and brightness.</span></span> <span data-ttu-id="84950-109">Une application peut définir les valeurs de réglage des couleurs à l’aide de la fonction [**SetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) .</span><span class="sxs-lookup"><span data-stu-id="84950-109">An application can set the color adjustment values by using the [**SetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) function.</span></span> <span data-ttu-id="84950-110">L’application peut récupérer les valeurs de réglage des couleurs pour le contexte de périphérique spécifié à l’aide de la fonction [**GetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) .</span><span class="sxs-lookup"><span data-stu-id="84950-110">The application can retrieve the color adjustment values for the specified device context by using the [**GetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) function.</span></span>

 

 



