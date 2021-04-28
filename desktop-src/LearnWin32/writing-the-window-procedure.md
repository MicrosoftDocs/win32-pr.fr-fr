---
title: Écriture de la procédure de fenêtre
description: Écriture de la procédure de fenêtre
ms.assetid: f022bb88-6e4c-4ec4-9eef-f125ad92167e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832aba88211a7decf20c233f5d9ab4fbeb1b1c27
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105717"
---
# <a name="writing-the-window-procedure"></a>Écriture de la procédure de fenêtre

La fonction [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) appelle la procédure de fenêtre de la fenêtre qui est la cible du message. La procédure de fenêtre a la signature suivante.

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);
```

Il y a quatre paramètres :

- *HWND* est un handle de la fenêtre.
- *uMsg* est le code du message ; par exemple, le message de [**\_ taille WM**](/windows/desktop/winmsg/wm-size) indique que la fenêtre a été redimensionnée.
- *wParam* et *lParam* contiennent des données supplémentaires relatives au message. La signification exacte dépend du code du message.

**LRESULT** est une valeur entière que votre programme retourne à Windows. Elle contient la réponse de votre programme à un message particulier. La signification de cette valeur dépend du code du message. Le **rappel** est la Convention d’appel de la fonction.

Une procédure de fenêtre classique est simplement une grande instruction switch qui bascule sur le code du message. Ajoutez des cas pour chaque message que vous souhaitez gérer.

```C++
switch (uMsg)
{
    case WM_SIZE: // Handle window resizing

    // etc
}
```

Les données supplémentaires du message sont contenues dans les paramètres *lParam* et *wParam* . Les deux paramètres sont des valeurs entières de la taille d’une largeur de pointeur (32 bits ou 64 bits). La signification de chaque dépend du code du message (*uMsg*). Pour chaque message, vous devrez rechercher le code du message sur MSDN et effectuer un cast des paramètres vers le type de données correct. En général, les données sont soit une valeur numérique, soit un pointeur vers une structure. Certains messages n’ont pas de données.

Par exemple, la documentation du message [**de \_ taille WM**](/windows/desktop/winmsg/wm-size) indique que :

- *wParam* est un indicateur qui indique si la fenêtre a été réduite, agrandie ou redimensionnée.
- *lParam* contient les nouvelles largeur et hauteur de la fenêtre sous forme de valeurs 16 bits compressées en nombre de 1 32 ou 64 bits. Vous devrez effectuer des décalages de bits pour récupérer ces valeurs. Heureusement, le fichier d’en-tête WinDef. h contient des macros d’assistance qui le font.

Une procédure de fenêtre classique gère des dizaines de messages, donc elle peut croître très longtemps. Une façon de rendre votre code plus modulaire consiste à placer la logique nécessaire pour gérer chaque message dans une fonction distincte. Dans la procédure de fenêtre, effectuez un cast des paramètres *wParam* et *lParam* vers le type de données correct, puis transmettez ces valeurs à la fonction. Par exemple, pour gérer le message de [**\_ taille WM**](/windows/desktop/winmsg/wm-size) , la procédure de fenêtre ressemble à ceci :

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_SIZE:
        {
            int width = LOWORD(lParam);  // Macro to get the low-order word.
            int height = HIWORD(lParam); // Macro to get the high-order word.

            // Respond to the message:
            OnSize(hwnd, (UINT)wParam, width, height);
        }
        break;
    }
}

void OnSize(HWND hwnd, UINT flag, int width, int height)
{
    // Handle resizing
}
```

Les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) et [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) récupèrent les valeurs de largeur et de hauteur de 16 bits à partir de *lParam*. (Vous pouvez rechercher ces types de détails dans la documentation MSDN pour chaque code de message). La procédure de fenêtre extrait la largeur et la hauteur, puis passe ces valeurs à la `OnSize` fonction.

## <a name="default-message-handling"></a>Gestion des messages par défaut

Si vous ne gérez pas un message particulier dans votre procédure de fenêtre, transmettez les paramètres de message directement à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Cette fonction effectue l’action par défaut pour le message, qui varie selon le type de message.

```C++
return DefWindowProc(hwnd, uMsg, wParam, lParam);
```

## <a name="avoiding-bottlenecks-in-your-window-procedure"></a>Éviter les goulots d’étranglement dans votre procédure de fenêtre

Pendant que votre procédure de fenêtre s’exécute, elle bloque tous les autres messages pour les fenêtres créées sur le même thread. Par conséquent, évitez un traitement long à l’intérieur de votre procédure de fenêtre. Par exemple, supposons que votre programme ouvre une connexion TCP et attend indéfiniment que le serveur réponde. Si vous le faites à l’intérieur de la procédure de fenêtre, votre interface utilisateur ne répondra pas tant que la demande n’est pas terminée. Pendant ce temps, la fenêtre ne peut pas traiter l’entrée de la souris ou du clavier, se redessiner ou même se fermer.

Au lieu de cela, vous devez déplacer le travail vers un autre thread, à l’aide de l’une des fonctionnalités multitâche intégrées à Windows :

- Créez un nouveau thread.
- Utiliser un pool de threads.
- Utilisez des appels d’e/s asynchrones.
- Utilisez des appels de procédure asynchrone.

## <a name="next"></a>Suivant

[Peindre la fenêtre](painting-the-window.md)
