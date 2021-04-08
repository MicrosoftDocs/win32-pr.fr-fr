---
title: À propos des contrôles de barre de progression
description: Une barre de progression est une fenêtre qu’une application peut utiliser pour indiquer la progression d’une longue opération. Il se compose d’un rectangle animé à mesure qu’une opération progresse.
ms.assetid: 1db7a5c9-71cd-4ebc-86b8-8159f30348fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00c80b1f9e97cec1657fe979a19437f607251b8
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730452"
---
# <a name="about-progress-bar-controls"></a>À propos des contrôles de barre de progression

Une barre de progression est une fenêtre qu’une application peut utiliser pour indiquer la progression d’une longue opération.

Il se compose d’un rectangle animé à mesure qu’une opération progresse.

L’illustration suivante montre une barre de progression qui n’utilise pas les styles visuels.

![capture d’écran d’une barre de progression qui ajoute des rectangles dans une ligne pour indiquer la progression](images/pb-oldstyle.png)

L’illustration suivante montre une barre de progression à l’aide de styles visuels. L’apparence du contrôle varie selon le système d’exploitation et le thème sélectionné. Pour plus d’informations, consultez [styles visuels](themes-overview.md).

![capture d’écran d’une barre de progression qui allonge un rectangle vert animé pour indiquer la progression](images/pb-newstyle.png)

Des informations supplémentaires sont contenues dans les en-têtes suivants.

-   [Utilisation des barres de progression](#using-progress-bars)
    -   [Plage et position actuelle](#range-and-current-position)
    -   [Traitement par défaut des messages de la barre de progression](#default-progress-bar-message-processing)
    -   [Style de texte défilant](#marquee-style)

## <a name="using-progress-bars"></a>Utilisation des barres de progression

Vous pouvez créer une barre de progression à l’aide de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant la classe de fenêtre [**Progress \_ Class**](common-control-window-classes.md) . Cette classe de fenêtre est inscrite lors du chargement de la DLL de contrôles communs. Pour plus d’informations, consultez [à propos des contrôles communs](common-controls-intro.md).

Le contrôle est également disponible dans la boîte à outils Microsoft Visual Studio, où il est appelé contrôle de progression.

### <a name="range-and-current-position"></a>Plage et position actuelle

La *plage* d’une barre de progression représente la durée totale de l’opération, tandis que la *position actuelle* représente la progression de l’application vers la fin de l’opération. La procédure de fenêtre utilise la plage et la position actuelle pour déterminer le pourcentage de la barre de progression à remplir avec la couleur de surbrillance.

Si vous ne définissez pas les valeurs de plage, le système définit la valeur minimale sur 0 et la valeur maximale sur 100. Vous pouvez ajuster la plage à des entiers pratiques à l’aide du message [**PBM \_ SetRange**](pbm-setrange.md) .

Une barre de progression fournit plusieurs messages que vous pouvez utiliser pour définir la position actuelle. Le message [**PBM \_ SetPos**](pbm-setpos.md) définit la position sur une valeur donnée. Le message [**PBM \_ DELTAPOS**](pbm-deltapos.md) avance la position en ajoutant une valeur spécifiée à la position actuelle.

Le message [**PBM \_ SETSTEP**](pbm-setstep.md) vous permet de spécifier un incrément d’étape pour une barre de progression. Par la suite, chaque fois que vous envoyez le message [**PBM \_ STEPIT**](pbm-stepit.md) à la barre de progression, la position actuelle avance de l’incrément spécifié. Par défaut, l’incrément de l’étape est défini sur 10.

### <a name="default-progress-bar-message-processing"></a>Traitement par défaut des messages de la barre de progression

Cette section décrit les messages traités par la procédure de fenêtre pour la classe de la [**\_ classe Progress**](common-control-window-classes.md) .



| Message            | Traitement effectué                                                                                                                                                               |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **création de WM \_**     | Alloue et Initialise une structure initiale.                                                                                                                                    |
| **\_destructeur WM**    | Libère toutes les ressources associées à la barre de progression.                                                                                                                              |
| **\_ERASEBKGND WM** | Dessine l’arrière-plan et les bordures de la barre de progression.                                                                                                                              |
| **WM \_ GETFONT**    | Retourne le handle de la police actuelle. La barre de progression ne dessine pas de texte. par conséquent, l’envoi de ce message n’a aucun effet sur le contrôle.                                       |
| **\_peinture WM**      | Dessine la barre de progression. Si le paramètre *wParam* est non **null**, le contrôle suppose que la valeur est un HDC et peint à l’aide de ce contexte de périphérique.                              |
| **\_SetFont WM**    | Enregistre le handle dans la nouvelle police et retourne le handle de la police précédente. La barre de progression ne dessine pas de texte. par conséquent, l’envoi de ce message n’a aucun effet sur le contrôle. |



 

### <a name="marquee-style"></a>Style de texte défilant

En créant le contrôle de barre de progression avec le style [**PBS \_ Marquee**](progress-bar-control-styles.md) , vous pouvez l’animer de façon à afficher l’activité, mais n’indique pas quelle proportion de la tâche est terminée. La partie mise en surbrillance de la barre de progression se déplace de façon répétée le long de la longueur de la barre. Vous pouvez démarrer et arrêter l’animation et contrôler sa vitesse, en envoyant le message [**PBM \_ SETMARQUEE**](pbm-setmarquee.md) . Les barres de progression de texte défilant n’ont pas de plage ou de position.

L’illustration suivante montre une barre de progression en mode palissade. La partie en surbrillance se déplace dans la barre.

![capture d’écran d’une barre de progression qui déplace une surbrillance verte dans un rectangle gris pour indiquer la progression](images/pb-marquee.png)

 

 