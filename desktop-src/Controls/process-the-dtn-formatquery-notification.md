---
title: Comment traiter la notification de DTN_FORMATQUERY
description: Cette rubrique montre comment traiter une notification de format de requête envoyée par le contrôle de sélecteur de date et d’heure (PAO).
ms.assetid: 74E29438-2F50-4ADD-B0C4-DB3450BF08D7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941c148332c36711e68b7c3b773fdb47acef202c5fd2a67f5620319f06c7fbc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696939"
---
# <a name="how-to-process-the-dtn_formatquery-notification"></a>Comment traiter la notification DTN \_ FORMATQUERY

Cette rubrique montre comment traiter une notification de format de requête envoyée par le contrôle de sélecteur de date et d’heure (PAO).

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions


Un contrôle de PAO envoie un code de notification [DTN \_ FORMATQUERY](dtn-formatquery.md) pour demander des informations sur la taille maximale possible d’un champ de rappel dans le contrôle. Votre application doit gérer ce message pour s’assurer que tous les champs sont affichés correctement.

L’exemple de code C++ suivant est une fonction définie par l’application qui traite le code de notification [DTN \_ FORMATQUERY](dtn-formatquery.md) en calculant la largeur de la chaîne la plus large possible pour un champ de rappel donné.

**Avertissement de sécurité :** L’utilisation incorrecte de **lstrcmp** peut compromettre la sécurité de votre application. Par exemple, avant d’appeler **lstrcmp** dans l’exemple de code suivant, vous devez vous assurer que les deux chaînes se terminent par un caractère null. vous devez examiner les [considérations relatives à la sécurité : contrôles Microsoft Windows](sec-comctls.md) avant de continuer.



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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles de sélecteur de date et heure](using-date-and-time-picker.md)
</dt> <dt>

[Référence de contrôle de sélecteur de date et heure](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Sélecteur de date et heure](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




