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
# <a name="how-to-create-task-dialogs"></a><span data-ttu-id="df114-103">Guide pratique pour créer des boîtes de dialogue de tâches</span><span class="sxs-lookup"><span data-stu-id="df114-103">How to Create Task Dialogs</span></span>

<span data-ttu-id="df114-104">Une boîte de dialogue de tâche est créée et affichée à l’aide de la fonction [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) ou de la fonction [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="df114-104">A task dialog is created and shown by using either the [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) function or the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="df114-105">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="df114-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="df114-106">Technologies</span><span class="sxs-lookup"><span data-stu-id="df114-106">Technologies</span></span>

-   [<span data-ttu-id="df114-107">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="df114-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="df114-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="df114-108">Prerequisites</span></span>

-   <span data-ttu-id="df114-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="df114-109">C/C++</span></span>
-   <span data-ttu-id="df114-110">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="df114-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="df114-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="df114-111">Instructions</span></span>

### <a name="taskdialog"></a><span data-ttu-id="df114-112">TaskDialog</span><span class="sxs-lookup"><span data-stu-id="df114-112">TaskDialog</span></span>

<span data-ttu-id="df114-113">La fonction **TaskDialog** est appropriée pour les boîtes de dialogue simples qui présentent des informations textuelles et demandent un choix standard.</span><span class="sxs-lookup"><span data-stu-id="df114-113">The **TaskDialog** function is suitable for simple dialog boxes that present textual information and ask for a standard choice.</span></span> <span data-ttu-id="df114-114">Cette fonction de création ne prend pas en charge les barres de progression, les cases à cocher, les pieds de page, les boutons développer/réduire, les boutons personnalisés ou les cases d’option.</span><span class="sxs-lookup"><span data-stu-id="df114-114">This creation function does not support progress bars, check boxes, footers, expand/collapse buttons, custom buttons, or radio buttons.</span></span>

### <a name="taskdialogindirect"></a><span data-ttu-id="df114-115">TaskDialogIndirect</span><span class="sxs-lookup"><span data-stu-id="df114-115">TaskDialogIndirect</span></span>

<span data-ttu-id="df114-116">La fonction **TaskDialogIndirect** est plus puissante, prend en charge tous les éléments d’interface disponibles et vous permet également de capturer des événements dans une procédure de rappel afin que votre application puisse mettre à jour une barre de progression ou répondre à un clic sur un lien hypertexte ou un bouton.</span><span class="sxs-lookup"><span data-stu-id="df114-116">The **TaskDialogIndirect** function is more powerful, supporting all available interface elements and also enabling you to capture events in a callback procedure so that your application can update a progress bar or respond to a click of a hyperlink or button.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df114-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="df114-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df114-118">Utilisation des boîtes de dialogue de tâches</span><span class="sxs-lookup"><span data-stu-id="df114-118">Using Task Dialogs</span></span>](using-task-dialogs.md)
</dt> </dl>

 

 




