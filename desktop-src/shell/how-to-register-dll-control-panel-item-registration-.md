---
description: Les éléments du panneau de configuration qui sont implémentés dans une DLL qui exporte la fonction CPlApplet ont des exigences d’inscription différentes des fichiers. exe.
title: Comment inscrire les éléments du panneau de configuration de la DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b82225dcb40487c60210752b2c15af23f95bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756507"
---
# <a name="how-to-register-dll-control-panel-items"></a><span data-ttu-id="b1643-103">Comment inscrire les éléments du panneau de configuration de la DLL</span><span class="sxs-lookup"><span data-stu-id="b1643-103">How to Register DLL Control Panel Items</span></span>

> [!Note]  
> <span data-ttu-id="b1643-104">Les instructions d’implémentation actuelles stipulent que les nouveaux éléments du panneau de configuration doivent être implémentés en tant que fichiers. exe plutôt qu’en tant que fichiers. cpl.</span><span class="sxs-lookup"><span data-stu-id="b1643-104">Current implementation guidelines state that new Control Panel items should be implemented as .exe files rather than .cpl files.</span></span> <span data-ttu-id="b1643-105">Les informations suivantes sont incluses principalement pour des raisons d’héritage.</span><span class="sxs-lookup"><span data-stu-id="b1643-105">The following information is included mainly for legacy purposes.</span></span>

 

<span data-ttu-id="b1643-106">Les éléments du panneau de configuration qui sont implémentés dans une DLL qui exporte la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) ont des exigences d’inscription différentes des fichiers. exe.</span><span class="sxs-lookup"><span data-stu-id="b1643-106">Control Panel items that are implemented in a DLL that exports the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function have different registration requirements than .exe files.</span></span> <span data-ttu-id="b1643-107">À compter de Windows XP, les nouvelles dll des éléments du panneau de configuration doivent être installées dans le dossier de l’application associée sous le dossier Program Files.</span><span class="sxs-lookup"><span data-stu-id="b1643-107">As of Windows XP, new Control Panel item DLLs should be installed in the associated application's folder under the Program Files folder.</span></span> <span data-ttu-id="b1643-108">Les éléments stockés dans le répertoire system32 avec une extension. cpl n’ont pas besoin d’être inscrits ; ils s’affichent automatiquement dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="b1643-108">Items that are stored in the System32 directory with a .cpl extension do not need to be registered; they are automatically shown in the Control Panel.</span></span> <span data-ttu-id="b1643-109">Tous les autres éléments du panneau de configuration qui utilisent **CPlApplet** doivent être inscrits de l’une des deux manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="b1643-109">All other Control Panel items that use **CPlApplet** must be registered in one of two ways:</span></span>

-   <span data-ttu-id="b1643-110">Si l’élément du panneau de configuration doit être mis à la disposition de tous les utilisateurs, enregistrez le chemin d’accès en fonction de l’ordinateur en ajoutant une valeur de **reg \_ expand \_ SZ** à la sous-clé **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Control Panel** \\  , définie sur le chemin d’accès de la dll.</span><span class="sxs-lookup"><span data-stu-id="b1643-110">If the Control Panel item is to be available to all users, register the path on a per-computer basis by adding a **REG\_EXPAND\_SZ** value to the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Control Panel**\\**Cpls** subkey, set to the DLL path.</span></span>
-   <span data-ttu-id="b1643-111">Si l’élément du panneau de configuration doit être disponible pour chaque utilisateur, utilisez **HKEY \_ Current \_ User** comme clé racine au lieu de **HKEY \_ local \_ machine**.</span><span class="sxs-lookup"><span data-stu-id="b1643-111">If the Control Panel item is to be available on a per-user basis, use **HKEY\_CURRENT\_USER** as the root key instead of **HKEY\_LOCAL\_MACHINE**.</span></span>

<span data-ttu-id="b1643-112">Les deux exemples suivants inscrivent l’élément du panneau de configuration *MyCplApp* .</span><span class="sxs-lookup"><span data-stu-id="b1643-112">The following two examples register the *MyCplApp* Control Panel item.</span></span> <span data-ttu-id="b1643-113">La DLL est nommée MyCpl.cpl et se trouve dans le répertoire de l’application *champ MyCorp \\ MonApp* .</span><span class="sxs-lookup"><span data-stu-id="b1643-113">The DLL is named MyCpl.cpl and is located in the *MyCorp\\MyApp* application directory.</span></span> <span data-ttu-id="b1643-114">Ce premier exemple illustre l’inscription par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b1643-114">This first example illustrates per-computer registration.</span></span>

