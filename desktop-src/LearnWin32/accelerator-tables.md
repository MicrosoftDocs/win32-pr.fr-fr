---
title: Tables d’accélérateurs
description: Tables d’accélérateurs
ms.assetid: 4F2CFD7C-90D3-4C3F-9A42-05B915914EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2951ee99a31a977e0909de5639fa3110cea10e0b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094449"
---
# <a name="accelerator-tables"></a>Tables d’accélérateurs

Les applications définissent souvent des raccourcis clavier, tels que CTRL + O pour la commande fichier ouvrir. Vous pouvez implémenter des raccourcis clavier en gérant des messages de [**\_ keyversion WM**](/windows/desktop/inputdev/wm-keydown) individuels, mais les tables d’accélérateurs offrent une meilleure solution :

-   Nécessite moins de codage.
-   Consolide tous vos raccourcis dans un seul fichier de données.
-   Prend en charge la localisation dans d’autres langues.
-   Permet aux raccourcis et aux commandes de menu d’utiliser la même logique d’application.

Une *table d’accélérateurs* est une ressource de données qui mappe les combinaisons de touches de clavier, telles que CTRL + O, aux commandes de l’application. Avant de voir comment utiliser une table d’accélérateurs, nous aurons besoin d’une présentation rapide des ressources. Une *ressource* est un objet blob de données qui est intégré à un fichier binaire d’application (exe ou dll). Les ressources stockent des données qui sont nécessaires à l’application, telles que des menus, des curseurs, des icônes, des images, des chaînes de texte ou des données d’application personnalisées. L’application charge les données de ressources à partir du fichier binaire au moment de l’exécution. Pour inclure des ressources dans un fichier binaire, procédez comme suit :

1.  Créez un fichier de définition de ressource (. RC). Ce fichier définit les types de ressources et leurs identificateurs. Le fichier de définition de ressource peut inclure des références à d’autres fichiers. Par exemple, une ressource icône est déclarée dans le fichier. RC, mais l’image d’icône est stockée dans un fichier séparé.
2.  utilisez le compilateur de ressources Microsoft Windows (RC) pour compiler le fichier de définition de ressource dans un fichier de ressources (. res) compilé. le compilateur RC est fourni avec Visual Studio, ainsi que le SDK Windows.
3.  Liez le fichier de ressources compilé au fichier binaire.

Ces étapes sont à peu près équivalentes au processus de compilation/liaison pour les fichiers de code. Visual Studio fournit un ensemble d’éditeurs de ressources qui facilitent la création et la modification des ressources. (Ces outils ne sont pas disponibles dans les éditions Express de Visual Studio.) Mais un fichier. RC est simplement un fichier texte et la syntaxe est documentée sur MSDN. il est donc possible de créer un fichier. RC à l’aide de n’importe quel éditeur de texte. Pour plus d’informations, consultez [à propos des fichiers de ressources](/windows/desktop/menurc/about-resource-files).

## <a name="defining-an-accelerator-table"></a>Définition d’une table d’accélérateurs

Une table d’accélérateurs est un tableau de raccourcis clavier. Chaque raccourci est défini par :

-   Identificateur numérique. Ce nombre identifie la commande d’application qui sera appelée par le raccourci.
-   Caractère ASCII ou code de touche virtuelle du raccourci.
-   Touches de modification facultatives : ALT, Maj ou CTRL.

La table d’accélérateurs elle-même a un identificateur numérique, qui identifie la table dans la liste des ressources d’application. Nous allons créer une table d’accélérateurs pour un programme de dessin simple. Ce programme aura deux modes, le mode dessin et le mode de sélection. En mode dessin, l’utilisateur peut dessiner des formes. En mode de sélection, l’utilisateur peut sélectionner des formes. Pour ce programme, nous souhaitons définir les raccourcis clavier suivants.



| Raccourci | Commande                   |
|----------|---------------------------|
| Ctrl+M   | Basculer entre les modes.     |
| F1       | Basculez en mode dessin.      |
| F2       | Basculez en mode de sélection. |



 

Tout d’abord, définissez des identificateurs numériques pour la table et pour les commandes de l’application. Ces valeurs sont arbitraires. Vous pouvez assigner des constantes symboliques pour les identificateurs en les définissant dans un fichier d’en-tête. Par exemple :


```C++
#define IDR_ACCEL1                      101
#define ID_TOGGLE_MODE                40002
#define ID_DRAW_MODE                  40003
#define ID_SELECT_MODE                40004
```



Dans cet exemple, la valeur `IDR_ACCEL1` identifie la table d’accélérateurs, et les trois constantes suivantes définissent les commandes de l’application. Par Convention, un fichier d’en-tête qui définit les constantes de ressource est souvent nommé Resource. h. La liste suivante montre le fichier de définition de ressource.


