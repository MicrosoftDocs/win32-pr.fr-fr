---
title: Comment imprimer le contenu de contrôles RichEdit
description: Cette section contient des informations sur l’impression du contenu des contrôles RichEdit.
ms.assetid: d61e2e11-d848-43fc-9622-b3b2032bda48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a304e5c09b5f8ea934c90873c3d915179295964e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106510910"
---
# <a name="how-to-print-the-contents-of-rich-edit-controls"></a><span data-ttu-id="830e5-103">Comment imprimer le contenu de contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="830e5-103">How to Print the Contents of Rich Edit Controls</span></span>

<span data-ttu-id="830e5-104">Cette section contient des informations sur l’impression du contenu des contrôles RichEdit.</span><span class="sxs-lookup"><span data-stu-id="830e5-104">This section contains information about how to print the contents of rich edit controls.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="830e5-105">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="830e5-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="830e5-106">Technologies</span><span class="sxs-lookup"><span data-stu-id="830e5-106">Technologies</span></span>

-   [<span data-ttu-id="830e5-107">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="830e5-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="830e5-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="830e5-108">Prerequisites</span></span>

-   <span data-ttu-id="830e5-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="830e5-109">C/C++</span></span>
-   <span data-ttu-id="830e5-110">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="830e5-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="830e5-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="830e5-111">Instructions</span></span>

### <a name="use-print-preview"></a><span data-ttu-id="830e5-112">Utiliser l’aperçu avant impression</span><span class="sxs-lookup"><span data-stu-id="830e5-112">Use Print Preview</span></span>

<span data-ttu-id="830e5-113">Pour mettre en forme le texte dans un contrôle RichEdit tel qu’il apparaîtra sur un appareil cible (généralement la page imprimée), envoyez le message [**em \_ SETTARGETDEVICE**](em-settargetdevice.md) , en transmettant le handle à un contexte de périphérique (HDC) de l’appareil cible et à la largeur de ligne souhaitée.</span><span class="sxs-lookup"><span data-stu-id="830e5-113">To format text in a rich edit control as it will appear on a target device (usually the printed page), send the [**EM\_SETTARGETDEVICE**](em-settargetdevice.md) message, passing in the handle to a device context (HDC) of the target device and the desired line width.</span></span> <span data-ttu-id="830e5-114">En général, vous obtiendrez la largeur de ligne en appelant [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) pour le HDC cible.</span><span class="sxs-lookup"><span data-stu-id="830e5-114">Usually you will obtain the line width by calling [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) for the target HDC.</span></span>

### <a name="format-print-for-a-specific-device"></a><span data-ttu-id="830e5-115">Mettre en forme l’impression pour un appareil spécifique</span><span class="sxs-lookup"><span data-stu-id="830e5-115">Format Print for a Specific Device</span></span>

<span data-ttu-id="830e5-116">Pour mettre en forme une partie du contenu d’un contrôle RichEdit pour un appareil spécifique, envoyez le message [**em \_ FormatRange**](em-formatrange.md) .</span><span class="sxs-lookup"><span data-stu-id="830e5-116">To format part of a rich edit control's contents for a specific device, send the [**EM\_FORMATRANGE**](em-formatrange.md) message.</span></span> <span data-ttu-id="830e5-117">La structure [**FormatRange**](/windows/desktop/api/Richedit/ns-richedit-formatrange) utilisée avec ce message spécifie la plage de texte à mettre en forme, ainsi que le HDC pour l’appareil cible.</span><span class="sxs-lookup"><span data-stu-id="830e5-117">The [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) structure that is used with this message specifies the range of text to format as well as the HDC for the target device.</span></span> <span data-ttu-id="830e5-118">Le cas échéant, ce message envoie également le texte à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="830e5-118">Optionally, this message also sends the text to the printer.</span></span>

### <a name="use-banding"></a><span data-ttu-id="830e5-119">Utiliser la bande</span><span class="sxs-lookup"><span data-stu-id="830e5-119">Use Banding</span></span>

<span data-ttu-id="830e5-120">La bande est le processus par lequel une seule page de sortie est générée à l’aide d’un ou de plusieurs rectangles séparés, ou de bandes.</span><span class="sxs-lookup"><span data-stu-id="830e5-120">Banding is the process by which a single page of output is generated using one or more separate rectangles, or bands.</span></span> <span data-ttu-id="830e5-121">Lorsque toutes les bandes sont placées sur la page, une image complète les résultats.</span><span class="sxs-lookup"><span data-stu-id="830e5-121">When all bands are placed on the page, a complete image results.</span></span> <span data-ttu-id="830e5-122">Cette approche est souvent utilisée par les imprimantes raster qui ne disposent pas de suffisamment de mémoire ou de capacité à effectuer une image de page entière à la fois.</span><span class="sxs-lookup"><span data-stu-id="830e5-122">This approach is often used by raster printers that do not have sufficient memory or ability to image a full page at one time.</span></span>

<span data-ttu-id="830e5-123">Pour implémenter des bandes, utilisez le message [**em \_ DISPLAYBAND**](em-displayband.md) pour envoyer des parties successives du contenu du contrôle RichEdit à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="830e5-123">To implement banding, use the [**EM\_DISPLAYBAND**](em-displayband.md) message to send successive portions of the rich edit control's content to the device.</span></span> <span data-ttu-id="830e5-124">Ce message s’imprime sur l’appareil qui a été spécifié dans un appel précédent à [**em \_ FormatRange**](em-formatrange.md).</span><span class="sxs-lookup"><span data-stu-id="830e5-124">This message prints to the device that was specified in a previous call to [**EM\_FORMATRANGE**](em-formatrange.md).</span></span> <span data-ttu-id="830e5-125">Bien entendu, le paramètre *wParam* du message **em \_ FormatRange** doit être égal à zéro, de sorte que l’impression n’est pas lancée par ce message.</span><span class="sxs-lookup"><span data-stu-id="830e5-125">Of course, the *wParam* parameter of the **EM\_FORMATRANGE** message should be zero, so that printing is not initiated by that message.</span></span>

## <a name="printrtf-code-example"></a><span data-ttu-id="830e5-126">Exemple de code PrintRTF</span><span class="sxs-lookup"><span data-stu-id="830e5-126">PrintRTF Code Example</span></span>

<span data-ttu-id="830e5-127">L’exemple de code suivant imprime le contenu d’un contrôle RichEdit sur l’imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="830e5-127">The following example code prints the contents of a rich edit control to the specified printer.</span></span>


```C++
// hwnd is the HWND of the rich edit control.
// hdc is the HDC of the printer. This value can be obtained for the 
// default printer as follows:
//
//     PRINTDLG pd = { sizeof(pd) };
//     pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
//
//     if (PrintDlg(&pd))
//     {
//        HDC hdc = pd.hDC;
//        ...
//     }

BOOL PrintRTF(HWND hwnd, HDC hdc)
{
    DOCINFO di = { sizeof(di) };
    
    if (!StartDoc(hdc, &di))
    {
        return FALSE;
    }

    int cxPhysOffset = GetDeviceCaps(hdc, PHYSICALOFFSETX);
    int cyPhysOffset = GetDeviceCaps(hdc, PHYSICALOFFSETY);
    
    int cxPhys = GetDeviceCaps(hdc, PHYSICALWIDTH);
    int cyPhys = GetDeviceCaps(hdc, PHYSICALHEIGHT);

    // Create "print preview". 
    SendMessage(hwnd, EM_SETTARGETDEVICE, (WPARAM)hdc, cxPhys/2);

    FORMATRANGE fr;

    fr.hdc       = hdc;
    fr.hdcTarget = hdc;

    // Set page rect to physical page size in twips.
    fr.rcPage.top    = 0;  
    fr.rcPage.left   = 0;  
    fr.rcPage.right  = MulDiv(cxPhys, 1440, GetDeviceCaps(hDC, LOGPIXELSX));  
    fr.rcPage.bottom = MulDiv(cyPhys, 1440, GetDeviceCaps(hDC, LOGPIXELSY)); 

    // Set the rendering rectangle to the pintable area of the page.
    fr.rc.left   = cxPhysOffset;
    fr.rc.right  = cxPhysOffset + cxPhys;
    fr.rc.top    = cyPhysOffset;
    fr.rc.bottom = cyPhysOffset + cyPhys;

    SendMessage(hwnd, EM_SETSEL, 0, (LPARAM)-1);          // Select the entire contents.
    SendMessage(hwnd, EM_EXGETSEL, 0, (LPARAM)&fr.chrg);  // Get the selection into a CHARRANGE.

    BOOL fSuccess = TRUE;

    // Use GDI to print successive pages.
    while (fr.chrg.cpMin < fr.chrg.cpMax && fSuccess) 
    {
        fSuccess = StartPage(hdc) > 0;
        
        if (!fSuccess) break;
        
        int cpMin = SendMessage(hwnd, EM_FORMATRANGE, TRUE, (LPARAM)&fr);
        
        if (cpMin <= fr.chrg.cpMin) 
        {
            fSuccess = FALSE;
            break;
        }
        
        fr.chrg.cpMin = cpMin;
        fSuccess = EndPage(hdc) > 0;
    }
    
    SendMessage(hwnd, EM_FORMATRANGE, FALSE, 0);
    
    if (fSuccess)
    {
        EndDoc(hdc);
    } 
    
    else 
    
    {
        AbortDoc(hdc);
    }
    
    return fSuccess;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="830e5-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="830e5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="830e5-129">Utilisation de contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="830e5-129">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="830e5-130">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="830e5-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 