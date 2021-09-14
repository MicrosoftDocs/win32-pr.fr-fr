---
title: Comment traiter des messages de notification
description: Une feuille de propriétés envoie \_ des messages de notification WM pour récupérer des informations à partir des pages et notifier les pages des actions de l’utilisateur.
ms.assetid: 82768E43-97BA-451A-9373-D5B8FD06ABED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c544910e44e0c865e738427285d7488147b9c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117601"
---
# <a name="how-to-process-notification-messages"></a>Comment traiter des messages de notification

Une feuille de propriétés envoie des messages de [**\_ notification WM**](wm-notify.md) pour récupérer des informations à partir des pages et notifier les pages des actions de l’utilisateur.

Le paramètre *lParam* du message est l’adresse d’une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , qui contient le descripteur de la boîte de dialogue de la feuille de propriétés, le handle de la boîte de dialogue de la page et un code de notification. La page doit répondre à certains messages de notification en affectant \_ à la valeur MSGRESULT de la page la valeur **true** ou **false**.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="process-notification-messages"></a>Traiter les messages de notification

L’exemple suivant est un fragment de code de la procédure de boîte de dialogue pour une page. Il montre comment traiter le code de notification [ \_ d’aide PSN](psn-help.md) .


```C++
case WM_NOTIFY:

    switch (((NMHDR FAR *) lParam)->code) 
    {
    case PSN_HELP:
        {
         
        char szBuf[FILE_LEN]; // Buffer for name of Help file

        // Display Help for the font properties page.
        LoadString(g_hinst, IDS_HELPFILE, &szBuf, sizeof(szBuf)/sizeof(szBuf[0]));
        WinHelp(((NMHDR FAR *)lParam)->hwndFrom, &szBuf, HELP_CONTEXT, IDH_FONT_PROPERTIES);                
        
        break;
        
         }
         
        // Process other property sheet notifications here.
    }
    
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des feuilles de propriétés](using-property-sheets.md)
</dt> <dt>

[Windows démonstration des contrôles communs (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




