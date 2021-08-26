---
title: S’assurer que le texte est affiché avec le sens de lecture correct
description: Certains langages, tels que l’arabe et l’hébreu, requièrent un sens de lecture de droite à gauche.
ms.assetid: fa9a3dd6-575a-4877-a488-22845c6726c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3774e4d237863a218cadf5206e4dc4921bceaeaa06c00ab81057f80dd8ee6549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982169"
---
# <a name="ensure-text-is-displayed-with-the-correct-reading-direction"></a>S’assurer que le texte est affiché avec le sens de lecture correct

Certains langages, tels que l’arabe et l’hébreu, requièrent un sens de lecture de droite à gauche. pour un objet de format texte [DirectWrite](direct-write-portal.md) , le sens de lecture par défaut est de gauche à droite. DirectWrite ne déduit pas automatiquement le sens de lecture des paramètres régionaux, vous devez donc le faire vous-même.

Tout d’abord, récupérez les indicateurs de style étendus pour la fenêtre dans laquelle le texte sera rendu à l’aide de la macro GetWindowStyleEx définie dans windowsx. h.


```C++
// Get the window extended style flagsfor the current window.
DWORD dwStyle = GetWindowExStyle(hwnd_);
```



La macro retourne une valeur DWORD composée de plusieurs indicateurs associés à des opérations de bits or. Vous devez déterminer si les indicateurs spécifiques qui affectent le sens de lecture sont là.

Il existe 2 indicateurs différents associés à la direction de lecture : WS \_ ex \_ LAYOUTRTL et WS \_ ex \_ RTLREADING.

Utilisez l’opérateur and au niveau du bit (&) avec la variable dwStyle et la \_ macro WS ex \_ LAYOUTRTL pour stocker une valeur bool qui indique si la disposition est mise en miroir.


```C++
// Is the WS_EX_LAYOUTRTL flag present?
BOOL bWSLayout = dwStyle & WS_EX_LAYOUTRTL;
```



Faites la même chose pour l' \_ indicateur WS ex \_ RTLREADING.


```C++
// Is the WS_EX_RLTREADING flag present?
BOOL bWSReading = dwStyle & WS_EX_RTLREADING;
```



Définissez le sens de lecture à l’aide de la méthode [**IDWriteTextFormat :: SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) . La valeur par défaut est de gauche à droite. vous devez donc uniquement définir la direction de lecture si elle est de droite à gauche.

> [!Note]  
> WS \_ ex \_ LAYOUTRTL reflète la totalité de la disposition et implique un sens de lecture de droite à gauche. par conséquent, définissez le sens de lecture uniquement si l’un de ces indicateurs est présent. Si les deux sont présents, ils s’annulent l’un l’autre et le sens de lecture du format texte doit être de gauche à droite.

 


```C++
// If either the WS_EX_LAYOUTRTL flag or the WS_EX_RLTREADING flag is present,
// but NOT BOTH, set the reading direction to right to left.
if ((bWSLayout && !bWSReading)
||  (!bWSLayout && bWSReading))
{
    pTextFormat_->SetReadingDirection(DWRITE_READING_DIRECTION_RIGHT_TO_LEFT);
}
```



 

 
