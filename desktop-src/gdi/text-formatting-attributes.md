---
description: 'Une application peut utiliser six fonctions pour définir les attributs de mise en forme du texte pour un contexte de périphérique : SetBkColor, SetBkMode, SetTextAlign, SetTextCharacterExtra, SetTextColor et SetTextJustification.'
ms.assetid: fd4d81ee-7f8f-41e8-88a5-d3ed89f4c7bd
title: Attributs Text-Formatting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e74cb8d30a0eb9b44f05be611da963b413e8798b81da2a334dc083bd3cc1651
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015279"
---
# <a name="text-formatting-attributes"></a>Attributs Text-Formatting

Une application peut utiliser six fonctions pour définir les attributs de mise en forme du texte pour un contexte de périphérique : [SetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor), [SetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode), [SetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign), [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra), [SetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor)et [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification). Ces fonctions affectent l’alignement du texte, l’espacement entre les caractères, la justification du texte, ainsi que les couleurs de texte et d’arrière-plan. En outre, six autres fonctions peuvent être utilisées pour récupérer les attributs de mise en forme du texte actuel pour tout contexte de périphérique : [GetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor), [GetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode), [GetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign), [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra), [GetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor)et [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a).

## <a name="text-alignment"></a>Alignement du texte

Les applications peuvent utiliser la fonction [SetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) pour spécifier la façon dont le système doit positionner les caractères dans une chaîne de texte lorsqu’ils appellent l’une des fonctions de dessin. Cette fonction peut être utilisée pour positionner des en-têtes, des numéros de page, des légendes, etc. Le système positionne une chaîne de texte en alignant un point de référence sur un rectangle imaginaire qui entoure la chaîne, avec la position actuelle du curseur ou un point passé comme argument à l’une des fonctions de dessin de texte. La fonction [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) permet à l’application de spécifier l’emplacement de ce point de référence. La liste suivante répertorie les emplacements de point de référence possibles.



| Emplacement         | Description                                                                                                             |
|------------------|-------------------------------------------------------------------------------------------------------------------------|
| gauche/bas      | Le point de référence se trouve dans l’angle inférieur gauche du rectangle.                                               |
| ligne gauche/base   | Le point de référence se trouve à l’intersection de la ligne de base de cellule de caractère et du bord gauche du rectangle.  |
| gauche/haut         | Le point de référence se trouve dans l’angle supérieur gauche du rectangle.                                                 |
| Centre/bas    | Le point de référence se trouve au centre du bas du rectangle.                                            |
| Centre/ligne de base | Le point de référence se trouve à l’intersection de la ligne de base de cellule de caractères et du centre du rectangle.     |
| Centre/haut       | Le point de référence se trouve au centre du haut du rectangle.                                               |
| droit/bas     | Le point de référence se trouve dans le coin inférieur droit du rectangle.                                              |
| droite/ligne de base  | Le point de référence se trouve à l’intersection de la ligne de base de cellule de caractère et du bord droit du rectangle. |
| droite/haut        | Le point de référence se trouve dans l’angle supérieur droit du rectangle.                                                |



 

L’illustration suivante montre une chaîne de texte dessinée en appelant la fonction [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) . Avant de dessiner le texte, la fonction [SetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) a été appelée pour déplacer le point de référence à chacun des neuf emplacements possibles.

![Illustration montrant le même texte neuf fois, un pour chaque emplacement de point de référence possible](images/csftx-04.png)

L’alignement du texte par défaut pour un contexte de périphérique est l’angle supérieur gauche du rectangle imaginaire qui entoure le texte. Une application peut récupérer le paramètre d’alignement de texte actuel pour tout contexte de périphérique en appelant la fonction [GetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) .

## <a name="intercharacter-spacing"></a>Espacement entre les caractères

Les applications peuvent utiliser la fonction [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) pour modifier l’espacement entre les caractères pour toutes les opérations de sortie de texte dans un contexte de périphérique spécifié. L’illustration suivante montre une chaîne de texte dessinée deux fois en appelant la fonction [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) . Avant de dessiner le texte la deuxième fois, la fonction [**SetTextCharacterExtra**](/windows/win32/api/wingdi/nf-wingdi-settextcharacterextra) a été appelée pour incrémenter l’espacement entre les caractères.

![l’illustration shoing le même texte à deux reprises : tout d’abord avec un espacement entre les intercaractères normal, puis avec un espacement plus grand](images/csftx-06.png)

La valeur d’espacement entre les caractères par défaut pour tout contexte de périphérique est égale à zéro. Une application peut récupérer la valeur actuelle de l’espacement entre les caractères d’un contexte de périphérique en appelant la fonction [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) .

## <a name="text-justification"></a>Justification du texte

Les applications peuvent utiliser les fonctions [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) et [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) pour justifier une ligne de texte. La justification du texte est une opération courante dans toute publication de bureau et dans la plupart des applications de traitement de texte. La fonction [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) calcule la largeur et la hauteur d’une chaîne de texte. Une fois la largeur calculée, l’application peut appeler la fonction [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) pour répartir l’espacement supplémentaire entre chacun des mots d’une ligne de texte. L’illustration suivante montre un paragraphe de texte imprimé deux fois : dans le premier paragraphe, le texte n’a pas été justifié. dans le deuxième paragraphe, le texte était justifié en appelant les fonctions **GetTextExtentPoint32** et **SetTextJustification** .

![Illustration montrant un paragraphe qui s’aligne uniquement à gauche, puis le même paragraphe aligné à gauche et à droite](images/csftx-05.png)

## <a name="text-and-background-color"></a>Couleur du texte et de l’arrière-plan

Les applications peuvent utiliser la fonction [SetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor) pour définir la couleur du texte dessiné dans la zone cliente de leurs fenêtres, ainsi que la couleur du texte dessiné sur une imprimante couleur. Une application peut utiliser la fonction [SetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor) pour définir la couleur qui apparaît derrière chaque caractère et la fonction [SetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode) pour spécifier la façon dont le système doit fusionner la couleur d’arrière-plan sélectionnée avec la ou les couleurs actuelles de l’affichage vidéo.

La couleur de texte par défaut pour un contexte de périphérique d’affichage est noire ; la couleur d’arrière-plan par défaut est blanc. et le mode d’arrière-plan par défaut est OPAQUE. Une application peut récupérer la couleur de texte actuelle pour un contexte de périphérique en appelant la fonction [GetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor) . Une application peut récupérer la couleur d’arrière-plan actuelle pour un contexte de périphérique en appelant la fonction [GetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor) et le mode d’arrière-plan actuel en appelant la fonction [GetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode) .

 

 
