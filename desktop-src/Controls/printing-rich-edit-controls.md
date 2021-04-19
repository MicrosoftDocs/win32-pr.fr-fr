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
# <a name="how-to-print-the-contents-of-rich-edit-controls"></a>Comment imprimer le contenu de contrôles RichEdit

Cette section contient des informations sur l’impression du contenu des contrôles RichEdit.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions

### <a name="use-print-preview"></a>Utiliser l’aperçu avant impression

Pour mettre en forme le texte dans un contrôle RichEdit tel qu’il apparaîtra sur un appareil cible (généralement la page imprimée), envoyez le message [**em \_ SETTARGETDEVICE**](em-settargetdevice.md) , en transmettant le handle à un contexte de périphérique (HDC) de l’appareil cible et à la largeur de ligne souhaitée. En général, vous obtiendrez la largeur de ligne en appelant [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) pour le HDC cible.

### <a name="format-print-for-a-specific-device"></a>Mettre en forme l’impression pour un appareil spécifique

Pour mettre en forme une partie du contenu d’un contrôle RichEdit pour un appareil spécifique, envoyez le message [**em \_ FormatRange**](em-formatrange.md) . La structure [**FormatRange**](/windows/desktop/api/Richedit/ns-richedit-formatrange) utilisée avec ce message spécifie la plage de texte à mettre en forme, ainsi que le HDC pour l’appareil cible. Le cas échéant, ce message envoie également le texte à l’imprimante.

### <a name="use-banding"></a>Utiliser la bande

La bande est le processus par lequel une seule page de sortie est générée à l’aide d’un ou de plusieurs rectangles séparés, ou de bandes. Lorsque toutes les bandes sont placées sur la page, une image complète les résultats. Cette approche est souvent utilisée par les imprimantes raster qui ne disposent pas de suffisamment de mémoire ou de capacité à effectuer une image de page entière à la fois.

Pour implémenter des bandes, utilisez le message [**em \_ DISPLAYBAND**](em-displayband.md) pour envoyer des parties successives du contenu du contrôle RichEdit à l’appareil. Ce message s’imprime sur l’appareil qui a été spécifié dans un appel précédent à [**em \_ FormatRange**](em-formatrange.md). Bien entendu, le paramètre *wParam* du message **em \_ FormatRange** doit être égal à zéro, de sorte que l’impression n’est pas lancée par ce message.

## <a name="printrtf-code-example"></a>Exemple de code PrintRTF

L’exemple de code suivant imprime le contenu d’un contrôle RichEdit sur l’imprimante spécifiée.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de contrôles RichEdit](using-rich-edit-controls.md)
</dt> <dt>

[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 