```C++
#include "resource.h"

IDR_ACCEL1 ACCELERATORS
{
    0x4D,   ID_TOGGLE_MODE, VIRTKEY, CONTROL    // ctrl-M
    0x70,   ID_DRAW_MODE, VIRTKEY               // F1
    0x71,   ID_SELECT_MODE, VIRTKEY             // F2
}
```



Les raccourcis d’accélérateur sont définis à l’intérieur des accolades. Chaque raccourci contient les entrées suivantes.

-   Code de la touche virtuelle ou caractère ASCII qui appelle le raccourci.
-   Commande de l’application. Notez que les constantes symboliques sont utilisées dans l’exemple. Le fichier de définition de ressource contient Resource. h, où ces constantes sont définies.
-   Le mot clé **VIRTKEY** signifie que la première entrée est un code de touche virtuelle. L’autre option consiste à utiliser des caractères ASCII.
-   Modificateurs facultatifs : ALT, CTRL ou Maj.

Si vous utilisez des caractères ASCII pour les raccourcis, un caractère minuscule est un raccourci différent de celui d’un caractère majuscule. (Par exemple, si vous tapez’a', vous pouvez appeler une commande différente de la saisie de’A'.) Comme cela peut entraîner une confusion pour les utilisateurs, il est généralement préférable d’utiliser des codes de touche virtuelle, plutôt que des caractères ASCII, pour les raccourcis.

## <a name="loading-the-accelerator-table"></a>Chargement de la table d’accélérateurs

La ressource de la table d’accélérateurs doit être chargée pour que le programme puisse l’utiliser. Pour charger une table d’accélérateurs, appelez la fonction [**LoadAccelerators**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) .


```C++
    HACCEL hAccel = LoadAccelerators(hInstance, MAKEINTRESOURCE(IDR_ACCEL1));
```



Appelez cette fonction avant d’entrer dans la boucle de message. Le premier paramètre est le handle du module. (Ce paramètre est passé à votre fonction [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) . Pour plus d’informations, consultez [WinMain : le point d’entrée de l’application](winmain--the-application-entry-point.md).) Le deuxième paramètre est l’identificateur de ressource. La fonction retourne un handle vers la ressource. Rappelez-vous qu’un handle est un type opaque qui fait référence à un objet géré par le système. Si la fonction échoue, elle retourne la **valeur null**.

Vous pouvez publier une table d’accélérateurs en appelant [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable). Toutefois, le système libère automatiquement la table lorsque le programme s’arrête. vous devez donc appeler cette fonction uniquement si vous remplacez une table par une autre. Un exemple intéressant de cela est illustré dans la rubrique [création d’accélérateurs modifiables](/windows/desktop/menurc/using-keyboard-accelerators)par l’utilisateur.

## <a name="translating-key-strokes-into-commands"></a>Conversion des frappes de touches en commandes

Une table d’accélérateurs fonctionne en traduisant les séquences de touches en messages de [**\_ commande WM**](/windows/desktop/menurc/wm-command) . Le paramètre *wParam* de **la \_ commande WM** contient l’identificateur numérique de la commande. Par exemple, à l’aide du tableau ci-dessus, le trait de touche CTRL + M est converti en message de **\_ commande WM** avec la valeur `ID_TOGGLE_MODE` . Pour ce faire, remplacez votre boucle de message par la suivante :


```C++
    MSG msg;
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(win.Window(), hAccel, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }
```



Ce code ajoute un appel à la fonction [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) à l’intérieur de la boucle de message. La fonction **TranslateAccelerator** examine chaque message de fenêtre, en recherchant des messages dépendants. Si l’utilisateur appuie sur l’une des combinaisons de touches listées dans la table d’accélérateurs, **TranslateAccelerator** envoie un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) à la fenêtre. La fonction envoie **la \_ commande WM** en appelant directement la procédure de fenêtre. Lorsque **TranslateAccelerator** convertit correctement un trait de touche, la fonction retourne une valeur différente de zéro, ce qui signifie que vous devez ignorer le traitement normal pour le message. Sinon, **TranslateAccelerator** retourne la valeur zéro. Dans ce cas, transmettez le message de fenêtre à [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) et [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), normalement.

Voici comment le programme de dessin peut gérer le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) :


```C++
    case WM_COMMAND:
        switch (LOWORD(wParam))
        {
        case ID_DRAW_MODE:
            SetMode(DrawMode);
            break;

        case ID_SELECT_MODE:
            SetMode(SelectMode);
            break;

        case ID_TOGGLE_MODE:
            if (mode == DrawMode)
            {
                SetMode(SelectMode);
            }
            else
            {
                SetMode(DrawMode);
            }
            break;
        }
        return 0;

```



Ce code suppose que `SetMode` est une fonction définie par l’application pour basculer entre les deux modes. Les détails de la façon dont vous géreriez chaque commande dépendent évidemment de votre programme.

## <a name="next"></a>Suivant

[Définition de l’image de curseur](setting-the-cursor-image.md)

 

 
