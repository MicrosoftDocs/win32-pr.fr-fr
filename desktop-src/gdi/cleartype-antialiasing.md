---
description: L’anticrénelage Microsoft ClearType est une méthode de lissage qui améliore la résolution d’affichage des polices par rapport à l’anticrénelage traditionnel.
ms.assetid: b9896934-1e4f-4ae1-922a-ef30e0edf94f
title: Anticrénelage ClearType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcc8444c1e1b594559f9c5b7f96529a0db00b20c6a10e560bc1dcb4574e079d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117888094"
---
# <a name="cleartype-antialiasing"></a>Anticrénelage ClearType

L’anticrénelage Microsoft ClearType est une méthode de lissage qui améliore la résolution d’affichage des polices par rapport à l’anticrénelage traditionnel. Cela améliore considérablement la lisibilité sur les moniteurs LCD couleur avec une interface numérique, tels que ceux des ordinateurs portables et des écrans plats de haute qualité. La lisibilité sur les écrans CRT est également un peu améliorée.

Toutefois, ClearType dépend de l’orientation et de l’ordre des bandes LCD. À l’heure actuelle, ClearType est implémenté uniquement pour les écrans LCD avec des bandes verticales classées RVB. En particulier, cela affecte les Tablet PC, où l’affichage peut être orienté dans n’importe quelle direction et les écrans qui peuvent être remplacés par le mode portrait.

L’anticrénelage ClearType est autorisé :

-   Pour les couleurs 16, 24 et 32 bits (désactivées pour 256 couleurs ou moins)
-   Pour le contrôleur de l’écran et la mémoire DC (pas pour l’imprimante DC)
-   Pour les polices TrueType et OpenType avec des contours TrueType

L’anticrénelage ClearType est désactivé :

-   Sous client Terminal Server
-   Pour les polices bitmap, les polices vectorielles, les polices de périphérique, les polices de type 1 ou les polices PostScript OpenType sans les contours TrueType
-   Si la police a réglé des bitmaps incorporées, uniquement pour les tailles de police qui contiennent les bitmaps incorporées

Pour activer l’anticrénelage ClearType, appelez [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) une fois pour activer le lissage des polices, puis une deuxième fois pour définir le type de lissage sur Fe \_ FONTSMOOTHINGCLEARTYPE, comme illustré dans l’exemple de code suivant :


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHING,
                     TRUE,
                     0,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE);
SystemParametersInfo(SPI_SETFONTSMOOTHINGTYPE,
                     0,
                     (PVOID)FE_FONTSMOOTHINGCLEARTYPE,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



Vous pouvez ajuster l’apparence du texte en modifiant la valeur de contraste utilisée dans l’algorithme ClearType. La valeur par défaut est 1 400, mais il peut s’agir de n’importe quelle valeur comprise entre 1 000 et 2 200. En fonction du périphérique d’affichage et de la sensibilité de l’utilisateur aux couleurs, une valeur de contraste supérieure ou inférieure peut améliorer la lisibilité. Pour modifier le contraste, appelez [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) avec SPI \_ SETFONTSMOOTHINGCONTRAST. Le code suivant définit la valeur de contraste sur 1 600.


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHINGCONTRAST,
                     0,
                     (PVOID)1600,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



Vous devez prendre en compte les détails suivants pour la compatibilité des applications :

-   Le rendu du texte avec ClearType est légèrement plus lent qu’avec l’anticrénelage standard.
-   Les applications ne doivent pas utiliser XOR pour afficher le texte sélectionné. Les applications doivent définir la couleur d’arrière-plan et afficher à nouveau le texte sélectionné.
-   Les applications ne doivent pas peindre le même texte sur lui-même en mode transparent. Si cela se produit, les pixels de bord qui sont anticrénelages sont fusionnés avec eux-mêmes et non avec la couleur d’arrière-plan. Cela donne des bords sombres et colorés.
-   Les applications ne doivent pas peindre du texte en peignant les caractères individuellement en mode opaque, car le bord d’un caractère peut être coupé par le caractère suivant. Cela est dû au fait qu’un caractère lissé avec ClearType peut avoir une largeur A ou C négative, où le caractère normal a une largeur positive a ou C. Seule la largeur B du caractère est garantie comme étant identique. De même, les applications doivent faire attention si le texte lissé est en regard de texte non lissé.
-   Si une application restitue le texte, puis manipule la bitmap, le lissage des polices doit être désactivé en définissant le membre **lfQuality** de la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) sur la \_ qualité NONANTIALIASED. Par exemple, un jeu peut ajouter un effet d’ombre bitmap, ou le texte rendu dans une bitmap peut être mis à l’échelle pour produire un Thumbview.
-   Si l’utilisateur s’exécute en mode Portrait (c’est-à-dire que l’entrelacement est horizontal), l’anticrénelage ClearType doit être désactivé.

Le paramètre *fdwQuality* dans [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) et le membre **lfQuality** de [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) acceptent l’indicateur de \_ qualité CLEARTYPE. La pixellisation des polices créées avec cet indicateur utilise le rastériseur ClearType. Cet indicateur n’a aucun effet sur les versions précédentes du système d’exploitation.

 

 