## <a name="instructions"></a><span data-ttu-id="b1643-115">Instructions</span><span class="sxs-lookup"><span data-stu-id="b1643-115">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="b1643-116">Étape 1 :</span><span class="sxs-lookup"><span data-stu-id="b1643-116">Step 1:</span></span>

<span data-ttu-id="b1643-117">Ajoutez ces informations au registre pour enregistrer l’existence du fichier. cpl.</span><span class="sxs-lookup"><span data-stu-id="b1643-117">Add this information to the registry to register the existence of the .cpl file.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Cpls
                     MyCpl = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl
```

### <a name="step-2"></a><span data-ttu-id="b1643-118">Étape 2 :</span><span class="sxs-lookup"><span data-stu-id="b1643-118">Step 2:</span></span>

<span data-ttu-id="b1643-119">**Windows Vista et versions ultérieures :** Ajoutez ces informations supplémentaires au registre pour fournir un GUID pour l’élément du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="b1643-119">**Windows Vista and later:** Add this additional information to the registry to provide a GUID for the Control Panel item.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.AppId
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = {A newly generated GUID}
```

<span data-ttu-id="b1643-120">En générant un GUID pour identifier de manière unique l’élément du panneau de configuration, vous pouvez ajouter des liens de tâches au panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="b1643-120">By generating a GUID to uniquely identify the Control Panel item, you can add task links to the Control Panel.</span></span> <span data-ttu-id="b1643-121">Sans ce GUID, les liens de tâche ne sont pas associés à l’élément du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="b1643-121">Without this GUID, there is no way for the task links to be associated with the Control Panel item.</span></span> <span data-ttu-id="b1643-122">Consultez [création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration](creating-searchable-task-links.md).</span><span class="sxs-lookup"><span data-stu-id="b1643-122">See [Creating Searchable Task Links for a Control Panel Item](creating-searchable-task-links.md).</span></span>

### <a name="step-3"></a><span data-ttu-id="b1643-123">Étape 3 :</span><span class="sxs-lookup"><span data-stu-id="b1643-123">Step 3:</span></span>

