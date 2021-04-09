---
title: À propos des accélérateurs clavier
description: Cette rubrique traite des accélérateurs de clavier.
ms.assetid: cbf7619d-289d-40c9-9a06-6ce47026d43f
keywords:
- Interface utilisateur Windows, entrée utilisateur
- Interface utilisateur Windows, accélérateurs clavier
- entrée d’utilisateur, accélérateurs de clavier
- capture de l’entrée utilisateur, accélérateurs de clavier
- accélérateurs de clavier
- accélérateurs
- Message WM_COMMAND
- WM_SYS message de commande
- tables d’accélérateurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be9c89301f58d7d76b5d9b28dd6835850c0674db
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940873"
---
# <a name="about-keyboard-accelerators"></a>À propos des accélérateurs clavier

Les accélérateurs sont étroitement liés aux menus, tous deux fournissant à l’utilisateur un accès au jeu de commandes d’une application. En règle générale, les utilisateurs s’appuient sur les menus d’une application pour connaître le jeu de commandes, puis passer à l’utilisation des accélérateurs à mesure qu’ils sont plus performants de l’application. Les accélérateurs offrent un accès plus rapide et plus direct aux commandes que les menus. Au minimum, une application doit fournir des accélérateurs pour les commandes les plus couramment utilisées. Bien que les accélérateurs génèrent généralement des commandes qui existent en tant qu’éléments de menu, ils peuvent également générer des commandes qui n’ont pas d’éléments de menu équivalents.

Cette section couvre les rubriques suivantes :

