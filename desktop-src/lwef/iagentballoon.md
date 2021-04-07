---
title: IAgentBalloon
description: IAgentBalloon
ms.assetid: 94a48cd9-bea5-4993-8991-50c6c86a646b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b811956e368abbaf2d2782c68017084f5e17a09f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725572"
---
# <a name="iagentballoon"></a>IAgentBalloon

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

**IAgentBalloon** définit une interface qui permet aux applications d’interroger les propriétés de la bulle de mot Microsoft Agent. Ces fonctions sont également disponibles à partir de [**IAgentBalloonEx**](https://www.bing.com/search?q=**IAgentBalloonEx**).

Les valeurs par défaut initiales des bulles de mots d’un caractère sont définies dans l’éditeur de caractères Microsoft Agent, mais une fois que l’application est en cours d’exécution, l’utilisateur peut remplacer les propriétés [**activées**](enabled-property.md) et de [police](fontname-property.md) . Si un utilisateur modifie les propriétés de la bulle, la modification affecte tous les caractères. Les propriétés de l’objet [**IAgentBalloon**](/windows/desktop/lwef/iagentballoon) s’appliquent également à la sortie de texte via la méthode de [**réflexion**](think-method.md) .

**Méthodes dans l'ordre Vtable**



| Méthodes IAgentBalloon                                       | Description                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [GetEnabled](iagentballoon--getenabled.md)                 | Retourne une valeur indiquant si la bulle de texte est activée.                                          |
| [GetNumLines](iagentballoon--getnumlines.md)               | Retourne le nombre de lignes affichées dans la bulle de mot.                            |
| [GetNumCharsPerLine](iagentballoon--getnumcharsperline.md) | Retourne le nombre moyen de caractères par ligne affichée dans la bulle de texte.      |
| [GetFontName](iagentballoon--getfontname.md)               | Retourne le nom de la police affichée dans la bulle de mot.                           |
| [GetFontSize](iagentballoon--getfontsize.md)               | Retourne la taille de la police affichée dans la bulle de mot.                           |
| [GetFontBold](iagentballoon--getfontbold.md)               | Retourne une valeur indiquant si la police affichée dans la bulle de mot est en gras.                       |
| [GetFontItalic](iagentballoon--getfontitalic.md)           | Retourne une valeur indiquant si la police affichée dans la bulle de mot est en italique.                     |
| [GetFontStrikethru](iagentballoon--getfontstrikethru.md)   | Retourne une valeur indiquant si la police affichée dans la bulle de mot est affichée sous forme de barré. |
| [GetFontUnderline](iagentballoon--getfontunderline.md)     | Retourne une valeur indiquant si la police affichée dans la bulle de texte est soulignée.                 |
| [GetForeColor](iagentballoon--getforecolor.md)             | Retourne la couleur de premier plan affichée dans la bulle de mot.                           |
| [GetBackColor](iagentballoon--getbackcolor.md)             | Retourne la couleur d’arrière-plan affichée dans la bulle de mot.                           |
| [GetBorderColor](iagentballoon--getbordercolor.md)         | Retourne la couleur de bordure affichée dans la bulle de mot.                               |
| [SetVisible](iagentballoon--setvisible.md)                 | Définit la bulle de texte pour qu’elle soit visible.                                                  |
| [GetVisible](iagentballoon--getvisible.md)                 | Retourne le paramètre de visibilité pour le mot-bulle.                                  |
| [SetFontName](iagentballoon--setfontname.md)               | Définit la police utilisée dans la bulle de mot.                                               |
| [SetFontSize](iagentballoon--setfontsize.md)               | Définit la taille de police utilisée dans le mot-bulle.                                          |
| [SetFontCharSet](iagentballoon--setfontcharset.md)         | Définit le jeu de caractères utilisé dans la bulle de mot.                                      |
| [GetFontCharSet](iagentballoon--getfontcharset.md)         | Retourne le jeu de caractères utilisé dans la bulle de mot.                                   |



 

 

 