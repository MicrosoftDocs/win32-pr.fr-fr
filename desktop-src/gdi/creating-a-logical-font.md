---
description: Vous pouvez utiliser la boîte de dialogue police commune pour afficher les polices disponibles.
ms.assetid: 317ea311-0592-432a-87b5-58296de003aa
title: Création d’une police logique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4398f426ae2dd0f18c21409422dfbcb53f0e6ee8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972726"
---
# <a name="creating-a-logical-font"></a><span data-ttu-id="52f5b-103">Création d’une police logique</span><span class="sxs-lookup"><span data-stu-id="52f5b-103">Creating a Logical Font</span></span>

<span data-ttu-id="52f5b-104">Vous pouvez utiliser la boîte de dialogue **police** commune pour afficher les polices disponibles.</span><span class="sxs-lookup"><span data-stu-id="52f5b-104">You can use the **Font** common dialog box to display available fonts.</span></span> <span data-ttu-id="52f5b-105">La boîte de dialogue **ChooseFont** s’affiche après qu’une application a initialisé les membres d’une structure [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) et appelle la fonction [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) .</span><span class="sxs-lookup"><span data-stu-id="52f5b-105">The **ChooseFont** dialog box is displayed after an application initializes the members of a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure and calls the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function.</span></span> <span data-ttu-id="52f5b-106">Une fois que l’utilisateur a sélectionné l’une des polices disponibles et appuie sur le bouton **OK** , la fonction **ChooseFont** Initialise une structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) avec les données pertinentes.</span><span class="sxs-lookup"><span data-stu-id="52f5b-106">After the user selects one of the available fonts and presses the **OK** button, the **ChooseFont** function initializes a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure with the relevant data.</span></span> <span data-ttu-id="52f5b-107">Votre application peut ensuite appeler la fonction [**CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta) et créer une police logique en fonction de la demande de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="52f5b-107">Your application can then call the [**CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta) function and create a logical font based on the user's request.</span></span> <span data-ttu-id="52f5b-108">L’exemple suivant montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="52f5b-108">The following example demonstrates how this is done.</span></span>


```C++
HFONT FAR PASCAL MyCreateFont( void ) 
{ 
    CHOOSEFONT cf; 
    LOGFONT lf; 
    HFONT hfont; 
 
    // Initialize members of the CHOOSEFONT structure.  
 
    cf.lStructSize = sizeof(CHOOSEFONT); 
    cf.hwndOwner = (HWND)NULL; 
    cf.hDC = (HDC)NULL; 
    cf.lpLogFont = &lf; 
    cf.iPointSize = 0; 
    cf.Flags = CF_SCREENFONTS; 
    cf.rgbColors = RGB(0,0,0); 
    cf.lCustData = 0L; 
    cf.lpfnHook = (LPCFHOOKPROC)NULL; 
    cf.lpTemplateName = (LPSTR)NULL; 
    cf.hInstance = (HINSTANCE) NULL; 
    cf.lpszStyle = (LPSTR)NULL; 
    cf.nFontType = SCREEN_FONTTYPE; 
    cf.nSizeMin = 0; 
    cf.nSizeMax = 0; 
 
    // Display the CHOOSEFONT common-dialog box.  
 
    ChooseFont(&cf); 
 
    // Create a logical font based on the user's  
    // selection and return a handle identifying  
    // that font.  
 
    hfont = CreateFontIndirect(cf.lpLogFont); 
    return (hfont); 
} 
```



 

 
