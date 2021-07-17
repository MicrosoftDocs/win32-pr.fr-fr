---
title: À propos de l’entrée au clavier
description: Cette rubrique traite de l’entrée au clavier.
ms.assetid: de34727e-e8c7-481d-982d-0e42a02704db
keywords:
- entrée d’utilisateur, entrée au clavier
- capture de l’entrée utilisateur, entrée au clavier
- entrée au clavier
- focus clavier
- messages de séquence de touches
- messages de caractères
- séquences de touches système
- séquences de touches du système
- messages de caractères non-système
- clés mortes
- messages de caractères morts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0de85794901be3fef37156bde29520039f85702b
ms.sourcegitcommit: b3839bea8d55c981d53cb8802d666bf49093b428
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/16/2021
ms.locfileid: "114373202"
---
# <a name="about-keyboard-input"></a>À propos de l’entrée au clavier

Les applications doivent accepter l’entrée utilisateur à partir du clavier et de la souris. Une application reçoit une entrée au clavier sous la forme de messages publiés dans son Windows.

Cette section couvre les sujets suivants :

-   [Modèle d’entrée au clavier](#keyboard-input-model)
-   [Focus clavier et activation](#keyboard-focus-and-activation)
-   [Messages de séquence de touches](#keystroke-messages)
    -   [Séquences de touches système et système](#system-and-nonsystem-keystrokes)
    -   [Codes de clé virtuelle décrits](#virtual-key-codes-described)
    -   [Indicateurs de message de frappe](#keystroke-message-flags)
-   [Messages de caractères](#character-messages)
    -   [Messages de caractères non-système](#nonsystem-character-messages)
    -   [Messages de caractères morts](#dead-character-messages)
-   [État de la clé](#key-status)
-   [Traductions de séquences de touches et de caractères](#keystroke-and-character-translations)
-   [Prise en charge des touches d’accès rapide](#hot-key-support)
-   [Touches du clavier pour la navigation et d’autres fonctions](#keyboard-keys-for-browsing-and-other-functions)
-   [Simulation de l’entrée](#simulating-input)
-   [Langues, paramètres régionaux et dispositions de clavier](#languages-locales-and-keyboard-layouts)

## <a name="keyboard-input-model"></a>Modèle d’entrée au clavier

Le système fournit une prise en charge du clavier indépendante de l’appareil pour les applications en installant un pilote de périphérique clavier approprié pour le clavier actuel. Le système fournit une prise en charge du clavier indépendante de la langue à l’aide de la disposition de clavier propre à la langue actuellement sélectionnée par l’utilisateur ou l’application. Le pilote de périphérique clavier reçoit des codes d’analyse à partir du clavier, qui sont envoyés à la disposition du clavier dans laquelle ils sont convertis en messages et publiés dans les fenêtres appropriées de votre application.

Affecté à chaque clé d’un clavier est une valeur unique appelée *code d’analyse*, un identificateur dépendant du périphérique pour la touche du clavier. Un clavier génère deux codes d’analyse lorsque l’utilisateur tape une clé (l’un lorsque l’utilisateur appuie sur la touche et l’autre lorsque l’utilisateur relâche la touche).

Le pilote de périphérique clavier interprète un code d’analyse et le convertit (mappe) en *Code de clé virtuelle*, une valeur indépendante du périphérique définie par le système qui identifie l’objectif d’une clé. Après la traduction d’un code d’analyse, la disposition du clavier crée un message qui comprend le code d’analyse, le code de la touche virtuelle et d’autres informations sur la séquence de touches, puis place le message dans la file d’attente des messages système. Le système supprime le message de la file d’attente des messages système et le publie dans la file d’attente de messages du thread approprié. Finalement, la boucle de message du thread supprime le message et le transmet à la procédure de fenêtre appropriée pour traitement. La figure suivante illustre le modèle d’entrée au clavier.

![modèle de traitement d’entrée au clavier](images/csinp-01.png)

## <a name="keyboard-focus-and-activation"></a>Focus clavier et activation

Le système publie des messages de clavier dans la file d’attente de messages du thread de premier plan qui a créé la fenêtre avec le focus clavier. Le *focus clavier* est une propriété temporaire d’une fenêtre. Le système partage le clavier entre toutes les fenêtres de l’affichage en décalant le focus clavier, à la direction de l’utilisateur, d’une fenêtre à l’autre. La fenêtre qui a le focus clavier reçoit (à partir de la file d’attente de messages du thread qui l’a créé) tous les messages de clavier jusqu’à ce que le focus passe à une autre fenêtre.

Un thread peut appeler la fonction [**getFocus**](/windows/win32/api/winuser/nf-winuser-getfocus) pour déterminer laquelle de ses fenêtres (le cas échéant) a actuellement le focus clavier. Un thread peut mettre le focus clavier sur l’une de ses fenêtres en appelant la fonction [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) . Lorsque le focus clavier passe d’une fenêtre à une autre, le système envoie un message [**WM \_ KILLFOCUS**](wm-killfocus.md) à la fenêtre qui a perdu le focus, puis envoie un message [**WM \_ SetFocus**](wm-setfocus.md) à la fenêtre qui a obtenu le focus.

Le concept de focus clavier est lié à celui de la fenêtre active. La *fenêtre active* est la fenêtre de niveau supérieur avec laquelle l’utilisateur travaille actuellement. La fenêtre avec le focus clavier est soit la fenêtre active, soit une fenêtre enfant de la fenêtre active. Pour aider l’utilisateur à identifier la fenêtre active, le système la place en haut de l’ordre de plan et met en surbrillance sa barre de titre (le cas échéant) et sa bordure.

L’utilisateur peut activer une fenêtre de niveau supérieur en cliquant dessus, en la sélectionnant à l’aide de la combinaison de touches ALT + TAB ou ALT + ÉCHAP, ou en la sélectionnant dans la Liste des tâches. Un thread peut activer une fenêtre de niveau supérieur à l’aide de la fonction [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) . Il peut déterminer si une fenêtre de niveau supérieur créée est active à l’aide de la fonction [**GetActiveWindow**](/windows/win32/api/winuser/nf-winuser-getactivewindow) .

Quand une fenêtre est désactivée et qu’une autre est activée, le système envoie le message [**WM \_ Activate**](wm-activate.md) . Le mot de poids faible du paramètre *wParam* est zéro si la fenêtre est désactivée et différente de zéro si elle est activée. Lorsque la procédure de fenêtre par défaut reçoit le message **WM \_ Activate** , elle définit le focus clavier sur la fenêtre active.

Pour empêcher les événements d’entrée de clavier et de souris d’atteindre les applications, utilisez [**BlockInput**](/windows/win32/api/winuser/nf-winuser-blockinput). Notez que la fonction **BlockInput** n’interfère pas avec la table d’état d’entrée du clavier asynchrone. Cela signifie que l’appel de la fonction [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) pendant que l’entrée est bloquée modifie la table d’état d’entrée du clavier asynchrone.

## <a name="keystroke-messages"></a>Messages de séquence de touches

Si vous appuyez sur une touche, un message [**WM \_ keyverse**](wm-keydown.md) ou [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) est placé dans la file d’attente de messages de thread attachée à la fenêtre qui a le focus clavier. La libération d’une clé entraîne le placement d’un message [**WM \_ KEYUP**](wm-keyup.md) ou [**WM \_ SYSKEYUP**](wm-syskeyup.md) dans la file d’attente.

Les messages de touche et de réduction de la clé se produisent généralement par paires, mais si l’utilisateur maintient une clé suffisamment longue pour démarrer la fonctionnalité de répétition automatique du clavier, le système génère un certain nombre de messages [**WM \_ keyverse**](wm-keydown.md) ou [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) dans une ligne. Il génère ensuite un message [**WM \_ KEYUP**](wm-keyup.md) ou [**WM \_ SYSKEYUP**](wm-syskeyup.md) unique lorsque l’utilisateur relâche la touche.

Cette section couvre les sujets suivants :

-   [Séquences de touches système et système](#system-and-nonsystem-keystrokes)
-   [Codes de clé virtuelle décrits](#virtual-key-codes-described)
-   [Indicateurs de message de frappe](#keystroke-message-flags)

### <a name="system-and-nonsystem-keystrokes"></a>Séquences de touches système et système

Le système fait une distinction entre les séquences de touches du système et les séquences de touches du système. Les séquences de touches système produisent des messages de frappe système, [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) et [**WM \_ SYSKEYUP**](wm-syskeyup.md). Les séquences de touches autres que le système produisent des messages de frappe de touche de système, [**WM \_ keyverse**](wm-keydown.md) et [**WM \_ KEYUP**](wm-keyup.md).

Si votre procédure de fenêtre doit traiter un message de frappe de touche système, assurez-vous qu’après le traitement du message, la procédure le transmet à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Dans le cas contraire, toutes les opérations système impliquant la touche ALT seront désactivées chaque fois que la fenêtre a le focus clavier. Autrement dit, l’utilisateur ne peut pas accéder au menu des menus ou du système de la fenêtre, ni utiliser la combinaison de touches ALT + ECHAP ou ALT + TAB pour activer une autre fenêtre.

Les messages de frappe de touche système sont principalement destinés à être utilisés par le système plutôt que par une application. Le système les utilise pour fournir son interface clavier intégrée aux menus et permettre à l’utilisateur de contrôler la fenêtre qui est active. Les messages de frappe de touche système sont générés lorsque l’utilisateur tape une clé en combinaison avec la touche ALT, ou lorsque l’utilisateur tape et qu’aucune fenêtre n’a le focus clavier (par exemple, lorsque l’application active est réduite). Dans ce cas, les messages sont publiés dans la file d’attente de messages attachée à la fenêtre active.

Les messages de séquence de touches autres que le système sont destinés à être utilisés par les fenêtres d’application. la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ne fait rien. Une procédure de fenêtre peut ignorer tous les messages de frappe de touche non-système dont elle n’a pas besoin.

### <a name="virtual-key-codes-described"></a>Codes Virtual-Key décrits

Le paramètre **wParam** d’un message de séquence de touches contient le code de la touche virtuelle de la touche qui a été enfoncée ou libérée. Une procédure de fenêtre traite ou ignore un message de séquence de touches, en fonction de la valeur du code de la touche virtuelle.

Une procédure de fenêtre classique traite uniquement un petit sous-ensemble des messages de frappe de touche qu’elle reçoit et ignore le reste. Par exemple, une procédure de fenêtre peut traiter uniquement des messages de séquence de touches [**WM \_**](wm-keydown.md) et uniquement celles qui contiennent des codes de touche virtuelle pour les touches de déplacement du curseur, des touches Maj (également appelées clés de contrôle) et des touches de fonction. Une procédure de fenêtre classique ne traite pas les messages de frappe de touche de caractères. Au lieu de cela, elle utilise la fonction [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) pour convertir le message en messages de caractères. Pour plus d’informations sur les **TranslateMessage** et les messages de caractères, consultez [messages de caractères](#character-messages).

### <a name="keystroke-message-flags"></a>Indicateurs de message de frappe

Le paramètre **lParam** d’un message de frappe de touche contient des informations supplémentaires sur la frappe de touche qui a généré le message. Ces informations incluent le nombre de répétitions, le code d’analyse, l’indicateur de clé étendue, le code de contexte, l’indicateur d’état de clé précédent et l’indicateur d’état de transition. L’illustration suivante montre les emplacements de ces indicateurs et valeurs dans le paramètre **lParam** .

![emplacements des indicateurs et des valeurs dans le paramètre lParam d’un message de frappe de touche](images/csinp-02.png)

Une application peut utiliser les valeurs suivantes pour manipuler les indicateurs de frappe.



| Valeur            | Description                                                                       |
|------------------|-----------------------------------------------------------------------------------|
| **KF \_ ALTDOWN**  | Manipule l’indicateur de touche ALT, qui indique si la touche ALT est enfoncée.     |
| **KF \_ DLGMODE**  | Manipule l’indicateur du mode de boîte de dialogue, qui indique si une boîte de dialogue est active. |
| **KF \_ étendu** | Manipule l’indicateur de clé étendue.                                                |
| **KF \_ MENUMODE** | Manipule l’indicateur de mode de menu, qui indique si un menu est actif.         |
| **KF \_ répéter**   | Manipule l’indicateur d’état de clé précédent.                                          |
| **KF \_**       | Manipule l’indicateur d’état de transition.                                            |

Exemple de code :

```cpp
case WM_KEYDOWN:
case WM_KEYUP:
case WM_SYSKEYDOWN:
case WM_SYSKEYUP:
{
    WORD vkCode = LOWORD(wParam);                                       // virtual-key code

    BYTE scanCode = LOBYTE(HIWORD(lParam));                             // scan code
    BOOL scanCodeE0 = (HIWORD(lParam) & KF_EXTENDED) == KF_EXTENDED;    // extended-key flag, 1 if scancode has 0xE0 prefix

    BOOL upFlag = (HIWORD(lParam) & KF_UP) == KF_UP;                    // transition-state flag, 1 on keyup
    BOOL repeatFlag = (HIWORD(lParam) & KF_REPEAT) == KF_REPEAT;        // previous key-state flag, 1 on autorepeat
    WORD repeatCount = LOWORD(lParam);                                  // repeat count, > 0 if several keydown messages was combined into one message

    BOOL altDownFlag = (HIWORD(lParam) & KF_ALTDOWN) == KF_ALTDOWN;     // ALT key was pressed

    BOOL dlgModeFlag = (HIWORD(lParam) & KF_DLGMODE) == KF_DLGMODE;     // dialog box is active
    BOOL menuModeFlag = (HIWORD(lParam) & KF_MENUMODE) == KF_MENUMODE;  // menu is active
    
    // ...
}
break;
```

### <a name="repeat-count"></a>Nombre de répétitions

Vous pouvez vérifier le nombre de répétitions pour déterminer si un message de frappe représente plusieurs séquences de touches. Le système incrémente le nombre lorsque le clavier génère des messages [**WM \_ keyverse**](wm-keydown.md) ou [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) plus rapidement qu’une application ne peut les traiter. Cela se produit souvent lorsque l’utilisateur maintient une clé suffisamment longue pour démarrer la fonctionnalité de répétition automatique du clavier. Au lieu de remplir la file d’attente des messages du système avec les messages de clé en aval résultants, le système combine les messages en un seul message de touche enfoncée et incrémente le nombre de répétitions. La libération d’une clé ne peut pas démarrer la fonctionnalité de répétition automatique. par conséquent, le nombre de répétitions pour les messages [**WM \_ KEYUP**](wm-keyup.md) et [**WM \_ SYSKEYUP**](wm-syskeyup.md) est toujours défini sur 1.

### <a name="scan-code"></a>Analyser le code

Le code d’analyse correspond à la valeur que le matériel du clavier génère lorsque l’utilisateur appuie sur une touche. Il s’agit d’une valeur dépendante de l’appareil qui identifie la touche enfoncée, par opposition au caractère représenté par la clé. En général, une application ignore les codes d’analyse. Au lieu de cela, il utilise les codes de clé virtuelle indépendants du périphérique pour interpréter les messages de séquence de touches.

### <a name="extended-key-flag"></a>Indicateur de Extended-Key

L’indicateur de clé étendue indique si le message de frappe de touche provient de l’une des touches supplémentaires du clavier amélioré. Les clés étendues sont composées des touches ALT et CTRL sur le côté droit du clavier. les touches Inser, DEL, début, fin, PAGE précédente, PAGE suivante et flèche dans les clusters à gauche du pavé numérique ; touche VERR. NUM. touche arrêt (CTRL + PAUSE); touche Impr. SCRN. et les touches de division (/) et de saisie dans le pavé numérique. L’indicateur de clé étendue est défini si la clé est une clé étendue.

S’il est spécifié, le code d’analyse était précédé d’un octet de préfixe ayant la valeur 0xE0 (224).

### <a name="context-code"></a>Code de contexte

Le code de contexte indique si la touche ALT était en aval lors de la génération du message de frappe. Le code est 1 si la touche ALT était déverrouillée et 0 si c’était le cas.

### <a name="previous-key-state-flag"></a>Indicateur de Key-State précédent

L’indicateur d’État clé précédent indique si la clé qui a généré le message de frappe était précédemment ou non. La valeur est 1 si la clé a été précédemment interrompue et 0 si la touche était précédemment. Vous pouvez utiliser cet indicateur pour identifier les messages de séquence de touches générés par la fonctionnalité de répétition automatique du clavier. Cet indicateur a la valeur 1 pour les messages de frappe de touche [**WM \_**](wm-keydown.md) et [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) générés par la fonctionnalité de répétition automatique. Elle est toujours définie sur 1 pour les messages [**WM \_ KEYUP**](wm-keyup.md) et [**WM \_ SYSKEYUP**](wm-syskeyup.md) .

### <a name="transition-state-flag"></a>Indicateur de Transition-State

L’indicateur d’état de transition indique si l’appui sur une touche ou la libération d’une clé a généré le message de frappe. Cet indicateur a toujours la valeur 0 pour les messages WM [**\_ keyverse**](wm-keydown.md) et [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) ; il a toujours la valeur 1 pour les messages [**WM \_ KEYUP**](wm-keyup.md) et [**WM \_ SYSKEYUP**](wm-syskeyup.md) .

## <a name="character-messages"></a>Messages de caractères

Les messages de séquence de touches fournissent un grand nombre d’informations sur les séquences de touches, mais ils ne fournissent pas de codes de caractères pour les séquences de touches de caractères. Pour récupérer des codes de caractères, une application doit inclure la fonction [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) dans sa boucle de messages de thread. **TranslateMessage** transmet un message [**WM \_ keyverse**](wm-keydown.md) ou [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) à la disposition du clavier. La disposition examine le code de la touche virtuelle du message et, si elle correspond à une touche de caractère, fournit l’équivalent du code de caractère (en tenant compte de l’état des touches Maj et verrouillage des MAJUSCULEs). Il génère ensuite un message de caractères qui contient le code de caractère et place le message en haut de la file d’attente de messages. L’itération suivante de la boucle de message supprime le message de la file d’attente et distribue le message à la procédure de fenêtre appropriée.

Cette section couvre les sujets suivants :

-   [Messages de caractères non-système](#nonsystem-character-messages)
-   [Messages de caractères morts](#dead-character-messages)

### <a name="nonsystem-character-messages"></a>Messages de caractères non-système

Une procédure de fenêtre peut recevoir les messages de caractères suivants : [**WM \_ char**](wm-char.md), [**WM \_ DEADCHAR**](wm-deadchar.md), [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar), [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md)et [**WM \_ UNICHAR**](wm-unichar.md). La fonction [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) génère un message **WM \_** ou **WM \_ DEADCHAR** lors du traitement d’un message [**WM \_**](wm-keydown.md) KeyOut. De même, il génère un message **WM \_ SYSCHAR** ou **WM \_ SYSDEADCHAR** lors du traitement d’un message [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) .

Une application qui traite les entrées au clavier ignore généralement tous les messages, sauf les [**\_ caractères WM**](wm-char.md) et [**WM \_ UNICHAR**](wm-unichar.md) , en passant tous les autres messages à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Notez que **WM \_ char** utilise UTF (Unicode Transformation Format), tandis que **WM \_ UNICHAR** utilise UTF-32. Le système utilise les messages [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) et [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md) pour implémenter les mnémoniques de menu.

Le paramètre **wParam** de tous les messages de caractères contient le code de caractère de la touche de caractère qui a été enfoncée. La valeur du code de caractère dépend de la classe de fenêtre de la fenêtre qui reçoit le message. Si la version Unicode de la fonction [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) a été utilisée pour inscrire la classe de fenêtre, le système fournit des caractères Unicode à toutes les fenêtres de cette classe. Dans le cas contraire, le système fournit des codes de caractères ASCII. Pour plus d’informations, consultez [Unicode et jeux de caractères](/windows/desktop/Intl/unicode-and-character-sets).

Le contenu du paramètre **lParam** d’un message de caractères est identique au contenu du paramètre **lParam** du message de clé en aval qui a été traduit pour produire le message de caractère. Pour plus d’informations, consultez [indicateurs de message de frappe](#keystroke-message-flags).

### <a name="dead-character-messages"></a>Messages Dead-Character

Certains claviers non anglais contiennent des touches de caractères qui ne sont pas censées produire des caractères. Au lieu de cela, ils sont utilisés pour ajouter un signe diacritique au caractère produit par la séquence de touches suivante. Ces clés sont appelées *clés mortes*. La touche circonflexe sur un clavier allemand est un exemple de touche morte. Pour entrer le caractère composé d’un « o » avec un accent circonflexe, un utilisateur allemand doit taper la touche circonflexe suivie de la touche « o ». La fenêtre avec le focus clavier reçoit la séquence de messages suivante :

1.  [**WM- \_ touche**](wm-keydown.md)
2.  [**\_DEADCHAR WM**](wm-deadchar.md)
3.  [**WM \_ KEYUP**](wm-keyup.md)
4.  [**WM- \_ touche**](wm-keydown.md)
5.  [**\_caractère WM**](wm-char.md)
6.  [**WM \_ KEYUP**](wm-keyup.md)

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) génère le message [**WM \_ DEADCHAR**](wm-deadchar.md) lors du traitement du [**message \_ WM**](wm-keydown.md) KeyOut à partir d’une clé morte. Bien que le paramètre *wParam* du message **WM \_ DEADCHAR** contienne le code de caractère de l’expression diacritiques pour la touche morte, une application ignore généralement le message. Au lieu de cela, il traite le message [**WM \_ char**](wm-char.md) généré par la séquence de touches suivante. Le paramètre *wParam* du message **WM \_ char** contient le code de caractère de la lettre avec le signe diacritique. Si la séquence de touches suivante génère un caractère qui ne peut pas être combiné avec un signe diacritique, le système génère deux messages **WM \_ char** . Le paramètre *wParam* de la première contient le code de caractère de l’diacritiques ; le paramètre *wParam* de la seconde contient le code de caractère de la touche de caractère suivante.

La fonction [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) génère le message [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md) lors du traitement du message [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) à partir d’une clé morte du système (une touche morte qui est enfoncée avec la touche Alt). Une application ignore généralement le message **WM \_ SYSDEADCHAR** .

## <a name="key-status"></a>État de la clé

Lors du traitement d’un message de clavier, une application peut avoir besoin de déterminer l’état d’une autre clé en plus de celle qui a généré le message en cours. Par exemple, une application de traitement de texte qui permet à l’utilisateur d’appuyer sur Maj + fin pour sélectionner un bloc de texte doit vérifier l’état de la touche Maj chaque fois qu’elle reçoit un message de frappe de la touche fin. L’application peut utiliser la fonction [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) pour déterminer l’état d’une clé virtuelle au moment de la génération du message actuel. elle peut utiliser la fonction [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate) pour récupérer l’état actuel d’une clé virtuelle.

La disposition du clavier gère une liste de noms. Le nom d’une clé qui produit un caractère unique est le même que le caractère produit par la clé. Le nom d’une touche non-caractère, tel que TAB et entrée, est stocké sous la forme d’une chaîne de caractères. Une application peut récupérer le nom de n’importe quelle clé du pilote de périphérique en appelant la fonction [**GetKeyNameText**](/windows/win32/api/winuser/nf-winuser-getkeynametexta) .

## <a name="keystroke-and-character-translations"></a>Traductions de séquences de touches et de caractères

Le système comprend plusieurs fonctions spéciales qui traduisent des codes d’analyse, des codes de caractères et des codes de touche virtuelle fournis par différents messages de frappe. Ces fonctions incluent [**MapVirtualKey**](/windows/win32/api/winuser/nf-winuser-mapvirtualkeya), [**toascii**](/windows/win32/api/winuser/nf-winuser-toascii), [**ToUnicode**](/windows/win32/api/winuser/nf-winuser-tounicode)et [**VkKeyScan**](/windows/win32/api/winuser/nf-winuser-vkkeyscana).

En outre, Microsoft Rich Edit 3,0 prend en charge l' [IME HexToUnicode](/windows/desktop/Intl/hextounicode-ime), qui permet à un utilisateur d’effectuer une conversion entre des caractères hexadécimaux et Unicode à l’aide de touches d’accès rapide. Cela signifie que lorsque Microsoft Rich Edit 3,0 est incorporé dans une application, l’application hérite des fonctionnalités de l’IME HexToUnicode.

## <a name="hot-key-support"></a>Support Hot-Key

Une *touche d’accès rapide* est une combinaison de touches qui génère un message de [**\_ raccourci WM**](wm-hotkey.md) , un message que le système place en haut de la file d’attente de messages d’un thread, en ignorant tous les messages existants dans la file d’attente. Les applications utilisent des touches d’accès rapide pour obtenir une entrée de clavier haute priorité auprès de l’utilisateur. Par exemple, en définissant une touche d’accès rapide composée de la combinaison de touches CTRL + C, une application peut permettre à l’utilisateur d’annuler une opération de longue durée.

Pour définir une touche d’accès rapide, une application appelle la fonction [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) , en spécifiant la combinaison de touches qui génère le message de [**\_ raccourci WM**](wm-hotkey.md) , le handle de la fenêtre pour recevoir le message et l’identificateur de la touche d’accès rapide. Quand l’utilisateur appuie sur la touche d’accès rapide, un message de **\_ raccourci WM** est placé dans la file d’attente de messages du thread qui a créé la fenêtre. Le paramètre *wParam* du message contient l’identificateur de la touche d’accès rapide. L’application peut définir plusieurs touches d’accès rapide pour un thread, mais chaque touche d’accès rapide du thread doit avoir un identificateur unique. Avant que l’application ne se termine, elle doit utiliser la fonction [**UnregisterHotKey**](/windows/win32/api/winuser/nf-winuser-unregisterhotkey) pour détruire la touche d’accès rapide.

Les applications peuvent utiliser un contrôle de touche d’accès rapide pour permettre à l’utilisateur de choisir facilement une touche d’accès rapide. Les contrôles de touche d’accès rapide sont généralement utilisés pour définir une touche d’accès rapide qui active une fenêtre ; ils n’utilisent pas les fonctions [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) et [**UnregisterHotKey**](/windows/win32/api/winuser/nf-winuser-unregisterhotkey) . Au lieu de cela, une application qui utilise un contrôle de touche d’accès rapide envoie généralement le message [**WM \_ SETHOTKEY**](wm-sethotkey.md) pour définir la touche d’accès rapide. Chaque fois que l’utilisateur appuie sur la touche d’accès rapide, le système envoie un message [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) en spécifiant SC \_ Hotkey. Pour plus d’informations sur les contrôles de touche d’accès rapide, consultez « Utilisation des contrôles de touche d’accès rapide » dans les [contrôles de touche d’accès rapide](../controls/hot-key-controls.md).

## <a name="keyboard-keys-for-browsing-and-other-functions"></a>Touches du clavier pour la navigation et d’autres fonctions

Windows assure la prise en charge des claviers avec des clés spéciales pour les fonctions de navigateur, les fonctions de média, le lancement d’applications et la gestion de l’alimentation. Le [**\_ APPCOMMAND WM**](wm-appcommand.md) prend en charge les touches de clavier supplémentaires. En outre, la fonction [**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85)) est modifiée pour prendre en charge les touches de clavier supplémentaires.

Il est peu probable qu’une fenêtre enfant dans une application de composant puisse implémenter directement des commandes pour ces touches de clavier supplémentaires. Ainsi, lorsque vous appuyez sur l’une de ces touches, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envoie un message [**WM \_ APPCOMMAND**](wm-appcommand.md) à une fenêtre. **DefWindowProc** propage également le message **WM \_ APPCOMMAND** à sa fenêtre parente. Cela est similaire à la façon dont les menus contextuels sont appelés avec le bouton droit de la souris, ce qui indique que **DefWindowProc** envoie un message [**WM \_ CONTEXTMENU**](/windows/desktop/menurc/wm-contextmenu) sur un clic de bouton droit et le propage à son parent. En outre, si **DefWindowProc** reçoit un message **WM \_ APPCOMMAND** pour une fenêtre de niveau supérieur, il appellera un hook de Shell avec le code **HSHELL \_ APPCOMMAND**.

Windows prend également en charge l’explorateur Microsoft IntelliMouse, qui est une souris avec cinq boutons. Les deux boutons supplémentaires prennent en charge la navigation vers l’avant et l’arrière du navigateur. Pour plus d’informations, consultez [XBUTTONs](about-mouse-input.md).

## <a name="simulating-input"></a>Simulation de l’entrée

Pour simuler une série ininterrompue d’événements d’entrée utilisateur, utilisez la fonction [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) . La fonction accepte trois paramètres. Le premier paramètre, *cInputs*, indique le nombre d’événements d’entrée qui seront simulés. Le deuxième paramètre, *rgInputs*, est un tableau de structures [**d’entrée**](/windows/win32/api/winuser/ns-winuser-input) , chacune décrivant un type d’événement d’entrée et des informations supplémentaires sur cet événement. Le dernier paramètre, *cbSize*, accepte la taille de la structure **d’entrée** , en octets.

La fonction [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) utilise l’injection d’une série d’événements d’entrée simulés dans le flux d’entrée d’un appareil. L’effet est semblable à l’appel de la fonction d’événement [**keybd \_**](/windows/win32/api/winuser/nf-winuser-keybd_event) ou de la fonction de [**souris \_**](/windows/win32/api/winuser/nf-winuser-mouse_event) à plusieurs reprises, à ceci près que le système garantit qu’aucun autre événement d’entrée ne se mélange avec les événements simulés. Lorsque l’appel est terminé, la valeur de retour indique le nombre d’événements d’entrée correctement joués. Si cette valeur est égale à zéro, l’entrée a été bloquée.

La fonction [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) ne réinitialise pas l’état actuel du clavier. Par conséquent, si des clés sont activées pour l’utilisateur lorsque vous appelez cette fonction, elles risquent d’interférer avec les événements générés par cette fonction. Si vous vous inquiétez des interférences possibles, vérifiez l’état du clavier avec la fonction [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate) et corrigez-le si nécessaire.

## <a name="languages-locales-and-keyboard-layouts"></a>Langues, paramètres régionaux et dispositions de clavier

Une *langue* est un langage naturel, tel que l’anglais, le français et le japonais. Une sous- *langue* est une variante d’un langage naturel parlée dans une région géographique spécifique, telle que les sous-langues anglaises parlées au Royaume-Uni et le États-Unis. Les applications utilisent des valeurs, appelées [identificateurs de langage](/windows/desktop/Intl/language-identifiers), pour identifier de manière unique les langues et les sous-langues.

Les applications utilisent généralement des *paramètres régionaux* pour définir le langage dans lequel l’entrée et la sortie sont traitées. La définition des paramètres régionaux pour le clavier, par exemple, affecte les valeurs de caractères générées par le clavier. La définition des paramètres régionaux pour l’affichage ou l’imprimante affecte les glyphes affichés ou imprimés. Les applications définissent les paramètres régionaux d’un clavier en chargeant et en utilisant des dispositions de clavier. Ils définissent les paramètres régionaux d’un affichage ou d’une imprimante en sélectionnant une police qui prend en charge les paramètres régionaux spécifiés.

Une disposition de clavier spécifie non seulement la position physique des touches sur le clavier, mais également les valeurs de caractère générées en appuyant sur ces touches. Chaque disposition identifie la langue d’entrée actuelle et détermine les valeurs de caractères qui sont générées par les combinaisons de clés et de clés.

Chaque disposition de clavier a un handle correspondant qui identifie la disposition et la langue. Le mot de poids faible du handle est un identificateur de langue. Le mot de poids fort est un handle d’appareil, spécifiant la disposition physique, ou est égal à zéro, ce qui indique une disposition physique par défaut. L’utilisateur peut associer n’importe quel langage d’entrée à une disposition physique. Par exemple, un utilisateur anglophone qui travaille très rarement en français peut définir la langue d’entrée du clavier sur le français sans modifier la disposition physique du clavier. Cela signifie que l’utilisateur peut entrer du texte en français à l’aide de la disposition anglaise familière.

En général, les applications ne sont pas censées manipuler directement les langues d’entrée. Au lieu de cela, l’utilisateur configure les combinaisons de langue et de disposition, puis passe de l’un à l’autre. Quand l’utilisateur clique sur un texte marqué d’une langue différente, l’application appelle la fonction [**ActivateKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout) pour activer la disposition par défaut de l’utilisateur pour cette langue. Si l’utilisateur modifie le texte dans une langue qui n’est pas dans la liste active, l’application peut appeler la fonction [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) avec la langue pour obtenir une disposition basée sur cette langue.

La fonction [**ActivateKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout) définit la langue d’entrée pour la tâche actuelle. Le paramètre *HKL* peut être soit le handle de la disposition du clavier, soit un identificateur de langue zéro étendu. Les poignées de disposition du clavier peuvent être obtenues à partir de la fonction [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) ou [**GetKeyboardLayoutList**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutlist) . Les valeurs précédentes **HKL \_ Next** et **HKL \_** peuvent également être utilisées pour sélectionner le clavier suivant ou précédent.

La fonction [**GetKeyboardLayoutName**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutnamea) récupère le nom de la disposition de clavier active pour le thread appelant. Si une application crée la disposition active à l’aide de la fonction [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) , **GetKeyboardLayoutName** récupère la même chaîne que celle utilisée pour créer la disposition. Dans le cas contraire, la chaîne est l’identificateur de langue primaire correspondant aux paramètres régionaux de la disposition active. Cela signifie que la fonction ne peut pas nécessairement faire la distinction entre différentes mises en page avec la même langue principale, de sorte que ne peut pas retourner des informations spécifiques sur la langue d’entrée. Toutefois, la fonction [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout) peut être utilisée pour déterminer la langue d’entrée.

La fonction [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) charge une disposition de clavier et met la disposition à la disposition de l’utilisateur. Les applications peuvent rendre la disposition immédiatement active pour le thread actuel à l’aide de la valeur d' **\_ activation KLF** . Une application peut utiliser la valeur de **\_ réorganisation KLF** pour réorganiser les dispositions sans spécifier également la valeur d' **\_ activation KLF** . Les applications doivent toujours utiliser la valeur de **\_ remplacement KLF \_ OK** lors du chargement des dispositions de clavier pour s’assurer que la préférence de l’utilisateur, le cas échéant, est sélectionnée.

Pour la prise en charge multilingue, la fonction [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) fournit les indicateurs **KLF \_ REPLACELANG** et **KLF \_ NOTELLSHELL** . L’indicateur **KLF \_ REPLACELANG** dirige la fonction pour remplacer une disposition de clavier existante sans modifier la langue. Toute tentative de remplacement d’une disposition existante à l’aide du même identificateur de langue mais sans spécifier **KLF \_ REPLACELANG** est une erreur. L’indicateur **KLF \_ NOTELLSHELL** empêche la fonction de notifier le shell quand une disposition de clavier est ajoutée ou remplacée. Cela est utile pour les applications qui ajoutent plusieurs dispositions dans une série consécutive d’appels. Cet indicateur doit être utilisé dans tous les appels sauf le dernier.

La fonction [**UnloadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-unloadkeyboardlayout) est limitée, car elle ne peut pas décharger la langue d’entrée par défaut du système. Cela garantit que l’utilisateur dispose toujours d’une disposition pour entrer du texte en utilisant le même jeu de caractères que celui utilisé par le shell et le système de fichiers.

 

 
