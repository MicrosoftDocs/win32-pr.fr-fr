---
title: Comment créer un lien de commande
description: Cette rubrique décrit une façon de créer un lien de commande.
ms.assetid: F342075B-2D3B-40E0-B657-E1C57EDC2E3A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8024a7f060a7bae3779b9ec9ebec40bd81c74bb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463818"
---
# <a name="how-to-create-a-command-link"></a>Comment créer un lien de commande

Cette rubrique décrit une façon de créer un lien de commande.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions

### <a name="step-1-create-an-instance-of-the-command-link-button"></a>Étape 1 : créer une instance du bouton lien de commande.

Dans l’exemple de code C++ suivant, le style constant [**BS \_ COMMANDLINK**](button-styles.md) spécifie le bouton sous la forme d’un bouton de lien de commande.


```C++
HWND hwndCommandLink = CreateWindow(
    L"BUTTON",  // Predefined class; Unicode assumed
    L"",        // Text will be defined later
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_COMMANDLINK,  // Styles
    200,        // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed
```



### <a name="step-2-set-the-command-link-label-and-explanation-text"></a>Étape 2 : définir l’étiquette du lien de commande et le texte d’explication

Utilisez la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) pour définir l’étiquette de lien de commande et le texte supplémentaire via le message [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) et le message [**\_ SETNOTE BCM**](bcm-setnote.md) , respectivement.


```C++
SendMessage(hwndCommandLink, WM_SETTEXT, 0, (LPARAM)L"Command link");
SendMessage(hwndCommandLink, BCM_SETNOTE, 0, (LPARAM)L"with note");
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

 

 