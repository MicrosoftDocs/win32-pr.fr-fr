---
title: Formats de pixel
description: Formats de pixel
ms.assetid: 2e179340-c487-4b72-a22e-078b800af11d
keywords:
- OpenGL sur Windows, pixels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbcd49b17c298d00d0ab41391172c8ae4c3bce8cb295db619d1c9787a2bca36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486189"
---
# <a name="pixel-formats"></a>Formats de pixel

Un *format de pixel* spécifie plusieurs propriétés d’une surface de dessin OpenGL. Voici quelques-unes des propriétés spécifiées par un format de pixel :

-   Indique si la mémoire tampon de pixels est une mémoire tampon simple ou double.
-   Indique si les données de pixels sont dans le format RVBA ou index des couleurs.
-   Nombre de bits utilisés pour stocker des données de couleur.
-   Nombre de bits utilisés pour la mémoire tampon de profondeur (axe z).
-   Nombre de bits utilisés pour la mémoire tampon du stencil.
-   Nombre de plans de superposition et de Underlay.
-   Différents masques de visibilité.

l’implémentation par Microsoft d’OpenGL pour Windows utilise la structure de données [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) pour transmettre les données au format de pixel. Les membres de la structure spécifient les propriétés précédentes et plusieurs autres.

Un contexte de périphérique donné peut prendre en charge plusieurs formats de pixel. Windows identifie les formats de pixel qu’un contexte de périphérique prend en charge avec des valeurs d’index de base 1 consécutives (1, 2, 3, 4, etc.). Un contexte de périphérique peut avoir un seul format de pixel actuel, choisi dans le jeu de formats de pixel pris en charge.

Chaque fenêtre a son propre format de pixel actuel dans OpenGL dans Windows. Cela signifie, par exemple, qu’une application peut afficher simultanément des fenêtres de couleurs RVBA et d’index de couleurs, ou des fenêtres OpenGL à une seule et deux mémoires tampons. Cette fonctionnalité de format de pixel par fenêtre est limitée aux fenêtres OpenGL.

En général, vous obtenez un contexte de périphérique, définissez le format de pixel du contexte de périphérique, puis créez un contexte de rendu OpenGL adapté à cet appareil.

> [!Note]  
> Vous définissez le format de pixel avant de créer un contexte de rendu, car le contexte de rendu hérite du format de pixel du contexte de périphérique.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions de format de pixel](pixel-format-functions.md)
</dt> </dl>

 

 




