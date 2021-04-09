---
title: Guide pratique pour créer des boîtes de dialogue de tâches
description: Une boîte de dialogue de tâche est créée et affichée à l’aide de la fonction TaskDialog ou de la fonction TaskDialogIndirect.
ms.assetid: CCEFF52F-D501-4145-9799-0A9C529017E1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ea8e3097454505acccf60c7cba3ef56c637af0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028784"
---
# <a name="how-to-create-task-dialogs"></a>Guide pratique pour créer des boîtes de dialogue de tâches

Une boîte de dialogue de tâche est créée et affichée à l’aide de la fonction [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) ou de la fonction [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions

### <a name="taskdialog"></a>TaskDialog

La fonction **TaskDialog** est appropriée pour les boîtes de dialogue simples qui présentent des informations textuelles et demandent un choix standard. Cette fonction de création ne prend pas en charge les barres de progression, les cases à cocher, les pieds de page, les boutons développer/réduire, les boutons personnalisés ou les cases d’option.

### <a name="taskdialogindirect"></a>TaskDialogIndirect

La fonction **TaskDialogIndirect** est plus puissante, prend en charge tous les éléments d’interface disponibles et vous permet également de capturer des événements dans une procédure de rappel afin que votre application puisse mettre à jour une barre de progression ou répondre à un clic sur un lien hypertexte ou un bouton.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des boîtes de dialogue de tâches](using-task-dialogs.md)
</dt> </dl>

 

 




