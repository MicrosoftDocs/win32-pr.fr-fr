---
description: L’aide en ligne peut se présenter sous différentes formes, des informations conceptuelles détaillées aux définitions rapides. Cette rubrique contient les sections suivantes.
title: Gestion de l’aide en ligne
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2a3f6034-6ba6-4204-a2e1-59995fbf40fe
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f1c125df135068c2eee37cb33a8a9d2b281b1f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991572"
---
# <a name="handling-online-help"></a>Gestion de l’aide en ligne

L’aide en ligne peut se présenter sous différentes formes, des informations conceptuelles détaillées aux définitions rapides. Cette rubrique contient les sections suivantes.

-   [À propos de l’aide](#about-help)
    -   [Demandes d’aide](#help-requests)
    -   [Affichage de l’aide et aide de Windows](#help-display-and-windows-help)
-   [Utilisation de l’aide](#using-help)
    -   [Fournir de l’aide dans une boîte de dialogue](#providing-help-in-a-dialog-box)
    -   [Définition de l’apparence d’une fenêtre d’aide secondaire](#setting-the-appearance-of-a-secondary-help-window)

## <a name="about-help"></a>À propos de l’aide

Un élément important d’une application conviviale est facilement disponible dans l’aide en ligne. Windows fournit des fonctions et des messages qui, lorsqu’ils sont utilisés conjointement avec l’application d’aide Windows, facilitent l’implémentation de l’aide en ligne dans votre application. Cette vue d’ensemble décrit les éléments de Windows qui prennent en charge l’aide en ligne. Il décrit comment utiliser ces éléments pour offrir aux utilisateurs un moyen de demander de l’aide, et il explique comment utiliser l’application d’aide Windows pour afficher de l’aide.

### <a name="help-requests"></a>Demandes d’aide

La plupart des applications basées sur Windows fournissent des informations d’aide en ligne sous différentes formes, à partir d’une aide conceptuelle qui explique l’objectif des fonctionnalités d’une application à l’aide contextuelle qui fournit des définitions rapides d’éléments individuels dans l’interface utilisateur de l’application. Vous utilisez des fonctions et des messages pour fournir aux utilisateurs plusieurs moyens de demander l’accès à ces informations. Les sections suivantes décrivent ces demandes d’aide.

### <a name="help-menu"></a>Menu aide

La plupart des applications fournissent un accès utilisateur aux informations d’aide en incluant un menu **aide** dans la fenêtre principale. Lorsque l’utilisateur sélectionne un élément dans un menu **aide** , la procédure de fenêtre correspondante reçoit un message de [**\_ commande WM**](../menurc/wm-command.md) qui identifie l’élément sélectionné. L’application répond en affichant les informations d’aide appropriées, telles qu’une liste de rubriques d’aide, un index ou une introduction à l’application.

### <a name="help-from-the-keyboard"></a>Aide à partir du clavier

Windows permet à l’utilisateur d’accéder à des informations d’aide à partir du clavier en avertissant l’application chaque fois que l’utilisateur appuie sur la touche F1. Le système envoie un message d' [**\_ aide WM**](wm-help.md) à la fenêtre qui avait le focus clavier lorsque l’utilisateur a appuyé sur la touche. Si la fenêtre est une fenêtre enfant (par exemple, un contrôle dans une boîte de dialogue), la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) passe le message à la fenêtre parente. Si un menu est actif lorsque la touche F1 est enfoncée, le système envoie le message à la fenêtre associée au menu. L’application répond en affichant des informations d’aide associées à la fenêtre, au contrôle ou au menu qui a le focus ou qui est actif. Par exemple, si l’utilisateur sélectionne un contrôle dans une boîte de dialogue et appuie sur la touche F1, l’application affiche des informations d’aide pour ce contrôle.

Le paramètre *lParam* de [**l' \_ aide WM**](wm-help.md) est un pointeur vers une structure [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) qui contient des informations détaillées sur l’élément pour lequel l’aide est demandée. Vous utilisez ces informations pour déterminer la rubrique d’aide à afficher. La structure **HELPINFO** comprend également les coordonnées du curseur de la souris au moment où l’utilisateur a appuyé sur la touche. Vous pouvez utiliser ces informations pour fournir de l’aide en fonction de l’emplacement du curseur de la souris.

### <a name="help-from-the-mouse"></a>Aide à partir de la souris

Windows permet à l’utilisateur d’accéder à des informations d’aide à partir de la souris en avertissant l’application chaque fois que l’utilisateur clique sur le bouton droit de la souris ou clique sur une fenêtre, un contrôle ou un menu après avoir cliqué sur le bouton de question ( ?). L’application répond en affichant des informations d’aide associées à la fenêtre, au contrôle ou au menu donné.

Le système envoie un message [**WM \_ CONTEXTMENU**](../menurc/wm-contextmenu.md) lorsque l’utilisateur clique avec le bouton droit de la souris. La fenêtre sur laquelle l’utilisateur a cliqué reçoit le message. Si la fenêtre est une fenêtre enfant, telle qu’un contrôle, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) passe le message à la fenêtre parente. Le message **WM \_ CONTEXTMENU** spécifie les coordonnées du curseur de la souris. La coordonnée x se trouve dans le mot de poids faible du paramètre *lParam* , et la coordonnée y est dans le mot de poids fort. Si l’utilisateur clique sur un contrôle, le paramètre *wParam* est le handle du contrôle qui a reçu le clic.

Le système envoie un [**message \_ d’aide WM**](wm-help.md) quand l’utilisateur clique sur un élément d’une fenêtre après avoir cliqué sur le bouton de question ( ?) qui apparaît dans la barre de titre de la fenêtre. Vous pouvez ajouter un bouton de question à une barre de titre en spécifiant le style **WS \_ ex \_ CONTEXTHELP** dans la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) lors de la création de la fenêtre. Le paramètre *lParam* de **l' \_ aide WM** est un pointeur vers une structure [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) qui contient des informations détaillées sur l’élément pour lequel l’aide est demandée, y compris les coordonnées du curseur de la souris au moment où l’utilisateur clique sur le bouton de la souris.

Le bouton de question est recommandé pour une utilisation dans les boîtes de dialogue uniquement. Auparavant, les applications fournissaient un accès utilisateur aux informations d’aide sur une boîte de dialogue en fournissant un bouton **aide** dans la boîte de dialogue. Cette méthode n’est plus recommandée. Utilisez le bouton de question à la place.

### <a name="help-display-and-windows-help"></a>Affichage de l’aide et aide de Windows

Une fois qu’une application reçoit une demande d’aide, elle doit afficher les informations d’aide appropriées. Étant donné que l’application d’aide Windows fournit une interface utilisateur cohérente, il est recommandé que les applications utilisent l’aide de Windows plutôt que d’autres méthodes. Pour demander à l’aide de Windows d’afficher des informations d’aide, une application utilise la fonction [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) , en spécifiant des détails tels que les informations à afficher et la forme de la fenêtre dans laquelle l’afficher. Les sections suivantes expliquent comment utiliser **WinHelp** pour afficher des informations d’aide.

### <a name="help-files"></a>fichiers d'aide

Pour afficher les informations d’aide, vous devez spécifier un fichier d’aide lors de l’appel de la fonction [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) . Le fichier d’aide doit avoir le format de fichier d’aide Windows (. hlp) et une ou plusieurs rubriques. Chaque rubrique est une unité d’information distincte, telle qu’une description conceptuelle, un ensemble d’instructions, une image, une définition de Glossaire, et ainsi de suite. Les rubriques doivent être identifiées de manière unique afin que l’aide de Windows puisse les localiser chaque fois qu’elles sont demandées. En interne, l’aide de Windows utilise des identificateurs de rubrique pour localiser les rubriques, mais les applications utilisent souvent des identificateurs de contexte (valeurs entières uniques) pour spécifier les rubriques à afficher. L’auteur du fichier d’aide doit mapper explicitement les identificateurs de contexte aux identificateurs de rubrique dans la \[ \] section de mappage du fichier projet utilisé pour générer le fichier d’aide.

Lorsque vous spécifiez un fichier d’aide mais que vous ne spécifiez pas de chemin d’accès, [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) recherche le fichier d’aide dans le répertoire d’aide ou dans un répertoire spécifié par la variable d’environnement PATH. En outre, **WinHelp** peut trouver un fichier d’aide dont le nom est indiqué dans l’emplacement de Registre suivant :

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Help
```

Pour tirer parti du Registre, vous devez créer un nom de valeur qui porte le même nom que votre fichier d’aide. La valeur assignée à ce nom doit être le répertoire où se trouve le fichier d’aide.

Si [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) ne trouve pas le fichier d’aide donné, il affiche une boîte de dialogue qui permet à l’utilisateur de spécifier l’emplacement du fichier d’aide. Étant donné que **WinHelp** enregistre les informations d’emplacement dans le registre, il ne redemande pas l’emplacement du même fichier d’aide.

Pour plus d’informations sur la création et la création d’un fichier d’aide, consultez la documentation fournie avec vos outils de développement.

### <a name="starting-windows-help"></a>Démarrage de l’aide Windows

L’exemple suivant utilise la fonction [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) pour démarrer l’application d’aide Windows et ouvrir le fichier d’aide dans son contenu.


```
HWND hwnd;     // main window handle 
BOOL bResult   // for checking Boolean function result 

bResult = WinHelp(hWnd, "WINNT.HLP", HELP_CONTENTS, 0L);
```



L’exemple suivant ouvre le fichier d’aide de l’utilisateur, recherche la rubrique associée à une chaîne de mot clé dans le fichier, puis affiche la rubrique.


```
HWND hwnd;     // main window handle 
BOOL bResult   // for checking Boolean function result 

bResult = WinHelp(hWnd, "WINNT.HLP", HELP_KEY, (DWORD) "finding topics");
```



### <a name="help-topics-dialog-box"></a>Rubriques d’aide (boîte de dialogue)

Vous pouvez afficher la boîte de dialogue **rubriques d’aide** en appelant la fonction [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) avec la commande de **\_ recherche** de l’aide. La boîte de dialogue **rubriques d’aide** permet à l’utilisateur de sélectionner les rubriques à afficher en affichant les titres des rubriques, les mots clés associés aux rubriques ou les mots et expressions figurant dans les rubriques. En général, les applications affichent cette boîte de dialogue lorsque l’utilisateur choisit une commande, telle que rubriques d’aide, dans le menu aide. Une application peut également afficher cette boîte de dialogue si l’utilisateur appuie sur la touche quand aucune fenêtre, contrôle ou menu spécifique dans l’application n’a le focus ou est actif.

Dans le passé, les applications utilisaient **le \_ Sommaire** de l’aide et les commandes **d' \_ index** avec la fonction [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) pour afficher la rubrique contenu et l’index du mot clé du fichier d’aide. Ces commandes ne sont plus recommandées. Utilisez la commande de **\_ recherche** de l’aide à la place.

### <a name="information-topics"></a>Rubriques d’informations

Vous pouvez afficher une rubrique spécifique en appelant la fonction [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) avec la commande de contexte d’aide \_ et en spécifiant l’identificateur de contexte pour la rubrique. Les applications utilisent généralement la \_ commande de contexte d’aide en réponse aux demandes de l’utilisateur pour les rubriques qui contiennent des informations conceptuelles ou une aide procédurale plutôt que des informations sur un contrôle ou un menu spécifique. Dans ce cas, l’utilisateur peut continuer à parcourir le fichier d’aide à la recherche d’informations connexes avant de revenir à l’application.

La \_ commande de contexte d’aide appelle une instance normale de l’aide de Windows, ce qui permet à l’utilisateur de rechercher d’autres rubriques dans le fichier d’aide. Il affiche généralement la fenêtre d’aide principale, qui comprend une barre de titre, un menu système, des boutons réduire et agrandir, un menu principal, une barre de navigation facultative, une bordure de redimensionnement et une zone cliente. Le texte de la rubrique sélectionnée apparaît dans la zone cliente et l’utilisateur peut naviguer dans le fichier d’aide à l’aide de liens hypertexte ou de boutons de navigation dans la fenêtre principale. L’instance normale de l’aide de Windows peut également être utilisée pour afficher l’aide dans une ou plusieurs fenêtres secondaires et non dans la fenêtre principale.

### <a name="pop-up-topics"></a>Rubriques indépendantes

Vous pouvez afficher une rubrique contextuelle qui contient des informations sur un contrôle ou un menu spécifique en appelant la fonction [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) avec l’aide \_ WM \_ help ou Help \_ CONTEXTMENU. Ces commandes affichent une rubrique dans une fenêtre indépendante près du contrôle ou du menu correspondant. Pour permettre à l’utilisateur de retourner immédiatement à l’application, la fenêtre indépendante est détruite dès que l’utilisateur appuie sur une touche ou clique avec le bouton gauche de la souris.

Vous utilisez la \_ commande help WM \_ Help lors du traitement des messages [**\_ d’aide WM**](wm-help.md) pour les fenêtres de contrôle. Étant donné que la plupart des contrôles transmettent le message d' **\_ aide WM** à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , la procédure de boîte de dialogue correspondante (ou la procédure de fenêtre parente) traite ce message. Au lieu de fournir un identificateur de contexte spécifique, la procédure de la boîte de dialogue doit passer un tableau de paires d’identificateurs de contrôle et de contexte à [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) avec le descripteur de contrôle spécifié dans le membre **hItemHandle** de la structure [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) passé avec le message **\_ d’aide WM** . La fonction détermine l’identificateur du contrôle pour lequel le message **\_ d’aide WM** a été généré et utilise l’identificateur de contexte correspondant pour afficher la rubrique appropriée.

Vous utilisez la \_ commande help ContextMenu lors du traitement des messages [**WM \_ CONTEXTMENU**](../menurc/wm-contextmenu.md) . Étant donné que la plupart des contrôles transmettent le message **WM \_ CONTEXTMENU** à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , la procédure de boîte de dialogue correspondante (ou la procédure de fenêtre parente) traite ce message. La procédure spécifie un tableau de paires d’identificateurs de contexte et de contrôle ; elle spécifie également le handle dans le paramètre *wParam* lors de l’appel de [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) afin que la fonction puisse sélectionner l’identificateur de contexte approprié dans le tableau et afficher la rubrique appropriée. Contrairement à la \_ commande help de l’aide WM \_ , Help \_ CONTEXTMENU affiche d’abord une commande **qu’est-ce que c’est ?** dans un menu. Si l’utilisateur choisit la commande, **WinHelp** affiche la rubrique. Dans le cas contraire, la demande est annulée.

Vous pouvez également afficher des rubriques contextuelles à l’aide de la \_ commande help CONTEXTPOPUP et en spécifiant un identificateur de contexte de la rubrique. Cette commande est similaire à la commande de contexte d’aide \_ , mais elle appelle l’instance contextuelle de l’aide de Windows utilisée par l’aide de \_ WM \_ et Help \_ CONTEXTMENU. Les applications peuvent utiliser cette commande en réponse aux messages d' [**\_ aide WM**](wm-help.md) pour afficher de l’aide sur les menus et les fenêtres qui ne sont pas des contrôles dans une boîte de dialogue. Pour utiliser cette commande de manière plus efficace, l’application doit assigner des identificateurs de contexte à ces menus et fenêtres.

Vous pouvez assigner un identificateur de contexte à n’importe quelle fenêtre ou menu dans l’application. Lorsqu’un [**message \_ d’aide WM**](wm-help.md) est généré, le système comprend l’identificateur de contexte dans la structure [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) qui est passé à la fenêtre parente dans le message **\_ d’aide WM** . La fenêtre parente peut ensuite passer l’identificateur de contexte à [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) pour afficher la rubrique d’aide demandée.

Vous utilisez la fonction [**SetWindowContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-setwindowcontexthelpid) pour assigner un identificateur de contexte à une fenêtre ou à un contrôle et la fonction [**SetMenuContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-setmenucontexthelpid) pour assigner un identificateur de contexte à un menu. Vous pouvez récupérer l’identificateur de contexte d’une fenêtre ou d’un menu à l’aide de la fonction [**GetWindowContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-getwindowcontexthelpid) ou [**GetMenuContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-getmenucontexthelpid) .

### <a name="keyword-searches"></a>Recherches par mot clé

Vous pouvez permettre à l’utilisateur de rechercher et d’afficher des rubriques en affectant des mots clés aux rubriques du fichier d’aide. Un mot clé est simplement une chaîne associée à une ou plusieurs rubriques. L’aide de Windows recueille tous les mots clés dans un fichier d’aide, les place dans un tableau et les affiche dans la liste index de la boîte de dialogue **rubriques d’aide** . Quand l’utilisateur sélectionne un mot clé, l’aide de Windows affiche la rubrique d’aide associée ou, si plusieurs rubriques sont associées au mot clé, affiche une liste des rubriques à partir desquelles l’utilisateur peut choisir.

Dans une application, vous pouvez utiliser la \_ \_ commande help PARTIALKEY ou Help \_ relations avec la fonction [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) pour rechercher et afficher les rubriques d’aide en fonction de mots clés entiers ou partiels. Vous spécifiez la commande, la chaîne de mot clé, le fichier d’aide et le handle de la fenêtre propriétaire. Dans tous les cas, si une correspondance unique est trouvée, **WinHelp** affiche la rubrique correspondante. Si plusieurs correspondances sont trouvées, la fonction affiche la boîte de dialogue rubriques trouvées et l’utilisateur peut choisir la rubrique à afficher. Si aucune correspondance n’est trouvée, **WinHelp** affiche la liste d’index (pour la clé d’aide \_ et l’aide \_ PARTIALKEY) ou affiche un message d’erreur (pour obtenir de l’aide \_ relations).

Votre application peut rechercher plusieurs mots clés dans un seul appel à [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) en séparant les mots clés par des points-virgules. (La recherche de plusieurs mots clés n’est pas prise en charge pour les fichiers d’aide créés pour Windows version 3. *x*) il peut également rechercher des mots clés dans plusieurs fichiers d’aide si le fichier d’aide spécifié possède un fichier Contents (. CNT) qui contient les commandes : index ou : Link. Avec la \_ commande clé d’aide, **WinHelp** recherche les mots clés dans tous les fichiers spécifiés par ces commandes. Avec les \_ commandes Help relations et Help \_ PARTIALKEY, la fonction recherche tous les fichiers, à l’exception de ceux spécifiés par : les commandes Link.

Par défaut, l’aide de Windows reconnaît uniquement le mot clé table identifié par le caractère de note de bas de page K dans le fichier source d’aide. Vous pouvez demander à l’aide de Windows de créer des tables de mots clés supplémentaires en ajoutant un caractère de note de bas de page, avec la définition du mot clé, dans le fichier source d’aide. (Toutefois, le caractère de note de bas de page A est réservé.) Vous devez définir des tables de mots clés supplémentaires à l’aide des instructions relations dans la \[ \] section Options du fichier projet lors de la génération du fichier d’aide.

Une application peut utiliser la \_ commande help SETINDEX avec la fonction [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) pour demander à l’aide de Windows d’afficher une table de mots clés autre que K dans sa liste d’index. Pour demander à l’aide de Windows de rechercher un mot clé dans une autre table de mots clés, une application peut utiliser la \_ commande help relations. Vous spécifiez le mot clé et la table des mots clés dans une structure [**MULTIKEYHELP**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa) , que vous transmettez à **WinHelp**.

Quand [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) affiche une rubrique, il l’affiche dans la fenêtre spécifiée par la note de bas de page « > » pour la rubrique, dans la fenêtre spécifiée par la commande : base dans le fichier de contenu, ou dans la fenêtre principale. Si la fenêtre principale est déjà ouverte dans un autre fichier d’aide lorsque vous appelez **WinHelp**, la fonction masque la fenêtre principale lors de la recherche. Dans ce cas, l’annulation de la boîte de dialogue **rubriques trouvées** et **rubriques d’aide** ferme la fenêtre principale.

### <a name="secondary-help-windows"></a>Fenêtres d’aide secondaires

La fenêtre principale de l’application d’aide Windows est appelée fenêtre principale. L’aide de Windows peut également afficher les rubriques d’aide dans une fenêtre secondaire. Contrairement à la fenêtre d’aide principale, une fenêtre secondaire ne contient pas de barre de menus. Vous pouvez inclure une barre de navigation dans une fenêtre secondaire, et vous pouvez ajouter des boutons à la barre. Vous pouvez également choisir de faire en sorte que l’aide de Windows ajuste automatiquement la hauteur de la fenêtre secondaire pour s’adapter à la rubrique.

Vous devez définir des fenêtres secondaires dans \[ la \] section Windows de votre fichier de projet d’aide, en fournissant le nom et, éventuellement, la taille initiale et la position de chaque fenêtre. Vous pouvez demander à l’application d’aide Windows d’afficher une rubrique dans une fenêtre secondaire en ajoutant un chevron (>) et le nom que vous avez défini pour la fenêtre secondaire au nom du fichier d’aide. La chaîne résultante est ensuite transmise à la fonction [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) .

Une application peut modifier la taille et la position d’une fenêtre principale ou secondaire en spécifiant l’adresse d’une structure [**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) et la \_ commande help SETWINPOS dans un appel à [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa). **HELPWININFO** spécifie le nom de la fenêtre et sa nouvelle taille et position.

### <a name="training-card-help"></a>Aide sur la carte de formation

À l’aide de la carte d’apprentissage, une application peut afficher une séquence d’instructions pour guider l’utilisateur à travers les étapes d’une tâche. Une carte de formation se compose généralement d’un texte expliquant une étape particulière et des boutons associés à des macros TCard, qui permettent à l’utilisateur d’indiquer à l’application ce qu’il doit faire ensuite. Les cartes de formation ne peuvent être affichées que dans des fenêtres secondaires et ne doivent pas contenir de liens hypertexte vers d’autres rubriques du fichier d’aide.

Une application démarre l’instance de la carte de formation de l’aide Windows en appelant la fonction [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) et en spécifiant la \_ commande help TCARD en combinaison avec une autre commande, telle que le contexte d’aide \_ . Par la suite, quand l’utilisateur clique sur un bouton dans la carte de formation, clique sur une zone réactive assignée à la macro TCard ou ferme la carte de formation, Windows Help notifie l’application en lui envoyant un message [**WM \_ TCard**](wm-tcard.md) . Le paramètre *wParam* identifie le bouton ou l’action de l’utilisateur, et le paramètre *lParam* contient des données supplémentaires, dont la signification dépend de la valeur de *wParam*.

### <a name="canceling-help"></a>Annulation de l’aide

L’aide de Windows requiert une application pour annuler explicitement l’aide afin qu’elle puisse libérer toutes les ressources utilisées pour effectuer le suivi de l’application et de ses fichiers d’aide. L’application peut le faire à tout moment en appelant la fonction [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) et en spécifiant la \_ commande help Quit. Notez que cela n’est pas vrai pour l’instance contextuelle de l’aide de Windows. Une application ne doit pas essayer de fermer une instance contextuelle.

Si une application a effectué des appels à [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), elle doit annuler l’aide avant de fermer sa fenêtre principale (par exemple, en réponse au \_ message WM Destroy dans la procédure de fenêtre principale). Une application doit appeler **WinHelp** une seule fois pour annuler l’aide, quel que soit le nombre de fichiers d’aide ouverts. L’aide de Windows reste en cours d’exécution jusqu’à ce que toutes les applications ou dll aient annulé l’aide.

Pour fermer l’instance de la carte de formation de l’aide de Windows, vous devez spécifier à la fois l’aide \_ TCARD et l’aide \_ pour quitter les commandes lors de l’appel de [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa). Une application n’a pas besoin d’annuler l’instance de la carte de formation de l’aide de Windows si l’utilisateur l’annule en premier. L’aide de Windows avertit une application lorsque l’utilisateur annule l’instance de la carte de formation en envoyant le message [**WM \_ TCARD**](wm-tcard.md) avec le paramètre *wParam* défini sur IDCLOSE.

## <a name="using-help"></a>Utilisation de l'aide

Cette section montre comment fournir une aide contextuelle pour une boîte de dialogue et comment définir l’apparence d’une fenêtre d’aide secondaire.

-   [Fournir de l’aide dans une boîte de dialogue](#providing-help-in-a-dialog-box)
-   [Définition de l’apparence d’une fenêtre d’aide secondaire](#setting-the-appearance-of-a-secondary-help-window)

### <a name="providing-help-in-a-dialog-box"></a>Fournir de l’aide dans une boîte de dialogue

Pour fournir une aide contextuelle dans une boîte de dialogue, vous devez créer un tableau constitué de paires de valeurs **DWORD** . La première valeur de chaque paire est l’identificateur d’un contrôle dans la boîte de dialogue, tandis que la seconde est l’identificateur de contexte de la rubrique d’aide pour le contrôle. Le tableau doit contenir une paire d’identificateurs pour chaque contrôle de la boîte de dialogue.

La procédure de la boîte de dialogue doit traiter l' [**\_ aide WM**](wm-help.md) et les messages [**WM \_ CONTEXTMENU**](../menurc/wm-contextmenu.md) . La procédure de boîte de dialogue reçoit l' **\_ aide de WM** quand l’utilisateur appuie sur la touche et **WM \_ CONTEXTMENU** quand l’utilisateur clique avec le bouton droit de la souris.

Le paramètre *lParam* de [**l' \_ aide WM**](wm-help.md) contient l’adresse d’une structure [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) . Le membre **hItemHandle** de cette structure identifie le contrôle pour lequel l’utilisateur a demandé de l’aide. Vous devez transmettre ce handle à la fonction [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) avec la commande help \_ WM \_ Help, le nom de votre fichier d’aide et un pointeur vers le tableau d’identificateurs. La fonction **WinHelp** recherche l’identificateur de contrôle du contrôle spécifié dans le tableau, puis récupère l’identificateur de contexte d’aide correspondant. Ensuite, la fonction passe l’identificateur de contexte d’aide à l’aide de Windows, qui recherche la rubrique correspondante et l’affiche dans une fenêtre indépendante. Si le contrôle a un identificateur de-1, le système recherche le contrôle suivant qui est un taquet de tabulation, puis utilise son identificateur pour Rechercher l’identificateur de contexte d’aide. Pour cette raison, il est important de placer le texte statique avant les contrôles dans un fichier de ressources.

Lors de l’appel de la fonction [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) , le traitement de [**WM \_ CONTEXTMENU**](../menurc/wm-contextmenu.md) est semblable au traitement de l' [**\_ aide WM**](wm-help.md) avec ces deux exceptions :

-   Vous transmettez le paramètre *wParam* à partir de [**WM \_ CONTEXTMENU**](../menurc/wm-contextmenu.md), qui est le handle du contrôle qui a envoyé le message.
-   Vous spécifiez la commande **Help \_ CONTEXTMENU** au lieu de **Help \_ WM \_ Help**.

La commande **Help \_ CONTEXTMENU** permet à l’aide de Windows d’afficher un menu avant d’afficher la rubrique d’aide. Le menu est défini par le système. Elle permet à l’utilisateur d’afficher de l’aide pour le contrôle ou d’afficher la boîte de dialogue **rubriques d’aide** .

L’exemple suivant montre comment implémenter l’aide contextuelle dans une boîte de dialogue.


```
LRESULT CALLBACK EditDlgProc(HWND hwndDlg, UINT uMsg, 
                             WPARAM wParam, LPARAM lParam) 
{ 
    // Create an array of control identifiers and context identifiers. 
    static DWORD aIds[ ] = 
    { 
        ID_SAVE,   IDH_SAVE, 
        ID_DELETE, IDH_DELETE, 
        ID_COPY,   IDH_COPY, 
        ID_PASTE,  IDH_PASTE, 
        0,0 
    }; 

    switch (uMsg) 
    { 
        case WM_HELP: 
            WinHelp(((LPHELPINFO)lParam)->hItemHandle, "helpfile.hlp", 
                    HELP_WM_HELP, (DWORD)(LPSTR)aIds); 
            break; 

        case WM_CONTEXTMENU: 
            WinHelp((HWND)wParam, "helpfile.hlp", HELP_CONTEXTMENU, 
                    (DWORD)(LPVOID)aIds); 
            break; 
        
        // Process other messages here. 
    } 
    return FALSE; 
}
```



### <a name="setting-the-appearance-of-a-secondary-help-window"></a>Définition de l’apparence d’une fenêtre d’aide secondaire

Une application peut définir la taille, la position et l’état d’affichage d’une fenêtre d’aide secondaire en passant la \_ commande help SETWINPOS et l’adresse d’une structure [**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) à la fonction [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) . Les membres de **HELPWININFO** spécifient le nom de la fenêtre à modifier et la nouvelle taille, la position et l’état de l’affichage de la fenêtre.

L’exemple suivant définit l’apparence d’une fenêtre secondaire nommée « WND \_ menu ». Le nom doit être défini dans la \[ \] section Windows du fichier projet d’aide.


```
BOOL DoWindowSize(VOID) 
{ 
    HANDLE hhwi; 
    LPHELPWININFO lphwi; 
    WORD wSize; 
    char *szWndName = "wnd_menu"; 
    size_t NameLength;      // Does not include the terminating null character
    HRESULT hr
    BOOL retval;

    hr = StringCbLengthA(szWndName, STRSAFE_MAX_CCH, &NameLength);
    
    if (SUCCEEDED(hr))
    {
        // Add 1 to account for the name string's terminating null character.
        NameLength++;
        
        // The HELPWININFO structure contains a minimal TCHAR array of size [2] 
        // that is used for the window name. Since sizeof(HELPWININFO) 
        // includes those two TCHARS, they must be subtracted from the 
        // total when adding the actual string length to calculate the  
        // size of the structure. 
        wSize = sizeof(HELPWININFO) - 2 + NameLength; 
    }
    else
        // Something's amiss with the string.
        return FALSE;
        
    hhwi  = GlobalAlloc(GHND, wSize); 
    lphwi = (LPHELPWININFO)GlobalLock(hhwi); 

    lphwi->wStructSize = wSize; 
    lphwi->x    = 256;      // horizontal position 
    lphwi->y    = 256;      // vertical position 
    lphwi->dx   = 767;      // width 
    lphwi->dy   = 512;      // height 
    lphwi->wMax = SW_SHOW;  // show the window 
    
    // secondary window
    hr = StringCbCopyA(lphwi->rgchMember, sizeof(lphwi->rgchMember), szWndName);
    
    if (SUCCEEDED(hr))
    {
        WinHelp(hwnd, "myhelp.hlp", HELP_SETWINPOS, (DWORD)lphwi); 
     
        GlobalUnlock(hhwi); 
        GlobalFree(hhwi); 

        return TRUE; 
    }
    else
        // There was a problem copying the window name.
        return FALSE;
}
```



 

 
