---
title: Comment traiter la notification de DTN_FORMATQUERY
description: Cette rubrique montre comment traiter une notification de format de requête envoyée par le contrôle de sélecteur de date et d’heure (PAO).
ms.assetid: 74E29438-2F50-4ADD-B0C4-DB3450BF08D7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e8de1e1a80d04f9a7f9e9d0cfcda198118e67c2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941502"
---
# <a name="how-to-process-the-dtn_formatquery-notification"></a><span data-ttu-id="a0daa-103">Comment traiter la notification DTN \_ FORMATQUERY</span><span class="sxs-lookup"><span data-stu-id="a0daa-103">How to Process the DTN\_FORMATQUERY Notification</span></span>

<span data-ttu-id="a0daa-104">Cette rubrique montre comment traiter une notification de format de requête envoyée par le contrôle de sélecteur de date et d’heure (PAO).</span><span class="sxs-lookup"><span data-stu-id="a0daa-104">This topic demonstrates how to process a Format Query notification that is sent by the date and time picker (DTP) control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a0daa-105">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="a0daa-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a0daa-106">Technologies</span><span class="sxs-lookup"><span data-stu-id="a0daa-106">Technologies</span></span>

-   [<span data-ttu-id="a0daa-107">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="a0daa-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a0daa-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="a0daa-108">Prerequisites</span></span>

-   <span data-ttu-id="a0daa-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="a0daa-109">C/C++</span></span>
-   <span data-ttu-id="a0daa-110">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="a0daa-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a0daa-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="a0daa-111">Instructions</span></span>


<span data-ttu-id="a0daa-112">Un contrôle de PAO envoie un code de notification [DTN \_ FORMATQUERY](dtn-formatquery.md) pour demander des informations sur la taille maximale possible d’un champ de rappel dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="a0daa-112">A DTP control sends a [DTN\_FORMATQUERY](dtn-formatquery.md) notification code to request information about the maximum possible size of a callback field within the control.</span></span> <span data-ttu-id="a0daa-113">Votre application doit gérer ce message pour s’assurer que tous les champs sont affichés correctement.</span><span class="sxs-lookup"><span data-stu-id="a0daa-113">Your application must handle this message to ensure that all fields are displayed properly.</span></span>

<span data-ttu-id="a0daa-114">L’exemple de code C++ suivant est une fonction définie par l’application qui traite le code de notification [DTN \_ FORMATQUERY](dtn-formatquery.md) en calculant la largeur de la chaîne la plus large possible pour un champ de rappel donné.</span><span class="sxs-lookup"><span data-stu-id="a0daa-114">The following C++ code example is an application-defined function that processes the [DTN\_FORMATQUERY](dtn-formatquery.md) notification code by calculating the width of the widest possible string for a given callback field.</span></span>

<span data-ttu-id="a0daa-115">**Avertissement de sécurité :** L’utilisation incorrecte de **lstrcmp** peut compromettre la sécurité de votre application.</span><span class="sxs-lookup"><span data-stu-id="a0daa-115">**Security Warning:** Using **lstrcmp** incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="a0daa-116">Par exemple, avant d’appeler **lstrcmp** dans l’exemple de code suivant, vous devez vous assurer que les deux chaînes se terminent par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="a0daa-116">For example, before calling **lstrcmp** in the following code example you should make sure the two strings are null-terminated.</span></span> <span data-ttu-id="a0daa-117">Vous devez examiner les [considérations relatives à la sécurité : contrôles Microsoft Windows](sec-comctls.md) avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="a0daa-117">You should review [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>



```C++
//  DoFormatQuery processes DTN_FORMATQUERY messages to ensure that the
//  DTP control displays callback fields properly.
//

void WINAPI DoFormatQuery(
 HWND hwndDP, 
 LPNMDATETIMEFORMATQUERY lpDTFQuery)
{
    HDC hdc;
    HFONT hFont, hOrigFont;

    //  Prepare the device context for GetTextExtentPoint32 call.
    hdc = GetDC(hwndDP);

    hFont = (HFONT) SendMessage(hwndDP, WM_GETFONT, 0L, 0L); 

    if(!hFont)
        hFont = (HFONT)GetStockObject(DEFAULT_GUI_FONT);

    hOrigFont = (HFONT) SelectObject(hdc, hFont);

    // Check to see if this is the callback segment desired. If so,
    // use the longest text segment to determine the maximum 
    // width of the callback field, and then place the information into 
    // the NMDATETIMEFORMATQUERY structure.
    if(!lstrcmp(L"XX",lpDTFQuery->pszFormat))
        GetTextExtentPoint32 (hdc,
                          L"366",  // widest date string
                          3,
                          &lpDTFQuery->szMax);

    // Reset the font in the device context; then release the context.
    SelectObject(hdc,hOrigFont);
    ReleaseDC(hwndDP, hdc);
}
```



## <a name="related-topics"></a><span data-ttu-id="a0daa-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0daa-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0daa-119">Utilisation des contrôles de sélecteur de date et heure</span><span class="sxs-lookup"><span data-stu-id="a0daa-119">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="a0daa-120">Référence de contrôle de sélecteur de date et heure</span><span class="sxs-lookup"><span data-stu-id="a0daa-120">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="a0daa-121">Sélecteur de date et heure</span><span class="sxs-lookup"><span data-stu-id="a0daa-121">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




