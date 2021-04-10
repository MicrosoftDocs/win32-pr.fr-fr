---
description: Les sections suivantes décrivent l’utilisation d’actions personnalisées.
ms.assetid: dd2a0681-f50d-4232-bdcc-8aee6bb121a1
title: Utilisation d’actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be1937adbf64b94667fc3e7c44d82843b561dfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201786"
---
# <a name="using-custom-actions"></a><span data-ttu-id="17c43-103">Utilisation d’actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="17c43-103">Using Custom Actions</span></span>

<span data-ttu-id="17c43-104">Les sections suivantes décrivent l’utilisation d’actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="17c43-104">The following sections describe using custom actions.</span></span>

-   [<span data-ttu-id="17c43-105">Appel d’actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="17c43-105">Invoking Custom Actions</span></span>](invoking-custom-actions.md)
-   [<span data-ttu-id="17c43-106">Séquencement des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="17c43-106">Sequencing Custom Actions</span></span>](sequencing-custom-actions.md)
-   [<span data-ttu-id="17c43-107">Obtention d’informations de contexte pour les actions personnalisées d’exécution différée</span><span class="sxs-lookup"><span data-stu-id="17c43-107">Obtaining Context Information for Deferred Execution Custom Actions</span></span>](obtaining-context-information-for-deferred-execution-custom-actions.md)
-   [<span data-ttu-id="17c43-108">Ajout d’actions personnalisées au ProgressBar</span><span class="sxs-lookup"><span data-stu-id="17c43-108">Adding Custom Actions to the ProgressBar</span></span>](adding-custom-actions-to-the-progressbar.md)
-   [<span data-ttu-id="17c43-109">Débogage des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="17c43-109">Debugging Custom Actions</span></span>](debugging-custom-actions.md)
-   [<span data-ttu-id="17c43-110">Détermination du niveau d’interface utilisateur à partir d’une action personnalisée</span><span class="sxs-lookup"><span data-stu-id="17c43-110">Determining UI Level from a Custom Action</span></span>](determining-ui-level-from-a-custom-action.md)
-   [<span data-ttu-id="17c43-111">Désinstallation des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="17c43-111">Uninstalling Custom Actions</span></span>](uninstalling-custom-actions.md)
-   [<span data-ttu-id="17c43-112">Retour de messages d’erreur à partir d’actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="17c43-112">Returning Error Messages from Custom Actions</span></span>](returning-error-messages-from-custom-actions.md)
-   [<span data-ttu-id="17c43-113">Définition d’un point de restauration à partir d’une action personnalisée</span><span class="sxs-lookup"><span data-stu-id="17c43-113">Setting a restore point from a Custom Action</span></span>](setting-a-restore-point-from-a-custom-action.md)
-   [<span data-ttu-id="17c43-114">Fonctions non utilisables dans les actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="17c43-114">Functions Not for Use in Custom Actions</span></span>](functions-not-for-use-in-custom-actions.md)
-   [<span data-ttu-id="17c43-115">Modification de l’état du système à l’aide d’une action personnalisée</span><span class="sxs-lookup"><span data-stu-id="17c43-115">Changing the System State Using a Custom Action</span></span>](changing-the-system-state-using-a-custom-action.md)
-   [<span data-ttu-id="17c43-116">Accès à la session de programme d’installation actuelle à partir d’une action personnalisée</span><span class="sxs-lookup"><span data-stu-id="17c43-116">Accessing the Current Installer Session from Inside a Custom Action</span></span>](accessing-the-current-installer-session-from-inside-a-custom-action.md)
-   [<span data-ttu-id="17c43-117">Accès à une base de données ou à une session à partir d’une action personnalisée</span><span class="sxs-lookup"><span data-stu-id="17c43-117">Accessing a Database or Session from Inside a Custom Action</span></span>](accessing-a-database-or-session-from-inside-a-custom-action.md)
-   [<span data-ttu-id="17c43-118">Utilisation d’une action personnalisée pour lancer un fichier installé à la fin de l’installation</span><span class="sxs-lookup"><span data-stu-id="17c43-118">Using a Custom Action to Launch an Installed File at the End of the Installation</span></span>](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
-   [<span data-ttu-id="17c43-119">Utilisation d’une action personnalisée pour créer des comptes d’utilisateur sur un ordinateur local</span><span class="sxs-lookup"><span data-stu-id="17c43-119">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
-   [<span data-ttu-id="17c43-120">Utilisation d’actions personnalisées 64 bits</span><span class="sxs-lookup"><span data-stu-id="17c43-120">Using 64-bit Custom Actions</span></span>](using-64-bit-custom-actions.md)

<span data-ttu-id="17c43-121">Pour obtenir une vue d’ensemble des actions personnalisées, consultez [à propos des actions personnalisées](about-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="17c43-121">For an overview of custom actions, see [About Custom Actions](about-custom-actions.md).</span></span>

<span data-ttu-id="17c43-122">Pour plus d’informations sur l’encodage des actions personnalisées dans la [table CustomAction](customaction-table.md), consultez [référence des actions personnalisées](custom-action-reference.md).</span><span class="sxs-lookup"><span data-stu-id="17c43-122">For more information about encoding custom actions into the [CustomAction table](customaction-table.md), see [Custom Action Reference](custom-action-reference.md).</span></span>

<span data-ttu-id="17c43-123">Pour obtenir un résumé des actions personnalisées et la façon dont elles sont encodées dans la table CustomAction, consultez [liste récapitulative de tous les types d’actions personnalisés](summary-list-of-all-custom-action-types.md).</span><span class="sxs-lookup"><span data-stu-id="17c43-123">For a summary of custom actions and how they are encoded into the CustomAction table, see [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md).</span></span>

 

 



