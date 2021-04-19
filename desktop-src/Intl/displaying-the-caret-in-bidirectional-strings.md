---
description: Dans le texte unidirectionnel, la position du signe insertion n’a aucune ambiguïté, car le bord de tête d’un caractère se trouve au même endroit que le bord de fin du caractère précédent.
ms.assetid: 3bebb329-3dd7-4b2e-8ff3-878aaf337a2c
title: Affichage du signe insertion dans les chaînes bidirectionnelles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76cce95362aa69564fd245ccad1da4a967dddc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528311"
---
# <a name="displaying-the-caret-in-bidirectional-strings"></a>Affichage du signe insertion dans les chaînes bidirectionnelles

Dans le texte unidirectionnel, la position du signe insertion n’a aucune ambiguïté, car le bord de tête d’un caractère se trouve au même endroit que le bord de fin du caractère précédent. Toutefois, dans le texte bidirectionnel, la position du signe insertion entre les exécutions de la direction opposée est ambiguë. Par exemple, dans le paragraphe de gauche à droite « hellosalaam », la dernière lettre de « Hello » précède immédiatement la première lettre de « Salaam ». La meilleure position pour afficher le signe insertion varie selon qu’il est considéré comme suivi du « o » de « Hello » ou qu’il doit précéder le « s » de « Salaam ».

Uniscribe utilise les conventions de positionnement du signe insertion indiquées dans le tableau suivant.



| Situation       | Positionnement du signe insertion visuel                       |
|-----------------|----------------------------------------------|
| Saisie          | Bord de fin du dernier caractère tapé.       |
| Collage         | Bord de fin du dernier caractère collé.      |
| Avancer le signe insertion | Bord de fin du dernier caractère passé. |
| Retrait du signe insertion  | Bord de tête du dernier caractère passé.  |
| Accueil            | Bord de tête de la ligne.                        |
| End             | Bord de fin de la ligne.                       |



 

Le signe insertion peut être positionné comme indiqué dans l’exemple suivant :


```C++
if (fAdvancing) {
    ScriptCPtoX(
        iCharPos - 1, TRUE, 
        cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
        );
} else {
    ScriptCPtoX(
        iCharPos, FALSE, 
        cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
        );
}
```



Le positionnement du signe insertion peut être plus simple, comme indiqué ci-dessous, en fonction d’une valeur *fAdvancing* limitée à **true** ou **false**:


```C++
ScriptCPtoX(
    iCharPos - fAdvancing, fAdvancing, 
    cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
    );
```



[**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) gère logiquement les positions hors limites. Elle retourne le bord de tête de la série pour *iCharPos* <0, et le bord de fin de la série pour *iCharPos* >= length. Pour plus d’informations, consultez [gestion du placement du signe insertion et test de positionnement](managing-caret-placement-and-hit-testing.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