<span data-ttu-id="b1643-124">**Windows Vista et versions ultérieures :** Ajoutez les informations suivantes au registre pour créer un nom canonique pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="b1643-124">**Windows Vista and later:** Add the following information to the registry to create a canonical name for the item.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ApplicationName
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] MyCorporation.MyCpl
```

<span data-ttu-id="b1643-125">En ajoutant un nom canonique, les utilisateurs peuvent lancer l’élément du panneau de configuration à partir d’une ligne de commande en entrant `control.exe /name MyCorporation.MyCpl` .</span><span class="sxs-lookup"><span data-stu-id="b1643-125">By adding a canonical name, users can launch the Control Panel item from a command line by entering `control.exe /name MyCorporation.MyCpl`.</span></span> <span data-ttu-id="b1643-126">Cela permet également de modifier ultérieurement une implémentation d’un fichier. cpl en un fichier. exe, sans exiger que les programmes d’appel apportent des modifications, car ils peuvent continuer à ouvrir l’élément via son nom canonique.</span><span class="sxs-lookup"><span data-stu-id="b1643-126">This also makes it possible to change an implementation from a .cpl file to a .exe file later, without requiring calling programs to make any changes since they can continue opening the item through its canonical name.</span></span> <span data-ttu-id="b1643-127">Pour plus d’informations sur les noms canoniques, consultez [exécution des éléments du panneau de configuration](executing-control-panel-items.md).</span><span class="sxs-lookup"><span data-stu-id="b1643-127">For more information on canonical names, see [Executing Control Panel Items](executing-control-panel-items.md).</span></span>

### <a name="step-4"></a><span data-ttu-id="b1643-128">Étape 4 :</span><span class="sxs-lookup"><span data-stu-id="b1643-128">Step 4:</span></span>

<span data-ttu-id="b1643-129">**Windows Vista et versions ultérieures :** Ajoutez les informations suivantes au registre pour assigner un élément du panneau de configuration à une ou plusieurs catégories.</span><span class="sxs-lookup"><span data-stu-id="b1643-129">**Windows Vista and later:** Add the following information to the registry to assign a Control Panel item to one or more categories.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.Category
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

<span data-ttu-id="b1643-130">**Windows XP :** Ajoutez les informations suivantes au registre pour assigner un élément du panneau de configuration à une ou plusieurs catégories.</span><span class="sxs-lookup"><span data-stu-id="b1643-130">**Windows XP:** Add the following information to the registry to assign a Control Panel item to one or more categories.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     {305CA226-D286-468e-B848-2B2E8E697B74} 2
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

<span data-ttu-id="b1643-131">Cet exemple affecte l’élément à la catégorie 3, qui correspond à réseau et Internet.</span><span class="sxs-lookup"><span data-stu-id="b1643-131">This example assigns the item to category 3, which is Network and Internet.</span></span> <span data-ttu-id="b1643-132">Pour ajouter un élément à plusieurs catégories, fournissez la liste sous la forme d’une valeur de REG \_ SZ séparée par des virgules, par exemple « 3, 8 ».</span><span class="sxs-lookup"><span data-stu-id="b1643-132">To add an item to multiple categories, provide the list as a REG\_SZ value separated by commas, such as "3,8".</span></span> <span data-ttu-id="b1643-133">Les valeurs peuvent être fournies sous la forme d’une valeur décimale ou hexadécimale.</span><span class="sxs-lookup"><span data-stu-id="b1643-133">Values can be provided as either decimal or hexadecimal.</span></span> <span data-ttu-id="b1643-134">Notez que la possibilité d’ajouter un élément à plusieurs catégories est possible uniquement dans Windows XP Service Pack 2 (SP2) et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b1643-134">Note that the ability to add an item to multiple categories is only possible in Windows XP Service Pack 2 (SP2) and later.</span></span> <span data-ttu-id="b1643-135">Consultez [assignation de catégories du panneau de configuration](assigning-control-panel-categories.md) pour toutes les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="b1643-135">See [Assigning Control Panel Categories](assigning-control-panel-categories.md) for all possible values.</span></span>

### <a name="step-5"></a><span data-ttu-id="b1643-136">Étape 5 :</span><span class="sxs-lookup"><span data-stu-id="b1643-136">Step 5:</span></span>

<span data-ttu-id="b1643-137">**Windows Vista et versions ultérieures :** Ajoutez les informations suivantes au registre pour créer et pointer vers un fichier XML pour contenir des liens de tâches pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="b1643-137">**Windows Vista and later:** Add the following information to the registry to create and point to an XML file to hold task links for the item.</span></span> <span data-ttu-id="b1643-138">La valeur doit être un \_ chemin d’accès reg SZ comme indiqué ici ou un module et un ID de ressource (par exemple, « C : \\ Program Files \\ champ MyCorp \\ MyApp \\MyApp.exe,-31 ») s’il s’agit d’une ressource incorporée.</span><span class="sxs-lookup"><span data-stu-id="b1643-138">The value must be a REG\_SZ path as shown here or a module and resource ID (for example, "C:\\Program Files\\MyCorp\\MyApp\\MyApp.exe,-31") if it is an embedded resource.</span></span> <span data-ttu-id="b1643-139">L’emplacement du fichier XML doit être entièrement spécifié.</span><span class="sxs-lookup"><span data-stu-id="b1643-139">The location of the XML file should be fully specified.</span></span> <span data-ttu-id="b1643-140">Elle ne peut pas utiliser une variable d’environnement telle que% ProgramFiles%.</span><span class="sxs-lookup"><span data-stu-id="b1643-140">It cannot use an environment variable such as %ProgramFiles%.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.TasksFileUrl
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] C:\ProgramFiles\MyCorp\MyApp\MyTasks.xml
```

<span data-ttu-id="b1643-141">Pour plus d’informations sur les liens de tâches et sur la façon de créer le fichier XML pour les stocker, consultez [création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration](creating-searchable-task-links.md).</span><span class="sxs-lookup"><span data-stu-id="b1643-141">For more details on task links and how to create the XML file to hold them, see [Creating Searchable Task Links for a Control Panel Item](creating-searchable-task-links.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1643-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b1643-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1643-143">Inscription des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="b1643-143">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="b1643-144">Comment inscrire des éléments du panneau de configuration exécutables</span><span class="sxs-lookup"><span data-stu-id="b1643-144">How To Register Executable Control Panel Items</span></span>](how-to-register-an-executable-control-panel-item-registration-.md)
</dt> </dl>

 

 
