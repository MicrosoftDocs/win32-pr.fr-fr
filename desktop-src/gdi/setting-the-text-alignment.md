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
# <a name="setting-the-text-alignment"></a><span data-ttu-id="ec73f-103">Définition de l’alignement du texte</span><span class="sxs-lookup"><span data-stu-id="ec73f-103">Setting the Text Alignment</span></span>

<span data-ttu-id="ec73f-104">Vous pouvez interroger et définir l’alignement du texte pour un contexte de périphérique à l’aide des fonctions [**GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) et [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) .</span><span class="sxs-lookup"><span data-stu-id="ec73f-104">You can query and set the text alignment for a device context by using the [**GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) and [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) functions.</span></span> <span data-ttu-id="ec73f-105">Les paramètres d’alignement du texte déterminent la position du texte par rapport à un emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="ec73f-105">The text-alignment settings determine how text is positioned relative to a specified location.</span></span> <span data-ttu-id="ec73f-106">Le texte peut être aligné à droite ou à gauche de la position ou centré dessus ; elle peut également être alignée au-dessus ou en dessous du point.</span><span class="sxs-lookup"><span data-stu-id="ec73f-106">Text can be aligned to the right or left of the position or centered over it; it can also be aligned above or below the point.</span></span>

<span data-ttu-id="ec73f-107">L’exemple suivant illustre une méthode permettant de déterminer l’indicateur d’alignement horizontal défini :</span><span class="sxs-lookup"><span data-stu-id="ec73f-107">The following example shows a method for determining which horizontal alignment flag is set:</span></span>


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



<span data-ttu-id="ec73f-108">Vous pouvez également utiliser la fonction [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) pour mettre à jour la position actuelle lorsqu’une fonction de sortie de texte est appelée.</span><span class="sxs-lookup"><span data-stu-id="ec73f-108">You can also use the [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) function to update the current position when a text-output function is called.</span></span> <span data-ttu-id="ec73f-109">Par exemple, l’exemple suivant utilise la fonction [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) pour mettre à jour la position actuelle lorsque la fonction [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) est appelée.</span><span class="sxs-lookup"><span data-stu-id="ec73f-109">For instance, the following example uses the [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) function to update the current position when the [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) function is called.</span></span> <span data-ttu-id="ec73f-110">Dans cet exemple, le paramètre *carial* est un entier qui spécifie le nombre de polices Arial.</span><span class="sxs-lookup"><span data-stu-id="ec73f-110">In this example, the *cArial* parameter is an integer that specifies the number of Arial fonts.</span></span>


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
> <span data-ttu-id="ec73f-111">Vous ne devez pas utiliser [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) avec ta \_ UPDATECP lorsque vous utilisez [**ScriptStringOut**](/windows/win32/api/usp10/nf-usp10-scriptstringout), car le texte sélectionné ne s’affiche pas correctement.</span><span class="sxs-lookup"><span data-stu-id="ec73f-111">You should not use [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) with TA\_UPDATECP when you are using [**ScriptStringOut**](/windows/win32/api/usp10/nf-usp10-scriptstringout), because selected text is not rendered correctly.</span></span> <span data-ttu-id="ec73f-112">Si vous devez utiliser cet indicateur, vous pouvez l’annuler et le réinitialiser si nécessaire pour éviter le problème.</span><span class="sxs-lookup"><span data-stu-id="ec73f-112">If you must use this flag, you can unset and reset it as necessary to avoid the problem.</span></span>

 

 

 
