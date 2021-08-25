---
title: entrée au clavier (Prise en main avec Win32 et C++)
description: Entrée au clavier
ms.assetid: FC682E8B-8360-4D58-AC42-4CEFD9CB750F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3ed8ac1e8d7cd8e6ea35c9e9f58c10fd516cca010b5e5dce667817b32028c5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822349"
---
# <a name="keyboard-input-get-started-with-win32-and-c"></a>entrée au clavier (Prise en main avec Win32 et C++)

Le clavier est utilisé pour plusieurs types d’entrée distincts, notamment :

-   Entrée de caractères. Texte que l’utilisateur tape dans un document ou une zone d’édition.
-   Raccourcis clavier. Séquences de touches qui appellent des fonctions d’application ; par exemple, appuyez sur CTRL + O pour ouvrir un fichier.
-   Commandes système. Séquences de touches qui appellent des fonctions système ; par exemple, ALT + TAB pour basculer entre les fenêtres.

Lorsque vous réfléchissez à l’entrée au clavier, il est important de se souvenir qu’un trait de touche n’est pas le même qu’un caractère. Par exemple, si vous appuyez sur la touche A, vous obtenez l’un des caractères suivants.

-   a
-   A
-   á (si le clavier prend en charge la combinaison de signes diacritiques)

En outre, si la touche ALT est maintenue enfoncée, le fait d’appuyer sur une touche A produit ALT + A, que le système ne considère pas comme un caractère, mais plutôt comme une commande système.

## <a name="key-codes"></a>Codes de touche

Lorsque vous appuyez sur une touche, le matériel génère un *code d’analyse*. Les codes d’analyse varient d’un clavier à l’autre, et il existe des codes d’analyse distincts pour les événements de touche et de réduction de la clé. Vous n’aurez presque jamais à vous soucier des codes d’analyse. Le pilote de clavier traduit les codes d’analyse en *codes de clé virtuelle*. Les codes de clé virtuelle sont indépendants des appareils. Si vous appuyez sur la touche A sur n’importe quel clavier, vous générez le même code de clé virtuelle.

En général, les codes de clé virtuelle ne correspondent pas aux codes ASCII ou à toute autre norme d’encodage de caractères. Cela est évident si vous y réfléchissez, car la même clé peut générer des caractères différents (a, A, á) et certaines clés, telles que les touches de fonction, ne correspondent à aucun caractère.

Cela dit, les codes de clé virtuelle suivants sont mappés à des équivalents ASCII :

-   0 à 9 clés = ASCII « 0 » – « 9 » (0x30 – 0x39)
-   A à Z, clés = ASCII’A' – 'Z' (0x41 vers – 0x5A)

Dans certains cas, ce mappage est malheureux, car vous ne devriez jamais considérer les codes de clé virtuelle comme des caractères, pour les raisons évoquées.

Le fichier d’en-tête WinUser. h définit des constantes pour la plupart des codes de touche virtuelle. Par exemple, le code de touche virtuelle pour la touche de direction gauche est **VK \_ gauche** (0x25). Pour obtenir la liste complète des codes de touche virtuelle, consultez la section [**codes de clé virtuelle**](/windows/desktop/inputdev/virtual-key-codes). Aucune constante n’est définie pour les codes de clé virtuelle qui correspondent aux valeurs ASCII. Par exemple, le code de la touche virtuelle pour la clé A est 0x41 vers, mais il n’existe aucune constante nommée **VK \_ a**. Au lieu de cela, utilisez simplement la valeur numérique.

## <a name="key-down-and-key-up-messages"></a>Messages Key-Down et Key-Up

Lorsque vous appuyez sur une touche, la fenêtre qui a le focus clavier reçoit l’un des messages suivants.

-   [**\_SYSKEYDOWN WM**](/windows/desktop/inputdev/wm-syskeydown)
-   [**WM- \_ touche**](/windows/desktop/inputdev/wm-keydown)

Le message [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) indique une *clé système*, qui est un trait de clé qui appelle une commande système. Il existe deux types de clé système :

-   ALT + n’importe quelle touche
-   F10

La touche F10 active la barre de menus d’une fenêtre. Différentes combinaisons de touches ALT appellent des commandes système. Par exemple, ALT + TAB bascule vers une nouvelle fenêtre. En outre, si une fenêtre possède un menu, la touche ALT peut être utilisée pour activer les éléments de menu. Certaines combinaisons de touches ALT ne font rien.

Tous les autres raccourcis clavier sont considérés comme des clés qui ne sont pas des clés système et produisent le message [**WM \_**](/windows/desktop/inputdev/wm-keydown) KeyOut. Cela comprend les touches de fonction autres que F10.

Lorsque vous publiez une clé, le système envoie un message de clé correspondant :

