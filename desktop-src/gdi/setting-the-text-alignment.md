---
description: Vous pouvez interroger et définir l’alignement du texte pour un contexte de périphérique à l’aide des fonctions GetTextAlign et SetTextAlign.
ms.assetid: 7fdfbadb-827a-4b42-9b9a-b9e46389e13c
title: Définition de l’alignement du texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538a8da060f9d854890ea004c855e2317986fd19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973095"
---
# <a name="setting-the-text-alignment"></a>Définition de l’alignement du texte

Vous pouvez interroger et définir l’alignement du texte pour un contexte de périphérique à l’aide des fonctions [**GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) et [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) . Les paramètres d’alignement du texte déterminent la position du texte par rapport à un emplacement spécifié. Le texte peut être aligné à droite ou à gauche de la position ou centré dessus ; elle peut également être alignée au-dessus ou en dessous du point.

L’exemple suivant illustre une méthode permettant de déterminer l’indicateur d’alignement horizontal défini :


```C++
switch ((TA_LEFT | TA_RIGHT | TA_CENTER) & GetTextAlign(hdc)) 
{ 
    case TA_LEFT: 
       . 
       . 
       . 
    case TA_RIGHT: 
       . 
       . 
       . 
    case TA_CENTER: 
       . 
       . 
       . 
} 
```



Vous pouvez également utiliser la fonction [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) pour mettre à jour la position actuelle lorsqu’une fonction de sortie de texte est appelée. Par exemple, l’exemple suivant utilise la fonction [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) pour mettre à jour la position actuelle lorsque la fonction [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) est appelée. Dans cet exemple, le paramètre *carial* est un entier qui spécifie le nombre de polices Arial.


```C++
UINT uAlignPrev; 
char szCount[8];
HRESULT hr;
size_t * pcch; 
 
uAlignPrev = SetTextAlign(hdc, TA_UPDATECP); 
MoveToEx(hdc, 10, 50, (LPPOINT) NULL); 
TextOut(hdc, 0, 0, "Number of Arial fonts: ", 23); 
itoa(cArial, szCount, 10); 

hr = StringCchLength(szCount, 9, pcch);
if (FAILED(hr))
{
// TODO: write error handler 
}
 
TextOut(hdc, 0, 0, (LPSTR) szCount, *pcch); 
SetTextAlign(hdc, uAlignPrev); 
```



> [!Note]  
> Vous ne devez pas utiliser [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) avec ta \_ UPDATECP lorsque vous utilisez [**ScriptStringOut**](/windows/win32/api/usp10/nf-usp10-scriptstringout), car le texte sélectionné ne s’affiche pas correctement. Si vous devez utiliser cet indicateur, vous pouvez l’annuler et le réinitialiser si nécessaire pour éviter le problème.

 

 

 
