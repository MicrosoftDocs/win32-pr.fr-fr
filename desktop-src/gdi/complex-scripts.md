---
description: Bien que les fonctions présentées dans le précédent fonctionnent bien pour de nombreuses langues, elles peuvent ne pas répondre aux besoins des scripts complexes.
ms.assetid: a60b50c8-13e8-4c61-989f-187bb67cf929
title: Scripts complexes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c149aa1d9a6f5caf78fec5227f25aa30146fc273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863682"
---
# <a name="complex-scripts"></a>Scripts complexes

Bien que les fonctions présentées dans le précédent fonctionnent bien pour de nombreuses langues, elles peuvent ne pas répondre aux besoins des scripts complexes. Les *scripts complexes* sont des langues dont le formulaire imprimé n’est pas rendu de manière simple. Par exemple, un script complexe peut permettre un rendu bidirectionnel, une mise en forme contextuelle de glyphes ou une combinaison de caractères. En raison de ces exigences spéciales, le contrôle de la sortie de texte doit être très flexible.

Les fonctions qui affichent du texte [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta), [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), [**TabbedTextOut**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext)et [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) ont été étendues pour prendre en charge des scripts complexes. En général, cette prise en charge est transparente pour l’application. Toutefois, les applications doivent enregistrer des caractères dans une mémoire tampon et afficher une ligne entière de texte à la fois, afin que les modules de mise en forme de script complexes puissent utiliser le contexte pour réorganiser et générer correctement les glyphes. En outre, étant donné que la largeur d’un glyphe peut varier en fonction du contexte, les applications doivent utiliser [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) pour déterminer la longueur de ligne au lieu d’utiliser des largeurs de caractères mises en cache.

En outre, les applications complexes prenant en charge les scripts doivent envisager l’ajout de la prise en charge de l’ordre de lecture de droite à gauche à leurs applications. Vous pouvez basculer l’ordre de lecture ou l’alignement entre gauche et droite avec le code suivant :


```C++
// Save lAlign (this example uses static variables) 
static LONG lAlign = TA_LEFT;

// When user toggles alignment (assuming TA_CENTER is not supported). 

lAlign = TA_RIGHT;

// When the user toggles reading order. 

lAlign = TA_RTLREADING;

// Before calling ExtTextOut, for example, when processing WM_PAINT  

SetTextAlign (hDc, lAlign);
```



Pour basculer les deux attributs en même temps, exécutez l’instruction suivante, puis appelez [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) et [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), comme indiqué précédemment :


```C++
lAlign = TA_RIGHT^TA_RTLREADING;  //pre-inline !
```



Vous pouvez également traiter des scripts complexes avec Uniscribe. Uniscribe est un ensemble de fonctions qui permettent un degré de contrôle précis des scripts complexes. Pour plus d’informations, consultez [Uniscribe](../intl/uniscribe.md) et [traitement de scripts complexes](../intl/processing-complex-scripts.md).

 

 