-   [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)
-   [**\_SYSKEYUP WM**](/windows/desktop/inputdev/wm-syskeyup)

Si vous maintenez la touche enfoncée suffisamment longtemps pour démarrer la fonctionnalité répéter du clavier, le système envoie plusieurs messages de déverrouillage, suivis d’un seul message de clé.

Dans les quatre messages de clavier abordés jusqu’à présent, le paramètre *wParam* contient le code de clé virtuelle de la clé. Le paramètre *lParam* contient des informations diverses compressées dans 32 bits. En général, vous n’avez pas besoin des informations contenues dans *lParam*. Un indicateur qui peut être utile est le bit 30, l’indicateur « état de la clé précédent », qui est défini sur 1 pour les messages de déverrouillage répétés.

Comme son nom l’indique, les séquences de touches système sont principalement destinées à être utilisées par le système d’exploitation. Si vous interceptez le message [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) , appelez [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) par la suite. Dans le cas contraire, vous empêchez le système d’exploitation de gérer la commande.

## <a name="character-messages"></a>Messages de caractères

Les séquences de touches sont converties en caractères à l’aide de la fonction [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) , que nous avons constatée pour la première fois dans le [module 1](your-first-windows-program.md). Cette fonction examine les messages dépendants et les convertit en caractères. Pour chaque caractère produit, la fonction **TranslateMessage** place un message [**WM \_**](/windows/desktop/inputdev/wm-char) ou [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) dans la file d’attente de messages de la fenêtre. Le paramètre *wParam* du message contient le caractère UTF-16.

Comme vous pouvez le deviner, les messages [**WM \_ char**](/windows/desktop/inputdev/wm-char) sont générés à partir des messages [**\_ WM**](/windows/desktop/inputdev/wm-keydown) KeyOut, tandis que les messages [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) sont générés à partir des messages [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) . Par exemple, supposons que l’utilisateur appuie sur la touche Maj suivie de la touche A. En supposant une disposition de clavier standard, vous obtiendriez la séquence de messages suivante :

**WM \_ touche PG. suiv**.  
**WM \_ keyverser**: A  
**WM \_ CHAR**: 'A'  


En revanche, la combinaison ALT + P générerait :

 **WM \_ SYSKEYDOWN**: \_ menu VK  
**WM \_ SYSKEYDOWN**: 0x50  
**WM \_ SYSCHAR**: « p »  
**WM \_ SYSKEYUP**: 0x50  
**WM \_ KEYUP**: \_ menu VK  


(Le code de touche virtuelle pour la touche ALT est appelé VK \_ MENU pour des raisons historiques.)

Le message [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) indique un caractère système. Comme avec [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown), vous devez généralement transmettre ce message directement à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Dans le cas contraire, vous risquez d’interférer avec les commandes système standard. En particulier, ne traitez pas **WM \_ SYSCHAR** comme du texte que l’utilisateur a tapé.

Le message [**WM \_ char**](/windows/desktop/inputdev/wm-char) correspond à ce que vous considérez normalement comme une entrée de caractères. Le type de données pour le caractère est **WCHAR \_ t**, qui représente un caractère Unicode UTF-16. L’entrée de caractères peut inclure des caractères en dehors de la plage ASCII, en particulier avec les dispositions de clavier qui sont couramment utilisées en dehors de la États-Unis. Vous pouvez essayer différentes dispositions du clavier en installant un clavier régional, puis en utilisant la fonctionnalité du clavier visuel.

Les utilisateurs peuvent également installer un éditeur de méthode d’entrée (IME) pour entrer des scripts complexes, tels que des caractères japonais, à l’aide d’un clavier standard. Par exemple, en utilisant un IME japonais pour entrer le caractère katakana カ (Ka), vous pouvez obtenir les messages suivants :

**WM \_ Keyverse**: VK \_ PROCESSKEY (clé de processus IME)  
**WM \_ KEYUP**: 0x4B  
**WM \_ keyverse**: VK \_ PROCESSKEY  
**WM \_ KEYUP**: 0x41 vers  
**WM \_ keyverse**: VK \_ PROCESSKEY  
**WM \_ CHAR**: カ  
**WM \_ KEYUP**: \_ retour VK  


Certaines combinaisons de touches CTRL sont converties en caractères de contrôle ASCII. Par exemple, CTRL + A est converti en caractère ASCII Ctrl-A (SOH) (valeur ASCII 0x01). Pour l’entrée de texte, vous devez généralement filtrer les caractères de contrôle. Évitez également d’utiliser [**WM \_ char**](/windows/desktop/inputdev/wm-char) pour implémenter des raccourcis clavier. Au lieu de cela, utilisez des messages de [**\_ keyversion WM**](/windows/desktop/inputdev/wm-keydown) ou bien mieux, utilisez une table d’accélérateurs. Les tables d’accélérateurs sont décrites dans la rubrique suivante, [tables d’accélérateurs](accelerator-tables.md).

