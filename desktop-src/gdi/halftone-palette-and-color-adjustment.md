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
# <a name="halftone-palette-and-color-adjustment"></a>Palette de demi-teintes et réglage des couleurs

Les palettes de demi-teintes sont destinées à être utilisées chaque fois que le mode d’étirement d’un contexte de périphérique est défini sur des demi-TEINTes. Une application crée une palette de demi-teintes à l’aide de la fonction [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) . L’application doit sélectionner et rendre cette palette dans le contexte de l’appareil avant d’appeler la fonction [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) ou [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) .

Le système ajuste automatiquement la couleur d’entrée des bitmaps sources chaque fois que les applications appellent les fonctions [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) et [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) et que le mode d’étirement d’un contexte de périphérique est défini sur des demi-teintes. Ces réglages de couleurs affectent certains attributs de l’image, tels que le contraste et la luminosité. Une application peut définir les valeurs de réglage des couleurs à l’aide de la fonction [**SetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) . L’application peut récupérer les valeurs de réglage des couleurs pour le contexte de périphérique spécifié à l’aide de la fonction [**GetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) .

 

 



