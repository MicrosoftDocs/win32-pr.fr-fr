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
# <a name="how-to-get-user-input-from-a-task-dialog"></a><span data-ttu-id="c93e0-103">Comment obtenir une entrée d’utilisateur à partir d’une boîte de dialogue de tâche</span><span class="sxs-lookup"><span data-stu-id="c93e0-103">How to Get User Input from a Task Dialog</span></span>

<span data-ttu-id="c93e0-104">Pour effectuer une tâche, les utilisateurs envoient les détails de la tâche à l’application en configurant les contrôles dans la boîte de dialogue de tâche, puis en cliquant sur un bouton de commande (généralement **OK**).</span><span class="sxs-lookup"><span data-stu-id="c93e0-104">To complete a task, users submit the task details to the application by configuring the controls within the task dialog, and then clicking a command button (usually **OK**).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c93e0-105">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="c93e0-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c93e0-106">Technologies</span><span class="sxs-lookup"><span data-stu-id="c93e0-106">Technologies</span></span>

-   [<span data-ttu-id="c93e0-107">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="c93e0-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c93e0-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="c93e0-108">Prerequisites</span></span>

-   <span data-ttu-id="c93e0-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="c93e0-109">C/C++</span></span>
-   <span data-ttu-id="c93e0-110">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="c93e0-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c93e0-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="c93e0-111">Instructions</span></span>

### <a name="getting-user-input-from-a-task-dialog"></a><span data-ttu-id="c93e0-112">Obtention d’une entrée d’utilisateur à partir d’une boîte de dialogue de tâche</span><span class="sxs-lookup"><span data-stu-id="c93e0-112">Getting User Input from a Task Dialog</span></span>

<span data-ttu-id="c93e0-113">Vous pouvez identifier le bouton sur lequel l’utilisateur a cliqué en examinant le paramètre *pnButton* de la fonction appelante.</span><span class="sxs-lookup"><span data-stu-id="c93e0-113">You can identify the button that was clicked by examining the *pnButton* parameter of the calling function.</span></span> <span data-ttu-id="c93e0-114">Vous pouvez également identifier la case d’option sélectionnée à partir du paramètre *pnRadioButton* de [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)et l’état de la case à cocher de vérification à partir du paramètre *pfVerificationFlagChecked* .</span><span class="sxs-lookup"><span data-stu-id="c93e0-114">You can also identify the selected radio button from the *pnRadioButton* parameter of [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect), and the state of the verification check box from the *pfVerificationFlagChecked* parameter.</span></span>

<span data-ttu-id="c93e0-115">Les clics sur les boutons et les liens hypertexte sont reçus par la fonction [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) sous la forme d' [ \_ \_ un clic sur le bouton TDN](tdn-button-clicked.md) et de notifications de [ \_ \_ clic de TDN](tdn-hyperlink-clicked.md) .</span><span class="sxs-lookup"><span data-stu-id="c93e0-115">Clicks on buttons and hyperlinks are received by the [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) function in the form of [TDN\_BUTTON\_CLICKED](tdn-button-clicked.md) and [TDN\_HYPERLINK\_CLICKED](tdn-hyperlink-clicked.md) notifications.</span></span> <span data-ttu-id="c93e0-116">Si votre fonction de rappel retourne S \_ OK après le traitement d’une notification de bouton, la boîte de dialogue de tâche se ferme et l’identificateur de commande du bouton est retourné dans *pnButton*.</span><span class="sxs-lookup"><span data-stu-id="c93e0-116">If your callback function returns S\_OK after handling a button notification, the task dialog closes and the command identifier of the button is returned in *pnButton*.</span></span> <span data-ttu-id="c93e0-117">Si vous renvoyez \_ la valeur S false ou si vous n’avez pas de fonction de rappel, la boîte de dialogue de tâche reste ouverte.</span><span class="sxs-lookup"><span data-stu-id="c93e0-117">If you return S\_FALSE, or do not have a callback function, the task dialog remains open.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c93e0-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c93e0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c93e0-119">Utilisation des boîtes de dialogue de tâches</span><span class="sxs-lookup"><span data-stu-id="c93e0-119">Using Task Dialogs</span></span>](using-task-dialogs.md)
</dt> </dl>

 

 