Le code suivant affiche les principaux messages du clavier dans le débogueur. Essayez d’utiliser différentes combinaisons de touches et consultez les messages générés.


```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    wchar_t msg[32];
    switch (uMsg)
    {
    case WM_SYSKEYDOWN:
        swprintf_s(msg, L"WM_SYSKEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSCHAR:
        swprintf_s(msg, L"WM_SYSCHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSKEYUP:
        swprintf_s(msg, L"WM_SYSKEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYDOWN:
        swprintf_s(msg, L"WM_KEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYUP:
        swprintf_s(msg, L"WM_KEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_CHAR:
        swprintf_s(msg, L"WM_CHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    /* Handle other messages (not shown) */

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



## <a name="miscellaneous-keyboard-messages"></a>Divers messages de clavier

Certains autres messages de clavier peuvent être ignorés en toute sécurité par la plupart des applications.

-   Le message [**WM \_ DEADCHAR**](/windows/desktop/inputdev/wm-deadchar) est envoyé pour une clé de combinaison, telle qu’un signe diacritique. Par exemple, sur un clavier en espagnol, si vous tapez accent (') suivi de E, vous obtenez le caractère é. Le **\_ DEADCHAR WM** est envoyé pour le caractère d’accentuation.
-   Le message [**WM \_ UNICHAR**](/windows/desktop/inputdev/wm-unichar) est obsolète. Il permet aux programmes ANSI de recevoir l’entrée de caractères Unicode.
-   Le caractère de caractère [**\_ \_ IME WM**](/windows/desktop/Intl/wm-ime-char) est envoyé lorsqu’un IME traduit une séquence de frappe en caractères. Il est envoyé en plus du message [**WM habituel \_**](/windows/desktop/inputdev/wm-char) .

## <a name="keyboard-state"></a>État du clavier

Les messages de clavier sont pilotés par les événements. Autrement dit, vous recevez un message quand un événement intéressant se produit, par exemple une pression sur une touche, et le message vous indique ce qui s’est produit. Toutefois, vous pouvez également tester l’état d’une clé à tout moment, en appelant la fonction [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) .

Par exemple, réfléchissez à la façon dont vous allez détecter la combinaison du bouton gauche de la souris et de la touche ALT. Vous pouvez suivre l’état de la touche ALT en écoutant les messages de frappe de touche et en stockant un indicateur, mais [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) vous évite les problèmes. Quand vous recevez le message [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) , il vous suffit d’appeler **GetKeyState** comme suit :


```C++
if (GetKeyState(VK_MENU) & 0x8000))
{
    // ALT key is down.
}
```



Le message [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) prend un code de touche virtuelle comme entrée et retourne un jeu d’indicateurs binaires (en réalité, il s’agit simplement de deux indicateurs). La valeur 0x8000 contient l’indicateur binaire qui teste si la touche est actuellement enfoncée.

La plupart des claviers ont deux touches ALT, gauche et droite. L’exemple précédent teste si l’un de ces éléments est enfoncé. Vous pouvez également utiliser [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) pour faire la distinction entre les instances de gauche et de droite des touches Alt, Maj ou Ctrl. Par exemple, le code suivant teste si la touche ALT droite est enfoncée.


```C++
if (GetKeyState(VK_RMENU) & 0x8000))
{
    // Right ALT key is down.
}
```



La fonction [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) est intéressante, car elle signale un État du clavier *virtuel* . Cet État virtuel est basé sur le contenu de la file d’attente de messages et est mis à jour lorsque vous supprimez des messages de la file d’attente. Au fur et à mesure que votre programme traite des messages de fenêtre, **GetKeyState** vous donne un instantané du clavier au moment où chaque message a été mis en file d’attente. Par exemple, si le dernier message de la file d’attente était [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown), **GetKeyState** signale l’état du clavier au moment où l’utilisateur clique sur le bouton de la souris.

Étant donné que [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) est basé sur la file d’attente de messages, il ignore également l’entrée au clavier qui a été envoyée à un autre programme. Si l’utilisateur bascule vers un autre programme, toute pression sur les touches qui sont envoyées à ce programme est ignorée par **GetKeyState**. Si vous souhaitez vraiment connaître l’état physique immédiat du clavier, il existe une fonction pour cela : [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate). Toutefois, pour la plupart du code d’interface utilisateur, la fonction correcte est **GetKeyState**.

## <a name="next"></a>Suivant

[Tables d’accélérateurs](accelerator-tables.md)

 

 
