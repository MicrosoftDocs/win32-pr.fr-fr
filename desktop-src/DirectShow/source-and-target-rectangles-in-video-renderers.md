---
description: Rectangles source et cible dans les convertisseurs vidéo
ms.assetid: fdddbffb-c44f-4364-9e2e-b721ba39c74f
title: Rectangles source et cible dans les convertisseurs vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556aea6aad22e5ea6df61c74ed0a46d2e3984d67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240695"
---
# <a name="source-and-target-rectangles-in-video-renderers"></a>Rectangles source et cible dans les convertisseurs vidéo

Trois tailles sont disponibles dans les structures de format [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)et [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) des types de média vidéo. Cet article explique ce qu’ils sont et comment ils fonctionnent.

Tout d’abord, il y a une taille dans le membre **bmiHeader** de ces structures. Le membre **bmiHeader** est une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) avec ses propres membres Width et Height, **BmiHeader. diwidth** et **bmiHeader. diheight**.

Deuxièmement, il existe un rectangle dans le membre **rcSource** de ces structures ; Enfin, il existe un rectangle dans le membre **rcTarget** de ces structures.

Supposons que vous disposez de deux filtres, A et B, et que ces filtres soient connectés les uns aux autres (à gauche, en amont, et B à droite, ou en aval) avec un certain type de média vidéo.

Les mémoires tampons qui passent entre les filtres A et B ont la taille (**bmiHeader. bilargeur**, **BmiHeader. bihauteur**). Le filtre A doit prendre une partie de sa vidéo d’entrée déterminée par **rcSource** et étirer cette vidéo pour remplir la partie **rcTarget** de la mémoire tampon. La partie de la vidéo d’entrée à utiliser est basée sur la façon dont **rcSource** compare à la taille (**bilargeur**, **bihauteur**) du type de média qui filtre A et B connectés à l’origine. Si **rcSource** est vide, le filtre a utilise sa vidéo d’entrée entière. Si **rcTarget** est vide, le filtre a remplit l’intégralité de la mémoire tampon de sortie.

Par exemple, supposons que le filtre A reçoit des données vidéo de 160 x 120 pixels. Supposons également que le filtre A est connecté au filtre B avec le type de média suivant.

-   (**bilargeur**, **bihauteur**) : 320, 240
-   **rcSource**: (0, 0, 0, 0)
-   **rcTarget**: (0, 0, 0, 0)

Cela signifie que le filtre A étire la vidéo qu’il reçoit de 2 dans les directions x et y, et remplit une mémoire tampon de sortie 320 x 240.

Autre exemple : Supposons que le filtre A reçoit des données vidéo 160 x 120 et qu’il soit connecté au filtre B avec le type de média suivant.

-   (**bilargeur**, **bihauteur**) : 320, 240
-   **rcSource**: (0, 0, 160, 240)
-   **rcTarget**: (0, 0, 0, 0)

Le membre **rcSource** est relatif à la taille de mémoire tampon connectée 320, 240. Car le **rcSource** spécifié (0, 0, 160, 240) est la moitié gauche de la mémoire tampon, le filtre a prend la moitié gauche de sa vidéo d’entrée, ou la partie (0, 0, 80, 120) et étire la vidéo sur une taille de (320, 240) (de 4 sur l’axe x et de 2 sur la direction y) et remplit la mémoire tampon de sortie 320 x 240.

Supposons à présent que Filter A appelle [**CBaseAllocator :: GetBuffer**](cbaseallocator-getbuffer.md)et que l’exemple de support retourné a un type de média associé, ce qui signifie que le filtre B souhaite filtrer un pour fournir une taille ou un type de vidéo différent de celui qu’il avait précédemment fourni. Supposons que le nouveau type de média est :

-   (**bilargeur**, **bihauteur**) : 640, 480
-   **rcSource**: (0, 0, 160, 120)
-   **rcTarget**: (0, 0, 80, 60)

Cela signifie que l’exemple de support a une mémoire tampon dont la taille est de 640 x 480. Le membre **rcSource** est relatif au type de support de connexion d’origine (320, 240) et non au nouveau type de média (640, 480), de sorte que **rcSource** spécifie que l’angle supérieur gauche (25%) de la vidéo d’entrée doit être utilisé. Cette partie de la vidéo d’entrée est placée en haut à gauche (80, 60) pixels de la mémoire tampon de sortie 640 x 480, comme spécifié par **rcTarget** (0, 0, 80, 60). Étant donné que le filtre A reçoit une vidéo 160 x 120, le coin supérieur gauche de la vidéo d’entrée est un élément (80, 60), dont la taille est identique à celle de la bitmap de sortie et aucun étirement n’est nécessaire.

Le filtre A n’placera aucune donnée dans les autres pixels de la mémoire tampon de sortie et laisse ces bits intacts. Le membre **rcSource** est limité par la **bilargeur** et la **bihauteur** du type de média connecté d’origine entre les filtres A et B, et **rcTarget** est délimité par la nouvelle **largeur** et la **bihauteur** de l’échantillon de support. Dans l’exemple précédent, **rcSource** n’a pas pu aller en dehors des limites de (0, 0, 320, 240) et **rcTarget** n’a pas pu sortir des limites de (0, 0, 640, 480).

 

 



