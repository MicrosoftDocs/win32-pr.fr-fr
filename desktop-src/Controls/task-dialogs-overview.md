---
title: À propos des boîtes de dialogue de tâche
description: Une boîte de dialogue de tâche est une boîte de dialogue qui peut être utilisée pour afficher des informations et recevoir une entrée simple de l’utilisateur.
ms.assetid: vs|controls|~\controls\toolbar\taskdialogsoverview.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eb5cafa452a4ed653c404d053e888c6de644236
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939803"
---
# <a name="about-task-dialogs"></a>À propos des boîtes de dialogue de tâche

Une boîte de dialogue de tâche est une boîte de dialogue qui peut être utilisée pour afficher des informations et recevoir une entrée simple de l’utilisateur. Comme une boîte de message, elle est mise en forme par le système d’exploitation en fonction des paramètres que vous définissez. Toutefois, une boîte de dialogue de tâche comporte beaucoup plus de fonctionnalités qu’une boîte de message.

> [!Note]  
> Les boîtes de dialogue de tâches requièrent le modèle STA (Single-Threaded Apartment).

 

## <a name="parts-of-a-task-dialog"></a>Parties d’une boîte de dialogue de tâches

Une boîte de dialogue de tâche est constituée de plusieurs éléments, dont la plupart sont facultatifs. L’illustration suivante montre les différentes parties d’une boîte de dialogue de tâche.

![capture d’écran d’une fenêtre montrant différents boutons, y compris un à côté du texte de contrôle réduit](images/taskdialog.jpg)

Dans l’illustration suivante, l’utilisateur a cliqué sur le bouton à côté du texte de contrôle réduit, ce qui provoque l’affichage d’un texte de remplacement à cet endroit et dans le pied de page.

![capture d’écran de la fenêtre précédente, mais avec deux lignes de texte de contrôle développé](images/taskdialogexpand.jpg)

Les illustrations montrent les éléments suivants :



| Partie                   | Description                                                                                                                                                                                                                                                                                                                                                                          | Membre TASKDIALOGCONFIG                                    |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| Titre de la fenêtre           | Légende de la fenêtre.                                                                                                                                                                                                                                                                                                                                                               | **pszWindowTitle**                                         |
| Icône principale              | Grande icône qui signifie l’objectif de la boîte de dialogue de tâche.                                                                                                                                                                                                                                                                                                                          | **hMainIcon** ou **pszMainIcon**                           |
| Instruction principale       | Texte principal.                                                                                                                                                                                                                                                                                                                                                                      | **pszMainInstruction**                                     |
| Content                | Texte supplémentaire.                                                                                                                                                                                                                                                                                                                                                                          | **pszContent**                                             |
| Barre de progression           | Barre animée qui affiche la progression d’une tâche.                                                                                                                                                                                                                                                                                                                                | **dwFlags**                                                |
| Cases d’option          | Options définies par l’application pour l’utilisateur.                                                                                                                                                                                                                                                                                                                                            | **pRadioButtons**                                          |
| Bouton personnalisé          | Bouton qui ne fait pas partie des boutons courants. Il peut s’agir d’un bouton normal ou, comme indiqué dans l’illustration, d’un lien de commande comportant jusqu’à deux lignes de texte.                                                                                                                                                                                                                    | **pButtons**                                               |
| Bouton Développer/réduire | Bouton qui peut être utilisé pour basculer entre le texte de contrôle réduit défini par l’application (tel que « afficher plus de détails ») et le texte de contrôle développé, qui peut se trouver sur deux lignes ou plus. Lorsque le texte du contrôle est développé, le texte supplémentaire dans **pszExpandedInformation** est également affiché, soit après le texte du contenu, soit (comme indiqué dans la deuxième illustration) dans le pied de page. | **pszCollapsedControlText** et **pszExpandedControlText** |
| Case à cocher vérification | Une case à cocher, accompagnée d’un texte défini par l’application, pour des choix simples tels que « ne plus afficher cette boîte de dialogue ».                                                                                                                                                                                                                                                                     | **pszVerificationText**                                    |
| Icône de pied de page            | Petite icône qui indique l’objectif du texte de pied de page.                                                                                                                                                                                                                                                                                                                          | **hFooterIcon** ou **pszFooterIcon**                       |
| Texte du pied de page            | Texte supplémentaire. Dans les illustrations, le texte contient un lien hypertexte.                                                                                                                                                                                                                                                                                                                | **pszFooter**                                              |
| Bouton commun          | Un bouton standard ; dans les illustrations, le bouton OK.                                                                                                                                                                                                                                                                                                                              | **dwCommonButtons**                                        |



 

 

 




