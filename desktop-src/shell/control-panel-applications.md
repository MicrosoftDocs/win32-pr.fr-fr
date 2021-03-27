---
description: Les éléments du panneau de configuration sont des dll ou des fichiers exécutables (. exe) qui permettent aux utilisateurs de configurer l’environnement de Windows. Ils sont généralement accessibles en cliquant sur une icône dans le panneau de configuration.
title: Implémentation des éléments du panneau de configuration
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2e61cbc0-fbb5-4680-8123-f8ffdcf98210
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 310d01f07d40cef69c6be30231bbf4780a1d8838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972055"
---
# <a name="implementing-control-panel-items"></a><span data-ttu-id="e7d34-104">Implémentation des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="e7d34-104">Implementing Control Panel Items</span></span>

<span data-ttu-id="e7d34-105">Les éléments du panneau de configuration sont des dll ou des fichiers exécutables (. exe) qui permettent aux utilisateurs de configurer l’environnement de Windows.</span><span class="sxs-lookup"><span data-stu-id="e7d34-105">Control Panel items are DLLs or executable (.exe) files that let users configure the environment of Windows.</span></span> <span data-ttu-id="e7d34-106">Ils sont généralement accessibles en cliquant sur une icône dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="e7d34-106">They are typically accessed by clicking an icon in the Control Panel.</span></span>

<span data-ttu-id="e7d34-107">Cette section décrit les éléments du panneau de configuration et explique comment les créer et les inscrire pour qu’ils apparaissent correctement dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="e7d34-107">This section describes Control Panel items and explains how to create and register them so that they appear appropriately in the Control Panel.</span></span> <span data-ttu-id="e7d34-108">Pour Windows Vista, vous trouverez des informations qui vous indiquent comment ajouter des liens de tâches qui s’affichent sous l’élément du panneau de configuration et dans les résultats de la recherche du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="e7d34-108">For Windows Vista, information is included that tells you how to add task links that appear under the Control Panel item and in Control Panel search results.</span></span>

-   [<span data-ttu-id="e7d34-109">Conseils sur l’expérience utilisateur</span><span class="sxs-lookup"><span data-stu-id="e7d34-109">User Experience Guidelines</span></span>](user-experience-guidelines.md)
-   [<span data-ttu-id="e7d34-110">Inscription des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="e7d34-110">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
-   [<span data-ttu-id="e7d34-111">Comment inscrire des éléments du panneau de configuration exécutables</span><span class="sxs-lookup"><span data-stu-id="e7d34-111">How To Register Executable Control Panel Items</span></span>](how-to-register-an-executable-control-panel-item-registration-.md)
-   [<span data-ttu-id="e7d34-112">Comment inscrire les éléments du panneau de configuration de la DLL</span><span class="sxs-lookup"><span data-stu-id="e7d34-112">How To Register DLL Control Panel Items</span></span>](how-to-register-dll-control-panel-item-registration-.md)
-   [<span data-ttu-id="e7d34-113">Utilisation de CPLApplet</span><span class="sxs-lookup"><span data-stu-id="e7d34-113">Using CPLApplet</span></span>](using-cplapplet.md)
-   [<span data-ttu-id="e7d34-114">Traitement des messages du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="e7d34-114">Control Panel Message Processing</span></span>](message-processing.md)
-   [<span data-ttu-id="e7d34-115">Exécution des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="e7d34-115">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
-   [<span data-ttu-id="e7d34-116">Extension des éléments du panneau de configuration système</span><span class="sxs-lookup"><span data-stu-id="e7d34-116">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
-   [<span data-ttu-id="e7d34-117">Affectation des catégories du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="e7d34-117">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
-   [<span data-ttu-id="e7d34-118">Création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="e7d34-118">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
-   [<span data-ttu-id="e7d34-119">Accès au panneau de configuration en mode sans échec</span><span class="sxs-lookup"><span data-stu-id="e7d34-119">Accessing the Control Panel in Safe Mode</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
-   [<span data-ttu-id="e7d34-120">Noms canoniques des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="e7d34-120">Canonical Names of Control Panel Items</span></span>](controlpanel-canonical-names.md)

 

 



