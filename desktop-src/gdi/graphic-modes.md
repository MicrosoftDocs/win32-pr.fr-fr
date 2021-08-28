---
description: Windows prend en charge cinq modes graphiques qui permettent à une application de spécifier le mode de mélange des couleurs, le mode de mise à l’échelle de la sortie, et ainsi de suite. Ces modes, qui sont stockés dans un DC, sont décrits dans le tableau suivant.
ms.assetid: 061af47e-fd49-4eb4-9b1b-03eb9c841622
title: Modes graphiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c36461935c8279e38e09afe9f7802e2f758d1cf45380beaa16d1911f4ed965f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558769"
---
# <a name="graphic-modes"></a>Modes graphiques

Windows prend en charge cinq modes graphiques qui permettent à une application de spécifier le mode de mélange des couleurs, le mode de mise à l’échelle de la sortie, et ainsi de suite. Ces modes, qui sont stockés dans un DC, sont décrits dans le tableau suivant.



| Mode graphique | Description                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| Arrière-plan    | Définit comment les couleurs d’arrière-plan sont mélangées avec des couleurs de fenêtre ou d’écran existantes pour les opérations de bitmap et de texte.              |
| Dessin       | Définit comment les couleurs de premier plan sont mélangées avec des couleurs de fenêtre ou d’écran existantes pour les opérations de stylet, de pinceau, de bitmap et de texte. |
| Mappage       | Définit la façon dont la sortie graphique est mappée de l’espace logique (ou universel) sur le papier de la fenêtre, de l’écran ou de l’imprimante.             |
| Polygone-remplissage  | Définit la façon dont le modèle de pinceau est utilisé pour remplir l’intérieur des régions complexes.                                             |
| Étirement    | Définit comment les couleurs de la bitmap sont mélangées avec des couleurs de fenêtre ou d’écran existantes lorsque la bitmap est compressée (ou réduite).  |



 

Comme c’est le cas avec les objets graphiques, le système Initialise un contrôleur de réseau avec les modes graphiques par défaut. Une application peut récupérer et examiner ces modes par défaut en appelant les fonctions suivantes.



| Mode graphique | Fonction                                       |
|---------------|------------------------------------------------|
| Arrière-plan    | [**GetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 |
| Dessin       | [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     |
| Mappage       | [**GetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)               |
| Polygone-remplissage  | [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)     |
| Étirement    | [**GetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode) |



 

Une application peut modifier les modes par défaut en appelant l’une des fonctions suivantes.



| Mode graphique | Fonction                                       |
|---------------|------------------------------------------------|
| Arrière-plan    | [**SetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 |
| Dessin       | [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     |
| Mappage       | [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)               |
| Polygone-remplissage  | [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)     |
| Étirement    | [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) |



 

 

 



