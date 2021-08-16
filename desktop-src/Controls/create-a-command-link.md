---
title: Comment créer un lien de commande
description: Cette rubrique décrit une façon de créer un lien de commande.
ms.assetid: F342075B-2D3B-40E0-B657-E1C57EDC2E3A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c61888921f06e017ec1ea625730c3cc52de5ab364db22fc01fd021ce5629c63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920899"
---
# <a name="how-to-create-a-command-link"></a>Comment créer un lien de commande

Cette rubrique décrit une façon de créer un lien de commande.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

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

 

 