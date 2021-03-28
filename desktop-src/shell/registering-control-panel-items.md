---
description: Les éléments du panneau de configuration doivent être enregistrés afin d’apparaître dans la fenêtre du panneau de configuration.
title: Inscription des éléments du panneau de configuration
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6f21f223-a293-47b5-95e9-06b7a4ff1652
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05c2a652314babc212e17b48198e9441f4d3465d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115727"
---
# <a name="registering-control-panel-items"></a><span data-ttu-id="c6a39-103">Inscription des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="c6a39-103">Registering Control Panel Items</span></span>

<span data-ttu-id="c6a39-104">Les éléments du panneau de configuration doivent être enregistrés afin d’apparaître dans la fenêtre du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="c6a39-104">Control Panel items must be registered in order to appear in the Control Panel window.</span></span> <span data-ttu-id="c6a39-105">Si l’élément du panneau de configuration est implémenté dans le cadre d’un fichier. exe, il est inscrit en tant qu’objet de commande.</span><span class="sxs-lookup"><span data-stu-id="c6a39-105">If the Control Panel item is implemented as part of a .exe file then it is registered as a command object.</span></span> <span data-ttu-id="c6a39-106">L’inscription diffère si l’élément est implémenté en tant que fichier. dll qui exporte la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) .</span><span class="sxs-lookup"><span data-stu-id="c6a39-106">Registration differs if the item is implemented as a .dll file that exports the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function.</span></span>

<span data-ttu-id="c6a39-107">Des exigences spécifiques sont décrites dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="c6a39-107">Specific requirements are discussed in these topics:</span></span>

-   [<span data-ttu-id="c6a39-108">Comment inscrire des éléments du panneau de configuration exécutables</span><span class="sxs-lookup"><span data-stu-id="c6a39-108">How To Register Executable Control Panel Items</span></span>](how-to-register-an-executable-control-panel-item-registration-.md)
-   [<span data-ttu-id="c6a39-109">Comment inscrire les éléments du panneau de configuration de la DLL</span><span class="sxs-lookup"><span data-stu-id="c6a39-109">How To Register DLL Control Panel Items</span></span>](how-to-register-dll-control-panel-item-registration-.md)

## <a name="related-topics"></a><span data-ttu-id="c6a39-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c6a39-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6a39-111">Éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="c6a39-111">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="c6a39-112">Conseils sur l’expérience utilisateur</span><span class="sxs-lookup"><span data-stu-id="c6a39-112">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="c6a39-113">Utilisation de CPLApplet</span><span class="sxs-lookup"><span data-stu-id="c6a39-113">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="c6a39-114">Traitement des messages du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="c6a39-114">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="c6a39-115">Exécution des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="c6a39-115">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="c6a39-116">Extension des éléments du panneau de configuration système</span><span class="sxs-lookup"><span data-stu-id="c6a39-116">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="c6a39-117">Affectation des catégories du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="c6a39-117">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="c6a39-118">Création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="c6a39-118">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="c6a39-119">Accès au panneau de configuration en mode sans échec sous Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6a39-119">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
