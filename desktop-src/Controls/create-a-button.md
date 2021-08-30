---
title: Comment créer un bouton
description: Pour créer des boutons de manière dynamique, vous utilisez la fonction CreateWindow ou CreateWindowEx. Cette rubrique montre comment utiliser la fonction CreateWindow pour créer un bouton de commande par défaut.
ms.assetid: A8C56D09-90A3-4C70-9907-61390521D1DA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4940016eaab8f64cd82f18579b31b13f2835ab8a0de00752eabfe81da316d6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920919"
---
# <a name="how-to-create-a-button"></a>Comment créer un bouton

Pour créer des boutons de manière dynamique, vous utilisez la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . Cette rubrique montre comment utiliser la fonction **CreateWindow** pour créer un bouton de commande par défaut.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions


Utilisez la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) pour créer un contrôle bouton.

Dans l’exemple C++ suivant, le paramètre *m \_ HWND* est le handle de la fenêtre parente. Le style [**BS \_ DEFPUSHBUTTON**](button-styles.md) spécifie qu’un bouton de commande par défaut doit être créé. Notez que les valeurs de taille et de position doivent être spécifiées car l’utilisation de **\_ usedefault en PV** pour un bouton définit les valeurs sur zéro.


```C++
HWND hwndButton = CreateWindow( 
    L"BUTTON",  // Predefined class; Unicode assumed 
    L"OK",      // Button text 
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_DEFPUSHBUTTON,  // Styles 
    10,         // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu.
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed.
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des boutons](about-buttons.md)
</dt> <dt>

[Référence du contrôle Button](bumper-button-button-control-reference.md)
</dt> <dt>

[Utilisation des boutons](using-buttons.md)
</dt> <dt>

[Button](buttons.md)
</dt> </dl>

 

 