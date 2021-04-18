---
description: Cette section décrit l’interface multidocument qui est une spécification qui définit une interface utilisateur pour les applications qui permettent à l’utilisateur de travailler avec plusieurs documents en même temps.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\multipledocumentinterface.htm
title: Interface multidocument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1898202aad6ec8d26f859bec2457124328c3a27b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533906"
---
# <a name="multiple-document-interface"></a>Interface multidocument

\[De nombreux utilisateurs nouveaux et intermédiaires trouvent qu’il est difficile d’apprendre à utiliser les applications MDI. Par conséquent, vous devez prendre en compte d’autres modèles pour votre interface utilisateur. Toutefois, vous pouvez utiliser MDI pour les applications qui ne tiennent pas facilement dans un modèle existant.\]

L’interface multidocument (MDI, multiple-document interface) est une spécification qui définit une interface utilisateur pour les applications qui permettent à l’utilisateur de travailler avec plusieurs documents en même temps.

### <a name="in-this-section"></a>Dans cette section



| Rubrique                                                                              | Description                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [À propos de l’interface multidocument](about-the-multiple-document-interface.md) | Décrit l’interface multidocument.<br/>                                     |
| [Utilisation de l’interface multidocument](using-the-multiple-document-interface.md) | Explique comment effectuer des tâches associées à l’interface de plusieurs documents.<br/> |
| [Référence MDI](multiple-document-interface-reference.md)                         | Contient la référence de l’API.<br/>                                                    |



 

### <a name="mdi-functions"></a>Fonctions MDI



| Nom                                                 | Description                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)           | Crée une fenêtre enfant MDI. <br/>                                                                                                                                                                                                                                                                                                                                    |
| [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca)                 | Fournit le traitement par défaut pour tous les messages de fenêtre que la procédure de fenêtre d’une fenêtre frame MDI ne traite pas. Tous les messages de fenêtre qui ne sont pas explicitement traités par la procédure de fenêtre doivent être passés à la fonction [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) , et non à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . <br/>                              |
| [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca)           | Fournit le traitement par défaut pour tout message de fenêtre que la procédure de fenêtre d’une fenêtre enfant MDI ne traite pas. Un message de fenêtre non traité par la procédure de fenêtre doit être passé à la fonction [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) , et non à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . <br/>                                             |
| [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) | Traite les séquences de touches d’accélérateur pour les commandes du menu fenêtre des fenêtres MDI enfants associées à la fenêtre du client MDI spécifiée. La fonction traduit les messages [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) et [**WM \_**](/windows/desktop/inputdev/wm-keydown) KeyOut en messages [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) et les envoie aux fenêtres enfants MDI appropriées. <br/> |



 

### <a name="mdi-messages"></a>Messages MDI



| Nom                                            | Description                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_MDIACTIVATE WM**](wm-mdiactivate.md)       | Envoyé à une fenêtre cliente MDI pour indiquer à la fenêtre cliente d’activer une autre fenêtre enfant MDI. <br/>                                                                                                                                                                                                                                                                                                                               |
| [**\_MDICASCADE WM**](wm-mdicascade.md)         | Envoyé à une fenêtre cliente MDI pour réorganiser toutes ses fenêtres enfants dans un format en cascade. <br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**\_MDICREATE WM**](wm-mdicreate.md)           | Envoyé à une fenêtre cliente MDI pour créer une fenêtre enfant MDI. <br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**\_MDIDESTROY WM**](wm-mdidestroy.md)         | Envoyé à une fenêtre cliente MDI pour fermer une fenêtre enfant MDI. <br/>                                                                                                                                                                                                                                                                                                                                                                         |
| [**\_MDIGETACTIVE WM**](wm-mdigetactive.md)     | Envoyé à une fenêtre cliente MDI pour récupérer le handle de la fenêtre enfant MDI active. <br/>                                                                                                                                                                                                                                                                                                                                                |
| [**\_MDIICONARRANGE WM**](wm-mdiiconarrange.md) | Envoyé à une fenêtre cliente MDI pour réorganiser toutes les fenêtres enfants MDI réduites. Elle n’affecte pas les fenêtres enfants qui ne sont pas réduites. <br/>                                                                                                                                                                                                                                                                                                  |
| [**\_MDIMAXIMIZE WM**](wm-mdimaximize.md)       | Envoyé à une fenêtre cliente MDI pour agrandir une fenêtre enfant MDI. Le système redimensionne la fenêtre enfant pour que sa zone cliente remplisse la fenêtre cliente. Le système place l’icône de menu fenêtre de la fenêtre enfant à la position la plus à droite de la barre de menus de la fenêtre frame et place l’icône de restauration de la fenêtre enfant à la position la plus à gauche. Le système ajoute également le texte de la barre de titre de la fenêtre enfant à celle de la fenêtre frame. <br/> |
| [**\_MDINEXT WM**](wm-mdinext.md)               | Envoyé à une fenêtre cliente MDI pour activer la fenêtre enfant suivante ou précédente. <br/>                                                                                                                                                                                                                                                                                                                                                        |
| [**\_MDIREFRESHMENU WM**](wm-mdirefreshmenu.md) | Envoyé à une fenêtre cliente MDI pour actualiser le menu fenêtre de la fenêtre frame MDI. <br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**\_MDIRESTORE WM**](wm-mdirestore.md)         | Envoyé à une fenêtre cliente MDI pour restaurer une fenêtre enfant MDI de taille agrandie ou réduite. <br/>                                                                                                                                                                                                                                                                                                                                      |
| [**\_MDISETMENU WM**](wm-mdisetmenu.md)         | Envoyé à une fenêtre cliente MDI pour remplacer le menu entier d’une fenêtre frame MDI, pour remplacer le menu fenêtre de la fenêtre frame, ou les deux. <br/>                                                                                                                                                                                                                                                                                           |
| [**\_MDITILE WM**](wm-mditile.md)               | Envoyé à une fenêtre cliente MDI pour réorganiser toutes ses fenêtres enfants MDI dans un format de mosaïque. <br/>                                                                                                                                                                                                                                                                                                                                             |



 

### <a name="mdi-structures"></a>Structures MDI



| Nom                                       | Description                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) | Contient des informations sur la classe, le titre, le propriétaire, l’emplacement et la taille d’une fenêtre enfant MDI. <br/> |



 

 

