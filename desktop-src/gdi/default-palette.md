---
description: La palette par défaut est un tableau de valeurs de couleur identifiant les couleurs qui peuvent être utilisées avec un contexte de périphérique par défaut.
ms.assetid: 7972d5da-2b73-4cd7-a2ee-fca3a571f611
title: Palette par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c100eeb144ab4f6483281b33739578642880a91f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863669"
---
# <a name="default-palette"></a>Palette par défaut

La *palette par défaut* est un tableau de valeurs de couleur identifiant les couleurs qui peuvent être utilisées avec un contexte de périphérique par défaut. le système associe la palette par défaut à un contexte chaque fois qu’une application crée un contexte pour un appareil qui prend en charge les palettes de couleurs. La palette par défaut garantit que les couleurs peuvent être utilisées par une application sans aucune action supplémentaire.

La palette par défaut comporte généralement 20 entrées (couleurs), mais le nombre exact d’entrées peut varier d’un appareil à l’appareil. Ce nombre est égal à la valeur NUMCOLORS retournée par la fonction [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) . Une application peut récupérer les valeurs de couleur des couleurs de la palette par défaut en énumérant les plumes solides, la même technique que celle utilisée pour détecter les couleurs disponibles sur les appareils non-palette. Les couleurs de la palette par défaut dépendent de l’appareil. Les appareils d’affichage, par exemple, utilisent souvent les 16 couleurs standard de l’affichage VGA et 4 autres couleurs définies par Windows. Les périphériques d’impression peuvent utiliser d’autres couleurs par défaut.

Lorsque vous utilisez la palette par défaut, les applications utilisent des valeurs de couleur pour spécifier les couleurs du stylet et du texte. Si la couleur demandée n’est pas dans la palette, le système se rapproche de la couleur à l’aide de la couleur la plus proche dans la palette. Si une application demande une couleur de pinceau unie qui ne figure pas dans la palette, le système simule la couleur en ditherant les couleurs qui se trouvent dans la palette.

Pour éviter les approximations et le tramage, les applications peuvent également spécifier des couleurs de stylet, de pinceau et de texte à l’aide d’index de palette de couleurs plutôt que de valeurs de couleur. Un index de palette de couleurs est une valeur entière qui identifie une entrée spécifique de la palette. Les applications peuvent utiliser des index de palette de couleurs à la place des valeurs de couleur, mais doivent utiliser la macro [**PALETTEINDEX**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex) pour créer les index.

Les index de palette de couleurs sont utiles uniquement pour les appareils qui prennent en charge les palettes de couleurs. Pour éviter cette dépendance d’appareil, les applications qui utilisent le même code pour dessiner à la fois sur les appareils palette et non-palette doivent utiliser des valeurs de couleurs relatives à la palette pour spécifier des couleurs de stylet, de pinceau et de texte. Ces valeurs sont identiques aux valeurs de couleur, sauf lors de la création de pinceaux solides. (Sur les appareils de palette, une couleur de pinceau unie spécifiée par une valeur de couleur relative à la palette est soumise à une approximation de couleur plutôt qu’à un tramage.) Les applications doivent utiliser la macro [**PALETTERGB**](/windows/desktop/api/Wingdi/nf-wingdi-palettergb) pour créer des valeurs de couleurs relatives à la palette.

Le système n’autorise pas une application à modifier les entrées dans la palette par défaut. Pour utiliser des couleurs autres que celles de la palette par défaut, une application doit créer sa propre palette logique et sélectionner la palette dans le contexte de périphérique.

 

 