-   [Tables d’accélérateurs](#accelerator-tables)
-   [Création d’une table d’accélérateurs](#accelerator-table-creation)
-   [Attributions de touches d’accès rapide](#accelerator-keystroke-assignments)
-   [Accélérateurs et menus](#accelerators-and-menus)
-   [État de l’interface utilisateur](#ui-state)

## <a name="accelerator-tables"></a>Tables d’accélérateurs

Une table d’accélérateurs se compose d’un tableau de structures d' [**accélération**](/windows/win32/api/winuser/ns-winuser-accel) , chacune définissant un accélérateur individuel. Chaque structure d' **accélération** comprend les informations suivantes :

-   Combinaison de touches de l’accélérateur.
-   Identificateur de l’accélérateur.
-   Différents indicateurs. Cela comprend une qui spécifie si le système doit fournir des commentaires visuels en mettant en surbrillance l’élément de menu correspondant, le cas échéant, lorsque l’accélérateur est utilisé.

Pour traiter les séquences de touches d’accélérateur pour un thread spécifié, le développeur doit appeler la fonction [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) dans la boucle de message associée à la file d’attente de messages du thread. La fonction **TranslateAccelerator** surveille l’entrée au clavier dans la file d’attente de messages, en vérifiant les combinaisons de touches qui correspondent à une entrée dans la table d’accélérateurs. Lorsque **TranslateAccelerator** trouve une correspondance, il convertit l’entrée au clavier (autrement dit, les messages [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) et [**WM \_ keyverse**](/windows/desktop/inputdev/wm-keydown) ) en une [**\_ commande WM**](wm-command.md) ou un message [**WM \_ SYSCOMMAND**](wm-syscommand.md) , puis envoie le message à la procédure de fenêtre de la fenêtre spécifiée. L’illustration suivante montre le mode de traitement des accélérateurs.

![modèle de traitement des raccourcis clavier](images/cskac-01.png)

Le message de [**\_ commande WM**](wm-command.md) comprend l’identificateur de l’accélérateur qui a provoqué la génération du message par [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) . La procédure de fenêtre examine l’identificateur pour déterminer la source du message, puis traite le message en conséquence.

Les tables d’accélérateurs existent à deux niveaux différents. Le système gère une table d’accélérateurs unique à l’ensemble du système qui s’applique à toutes les applications. Une application ne peut pas modifier la table d’accélérateurs système. Pour obtenir une description des accélérateurs fournis par la table d’accélérateurs système, consultez [affectations de touches](#accelerator-keystroke-assignments)d’accès rapide.

Le système gère également les tables d’accélérateurs pour chaque application. Une application peut définir n’importe quel nombre de tables d’accélérateurs à utiliser avec ses propres fenêtres. Un handle 32 bits unique (**HACCEL**) identifie chaque table. Toutefois, une seule table d’accélérateurs peut être active à la fois pour un thread spécifié. Le descripteur de la table d’accélérateurs transmis à la fonction [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) détermine quelle table d’accélérateurs est active pour un thread. La table active Accelerator peut être modifiée à tout moment en passant un autre descripteur de table d’accélérateurs à **TranslateAccelerator**.

## <a name="accelerator-table-creation"></a>Création de Accelerator-Table

Plusieurs étapes sont nécessaires pour créer une table d’accélérateurs pour une application. Tout d’abord, un compilateur de ressources est utilisé pour créer des ressources de table d’accélérateurs et les ajouter au fichier exécutable de l’application. Au moment de l’exécution, la fonction [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) est utilisée pour charger la table d’accélérateurs en mémoire et récupérer le descripteur de la table d’accélérateurs. Ce descripteur est passé à la fonction [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) pour activer la table d’accélérateurs.

Une table d’accélérateurs peut également être créée pour une application au moment de l’exécution en passant un tableau de structures d' [**accélération**](/windows/win32/api/winuser/ns-winuser-accel) à la fonction [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) . Cette méthode prend en charge les accélérateurs définis par l’utilisateur dans l’application. À l’instar de la fonction [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) , **CreateAcceleratorTable** retourne un handle de table d’accélérateurs qui peut être passé à [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) pour activer la table d’accélérateurs.

Le système détruit automatiquement les tables d’accélérateurs chargées par [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) ou créées par [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea). Toutefois, une application peut libérer des ressources pendant qu’elle s’exécute en détruisant les tables d’accélérateurs qui ne sont plus nécessaires en appelant la fonction [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) .

Une table d’accélérateurs existante peut être copiée et modifiée. La table d’accélérateurs existante est copiée à l’aide de la fonction [**CopyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-copyacceleratortablea) . Une fois la copie modifiée, un handle vers la nouvelle table d’accélérateurs est récupéré en appelant [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea). Enfin, le descripteur est passé à [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) pour activer la nouvelle table.

## <a name="accelerator-keystroke-assignments"></a>Attributions de touches d’accès rapide

Un code de caractère ASCII ou une clé virtuelle peut être utilisé pour définir l’accélérateur. Un code de caractère ASCII rend l’accélérateur sensible à la casse. Par conséquent, l’utilisation du caractère ASCII « C » définit l’accélérateur comme ALT + C au lieu de ALT + c. Toutefois, les accélérateurs sensibles à la casse peuvent être déroutants à utiliser. Par exemple, l’accélérateur ALT + C sera généré si la touche VERR. MAJ est enfoncée ou si la touche Maj est enfoncée, mais pas si les deux sont en baisse.

En règle générale, les accélérateurs n’ont pas besoin d’être sensibles à la casse, si bien que la plupart des applications utilisent des codes de clé virtuelle pour les accélérateurs plutôt que des codes de caractères ASCII.

Évitez les accélérateurs qui sont en conflit avec les mnémoniques de menu d’une application, car l’accélérateur remplace le mnémonique, qui peut dérouter l’utilisateur. Pour plus d’informations sur les mnémoniques de menu, consultez [menus](menus.md).

Si une application définit un accélérateur qui est également défini dans la table d’accélérateurs système, l’accélérateur défini par l’application remplace l’accélérateur système, mais uniquement dans le contexte de l’application. Évitez toutefois cette pratique, car elle empêche l’accélérateur système d’effectuer son rôle standard dans l’interface utilisateur. Les accélérateurs à l’ensemble du système sont décrits dans la liste suivante :



|                  |                                                                                                       |
|------------------|-------------------------------------------------------------------------------------------------------|
| ALT+ÉCHAP          | Bascule vers l’application suivante.                                                                     |
| ALT+F4           | Ferme une application ou une fenêtre.                                                                    |
| Alt+Trait d'union       | Ouvre le menu **fenêtre** pour une fenêtre de document.                                                      |
| ALT + IMPR. ÉCRAN | Copie une image dans la fenêtre active dans le presse-papiers.                                              |
| ALT + BARRE D’ESPACE     | Ouvre le menu **fenêtre** de la fenêtre principale de l’application.                                          |
| ALT+TAB          | Bascule vers l’application suivante.                                                                     |
| CTRL+ECHAP         | Bascule vers le menu **Démarrer** .                                                                       |
| Ctrl+F4          | Ferme le groupe actif ou la fenêtre de document.                                                           |
| F1               | Démarre le fichier d’aide de l’application, s’il en existe un.                                                    |
| ÉCRAN D’IMPRESSION     | Copie une image sur l’écran dans le presse-papiers.                                                     |
| MAJ + ALT + TAB    | Bascule vers l’application précédente. L’utilisateur doit appuyer sur ALT + MAJ et le maintenir enfoncé tout en appuyant sur la touche TAB. |



 

## <a name="accelerators-and-menus"></a>Accélérateurs et menus

L’utilisation d’un accélérateur revient à choisir un élément de menu : les deux actions entraînent l’envoi par le système d’une [**\_ commande WM**](wm-command.md) ou d’un message [**WM \_ SYSCOMMAND**](wm-syscommand.md) à la procédure de fenêtre correspondante. Le message de **\_ commande WM** comprend un identificateur que la procédure de fenêtre examine pour déterminer la source du message. Si un accélérateur a généré le message de **\_ commande WM** , l’identificateur est celui de l’accélérateur. De même, si un élément de menu a généré le message de **\_ commande WM** , l’identificateur est celui de l’élément de menu. Étant donné qu’un accélérateur fournit un raccourci pour choisir une commande dans un menu, une application affecte généralement le même identificateur à l’accélérateur et à l’élément de menu correspondant.

Une application traite un message [**de \_ commande**](wm-command.md) d’accélérateur WM exactement de la même façon que le message **de \_ commande WM** de l’élément de menu correspondant. Toutefois, le message de **\_ commande WM** contient un indicateur qui spécifie si le message provient d’un accélérateur ou d’un élément de menu, au cas où les accélérateurs doivent être traités différemment de leurs éléments de menu correspondants. Le message [**WM \_ SYSCOMMAND**](wm-syscommand.md) ne contient pas cet indicateur.

L’identificateur détermine si un accélérateur génère une [**\_ commande WM**](wm-command.md) ou un message [**WM \_ SYSCOMMAND**](wm-syscommand.md) . Si l’identificateur a la même valeur qu’un élément de menu dans le menu système, l’accélérateur génère un message **WM \_ SYSCOMMAND** . Dans le cas contraire, l’accélérateur génère un message de **\_ commande WM** .

Si un accélérateur a le même identificateur qu’un élément de menu et que l’élément de menu est grisé ou désactivé, l’accélérateur est désactivé et ne génère pas [**de \_ commande WM**](wm-command.md) ou de message [**WM \_ SYSCOMMAND**](wm-syscommand.md) . En outre, un accélérateur ne génère pas de message de commande si la fenêtre correspondante est réduite.

Lorsque l’utilisateur utilise un accélérateur qui correspond à un élément de menu, la procédure de fenêtre reçoit les messages [**WM \_ INITMENU**](wm-initmenu.md) et [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) comme si l’utilisateur avait sélectionné l’élément de menu. Pour plus d’informations sur le traitement de ces messages, consultez [menus](menus.md).

Un accélérateur qui correspond à un élément de menu doit être inclus dans le texte de l’élément de menu.

## <a name="ui-state"></a>État de l’interface utilisateur

Windows permet aux applications de masquer ou d’afficher diverses fonctionnalités dans son interface utilisateur. Ces paramètres sont appelés état de l’interface utilisateur. L’état de l’interface utilisateur comprend les paramètres suivants :

-   indicateurs de focus (tels que les rectangles de focus sur les boutons)
-   accélérateurs de clavier (indiqués par des traits de soulignement dans les étiquettes de contrôle)

Une fenêtre peut envoyer des messages pour demander une modification de l’état de l’interface utilisateur, peut interroger l’état de l’interface utilisateur ou appliquer un certain État à ses fenêtres enfants. Ces messages sont les suivants.



| Message                                       | Description                                |
|-----------------------------------------------|--------------------------------------------|
| [**\_CHANGEUISTATE WM**](wm-changeuistate.md) | Indique que l’état de l’interface utilisateur doit changer. |
| [**\_QUERYUISTATE WM**](wm-queryuistate.md)   | Récupère l’état d’interface utilisateur d’une fenêtre.       |
| [**\_UPDATEUISTATE WM**](wm-updateuistate.md) | Modifie l’état de l’interface utilisateur.                      |



 

Par défaut, toutes les fenêtres enfants d’une fenêtre de niveau supérieur sont créées avec le même état d’interface utilisateur que leur parent.

Le système gère l’état de l’interface utilisateur pour les contrôles dans les boîtes de dialogue. Au moment de la création de la boîte de dialogue, le système initialise l’état de l’interface utilisateur en conséquence. Tous les contrôles enfants héritent de cet État. Une fois la boîte de dialogue créée, le système surveille les séquences de touches de l’utilisateur. Si les paramètres d’état de l’interface utilisateur sont masqués et que l’utilisateur navigue à l’aide du clavier, le système met à jour l’état de l’interface utilisateur. Par exemple, si l’utilisateur appuie sur la touche Tab pour déplacer le focus vers le contrôle suivant, le système appelle [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) pour afficher les indicateurs de focus. Si l’utilisateur appuie sur la touche Alt, le système appelle **WM \_ CHANGEUISTATE** pour rendre les accélérateurs de clavier visibles.

Si un contrôle prend en charge la navigation entre les éléments d’interface utilisateur qu’il contient, il peut mettre à jour son propre état d’interface utilisateur. Le contrôle peut appeler [**WM \_ QUERYUISTATE**](wm-queryuistate.md) pour récupérer et mettre en cache l’état initial de l’interface utilisateur. Chaque fois que le contrôle reçoit un message [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) , il peut mettre à jour son état d’interface utilisateur et envoyer un message [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) à son parent. Chaque fenêtre continue à envoyer le message à son parent jusqu’à ce qu’il atteigne la fenêtre de niveau supérieur. La fenêtre de niveau supérieur envoie le message **WM \_ UPDATEUISTATE** aux fenêtres dans l’arborescence de la fenêtre. Si une fenêtre ne passe pas sur le message **WM \_ CHANGEUISTATE** , elle n’atteint pas la fenêtre de niveau supérieur et l’état de l’interface utilisateur n’est pas mis à jour.

 

 