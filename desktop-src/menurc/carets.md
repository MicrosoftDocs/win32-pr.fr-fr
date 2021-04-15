---
title: Signes
description: Cette section traite des signes d’insertion qui sont des lignes clignotantes, des blocs ou des bitmaps dans la zone cliente d’une fenêtre.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\carets.htm
keywords:
- ressources, signes
- signes d’insertion, à propos de
- lignes clignotantes
- blocs clignotants
- bitmaps clignotantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cb99dfc324aa039924fa26683ab0a7674706ea
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104393827"
---
# <a name="carets"></a>Signes

Un *signe insertion* est une ligne, un bloc ou un bitmap clignotant dans la zone cliente d’une fenêtre. Le signe insertion indique généralement l’emplacement où le texte ou les graphiques seront insérés.

L’illustration suivante montre certaines variations courantes de l’apparence du signe insertion.

![Affiche 5 différentes façons d’afficher un signe insertion.](images/cscrt-01.png)

Les applications peuvent créer un signe insertion, modifier la durée de clignotement et afficher, masquer ou déplacer le signe insertion.

### <a name="in-this-section"></a>Dans cette section



| Nom                                   | Description                                                               |
|----------------------------------------|---------------------------------------------------------------------------|
| [À propos des signes](about-carets.md)       | Décrit les signes d’insertion.<br/>                                              |
| [Utilisation des signes d’insertion](using-carets.md)       | Exemples de code qui montrent comment effectuer des tâches liées aux signes d’insertion.<br/> |
| [Référence du signe insertion](caret-reference.md) | Contient la référence de l’API.<br/>                                    |



 

### <a name="caret-functions"></a>Fonctions de signe insertion



| Nom                                           | Description                                                                                                                                                                                                                                                   |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret)             | Crée une nouvelle forme pour le signe insertion système et assigne la propriété du signe insertion à la fenêtre spécifiée. La forme du signe insertion peut être une ligne, un bloc ou une image bitmap. <br/>                                                                                         |
| [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret)           | Détruit la forme actuelle du signe insertion, libère le signe insertion de la fenêtre et supprime le signe insertion de l’écran. <br/>                                                                                                                                       |
| [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) | Récupère le temps nécessaire pour inverser les pixels du signe insertion. L’utilisateur peut définir cette valeur. <br/>                                                                                                                                                            |
| [**GetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos)             | Copie la position du signe insertion vers la structure de [**point**](/previous-versions//dd162805(v=vs.85)) spécifiée. <br/>                                                                                                                                                                    |
| [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret)                 | Supprime le signe insertion de l’écran. Le masquage d’un signe insertion ne détruit pas sa forme actuelle ou n’invalide pas le point d’insertion. <br/>                                                                                                                           |
| [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) | Définit la durée de clignotement du signe insertion sur le nombre de millisecondes spécifié. L’heure de clignotement est le temps écoulé, en millisecondes, nécessaire pour inverser les pixels du signe insertion. <br/>                                                                                    |
| [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos)             | Déplace le signe insertion vers les coordonnées spécifiées. Si la fenêtre qui possède le signe insertion a été créée avec le style de classe **cs \_ OWNDC** , les coordonnées spécifiées sont soumises au mode de mappage du contexte de périphérique associé à cette fenêtre. <br/> |
| [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret)                 | Rend le signe insertion visible à l’écran à la position actuelle du signe insertion. Lorsque le signe insertion devient visible, il commence automatiquement à clignoter. <br/>                                                                                                          |



 

 

