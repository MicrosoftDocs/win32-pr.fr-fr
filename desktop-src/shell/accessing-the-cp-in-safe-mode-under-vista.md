---
description: Par défaut, les éléments du panneau de configuration de Windows Vista ne sont pas affichés lorsque Windows est exécuté en mode sans échec.
title: Accès au panneau de configuration en mode sans échec
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f37bcb0f-9417-4cc4-a57d-4f67a9ccda19
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 0f7a401bbc22a7f8de3618f844bfe463fa3baa50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972079"
---
# <a name="accessing-the-control-panel-in-safe-mode"></a><span data-ttu-id="5fb88-103">Accès au panneau de configuration en mode sans échec</span><span class="sxs-lookup"><span data-stu-id="5fb88-103">Accessing the Control Panel in Safe Mode</span></span>

<span data-ttu-id="5fb88-104">Par défaut, les éléments du panneau de configuration de Windows Vista ne sont pas affichés lorsque Windows est exécuté en mode sans échec.</span><span class="sxs-lookup"><span data-stu-id="5fb88-104">By default, as of Windows Vista Control Panel items are not shown when Windows is run in safe mode.</span></span> <span data-ttu-id="5fb88-105">Pour permettre l’affichage d’un nouvel élément du panneau de configuration en mode sans échec, les valeurs de Registre appropriées au type d’élément peuvent être définies.</span><span class="sxs-lookup"><span data-stu-id="5fb88-105">To allow a new Control Panel item to be viewed in safe mode, registry values appropriate to the item type can be set.</span></span> <span data-ttu-id="5fb88-106">Les valeurs sont interprétées comme suit :</span><span class="sxs-lookup"><span data-stu-id="5fb88-106">The values are interpreted as follows:</span></span>



| <span data-ttu-id="5fb88-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fb88-107">Value</span></span> | <span data-ttu-id="5fb88-108">Signification</span><span class="sxs-lookup"><span data-stu-id="5fb88-108">Meaning</span></span>                                                            |
|-------|--------------------------------------------------------------------|
| <span data-ttu-id="5fb88-109">1</span><span class="sxs-lookup"><span data-stu-id="5fb88-109">1</span></span>     | <span data-ttu-id="5fb88-110">L’élément doit apparaître en mode sans échec minimal.</span><span class="sxs-lookup"><span data-stu-id="5fb88-110">The item should appear in minimal safe mode only.</span></span>                  |
| <span data-ttu-id="5fb88-111">2</span><span class="sxs-lookup"><span data-stu-id="5fb88-111">2</span></span>     | <span data-ttu-id="5fb88-112">L’élément doit apparaître en mode sans échec uniquement si la mise en réseau est activée.</span><span class="sxs-lookup"><span data-stu-id="5fb88-112">The item should appear in safe mode only if networking is enabled.</span></span> |
| <span data-ttu-id="5fb88-113">3</span><span class="sxs-lookup"><span data-stu-id="5fb88-113">3</span></span>     | <span data-ttu-id="5fb88-114">L’élément doit toujours apparaître dans toute forme de mode sans échec.</span><span class="sxs-lookup"><span data-stu-id="5fb88-114">The item should always appear in any form of safe mode.</span></span>            |



 

<span data-ttu-id="5fb88-115">Cet exemple montre les entrées requises pour un élément implémenté sous la forme d’un fichier. cpl ou. dll.</span><span class="sxs-lookup"><span data-stu-id="5fb88-115">This example shows the entries required for an item implemented as a .cpl or .dll file.</span></span> <span data-ttu-id="5fb88-116">Il spécifie que l’élément doit apparaître en mode sans échec avec mise en réseau.</span><span class="sxs-lookup"><span data-stu-id="5fb88-116">It specifies that the item should appear in safe mode with networking.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.EnableInSafeMode
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 2
```

<span data-ttu-id="5fb88-117">Cet exemple montre les entrées requises pour un élément implémenté sous la forme d’un fichier. exe.</span><span class="sxs-lookup"><span data-stu-id="5fb88-117">This example shows the entries required for an item implemented as a .exe file.</span></span> <span data-ttu-id="5fb88-118">Il spécifie que l’élément doit apparaître dans n’importe quelle forme de mode sans échec.</span><span class="sxs-lookup"><span data-stu-id="5fb88-118">It specifies that the item should appear in any form of safe mode.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         System.ControlPanel.EnableInSafeMode = [REG_DWORD] 3
```

## <a name="related-topics"></a><span data-ttu-id="5fb88-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5fb88-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fb88-120">Éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="5fb88-120">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="5fb88-121">Conseils sur l’expérience utilisateur</span><span class="sxs-lookup"><span data-stu-id="5fb88-121">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="5fb88-122">Inscription des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="5fb88-122">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="5fb88-123">Utilisation de CPLApplet</span><span class="sxs-lookup"><span data-stu-id="5fb88-123">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="5fb88-124">Traitement des messages du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="5fb88-124">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="5fb88-125">Exécution des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="5fb88-125">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="5fb88-126">Extension des éléments du panneau de configuration système</span><span class="sxs-lookup"><span data-stu-id="5fb88-126">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="5fb88-127">Affectation des catégories du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="5fb88-127">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="5fb88-128">Création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="5fb88-128">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> </dl>

 

 



