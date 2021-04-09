---
title: Comment obtenir une entrée d’utilisateur à partir d’une boîte de dialogue de tâche
description: Pour effectuer une tâche, les utilisateurs envoient les détails de la tâche à l’application en configurant les contrôles dans la boîte de dialogue de tâche, puis en cliquant sur un bouton de commande (généralement OK).
ms.assetid: 73CD8FBF-95C9-43C8-B9D8-3823840C23A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd53c8051747187123821211ac7e17c9915b5fd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941419"
---
# <a name="how-to-get-user-input-from-a-task-dialog"></a>Comment obtenir une entrée d’utilisateur à partir d’une boîte de dialogue de tâche

Pour effectuer une tâche, les utilisateurs envoient les détails de la tâche à l’application en configurant les contrôles dans la boîte de dialogue de tâche, puis en cliquant sur un bouton de commande (généralement **OK**).

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions

### <a name="getting-user-input-from-a-task-dialog"></a>Obtention d’une entrée d’utilisateur à partir d’une boîte de dialogue de tâche

Vous pouvez identifier le bouton sur lequel l’utilisateur a cliqué en examinant le paramètre *pnButton* de la fonction appelante. Vous pouvez également identifier la case d’option sélectionnée à partir du paramètre *pnRadioButton* de [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)et l’état de la case à cocher de vérification à partir du paramètre *pfVerificationFlagChecked* .

Les clics sur les boutons et les liens hypertexte sont reçus par la fonction [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) sous la forme d' [ \_ \_ un clic sur le bouton TDN](tdn-button-clicked.md) et de notifications de [ \_ \_ clic de TDN](tdn-hyperlink-clicked.md) . Si votre fonction de rappel retourne S \_ OK après le traitement d’une notification de bouton, la boîte de dialogue de tâche se ferme et l’identificateur de commande du bouton est retourné dans *pnButton*. Si vous renvoyez \_ la valeur S false ou si vous n’avez pas de fonction de rappel, la boîte de dialogue de tâche reste ouverte.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des boîtes de dialogue de tâches](using-task-dialogs.md)
</dt> </dl>

 

 