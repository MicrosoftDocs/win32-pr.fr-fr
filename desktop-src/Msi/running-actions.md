---
description: Les fonctions du programme d’installation peuvent être utilisées pour exécuter des actions ou des séquences d’action spécifiques.
ms.assetid: ceb4f70b-1179-416a-9030-3d87341cb956
title: Actions en cours d’exécution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ab566b90ec43a33f3e70b994b01446700e353b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531848"
---
# <a name="running-actions"></a><span data-ttu-id="2af93-103">Actions en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="2af93-103">Running Actions</span></span>

<span data-ttu-id="2af93-104">Les fonctions du programme d’installation peuvent être utilisées pour exécuter des actions ou des séquences d’action spécifiques.</span><span class="sxs-lookup"><span data-stu-id="2af93-104">The installer functions can be used to run specific actions or action sequences.</span></span> <span data-ttu-id="2af93-105">Ces actions peuvent être des actions [standard](standard-actions.md) ou [personnalisées](custom-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="2af93-105">These actions can either be [standard](standard-actions.md) or [custom](custom-actions.md) actions.</span></span> <span data-ttu-id="2af93-106">La procédure suivante décrit comment exécuter des actions :</span><span class="sxs-lookup"><span data-stu-id="2af93-106">The following procedure describes how to run actions:</span></span>

<span data-ttu-id="2af93-107">**Pour exécuter une séquence d’action**</span><span class="sxs-lookup"><span data-stu-id="2af93-107">**To run an action sequence**</span></span>

1.  <span data-ttu-id="2af93-108">Exécutez une séquence d’actions définie dans une table en appelant la fonction [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea) .</span><span class="sxs-lookup"><span data-stu-id="2af93-108">Run a sequence of actions defined in a table by calling the [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea) function.</span></span>

    <span data-ttu-id="2af93-109">Le programme d’installation interroge la table indiquée et exécute chaque action si son expression conditionnelle prend la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="2af93-109">The installer queries the indicated table and runs each action if its conditional expression evaluates to TRUE.</span></span>

2.  <span data-ttu-id="2af93-110">Vérifiez les expressions conditionnelles en appelant la fonction [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) .</span><span class="sxs-lookup"><span data-stu-id="2af93-110">Check conditional expressions by calling the [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) function.</span></span>
3.  <span data-ttu-id="2af93-111">Exécutez l’action en appelant la fonction [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) .</span><span class="sxs-lookup"><span data-stu-id="2af93-111">Run the action by calling the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function.</span></span> <span data-ttu-id="2af93-112">L’action peut être une action standard, une action personnalisée ou une boîte de dialogue d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2af93-112">The action can be a standard action, a custom action, or a user interface dialog box.</span></span>
4.  <span data-ttu-id="2af93-113">Si une erreur s’est produite lors de l’exécution de cette action, appelez la fonction [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) .</span><span class="sxs-lookup"><span data-stu-id="2af93-113">If an error occurred during the execution of this action, call the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function.</span></span> <span data-ttu-id="2af93-114">Le programme d’installation traitera l’erreur.</span><span class="sxs-lookup"><span data-stu-id="2af93-114">The installer will process the error.</span></span>

 

 



