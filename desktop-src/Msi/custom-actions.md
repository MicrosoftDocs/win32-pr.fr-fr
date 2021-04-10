---
description: Le Windows Installer fournit de nombreuses actions intégrées pour exécuter le processus d’installation. Pour obtenir la liste de ces actions, consultez les informations de référence sur les actions standard.
ms.assetid: 4a1f3ccc-4904-47d0-bfc6-013e404de47e
title: Actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9623351bdcd4cd109d2112724d13e0f9ccaa6b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034648"
---
# <a name="custom-actions"></a><span data-ttu-id="90b4c-104">Actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="90b4c-104">Custom Actions</span></span>

<span data-ttu-id="90b4c-105">Le Windows Installer fournit de nombreuses actions intégrées pour exécuter le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="90b4c-105">The Windows Installer provides many built-in actions for performing the installation process.</span></span> <span data-ttu-id="90b4c-106">Pour obtenir la liste de ces actions, consultez les informations de référence sur les [actions standard](standard-actions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="90b4c-106">For a list of these actions, see the [Standard Actions Reference](standard-actions-reference.md).</span></span>

<span data-ttu-id="90b4c-107">Les actions standard sont suffisantes pour exécuter une installation dans la plupart des cas.</span><span class="sxs-lookup"><span data-stu-id="90b4c-107">Standard actions are sufficient to execute an installation in most cases.</span></span> <span data-ttu-id="90b4c-108">Toutefois, il existe des situations où le développeur d’un package d’installation trouve qu’il est nécessaire d’écrire une action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="90b4c-108">However, there are situations where the developer of an installation package finds it necessary to write a custom action.</span></span> <span data-ttu-id="90b4c-109">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="90b4c-109">For example:</span></span>

-   <span data-ttu-id="90b4c-110">Vous souhaitez lancer un fichier exécutable au cours de l’installation qui est installée sur l’ordinateur de l’utilisateur ou qui est installée avec l’application.</span><span class="sxs-lookup"><span data-stu-id="90b4c-110">You want to launch an executable during installation that is installed on the user's machine or that is being installed with the application.</span></span>
-   <span data-ttu-id="90b4c-111">Vous souhaitez appeler des fonctions spéciales pendant une installation qui sont définies dans une bibliothèque de liens dynamiques (DLL).</span><span class="sxs-lookup"><span data-stu-id="90b4c-111">You want to call special functions during an installation that are defined in a dynamic-link library (DLL).</span></span>
-   <span data-ttu-id="90b4c-112">Vous souhaitez utiliser des fonctions écrites dans les langages de développement Microsoft Visual Basic Scripting Edition ou le texte de script littéral Microsoft JScript pendant une installation.</span><span class="sxs-lookup"><span data-stu-id="90b4c-112">You want to use functions written in the development languages Microsoft Visual Basic Scripting Edition or Microsoft JScript literal script text during an installation.</span></span>
-   <span data-ttu-id="90b4c-113">Vous souhaitez différer l’exécution de certaines actions jusqu’à l’exécution du script d’installation.</span><span class="sxs-lookup"><span data-stu-id="90b4c-113">You want to defer the execution of some actions until the time when the installation script is being executed.</span></span>
-   <span data-ttu-id="90b4c-114">Vous souhaitez ajouter des informations de temps et de progression à un contrôle ProgressBar et à un contrôle de texte TimeRemaining.</span><span class="sxs-lookup"><span data-stu-id="90b4c-114">You want to add time and progress information to a ProgressBar control and a TimeRemaining Text control.</span></span>

<span data-ttu-id="90b4c-115">Les sections suivantes décrivent les actions personnalisées et la façon de les incorporer dans un package d’installation :</span><span class="sxs-lookup"><span data-stu-id="90b4c-115">The following sections describe custom actions and how to incorporate them into an installation package:</span></span>

-   [<span data-ttu-id="90b4c-116">À propos des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="90b4c-116">About Custom Actions</span></span>](about-custom-actions.md)
-   [<span data-ttu-id="90b4c-117">Utilisation d’actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="90b4c-117">Using Custom Actions</span></span>](using-custom-actions.md)
-   [<span data-ttu-id="90b4c-118">Référence des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="90b4c-118">Custom Action Reference</span></span>](custom-action-reference.md)
-   [<span data-ttu-id="90b4c-119">Liste récapitulative de tous les types d’actions personnalisés</span><span class="sxs-lookup"><span data-stu-id="90b4c-119">Summary List of All Custom Action Types</span></span>](summary-list-of-all-custom-action-types.md)

 

 



