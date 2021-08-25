---
title: Comment créer un contrôle de List-View
description: Cette rubrique montre comment créer un contrôle List-View. Pour créer un contrôle List-View, utilisez la fonction CreateWindow ou CreateWindowEx et spécifiez la classe de fenêtre de la vue ListView de WC \_ .
ms.assetid: FEAA0ACA-A086-46DF-9DD2-A3E32F2CCDA3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71eddfb60a2ea035a5afe62423289da40a47b61841d3ba58c4cafa2824a65b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826609"
---
# <a name="how-to-create-a-list-view-control"></a>Comment créer un contrôle de List-View

Cette rubrique montre comment créer un contrôle List-View. Pour créer un contrôle List-View, utilisez la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) et spécifiez la classe de fenêtre de la vue [**\_ ListView de WC**](common-control-window-classes.md) .

Un contrôle List-View peut également être créé dans le cadre d’un modèle de boîte de dialogue. Vous devez spécifier [**WC \_ ListView**](common-control-window-classes.md) comme nom de classe. Pour utiliser un contrôle List-View dans le cadre d’un modèle de boîte de dialogue, vous devez appeler [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) ou [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) avant de créer une instance de la boîte de dialogue.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions


Inscrivez d’abord la classe de fenêtre en appelant la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) et en spécifiant le bit des [**\_ \_ classes ListView ICC**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) dans la structure **InitCommonControlsEx** qui l’accompagne. Cela permet de s’assurer que la DLL de contrôles communs est chargée. Ensuite, utilisez la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) et spécifiez la classe de fenêtre du [**\_ ListView de WC**](common-control-window-classes.md) .

> [!Note]  
> Par défaut, un contrôle List-View utilise la police du titre de l’icône. Toutefois, vous pouvez utiliser un message [**WM \_ SetFont**](/windows/desktop/winmsg/wm-setfont) pour spécifier la police à utiliser pour le texte. Vous devez envoyer ce message avant d’insérer des éléments. Le contrôle utilise les dimensions de la police spécifiée par le message **WM \_ SetFont** pour déterminer l’espacement et la mise en page. Vous pouvez également personnaliser la police pour chaque élément. Pour plus d’informations, consultez [dessin personnalisé](custom-draw.md).

 

L’exemple de code C++ suivant crée un contrôle de liste en mode rapport.


```C++
// CreateListView: Creates a list-view control in report view.
// Returns the handle to the new control
// TO DO:  The calling procedure should determine whether the handle is NULL, in case 
// of an error in creation.
//
// HINST hInst: The global handle to the applicadtion instance.
// HWND  hWndParent: The handle to the control's parent window. 
//
HWND CreateListView (HWND hwndParent) 
{
    INITCOMMONCONTROLSEX icex;           // Structure for control initialization.
    icex.dwICC = ICC_LISTVIEW_CLASSES;
    InitCommonControlsEx(&icex);

    RECT rcClient;                       // The parent window's client area.

    GetClientRect (hwndParent, &rcClient); 

    // Create the list-view window in report view with label editing enabled.
    HWND hWndListView = CreateWindow(WC_LISTVIEW, 
                                     L"",
                                     WS_CHILD | LVS_REPORT | LVS_EDITLABELS,
                                     0, 0,
                                     rcClient.right - rcClient.left,
                                     rcClient.bottom - rcClient.top,
                                     hwndParent,
                                     (HMENU)IDM_CODE_SAMPLES,
                                     g_hInst,
                                     NULL); 

    return (hWndListView);
}

```




En règle générale, les applications de vue de liste permettent à l’utilisateur de passer d’une vue à une autre.

L’exemple de code C++ suivant modifie le style de fenêtre de l’affichage de liste, qui modifie à son tour l’affichage.


```C++
// SetView: Sets a list-view's window style to change the view.
// hWndListView: A handle to the list-view control. 
// dwView:       A value specifying the new view style.
//
VOID SetView(HWND hWndListView, DWORD dwView) 
{ 
    // Retrieve the current window style. 
    DWORD dwStyle = GetWindowLong(hWndListView, GWL_STYLE); 
    
    // Set the window style only if the view bits changed.
    if ((dwStyle & LVS_TYPEMASK) != dwView) 
    {
        SetWindowLong(hWndListView,
                      GWL_STYLE,
                      (dwStyle & ~LVS_TYPEMASK) | dwView);
    }               // Logical OR'ing of dwView with the result of 
}                   // a bitwise AND between dwStyle and 
                    // the Unary complenent of LVS_TYPEMASK.

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence du contrôle List-View](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[À propos des contrôles List-View](list-view-controls-overview.md)
</dt> <dt>

[Utilisation de contrôles List-View](using-list-view-controls.md)
</dt> </dl>

 

 