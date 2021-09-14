---
title: Contrôles de sous-classe
description: Si un contrôle effectue presque tout ce que vous souhaitez, mais que vous avez besoin de quelques fonctionnalités supplémentaires, vous pouvez modifier ou ajouter des fonctionnalités au contrôle d’origine en le sous-classant.
ms.assetid: 7f558674-c8b2-4461-96ba-e139416b7a1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c013ee317ddeee6ff80dc4a26982d40d7117950
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116921"
---
# <a name="subclassing-controls"></a>Contrôles de sous-classe

Si un contrôle effectue presque tout ce que vous souhaitez, mais que vous avez besoin de quelques fonctionnalités supplémentaires, vous pouvez modifier ou ajouter des fonctionnalités au contrôle d’origine en le sous-classant. Une sous-classe peut avoir toutes les fonctionnalités d’une classe existante, ainsi que toutes les fonctionnalités supplémentaires que vous souhaitez lui attribuer.

Ce document explique comment créer des sous-classes et comprend les rubriques suivantes.

-   [Sous-classement des contrôles avant ComCtl32.dll version 6](#subclassing-controls-prior-to-comctl32dll-version-6)
    -   [Stockage des données utilisateur](#storing-user-data)
    -   [Inconvénients de l’ancienne approche de sous-classe](#disadvantages-of-the-old-subclassing-approach)
-   [Sous-classer des contrôles à l’aide de ComCtl32.dll version 6](#subclassing-controls-using-comctl32dll-version-6)
    -   [SetWindowSubclass](#setwindowsubclass)
    -   [GetWindowSubclass](#getwindowsubclass)
    -   [RemoveWindowSubclass](#removewindowsubclass)
    -   [DefSubclassProc](#defsubclassproc)

## <a name="subclassing-controls-prior-to-comctl32dll-version-6"></a>Sous-classement des contrôles avant ComCtl32.dll version 6

Vous pouvez placer un contrôle dans une sous-classe et stocker des données utilisateur dans un contrôle. Vous effectuez cette opération lorsque vous utilisez des versions de ComCtl32.dll antérieures à la version 6. La création de sous-classes avec des versions antérieures de ComCtl32.dll présente quelques inconvénients.

pour créer un nouveau contrôle, il est préférable de commencer par l’un des Windows contrôles communs et de l’étendre pour répondre à un besoin particulier. Pour étendre un contrôle, créez un contrôle et remplacez sa procédure de fenêtre existante par un nouveau. La nouvelle procédure intercepte les messages du contrôle et les agit ou les transmet à la procédure d’origine pour le traitement par défaut. Utilisez la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) ou [**SETWINDOWLONGPTR**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) pour remplacer WNDPROC du contrôle. L’exemple de code suivant montre comment remplacer un WNDPROC.


```
OldWndProc = (WNDPROC)SetWindowLongPtr (hButton,
GWLP_WNDPROC, (LONG_PTR)NewWndProc);
```



### <a name="storing-user-data"></a>Stockage des données utilisateur

Vous souhaiterez peut-être stocker les données utilisateur avec une fenêtre individuelle. Ces données peuvent être utilisées par la nouvelle procédure de fenêtre pour déterminer comment dessiner le contrôle ou où envoyer certains messages. Par exemple, vous pouvez utiliser des données pour stocker un pointeur de classe C++ vers la classe qui représente le contrôle. L’exemple de code suivant montre comment utiliser [**échec SetProp**](/windows/desktop/api/winuser/nf-winuser-setpropa) pour stocker des données avec une fenêtre.


```
SetProp (hwnd, TEXT("MyData"), (HANDLE)pMyData);
```



### <a name="disadvantages-of-the-old-subclassing-approach"></a>Inconvénients de l’ancienne approche de sous-classe

La liste suivante décrit certains des inconvénients liés à l’utilisation de l’approche décrite précédemment pour la sous-classement d’un contrôle.

-   La procédure de fenêtre ne peut être remplacée qu’une seule fois.
-   Il est difficile de supprimer une sous-classe après sa création.
-   L’Association de données privées à une fenêtre est inefficace.
-   Pour appeler la procédure suivante dans une chaîne de sous-classes, vous ne pouvez pas effectuer un cast de l’ancienne procédure de fenêtre et l’appeler, vous devez l’appeler à l’aide de la fonction [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) .

## <a name="subclassing-controls-using-comctl32dll-version-6"></a>Sous-classer des contrôles à l’aide de ComCtl32.dll version 6

> [!Note]  
> ComCtl32.dll version 6 est Unicode uniquement. Les contrôles communs pris en charge par ComCtl32.dll version 6 ne doivent pas être sous-classés (ou superclassés) avec des procédures de fenêtre ANSI.

 

ComCtl32.dll version 6 contient quatre fonctions qui facilitent la création de sous-classes et éliminent les inconvénients évoqués précédemment. Les nouvelles fonctions encapsulent la gestion impliquée dans plusieurs jeux de données de référence. par conséquent, le développeur peut se concentrer sur les fonctionnalités de programmation et non sur la gestion des sous-classes. Les fonctions de sous-classe sont les suivantes :

-   [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass)
-   [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass)
-   [**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass)
-   [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc)

### <a name="setwindowsubclass"></a>SetWindowSubclass

Cette fonction est utilisée pour initialiser la sous-classe d’une fenêtre. Chaque sous-classe est identifiée de manière unique par l’adresse du *pfnSubclass* et de son *uIdSubclass*. Il s’agit des paramètres de la fonction [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) . Plusieurs sous-classes peuvent partager la même procédure de sous-classe et l’ID peut identifier chaque appel. Pour modifier des données de référence, vous pouvez effectuer des appels ultérieurs à **SetWindowSubclass**. L’avantage principal est que chaque instance de sous-classe possède ses propres données de référence.

La déclaration d’une procédure de sous-classe est légèrement différente de celle d’une procédure de fenêtre normale, car elle contient deux éléments de données supplémentaires : l’ID de sous-classe et les données de référence. Les deux derniers paramètres de la déclaration de fonction suivante illustrent cela.


```
LRESULT CALLBACK MyWndProc (HWND hWnd, UINT msg,
WPARAM wParam, LPARAM lParam, UINT_PTR uIdSubclass,
DWORD_PTR dwRefData);
```



Chaque fois qu’un message est reçu par la nouvelle procédure de fenêtre, un ID de sous-classe et des données de référence sont inclus.

> [!Note]  
> Toutes les chaînes passées à la procédure sont des chaînes Unicode même si Unicode n’est pas spécifié en tant que définition de préprocesseur.

 

L’exemple suivant montre une implémentation squelette d’une procédure de fenêtre pour un contrôle sous-classé.


```
LRESULT CALLBACK OwnerDrawButtonProc(HWND hWnd, UINT uMsg, WPARAM wParam,
                               LPARAM lParam, UINT_PTR uIdSubclass, DWORD_PTR dwRefData)
{
    switch (uMsg)
    {
    case WM_PAINT:
        .
        .
        .
        return TRUE;
    // Other cases...
    } 
    return DefSubclassProc(hWnd, uMsg, wParam, lParam);
}
```



La procédure de fenêtre peut être attachée au contrôle dans le gestionnaire [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) de la procédure de dialogue, comme indiqué dans l’exemple suivant.


```
case WM_INITDIALOG:
{
    HWND button = GetDlgItem(hDlg, IDC_OWNERDRAWBUTTON);
    SetWindowSubclass(button, OwnerDrawButtonProc, 0, 0);
    return TRUE;
}
```



### <a name="getwindowsubclass"></a>GetWindowSubclass

Cette fonction récupère des informations sur une sous-classe. Par exemple, vous pouvez utiliser [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) pour accéder aux données de référence.

### <a name="removewindowsubclass"></a>RemoveWindowSubclass

Cette fonction supprime les sous-classes. [**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass) en association avec [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) vous permet d’ajouter et de supprimer dynamiquement des sous-classes.

### <a name="defsubclassproc"></a>DefSubclassProc

La fonction [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc) appelle le gestionnaire suivant dans la chaîne de sous-classe. La fonction récupère également l’ID et les données de référence appropriés et transmet les informations à la procédure de fenêtre suivante.

 

 