---
title: Considérations sur les performances et meilleures pratiques
description: Cette rubrique présente un ensemble de meilleures pratiques pour l’utilisation des API Gestionnaire de fenêtrage (DWM).
ms.assetid: 5b1f6ff8-1d3f-4a70-8efd-90f8802e8532
keywords:
- Gestionnaire de fenêtrage (DWM), meilleures pratiques
- DWM (Gestionnaire de fenêtrage), meilleures pratiques
- Gestionnaire de fenêtrage (DWM), applications pratiques
- DWM (Gestionnaire de fenêtrage), applications pratiques
- Gestionnaire de fenêtrage (DWM), pratiques de dessin
- DWM (Gestionnaire de fenêtrage), pratiques de dessin
- Gestionnaire de fenêtrage (DWM), flou derrière l’effet
- DWM (Gestionnaire de fenêtrage), flou derrière l’effet
- applications pratiques
- pratiques de dessin
- flou derrière l’effet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec76a4920a91f9502940e866d58641a2550d9354
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510898"
---
# <a name="performance-considerations-and-best-practices"></a>Considérations sur les performances et meilleures pratiques

Cette rubrique présente un ensemble de meilleures pratiques pour l’utilisation des API Gestionnaire de fenêtrage (DWM).

Cette rubrique contient les sections suivantes :

-   [Applications pratiques pour DWM](#application-practices-for-dwm)
-   [Pratiques de dessin pour DWM](#drawing-practices-for-dwm)
-   [DWM Blur-Behind région cliente](#dwm-blur-behind-client-region)

## <a name="application-practices-for-dwm"></a>Applications pratiques pour DWM

Si votre application gère la mise à l’échelle en points par pouce (dpi), vous pouvez déclarer une application avec prise en charge DPI et empêcher la mise à l’échelle automatique en définissant l’indicateur de prise en charge DPI dans le manifeste du programme ou en appelant la fonction [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) lors de l’initialisation du programme.

Avec la composition DWM activée, les applications masquées ne reçoivent plus de messages de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) et ne sont pas invitées à effectuer un nouveau rendu. Le contenu de chaque fenêtre est déjà disponible pour composer l’image de l’écran.

Les fenêtres de niveau supérieur des fenêtres [**WS \_ ex \_ transparent**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) doivent être combinées avec un style de **couche WS par \_ \_ couche** à des fins de test de positionnement. **WS \_ Par \_ exemple** , le sens classique, sans redirection, est utile pour les fenêtres enfants dans une hiérarchie de fenêtres qui appartiennent au même thread, mais n’est pas destiné aux fenêtres de niveau supérieur.

Utilisez des régions ou des couches pour créer des fenêtres mises en forme ou mélangées. Notez que dans Windows Vista et les versions ultérieures de Windows, le fait de dessiner uniquement une partie d’une fenêtre de niveau supérieur ne fournit pas le contenu obsolète souhaité dans les régions non dessinées.

Des API telles que [**GetDCOrgEx**](/windows/desktop/api/wingdi/nf-wingdi-getdcorgex) peuvent être utilisées pour déterminer certaines valeurs réelles. Si vous avez un contexte de périphérique (DC) pour une fenêtre redirigée, l’origine retournée par **GetDCOrgEx** ne correspondra pas à l’origine de votre fenêtre à l’écran. L’origine sera à la place l’origine de la surface de la mémoire tampon d’arrière-plan pour votre fenêtre : (0,0).

Si tout le reste échoue, désactivez le rendu de fenêtre en appelant la fonction [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) .

## <a name="drawing-practices-for-dwm"></a>Pratiques de dessin pour DWM

Évitez de dessiner directement sur la surface d’affichage principale. Cela forcera le DWM à désactiver la composition jusqu’à ce que votre application libère la surface de l’appareil principal.

Déterminez si votre application doit fournir sa propre double mise en mémoire tampon. Le DWM double effectivement la mémoire tampon du contenu et affiche la fenêtre dans un seul Frame.

Évitez de lire ou d’écrire sur un contrôleur de périphérique d’affichage. Bien qu’il soit pris en charge par DWM, nous ne le recommandons pas en raison de la baisse des performances.

Évitez de dessiner dans la zone non cliente. Bien que cette zone soit accessible par l’application et que le dessin soit pris en charge par l’API Microsoft Win32, cela peut entraîner la perte de la bordure de la fenêtre.

Évitez de mélanger Windows Graphics Device Interface (GDI) et Microsoft DirectX, sauf s’ils ne se chevauchent pas. Si la combinaison est nécessaire, dessinez le contenu GDI dans une surface DirectX et associez-le avant de le composer, ou bien dessinez-le dans des fenêtres distinctes.

Utilisez la fonction [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) ou [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) au lieu de Windows GDI+ pour présenter votre dessin en vue d’un rendu. GDI+ affiche une ligne d’analyse à la fois avec le rendu logiciel. Cela peut entraîner un scintillement dans vos applications.

## <a name="dwm-blur-behind-client-region"></a>DWM Blur-Behind région cliente

Le rendu de l’effet Flou-behind est une opération gourmande en ressources pour le processeur et l’unité de traitement graphique (GPU). Les développeurs d’applications sont invités à prendre en compte les implications de l’utilisation de l’atténuation de la zone cliente afin qu’elle ne consomme pas de ressources excessives. Vous devez être particulièrement vigilant dans les cas suivants :

-   Lorsque vous vous attendez à ce que la taille du flou de la zone client soit significative, même si aucune mise à jour ne se produit dans la zone floue elle-même. Le flou doit être rendu au cas où des mises à jour se produiront sous la zone floue de la fenêtre, ce qui entraîne des coûts d’UC et de GPU. En outre, les opérations de fenêtre sur la fenêtre (déplacement/redimensionnement/transitions) entraînent davantage de coûts.
-   Quand vous vous attendez à des mises à jour importantes dans la zone cliente floue. Cela nécessitera un redessin du flou sur chaque mise à jour et consommera des ressources excessives.
-   Si le flou est supposé couvrir une zone importante et que les mises à jour de cette zone sont également prévues, nous vous recommandons vivement de ne pas brouiller la zone cliente.

 

 