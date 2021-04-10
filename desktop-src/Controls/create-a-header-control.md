---
title: Comment créer un contrôle header
description: Cette rubrique montre comment créer un contrôle header et le positionner dans la zone cliente de la fenêtre parente.
ms.assetid: 094AF70C-2761-439E-A1E3-0FD04212FE87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bce9bf9d7b117f5f61766ca326b91b0d19a2c903
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104032119"
---
# <a name="how-to-create-a-header-control"></a>Comment créer un contrôle header

Cette rubrique montre comment créer un contrôle header et le positionner dans la zone cliente de la fenêtre parente. Vous pouvez créer un contrôle header à l’aide de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) et en spécifiant la classe de fenêtre d' [**\_ en-tête WC**](common-control-window-classes.md) et les [styles de contrôle d’en-tête](header-control-styles.md)appropriés. Cette classe de fenêtre est inscrite lors du chargement de la DLL de contrôles communs. Pour vous assurer que cette DLL est chargée, utilisez la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) .

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions


L’exemple de code C++ suivant appelle d’abord la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) pour charger la dll de contrôle commune. Il appelle ensuite la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) pour créer un contrôle header. Le contrôle est initialement masqué. Le message de [**\_ disposition HDM**](hdm-layout.md) est utilisé pour calculer la taille et la position du contrôle dans la fenêtre parente. Le contrôle est ensuite repositionné et rendu visible.



```C++
// DoCreateHeader - creates a header control that is positioned along 
//     the top of the parent window's client area. 
// Returns the handle to the header control. 
// hwndParent - handle to the parent window. 
// 
// Global variable 
//    g_hinst - handle to the application instance 
extern HINSTANCE g_hinst; 
//
// child-window identifier
int ID_HEADER;
//
HWND DoCreateHeader(HWND hwndParent) 
{ 
        HWND hwndHeader; 
        RECT rcParent; 
        HDLAYOUT hdl; 
        WINDOWPOS wp; 
 
        // Ensure that the common control DLL is loaded, and then create 
        // the header control. 
        INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
        icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
        icex.dwICC = ICC_LISTVIEW_CLASSES;   //set dwICC member to ICC_LISTVIEW_CLASSES    
                                             // this loads list-view and header control classes.
    InitCommonControlsEx(&icex); 
 
        if ((hwndHeader = CreateWindowEx(0, WC_HEADER, (LPCTSTR) NULL, 
                WS_CHILD | WS_BORDER | HDS_BUTTONS | HDS_HORZ, 
                0, 0, 0, 0, hwndParent, (HMENU) ID_HEADER, g_hinst, 
                (LPVOID) NULL)) == NULL) 
            return (HWND) NULL; 
 
        // Retrieve the bounding rectangle of the parent window's 
        // client area, and then request size and position values 
        // from the header control. 
        GetClientRect(hwndParent, &rcParent); 
 
        hdl.prc = &rcParent; 
        hdl.pwpos = &wp; 
        if (!SendMessage(hwndHeader, HDM_LAYOUT, 0, (LPARAM) &hdl)) 
            return (HWND) NULL; 
 
        // Set the size, position, and visibility of the header control. 
        SetWindowPos(hwndHeader, wp.hwndInsertAfter, wp.x, wp.y, 
            wp.cx, wp.cy, wp.flags | SWP_SHOWWINDOW); 
 
        return hwndHeader; 
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des contrôles Header](header-controls.md)
</dt> <dt>

[Référence de contrôle header](bumper-header-control-header-control-reference.md)
</dt> <dt>

[Utilisation des contrôles Header](using-header-controls.md)
</dt> </dl>

 

 