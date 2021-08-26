---
title: Comment créer un contrôle de sélecteur de date et d’heure
description: Cette rubrique montre comment créer dynamiquement un contrôle de sélecteur de date et d’heure (PAO).
ms.assetid: D4ACA939-3004-48D3-ADD9-FC5E53128BA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afa3f18e6033d3764e385280da383d74c351201694969266dcc383654a4372ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920889"
---
# <a name="how-to-create-a-date-and-time-picker-control"></a>Comment créer un contrôle de sélecteur de date et d’heure

Cette rubrique montre comment créer dynamiquement un contrôle de sélecteur de date et d’heure (PAO). L’exemple de code C++ qui l’accompagne crée un contrôle PAO dans une boîte de dialogue non modale. Elle utilise le style [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) pour permettre à l’utilisateur de simuler la désactivation de la date dans le contrôle.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Étape 1 :

Inscrivez la classe de fenêtre en appelant la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) et en spécifiant le \_ bit des \_ classes de date ICC dans la structure [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) qui l’accompagne.


```C++
 INITCOMMONCONTROLSEX icex;

 icex.dwSize = sizeof(icex);
 icex.dwICC = ICC_DATE_CLASSES;

 InitCommonControlsEx(&icex);
```



### <a name="step-2"></a>Étape 2 :

Pour créer le contrôle PAO, utilisez la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . Spécifiez la [**\_ classe DATETIMEPICK**](common-control-window-classes.md) comme classe de fenêtre et transmettez le descripteur à la boîte de dialogue parent.

L’exemple de code C++ suivant utilise la fonction [**createDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga) pour créer une boîte de dialogue non modale. Il appelle ensuite **CreateWindowEx** pour créer le contrôle de PAO.


```C++
  hwndDlg = CreateDialog  (g_hinst,
                           MAKEINTRESOURCE(IDD_DIALOG1),
                           hwndMain,
                           DlgProc);

  if(hwndDlg)
      hwndDP = CreateWindowEx(0,
                           DATETIMEPICK_CLASS,
                           TEXT("DateTime"),
                           WS_BORDER|WS_CHILD|WS_VISIBLE|DTS_SHOWNONE,
                           20,50,220,20,
                           hwndDlg,
                           NULL,
                           g_hinst,
                           NULL);
```



## <a name="complete-example"></a>Exemple complet


```C++
//  CreateDatePick creates a DTP control within a dialog box.
//  Returns the handle to the new DTP control if successful, or NULL 
//  otherwise.
// 
//    hwndMain - The handle to the main window.
//    g_hinst  - global handle to the program instance.

HWND WINAPI CreateDatePick(HWND hwndMain)
{
    HWND hwndDP = NULL;
    HWND hwndDlg = NULL;

    INITCOMMONCONTROLSEX icex;

    icex.dwSize = sizeof(icex);
    icex.dwICC = ICC_DATE_CLASSES;

    InitCommonControlsEx(&icex);

    hwndDlg = CreateDialog  (g_hinst,
                             MAKEINTRESOURCE(IDD_DIALOG1),
                             hwndMain,
                             DlgProc);

    if(hwndDlg)
        hwndDP = CreateWindowEx(0,
                             DATETIMEPICK_CLASS,
                             TEXT("DateTime"),
                             WS_BORDER|WS_CHILD|WS_VISIBLE|DTS_SHOWNONE,
                             20,50,220,20,
                             hwndDlg,
                             NULL,
                             g_hinst,
                             NULL);

    return (hwndDP);
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

 

 