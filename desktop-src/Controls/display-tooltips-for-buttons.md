---
title: Comment afficher des info-bulles pour les boutons
description: Quand vous spécifiez le \_ style des info-bulles TBSTYLE, la barre d’outils crée et gère un contrôle ToolTip. Le contrôle ToolTip est masqué et s’affiche uniquement lorsque les utilisateurs déplacent le pointeur sur un bouton de barre d’outils et le laissent pendant environ une seconde.
ms.assetid: 0383DB63-A10E-4235-A974-AB21551E086B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb37de7c21c904673a1f656533497130d50bd8f7
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103841990"
---
# <a name="how-to-display-tooltips-for-buttons"></a>Comment afficher des info-bulles pour les boutons

Quand vous spécifiez le style des [**\_ info-bulles TBSTYLE**](toolbar-control-and-button-styles.md) , la barre d’outils crée et gère un contrôle ToolTip. Le contrôle ToolTip est masqué et s’affiche uniquement lorsque les utilisateurs déplacent le pointeur sur un bouton de barre d’outils et le laissent pendant environ une seconde.

Votre application peut fournir du texte au contrôle ToolTip de l’une des manières suivantes :

-   Définissez le texte d’info-bulle en tant que membre **iString** de la structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) pour chaque bouton. Vous devez également envoyer un [**message \_ SETMAXTEXTROWS to**](tb-setmaxtextrows.md) et définir le nombre maximal de lignes de texte sur 0, afin que le texte ne s’affiche pas en tant qu’info-bulle plutôt que sous forme d’info-bulle.
-   Créez la barre d’outils avec le style de [**\_ liste TBSTYLE**](toolbar-control-and-button-styles.md) , puis définissez le style étendu [**TBSTYLE \_ ex \_ MIXEDBUTTONS**](toolbar-extended-styles.md) . Les étiquettes s’affichent uniquement pour les boutons qui ont le style [**BTNS \_ SHOWTEXT**](toolbar-control-and-button-styles.md) . Pour les boutons qui n’ont pas ce style, une info-bulle est affichée et contient le texte du bouton.
-   Répondez au code de notification [ttn \_ GETDISPINFO](ttn-getdispinfo.md) .
-   Répondez au code de notification [TBN \_ GETINFOTIP](tbn-getinfotip.md) .

Une application qui doit envoyer des messages directement au contrôle ToolTip peut récupérer le handle du contrôle à l’aide du message [**to \_ GETTOOLTIPS**](tb-gettooltips.md) . Une application peut remplacer le contrôle ToolTip d’une barre d’outils par un autre contrôle ToolTip en utilisant le message [**to \_ SETTOOLTIPS**](tb-settooltips.md) .

La méthode la plus souple pour fournir le texte info-bulle consiste à répondre au code de notification [ttn \_ GETDISPINFO](ttn-getdispinfo.md) ou [TBN \_ GETINFOTIP](tbn-getinfotip.md) envoyé par le contrôle ToolBar à son parent sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . Pour [ttn \_ GETDISPINFO](ttn-getdispinfo.md), le paramètre *lParam* comprend un pointeur vers une structure [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) (également définie comme **LPTOOLTIPTEXT**) qui spécifie l’identificateur de commande du bouton pour lequel le texte d’aide est nécessaire. Cet identificateur se trouve dans le membre **NMTTDISPINFO. HDR. idFrom** . Une application peut copier le texte d’aide dans la structure, spécifier l’adresse d’une chaîne contenant le texte d’aide ou spécifier le handle d’instance et l’identificateur de ressource d’une ressource de type chaîne.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions

### <a name="display-a-tooltip-for-a-button"></a>Afficher une info-bulle pour un bouton

L’exemple de code suivant gère le code de notification d’info-bulle [ttn \_ GETDISPINFO](ttn-getdispinfo.md) en fournissant du texte à partir d’identificateurs de ressource.


```C++
case WM_NOTIFY: 
            
    switch (((LPNMHDR) lParam)->code) 
    {
    
    case TTN_GETDISPINFO: 
        { 
            LPTOOLTIPTEXT lpttt = (LPTOOLTIPTEXT)lParam; 
            
            // Set the instance of the module that contains the resource.
            lpttt->hinst = g_hInst; 
            
            UINT_PTR idButton = lpttt->hdr.idFrom;
            
            switch (idButton) 
            { 
            case IDM_NEW: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_NEW); 
                break; 
                
            case IDM_OPEN: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_OPEN); 
                break; 
                
            case IDM_SAVE: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_SAVE); 
                break; 
            } 
            
            break; 
        } 
    }
    return TRUE;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles ToolBar](using-toolbar-controls.md)
</dt> <dt>

[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




