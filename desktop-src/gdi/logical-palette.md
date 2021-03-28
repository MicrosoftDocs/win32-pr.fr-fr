---
description: Une palette logique est une palette de couleurs qu’une application crée et associe à un contexte de périphérique donné.
ms.assetid: 7cc86771-237d-4539-8f48-2474edb764a4
title: Palette logique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 597e049c4320ff3ac30099e767c35a3438237904
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972655"
---
# <a name="logical-palette"></a>Palette logique

Une *palette logique* est une palette de couleurs qu’une application crée et associe à un contexte de périphérique donné. Les palettes logiques permettent aux applications de définir et d’utiliser des couleurs qui répondent à leurs besoins spécifiques. Les applications peuvent créer un nombre quelconque de palettes logiques, en les utilisant pour des contextes d’appareil distincts ou en basculant entre elles pour un contexte de périphérique unique. Le nombre maximal de palettes qu’une application peut créer dépend des ressources du système.

Une application crée une palette logique à l’aide de la fonction [**CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette) . L’application remplit une structure [**LOGPALETTE**](/windows/win32/api/wingdi/ns-wingdi-logpalette) , qui spécifie le nombre d’entrées et les valeurs de couleur pour chaque entrée, puis l’application transmet la structure à **CreatePalette**. La fonction retourne un handle de palette que l’application utilise dans toutes les opérations suivantes pour identifier la palette. Pour utiliser des couleurs dans la palette logique, l’application sélectionne la palette dans un contexte de périphérique à l’aide de la fonction [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) , puis réalise la palette à l’aide de la fonction [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) . Les couleurs de la palette sont disponibles dès que la palette logique est obtenue.

Une application doit limiter la taille de ses palettes logiques à juste assez d’entrées pour représenter les couleurs nécessaires. Les applications ne peuvent pas créer de palettes logiques supérieures à la taille maximale de la palette, une valeur dépendante de l’appareil. Les applications peuvent obtenir la taille maximale à l’aide de la fonction [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) pour récupérer la valeur SIZEPALETTE.

Bien qu’une application puisse spécifier n’importe quelle valeur de couleur pour une entrée donnée dans une palette logique, toutes les couleurs ne peuvent pas être générées par l’appareil donné. Le système n’offre aucun moyen de détecter les couleurs prises en charge, mais l’application peut découvrir le nombre total de ces couleurs en récupérant la résolution de couleur de l’appareil. La résolution de couleur, spécifiée en bits de couleur par pixel, est égale à la valeur COLORRES retournée par la fonction [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) . Un appareil dont la résolution de couleurs est 18 présente 262 144 couleurs possibles. Si une application demande une couleur qui n’est pas prise en charge, le système choisit une approximation appropriée.

Une fois qu’une palette logique est créée, une application peut modifier les couleurs de la palette à l’aide de la fonction [**SetPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-setpaletteentries) . Si la palette logique a été sélectionnée et réalisée, la modification de la palette n’affecte pas immédiatement les couleurs affichées. L’application doit utiliser les fonctions [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) et [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) pour mettre à jour les couleurs. Dans certains cas, l’application doit peut-être désélectionner, inréaliser, sélectionner et réaliser la palette logique pour s’assurer que les couleurs sont mises à jour exactement comme demandé. Si une application sélectionne une palette logique dans plusieurs contextes de périphérique, les modifications apportées à la palette logique affectent tous les contextes de périphérique pour lesquels elle est sélectionnée.

Une application peut modifier le nombre d’entrées dans une palette logique à l’aide de la fonction [**ResizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-resizepalette) . Si l’application réduit la taille, les entrées restantes sont inchangées. Si l’application augmente la taille, le système définit la couleur de chaque nouvelle entrée sur noir (0, 0, 0) et l’indicateur sur zéro.

Une application peut récupérer les valeurs de couleur et d’indicateur pour les entrées d’une palette logique donnée à l’aide de la fonction [**GetPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getpaletteentries) . Une application peut récupérer l’index de l’entrée dans une palette logique donnée qui correspond le mieux à une valeur de couleur spécifiée à l’aide de la fonction [**GetNearestPaletteIndex**](/windows/desktop/api/Wingdi/nf-wingdi-getnearestpaletteindex) .

Quand une application n’a plus besoin d’une palette logique, elle peut la supprimer à l’aide de la fonction [**SupprimerObjet**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) . L’application doit s’assurer que la palette logique n’est plus sélectionnée dans un contexte de périphérique avant de supprimer la palette.

 

 



