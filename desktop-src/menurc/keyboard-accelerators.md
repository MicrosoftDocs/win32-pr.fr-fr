---
title: Raccourcis clavier
description: Cette section traite des accélérateurs de clavier. Une touche d’accès rapide est une séquence de touches ou une combinaison de touches qui génère un message de commande pour une application.
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\keyboardaccelerators.htm
keywords:
- entrée d’utilisateur, accélérateurs de clavier
- capture de l’entrée utilisateur, accélérateurs de clavier
- accélérateurs de clavier
- accélérateurs
- Message WM_COMMAND
- WM_SYS message de commande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df67f4879edc2e0e81a8715155bf2edfac05f1e5ce9d3557f9b051ae682a6afa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734467"
---
# <a name="keyboard-accelerators"></a>Raccourcis clavier

Une touche d’accès *rapide* (ou simplement un accélérateur) est une séquence de touches ou une combinaison de touches qui génère une [**\_ commande WM**](wm-command.md) ou un message [**WM \_ SYSCOMMAND**](wm-syscommand.md) pour une application.

### <a name="in-this-section"></a>Dans cette section



| Nom                                                                 | Description                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------|
| [À propos des accélérateurs clavier](about-keyboard-accelerators.md)       | Décrit les accélérateurs de clavier.<br/>                                |
| [Utilisation des accélérateurs clavier](using-keyboard-accelerators.md)       | Décrit les tâches associées aux accélérateurs de clavier.<br/> |
| [Informations de référence sur les raccourcis clavier](keyboard-accelerator-reference.md) | Contient la référence de l’API.<br/>                                     |



 

### <a name="keyboard-accelerator-functions"></a>Fonctions d’accélérateur du clavier



| Nom                                                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CopyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-copyacceleratortablea)       | Copie la table d’accélérateurs spécifiée. Cette fonction permet d’obtenir les données de la table d’accélérateurs qui correspondent à un handle de table d’accélérateurs, ou de déterminer la taille des données de la table d’accélérateurs. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)   | Crée une table d’accélérateurs. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) | Détruit une table d’accélérateurs.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa)               | Charge la table d’accélérateurs spécifiée. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)       | Traite les touches accélérateur pour les commandes de menu. La fonction convertit un message [**WM \_ keyverse**](/windows/desktop/inputdev/wm-keydown) ou [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) en [**une \_ commande WM**](wm-command.md) ou un message [**WM \_ SYSCOMMAND**](wm-syscommand.md) (s’il existe une entrée pour la clé dans la table d’accélérateurs spécifiée), puis envoie la **\_ commande WM** ou le message **WM \_ SYSCOMMAND** directement à la procédure de fenêtre spécifiée. [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) n’est pas retourné tant que la procédure de fenêtre n’a pas traité le message. <br/> |



 

### <a name="keyboard-accelerator-messages"></a>Messages d’accélérateur du clavier



| Nom                                          | Description                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CHANGEUISTATE WM**](wm-changeuistate.md) | Envoyé pour indiquer que l’état de l’interface utilisateur doit être modifié.<br/>                                                                                                                                                                                                                                                  |
| [**\_INITMENU WM**](wm-initmenu.md)           | Envoyé lorsqu’un menu va devenir actif. Il se produit lorsque l’utilisateur clique sur un élément dans la barre de menus ou appuie sur une touche de menu. Cela permet à l’application de modifier le menu avant qu’il ne soit affiché. <br/> Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . <br/> |
| [**\_QUERYUISTATE WM**](wm-queryuistate.md)   | Envoyé pour récupérer l’état d’interface utilisateur d’une fenêtre.<br/>                                                                                                                                                                                                                                                            |
| [**\_UPDATEUISTATE WM**](wm-updateuistate.md) | Envoyé pour modifier l’état de l’interface utilisateur pour la fenêtre spécifiée et toutes ses fenêtres enfants.<br/>                                                                                                                                                                                                                        |



 

### <a name="keyboard-accelerator-notifications"></a>Notifications de l’accélérateur clavier



| Nom                                          | Description                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_INITMENUPOPUP WM**](wm-initmenupopup.md) | Envoyé lorsqu’un menu déroulant ou un sous-menu est sur le paragraphe actif. Cela permet à une application de modifier le menu avant qu’il ne soit affiché, sans modifier le menu entier. <br/>                                                                                                                                              |
| [**\_MENUCHAR WM**](wm-menuchar.md)           | Envoyé lorsqu’un menu est actif et que l’utilisateur appuie sur une touche qui ne correspond à aucun mnémonique ou touche d’accès rapide. Ce message est envoyé à la fenêtre qui possède le menu. <br/>                                                                                                                                             |
| [**\_MENUSELECT WM**](wm-menuselect.md)       | Envoyé à la fenêtre propriétaire d’un menu lorsque l’utilisateur sélectionne un élément de menu. <br/>                                                                                                                                                                                                                                                      |
| [**\_SYSCHAR WM**](wm-syschar.md)             | Publié dans la fenêtre qui a le focus clavier lorsqu’un message [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) est traduit par la fonction [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) . Elle spécifie le code de caractère d’une touche de caractère système, c’est-à-dire une touche de caractère qui est enfoncée pendant que la touche ALT est enfoncée. <br/> |
| [**\_SYSCOMMAND WM**](wm-syscommand.md)       | Une fenêtre reçoit ce message lorsque l’utilisateur choisit une commande dans le menu **fenêtre** ou lorsque l’utilisateur choisit le bouton Agrandir, le bouton réduire, le bouton restaurer ou le bouton Fermer.<br/>                                                                                                                                |



 

### <a name="keyboard-accelerator-structures"></a>Structures d’accélérateurs clavier



| Nom                   | Description                                                          |
|------------------------|----------------------------------------------------------------------|
| [**Voice**](/windows/win32/api/winuser/ns-winuser-accel) | Définit une touche d’accès rapide utilisée dans une table d’accélérateurs. <br/> |



 

 

