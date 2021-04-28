---
title: Création d’une fenêtre
description: Création d’une fenêtre
ms.assetid: e036519f-26b5-436c-b909-bb280d758e81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eea5ec39187b389405d3c6d8eca475944278a3d5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103967"
---
# <a name="creating-a-window"></a>Création d’une fenêtre

## <a name="window-classes"></a>classes de fenêtre

Une *classe de fenêtre* définit un ensemble de comportements que plusieurs fenêtres peuvent avoir en commun. Par exemple, dans un groupe de boutons, chaque bouton a un comportement similaire quand l’utilisateur clique sur le bouton. Bien entendu, les boutons ne sont pas complètement identiques ; chaque bouton affiche sa propre chaîne de texte et possède ses propres coordonnées d’écran. Les données uniques pour chaque fenêtre sont appelées *données d’instance*.

Chaque fenêtre doit être associée à une classe de fenêtre, même si votre programme ne crée jamais qu’une seule instance de cette classe. Il est important de comprendre qu’une classe de fenêtre n’est pas une « classe » dans le sens C++. Au lieu de cela, il s’agit d’une structure de données utilisée en interne par le système d’exploitation. Les classes de fenêtre sont inscrites auprès du système au moment de l’exécution. Pour inscrire une nouvelle classe de fenêtre, commencez par remplir une structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) :

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;
```

Vous devez définir les membres de structure suivants :

- **lpfnWndProc** est un pointeur vers une fonction définie par l’application appelée *procédure de fenêtre* ou « procédure de fenêtre ». La procédure de fenêtre définit la plus grande partie du comportement de la fenêtre. Nous examinerons plus en détail la procédure de la fenêtre. Pour le moment, traitez simplement cela comme une référence anticipée.
- **HINSTANCE** est le handle de l’instance de l’application. Obtient cette valeur à partir du paramètre *HINSTANCE* de **wWinMain**.
- **lpszClassName** est une chaîne qui identifie la classe de fenêtre.

Comme les noms de classe sont locaux pour le processus actuel, le nom doit être unique au sein du processus. Toutefois, les contrôles Windows standard ont également des classes. Si vous utilisez l’un de ces contrôles, vous devez choisir des noms de classe qui ne sont pas en conflit avec les noms de classe de contrôle. Par exemple, la classe de fenêtre pour le contrôle Button est nommée « Button ».

La structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) a d’autres membres qui ne sont pas indiqués ici. Vous pouvez les définir sur zéro, comme indiqué dans cet exemple, ou les remplir. La documentation MSDN décrit en détail la structure.

Ensuite, transmettez l’adresse de la structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) à la fonction [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) . Cette fonction enregistre la classe de fenêtre avec le système d’exploitation.

```C++
RegisterClass(&wc);
```

## <a name="creating-the-window"></a>Création de la fenêtre

Pour créer une nouvelle instance d’une fenêtre, appelez la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) :

```C++
HWND hwnd = CreateWindowEx(
    0,                              // Optional window styles.
    CLASS_NAME,                     // Window class
    L"Learn to Program Windows",    // Window text
    WS_OVERLAPPEDWINDOW,            // Window style

    // Size and position
    CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

    NULL,       // Parent window    
    NULL,       // Menu
    hInstance,  // Instance handle
    NULL        // Additional application data
    );

if (hwnd == NULL)
{
    return 0;
}
```

Vous pouvez consulter les descriptions des paramètres détaillés sur MSDN, mais voici un récapitulatif rapide :

- Le premier paramètre vous permet de spécifier des comportements facultatifs pour la fenêtre (par exemple, des fenêtres transparentes). Définissez ce paramètre sur zéro pour les comportements par défaut.
- `CLASS_NAME` nom de la classe de fenêtre. Définit le type de fenêtre que vous êtes en train de créer.
- Le texte de la fenêtre est utilisé de différentes façons par différents types de fenêtres. Si la fenêtre a une barre de titre, le texte est affiché dans la barre de titre.
- Le style de fenêtre est un ensemble d’indicateurs qui définissent l’apparence et la convivialité d’une fenêtre. En fait, la constante **WS \_ OVERLAPPEDWINDOW** est associée à plusieurs indicateurs avec une **opération or au** niveau du bit. Ensemble, ces indicateurs donnent à la fenêtre une barre de titre, une bordure, un menu système et des boutons **réduire** et **agrandir** . Cet ensemble d’indicateurs est le style le plus courant pour une fenêtre d’application de niveau supérieur.
- Pour la position et la taille, la constante **CW \_ usedefault** signifie utiliser les valeurs par défaut.
- Le paramètre suivant définit une fenêtre parente ou une fenêtre propriétaire pour la nouvelle fenêtre. Définissez le parent si vous créez une fenêtre enfant. Pour une fenêtre de niveau supérieur, affectez-lui la valeur **null**.
- Pour une fenêtre d’application, le paramètre suivant définit le menu de la fenêtre. Cet exemple n’utilise pas de menu, donc la valeur est **null**.
- *HINSTANCE* est le descripteur d’instance, décrit précédemment. (Consultez [WinMain : le point d’entrée de l’application](winmain--the-application-entry-point.md).)
- Le dernier paramètre est un pointeur vers des données arbitraires de type **void \***. Vous pouvez utiliser cette valeur pour passer une structure de données à votre procédure de fenêtre. Nous allons vous montrer une manière possible d’utiliser ce paramètre dans la section gestion de l’état de l' [application](managing-application-state-.md).

[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) retourne un handle vers la nouvelle fenêtre, ou zéro si la fonction échoue. Pour afficher la fenêtre, c’est-à-dire rendre la fenêtre visible, transmettez le handle de fenêtre à la fonction [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) :

```C++
ShowWindow(hwnd, nCmdShow);
```

Le paramètre *HWND* est le handle de fenêtre retourné par [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Le paramètre *nCmdShow* peut être utilisé pour réduire ou agrandir une fenêtre. Le système d’exploitation transmet cette valeur au programme par le biais de la fonction **wWinMain** .

Voici le code complet pour créer la fenêtre. N’oubliez pas que `WindowProc` n’est toujours qu’une déclaration anticipée d’une fonction.

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;

RegisterClass(&wc);

// Create the window.

HWND hwnd = CreateWindowEx(
    0,                              // Optional window styles.
    CLASS_NAME,                     // Window class
    L"Learn to Program Windows",    // Window text
    WS_OVERLAPPEDWINDOW,            // Window style

    // Size and position
    CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

    NULL,       // Parent window    
    NULL,       // Menu
    hInstance,  // Instance handle
    NULL        // Additional application data
    );

if (hwnd == NULL)
{
    return 0;
}

ShowWindow(hwnd, nCmdShow);
```

Félicitations, vous avez créé une fenêtre ! Pour le moment, la fenêtre ne contient pas de contenu ou n’interagit pas avec l’utilisateur. Dans une application GUI réelle, la fenêtre répond aux événements de l’utilisateur et du système d’exploitation. La section suivante décrit comment les messages de fenêtre fournissent ce type d’interactivité.

### <a name="next"></a>Suivant

[Messages de fenêtre](window-messages.md)
