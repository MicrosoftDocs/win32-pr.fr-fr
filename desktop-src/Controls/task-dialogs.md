---
title: Boîte de dialogue de tâches
description: Cette section contient des informations sur les éléments de programmation utilisés avec une boîte de dialogue de tâche. Une boîte de dialogue de tâche est semblable à, alors qu’elle est bien plus flexible qu’une simple boîte de message.
ms.assetid: vs|controls|~\controls\taskdialogs\taskdialogs.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6797314b75fff46ddf8a4f64638fefb5ea0181d2353bd1a1d3caa57325d28e7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168549"
---
# <a name="task-dialog"></a>Boîte de dialogue de tâches

Cette section contient des informations sur les éléments de programmation utilisés avec une boîte de dialogue de tâche. Une *boîte de dialogue de tâche* est semblable à, alors qu’elle est bien plus flexible qu’une simple boîte de message.

### <a name="overviews"></a>Vues d'ensemble



| Rubrique                                           | Contenu                                            |
|-------------------------------------------------|-----------------------------------------------------|
| [À propos des boîtes de dialogue de tâche](task-dialogs-overview.md) | Décrit les éléments d’une boîte de dialogue de tâche.<br/> |



 

### <a name="functions"></a>Fonctions



| Rubrique                                                  | Contenu                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog)                       | Crée, affiche et exécute une boîte de dialogue de tâche. La boîte de dialogue tâche contient le texte et le titre du message défini par l’application, les icônes et toute combinaison de boutons de commande prédéfinis. Cette fonction ne prend pas en charge l’inscription d’une fonction de rappel pour recevoir des notifications.<br/>                                                                                                                |
| [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) | Fonction définie par l’application utilisée avec la fonction [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . Elle reçoit des messages de la boîte de dialogue de tâches lorsque différents événements se produisent.<br/> Le type **PFTASKDIALOGCALLBACK** définit un pointeur vers cette fonction de rappel. [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) est un espace réservé pour le nom de la fonction définie par l’application.<br/> |
| [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)       | Crée, affiche et exécute une boîte de dialogue de tâche. La boîte de dialogue tâche contient des icônes définies par l’application, des messages, un titre, une case à cocher de vérification, des liens de commande, des boutons de commande et des cases d’option. Cette fonction peut inscrire une fonction de rappel pour recevoir des messages de notification.<br/>                                                                                                               |



 

### <a name="messages"></a>Messages



| Rubrique                                                                                           | Contenu                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_bouton de clic TDM \_**](tdm-click-button.md)                                                  | Simule l’action d’un clic sur un bouton dans une boîte de dialogue de tâche.<br/>                                                                                                                                  |
| [**case d' \_ option de clic TDM \_ \_**](tdm-click-radio-button.md)                                     | Simule l’action d’un clic sur une case d’option dans une boîte de dialogue de tâche.<br/>                                                                                                                            |
| [**\_vérification de clic TDM \_**](tdm-click-verification.md)                                      | Simule l’action d’une case à cocher de vérification cliquer dans une boîte de dialogue de tâche.<br/>                                                                                                                   |
| [**\_bouton d’activation TDM \_**](tdm-enable-button.md)                                                | Active ou désactive un bouton de commande dans une boîte de dialogue de tâche.<br/>                                                                                                                                       |
| [**case \_ d' \_ option Activer TDM \_**](tdm-enable-radio-button.md)                                   | Active ou désactive une case d’option dans une boîte de dialogue de tâche.<br/>                                                                                                                                      |
| [**\_page de navigation TDM \_**](tdm-navigate-page.md)                                                | Recrée une boîte de dialogue de tâches avec le nouveau contenu, en simulant la fonctionnalité d’un Assistant multipage.<br/>                                                                                           |
| [**\_ \_ \_ \_ \_ État requis de l’élévation de bouton de l’ensemble TDM**](tdm-set-button-elevation-required-state.md) | Spécifie si un lien de commande ou un bouton de boîte de dialogue de tâche donné doit avoir une icône de protection de contrôle de compte d’utilisateur (UAC). autrement dit, si l’action appelée par le bouton requiert une élévation. <br/> |
| [**texte de l' \_ élément de jeu TDM \_ \_**](tdm-set-element-text.md)                                         | Met à jour un élément de texte dans une boîte de dialogue de tâche.<br/>                                                                                                                                                  |
| [**\_barre de \_ progression du texte défilant de l’ensemble TDM \_ \_**](tdm-set-marquee-progress-bar.md)                        | Indique si la barre de progression hébergée doit être affichée en mode palissade.<br/>                                                                                                            |
| [**\_ \_ \_ texte défilant barre de progression TDM Set \_**](tdm-set-progress-bar-marquee.md)                        | Démarre et arrête l’affichage du texte défilant de la barre de progression et définit la vitesse du texte défilant.<br/>                                                                                              |
| [**POS de la barre de progression de l' \_ ensemble TDM \_ \_ \_**](tdm-set-progress-bar-pos.md)                                | Définit la position actuelle d’une barre de progression.<br/>                                                                                                                                             |
| [**plage de la \_ \_ barre de progression définie \_ par TDM \_**](tdm-set-progress-bar-range.md)                            | Définit les valeurs minimale et maximale de la barre de progression hébergée.<br/>                                                                                                                          |
| [**État de la barre de progression de l' \_ ensemble TDM \_ \_ \_**](tdm-set-progress-bar-state.md)                            | Définit l’état actuel de la barre de progression.<br/>                                                                                                                                               |
| [**texte de l' \_ élément de mise à jour TDM \_ \_**](tdm-update-element-text.md)                                   | Met à jour un élément de texte dans une boîte de dialogue de tâche. <br/>                                                                                                                                                 |
| [**\_icône de mise à jour TDM \_**](tdm-update-icon.md)                                                    | Actualise l’icône d’une boîte de dialogue de tâche. <br/>                                                                                                                                                     |



 

### <a name="notifications"></a>Notifications



| Rubrique                                                           | Contenu                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_clic sur le bouton TDN \_](tdn-button-clicked.md)                  | Envoyé par une boîte de dialogue de tâche lorsque l’utilisateur sélectionne un bouton ou un lien de commande dans la boîte de dialogue de tâche. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .<br/>                                                                                                                                                                                                   |
| [TDN \_ créé](tdn-created.md)                                 | Envoyé par une boîte de dialogue de tâche après la création de la boîte de dialogue de tâche et avant son affichage. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . <br/>                                                                                                                                                                                                  |
| [TDN \_ détruit](tdn-destroyed.md)                             | Envoyé par une boîte de dialogue de tâche lorsqu’elle est détruite et que son handle de fenêtre n’est plus valide. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .<br/>                                                                                                                                                                                                       |
| [\_boîte de dialogue TDN \_ construite](tdn-dialog-constructed.md)          | Envoyé par une boîte de dialogue de tâche après la création de la boîte de dialogue de tâche et avant son affichage. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . <br/>                                                                                                                                                                                                  |
| [\_ \_ clic sur le bouton TDN Expander \_](tdn-expando-button-clicked.md) | Envoyé par une boîte de dialogue de tâche lorsque l’utilisateur clique sur le bouton développé de la boîte de dialogue de tâche. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .<br/>                                                                                                                                                                                                            |
| [aide de TDN \_](tdn-help.md)                                       | Envoyé par une boîte de dialogue de tâche quand l’utilisateur appuie sur la touche F1 du clavier pendant que la boîte de dialogue de tâche a le focus. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .<br/>                                                                                                                                                                                            |
| [\_clic sur le lien hypertexte TDN \_](tdn-hyperlink-clicked.md)            | Envoyé par une boîte de dialogue de tâche quand l’utilisateur clique sur un lien hypertexte dans le contenu de la boîte de dialogue de tâche. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . <br/>                                                                                                                                                                                                        |
| [TDN \_ parcouru](tdn-navigated.md)                             | Envoyé par une boîte de dialogue de tâche lorsqu’une navigation s’est produite. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . <br/>                                                                                                                                                                                                                                     |
| [\_ \_ clic sur le bouton radio TDN \_](tdn-radio-button-clicked.md)     | Envoyé par une boîte de dialogue de tâche lorsque l’utilisateur sélectionne un bouton ou un lien de commande dans la boîte de dialogue de tâche. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . <br/>                                                                                                                                                                                                  |
| [\_minuteur TDN](tdn-timer.md)                                     | Envoyé par une boîte de dialogue de tâche environ toutes les 200 millisecondes. Ce code de notification est envoyé lorsque l' \_ indicateur de minuterie de rappel TDF \_ a été défini dans le membre **dwFlags** de la structure [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) qui a été passée à la fonction [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode **TaskDialogIndirect** .<br/> |
| [vérification de la TDN sur laquelle l' \_ \_ utilisateur a cliqué](tdn-verification-clicked.md)      | Envoyé par la boîte de dialogue de tâche lorsque l’utilisateur clique sur la case à cocher vérification de la boîte de dialogue des tâches. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .<br/>                                                                                                                                                                                                       |



 

### <a name="structures"></a>Structures



| Rubrique                                           | Contenu                                                                                                                                                   |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_bouton TASKDIALOG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialog_button) | Contient des informations utilisées pour afficher un bouton dans une boîte de dialogue de tâche. La structure [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilise cette structure.<br/> |
| [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)    | Contient des informations utilisées pour afficher une boîte de dialogue de tâche. La fonction [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) utilise cette structure.<br/>          |



 

 

