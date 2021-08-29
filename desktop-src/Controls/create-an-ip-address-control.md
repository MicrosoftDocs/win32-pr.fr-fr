---
title: Comment créer un contrôle d’adresse IP
description: Cette rubrique montre comment créer une instance d’un contrôle d’adresse IP.
ms.assetid: E4DBECA6-B3F2-405F-8D95-32FA2334114D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 308893b436760ad970025b93d49a368fa44b28c7913c433ff4febad105cc41b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063109"
---
# <a name="how-to-create-an-ip-address-control"></a>Comment créer un contrôle d’adresse IP

Cette rubrique montre comment créer une instance d’un contrôle d’adresse IP.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions


Avant de créer un contrôle d’adresse IP, chargez la DLL des contrôles communs en appelant [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex). Utilisez ensuite la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) pour créer un contrôle d’adresse IP d’instance. Le nom de classe du contrôle est [**WC \_ IPAddress**](common-control-window-classes.md). Utilisez le style [**WS \_ Child**](/windows/desktop/winmsg/window-styles) , car aucune constante de style spécifique n’est associée au contrôle d’adresse IP.

Dans l’exemple de code C++ suivant, la fonction définie par l’application appelle d’abord [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) et définit le membre **dwICC** de la structure [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) sur les [**\_ \_ classes Internet ICC**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex), qui spécifie la classe d’adresses IP. Il appelle ensuite [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) pour créer une instance du contrôle d’adresse IP.


```C++
// CreateIPAdressFld - creates a IPAddress control.
// Returns the handle to the new control
// TO DO:  calling procedure needs to check whether the handle is NULL, in case 
// of an error in creation.
// int xcoord, ycoord the coordinates of location of the control in the parent window
// HINST hInst is the global handle to the application instance.
// HWND  hWndParent is the handle to the control's parent window. 
//
//
HWND CreateIPAddressFld (HWND hwndParent, int xcoord, int ycoord) 
{     
     
    INITCOMMONCONTROLSEX icex;
    
    // Ensure that the common control DLL is loaded. 
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC  = ICC_INTERNET_CLASSES ;
    InitCommonControlsEx(&icex); 
    
    // Create the IPAddress control.        
    HWND hWndIPAddressFld = CreateWindow(WC_IPADDRESS, 
                                L"", 
                                WS_CHILD | WS_OVERLAPPED | WS_VISIBLE, 
                                xcoord, 
                                ycoord,
                                150, 
                                20,  
                                hwndParent, 
                                NULL, 
                                hInst, 
                                NULL); 
                                
    return (hWndIPAddressFld);
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de contrôle d’adresse IP](bumper-ip-address-control-ip-address-control-reference.md)
</dt> <dt>

[À propos des contrôles d’adresse IP](ip-address-controls.md)
</dt> <dt>

[Utilisation des contrôles d’adresse IP](using-ip-address-controls.md)
</dt> </dl>

 

 