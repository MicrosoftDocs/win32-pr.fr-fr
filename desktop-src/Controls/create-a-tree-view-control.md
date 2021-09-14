---
title: Comment créer un contrôle de Tree-View
description: Pour créer un contrôle Tree-View, utilisez la fonction CreateWindowEx, en spécifiant la valeur de l’arborescence WC \_ pour la classe Window.
ms.assetid: FEC3BF62-3085-47D4-B82E-7BD7B34B397D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136ec22cc4f3f88e57266a4c2ac88df542a39429
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223633"
---
# <a name="how-to-create-a-tree-view-control"></a>Comment créer un contrôle de Tree-View

Pour créer un contrôle Tree-View, utilisez la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant la valeur de l’arborescence [**WC \_**](common-control-window-classes.md) pour la classe Window. La classe de fenêtre d’arborescence est inscrite dans l’espace d’adressage de l’application lors du chargement de la DLL de contrôle commune. Pour vous assurer que la DLL est chargée, utilisez la fonction [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) .

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="create-an-instance-of-a-tree-view-control"></a>Créer une instance d’un contrôle Tree-View

L’exemple suivant crée un contrôle d’arborescence dimensionné pour s’ajuster à la zone cliente de la fenêtre parente. Il utilise également des fonctions définies par l’application pour associer une liste d’images au contrôle et ajouter des éléments au contrôle.


```C++
// Create a tree-view control. 
// Returns the handle to the new control if successful,
// or NULL otherwise. 
// hwndParent - handle to the control's parent window. 
// lpszFileName - name of the file to parse for tree-view items.
// g_hInst - the global instance handle.
// ID_TREEVIEW - the resource ID of the control.

HWND CreateATreeView(HWND hwndParent)
{ 
    RECT rcClient;  // dimensions of client area 
    HWND hwndTV;    // handle to tree-view control 

    // Ensure that the common control DLL is loaded. 
    InitCommonControls(); 

    // Get the dimensions of the parent window's client area, and create 
    // the tree-view control. 
    GetClientRect(hwndParent, &rcClient); 
    hwndTV = CreateWindowEx(0,
                            WC_TREEVIEW,
                            TEXT("Tree View"),
                            WS_VISIBLE | WS_CHILD | WS_BORDER | TVS_HASLINES, 
                            0, 
                            0, 
                            rcClient.right, 
                            rcClient.bottom,
                            hwndParent, 
                            (HMENU)ID_TREEVIEW, 
                            g_hInst, 
                            NULL); 

    // Initialize the image list, and add items to the control. 
    // InitTreeViewImageLists and InitTreeViewItems are application- 
    // defined functions, shown later. 
    if (!InitTreeViewImageLists(hwndTV) || 
                !InitTreeViewItems(hwndTV))
    { 
        DestroyWindow(hwndTV); 
        return FALSE; 
    } 
    return hwndTV;
} 
```



## <a name="remarks"></a>Notes

Lorsque vous créez un contrôle Tree-View, vous pouvez également lui envoyer un message [**WM \_ SetFont**](/windows/desktop/winmsg/wm-setfont) pour définir la police à utiliser pour le texte. Vous devez envoyer ce message avant d’insérer des éléments. Par défaut, une arborescence utilise la police du titre de l’icône. Bien que vous puissiez personnaliser la police par élément à l’aide d’un [dessin personnalisé](custom-draw.md), le contrôle d’arborescence utilise les dimensions de la police spécifiées par le message **WM \_ SetFont** pour déterminer l’espacement et la mise en page.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de contrôles Tree-View](using-treeview.md)
</dt> <dt>

[L’exemple CustDTv illustre un dessin personnalisé dans un contrôle Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 