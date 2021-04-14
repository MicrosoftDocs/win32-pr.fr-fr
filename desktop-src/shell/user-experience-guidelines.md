---
description: La responsabilité principale de tout élément du panneau de configuration est d’afficher une fenêtre qui permet à l’utilisateur d’afficher et de manipuler des paramètres.
title: Conseils sur l’expérience utilisateur
ms.topic: article
ms.date: 09/24/2020
ms.assetid: f03a154b-9781-4718-8244-3d57fee0755e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e25f8885c2444a51d5d5d8cc917121c7f3b26a09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991773"
---
# <a name="user-experience-guidelines"></a><span data-ttu-id="b24f3-103">Conseils sur l’expérience utilisateur</span><span class="sxs-lookup"><span data-stu-id="b24f3-103">User Experience Guidelines</span></span>

<span data-ttu-id="b24f3-104">La responsabilité principale de tout élément du panneau de configuration est d’afficher une fenêtre qui permet à l’utilisateur d’afficher et de manipuler des paramètres.</span><span class="sxs-lookup"><span data-stu-id="b24f3-104">The primary responsibility of any Control Panel item is to display a window that allows the user to view and manipulate settings.</span></span> <span data-ttu-id="b24f3-105">Consultez les [instructions de l’expérience utilisateur des panneaux](../uxguide/winenv-ctrl-panels.md) de configuration pour connaître le comportement et la conception des éléments du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="b24f3-105">See the [Control Panels user experience (UX) guidelines](../uxguide/winenv-ctrl-panels.md) for the behavior and design of Control Panel items.</span></span> <span data-ttu-id="b24f3-106">Les instructions présentées dans cette rubrique illustrent une méthode de déroulement des tâches qui consiste à organiser un élément du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="b24f3-106">The guidelines discussed in that topic show a task flow method of organizing a Control Panel item.</span></span> <span data-ttu-id="b24f3-107">Cela place les paramètres les plus importants sur une page d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="b24f3-107">This places the most important settings on a home page.</span></span> <span data-ttu-id="b24f3-108">Les paramètres moins fréquemment utilisés sont placés sur les pages spoke ou accessibles à partir de liens dans un volet latéral.</span><span class="sxs-lookup"><span data-stu-id="b24f3-108">Less frequently used settings are placed on spoke pages or accessed from links in a side pane.</span></span>

<span data-ttu-id="b24f3-109">Le panneau de configuration comprend de nombreux éléments qui suivent ces recommandations, telles que la facilité d’accès et le centre réseau et partage.</span><span class="sxs-lookup"><span data-stu-id="b24f3-109">The Control Panel includes many items that follow these guidelines, such as Ease of Access Center and Network and Sharing Center.</span></span> <span data-ttu-id="b24f3-110">Les autres éléments du panneau de configuration utilisent le format de feuille de propriétés de la boîte de dialogue à onglets, comme dans les versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="b24f3-110">Other Control Panel items use the tabbed dialog property sheet format as in earlier versions of Windows.</span></span> <span data-ttu-id="b24f3-111">Les exemples incluent l’élément Mouse et les options Internet.</span><span class="sxs-lookup"><span data-stu-id="b24f3-111">Examples include the Mouse item and Internet Options.</span></span> <span data-ttu-id="b24f3-112">L’utilisation du format de la feuille de propriétés doit être supprimée.</span><span class="sxs-lookup"><span data-stu-id="b24f3-112">Use of the property sheet format should be discontinued.</span></span> <span data-ttu-id="b24f3-113">Si vous créez des éléments du panneau de configuration, vous devez suivre les instructions relatives au déroulement des tâches.</span><span class="sxs-lookup"><span data-stu-id="b24f3-113">If you create new Control Panel items, you should follow the task flow guidelines.</span></span>

<span data-ttu-id="b24f3-114">Par le passé, les éléments du panneau de configuration étaient empaquetés sous forme de fichiers. cpl.</span><span class="sxs-lookup"><span data-stu-id="b24f3-114">In the past, Control Panel items were packaged as .cpl files.</span></span> <span data-ttu-id="b24f3-115">Cela n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b24f3-115">That is no longer necessary.</span></span> <span data-ttu-id="b24f3-116">Les nouveaux éléments du panneau de configuration doivent être implémentés en tant que fichier. exe autonome ou en tant qu’option d’indicateur de ligne de commande pour le fichier exécutable principal de l’application.</span><span class="sxs-lookup"><span data-stu-id="b24f3-116">New Control Panel items should be implemented as a standalone .exe file or as a command-line flag option for the application's main executable file.</span></span>

> [!Note]  
> <span data-ttu-id="b24f3-117">Sur les systèmes 64 bits, les éléments du panneau de configuration de 32 bits s’affichent dans le panneau de configuration lorsque l’option de **dossier éléments du panneau de configuration de la vue 32** est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="b24f3-117">On 64-bit systems, 32-bit Control Panel items are displayed in the Control Panel when the **View 32-bit Control Panel Items folder** option is selected.</span></span> <span data-ttu-id="b24f3-118">Les éléments 32 bits doivent se trouver dans le dossier% SystemRoot% \\ SysWOW64 à afficher.</span><span class="sxs-lookup"><span data-stu-id="b24f3-118">The 32-bit items must be located in the %SystemRoot%\\SysWOW64 folder to be displayed.</span></span> <span data-ttu-id="b24f3-119">Ils ne nécessitent pas d’inscription supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="b24f3-119">They do not require any further registration.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b24f3-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b24f3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b24f3-121">Éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="b24f3-121">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="b24f3-122">Inscription des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="b24f3-122">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="b24f3-123">Utilisation de CPLApplet</span><span class="sxs-lookup"><span data-stu-id="b24f3-123">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="b24f3-124">Traitement des messages du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="b24f3-124">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="b24f3-125">Exécution des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="b24f3-125">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="b24f3-126">Extension des éléments du panneau de configuration système</span><span class="sxs-lookup"><span data-stu-id="b24f3-126">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="b24f3-127">Affectation des catégories du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="b24f3-127">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="b24f3-128">Création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="b24f3-128">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="b24f3-129">Accès au panneau de configuration en mode sans échec</span><span class="sxs-lookup"><span data-stu-id="b24f3-129">Accessing the Control Panel in Safe Mode</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



