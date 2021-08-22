---
description: Les palettes de demi-teintes sont destinées à être utilisées chaque fois que le mode d’étirement d’un contexte de périphérique est défini sur des demi-TEINTes.
ms.assetid: ee171379-2ab3-4c38-8e86-ff80fa63a357
title: Palette de demi-teintes et réglage des couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8be13f780dc5496173ffb4ddb990a96f7dbe462223e41e8a48d4a58329451277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761003"
---
# <a name="halftone-palette-and-color-adjustment"></a>Palette de demi-teintes et réglage des couleurs

Les palettes de demi-teintes sont destinées à être utilisées chaque fois que le mode d’étirement d’un contexte de périphérique est défini sur des demi-TEINTes. Une application crée une palette de demi-teintes à l’aide de la fonction [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) . L’application doit sélectionner et rendre cette palette dans le contexte de l’appareil avant d’appeler la fonction [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) ou [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) .

Le système ajuste automatiquement la couleur d’entrée des bitmaps sources chaque fois que les applications appellent les fonctions [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) et [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) et que le mode d’étirement d’un contexte de périphérique est défini sur des demi-teintes. Ces réglages de couleurs affectent certains attributs de l’image, tels que le contraste et la luminosité. Une application peut définir les valeurs de réglage des couleurs à l’aide de la fonction [**SetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) . L’application peut récupérer les valeurs de réglage des couleurs pour le contexte de périphérique spécifié à l’aide de la fonction [**GetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) .

 

 



