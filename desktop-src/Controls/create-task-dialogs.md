---
title: Guide pratique pour créer des boîtes de dialogue de tâches
description: Une boîte de dialogue de tâche est créée et affichée à l’aide de la fonction TaskDialog ou de la fonction TaskDialogIndirect.
ms.assetid: CCEFF52F-D501-4145-9799-0A9C529017E1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f6f74f1922330cae1550fda1a9ad6d451221452017f3856ae5e859948019828
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504019"
---
# <a name="how-to-create-task-dialogs"></a>Guide pratique pour créer des boîtes de dialogue de tâches

Une boîte de dialogue de tâche est créée et affichée à l’aide de la fonction [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) ou de la fonction [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="taskdialog"></a>TaskDialog

La fonction **TaskDialog** est appropriée pour les boîtes de dialogue simples qui présentent des informations textuelles et demandent un choix standard. Cette fonction de création ne prend pas en charge les barres de progression, les cases à cocher, les pieds de page, les boutons développer/réduire, les boutons personnalisés ou les cases d’option.

### <a name="taskdialogindirect"></a>TaskDialogIndirect

La fonction **TaskDialogIndirect** est plus puissante, prend en charge tous les éléments d’interface disponibles et vous permet également de capturer des événements dans une procédure de rappel afin que votre application puisse mettre à jour une barre de progression ou répondre à un clic sur un lien hypertexte ou un bouton.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des boîtes de dialogue de tâches](using-task-dialogs.md)
</dt> </dl>

 

 




