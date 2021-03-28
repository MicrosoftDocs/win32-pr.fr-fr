---
description: Pour les éléments du panneau de configuration qui sont implémentés en tant que fichiers. exe, aucune exportation spéciale ou gestion des messages n’est requise. Tout fichier. exe peut être enregistré en tant qu’objet de commande pour s’afficher avec un point d’entrée dans le dossier du panneau de configuration.
title: Comment inscrire des éléments du panneau de configuration exécutables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 778bac10fea661f73c0967401a7c708ebf6b8273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034496"
---
# <a name="how-to-register-executable-control-panel-items"></a><span data-ttu-id="10195-104">Comment inscrire des éléments du panneau de configuration exécutables</span><span class="sxs-lookup"><span data-stu-id="10195-104">How to Register Executable Control Panel Items</span></span>

<span data-ttu-id="10195-105">Pour les éléments du panneau de configuration qui sont implémentés en tant que fichiers. exe, aucune exportation spéciale ou gestion des messages n’est requise.</span><span class="sxs-lookup"><span data-stu-id="10195-105">For Control Panel items that are implemented as .exe files, no special exports or message handling is required.</span></span> <span data-ttu-id="10195-106">Tout fichier. exe peut être enregistré en tant qu’objet de commande pour s’afficher avec un point d’entrée dans le dossier du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="10195-106">Any .exe file can be registered as a command object to appear with an entry point in the Control Panel folder.</span></span>

<span data-ttu-id="10195-107">Un exemple est utilisé ici pour illustrer les exigences d’inscription.</span><span class="sxs-lookup"><span data-stu-id="10195-107">An example is used here to demonstrate the registration requirements.</span></span> <span data-ttu-id="10195-108">L’exemple montre comment inscrire un élément du panneau de configuration appelé **mes paramètres** comme objet de commande afin qu’il apparaisse dans la fenêtre du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="10195-108">The example shows how to register a Control Panel item called **My Settings** as a command object so that it appears in the Control Panel window.</span></span> <span data-ttu-id="10195-109">La fenêtre **mes paramètres** s’affiche également lorsque la commande `MyApp.exe /settings` est exécutée.</span><span class="sxs-lookup"><span data-stu-id="10195-109">The **My Settings** window also appears when the command `MyApp.exe /settings` is run.</span></span>

## <a name="instructions"></a><span data-ttu-id="10195-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="10195-110">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="10195-111">Étape 1 :</span><span class="sxs-lookup"><span data-stu-id="10195-111">Step 1:</span></span>

<span data-ttu-id="10195-112">Générez un GUID pour l’élément du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="10195-112">Generate a GUID for the Control Panel item.</span></span> <span data-ttu-id="10195-113">Le GUID identifie de façon unique l’élément du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="10195-113">The GUID uniquely identifies the Control Panel item.</span></span> <span data-ttu-id="10195-114">Dans cet exemple, `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` est le GUID de l’élément du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="10195-114">In this example, `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` is the GUID of the Control Panel item.</span></span>

### <a name="step-2"></a><span data-ttu-id="10195-115">Étape 2 :</span><span class="sxs-lookup"><span data-stu-id="10195-115">Step 2:</span></span>

<span data-ttu-id="10195-116">En utilisant le GUID comme nom, ajoutez une sous-clé au registre comme suit.</span><span class="sxs-lookup"><span data-stu-id="10195-116">Using the GUID as a name, add a subkey to the registry as follows.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ControlPanel
                     NameSpace
                        {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
                           (Default) = My Settings
```

<span data-ttu-id="10195-117">Les données de l’entrée par défaut sont simplement le \_ nom de la reg SZ de l’élément du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="10195-117">The data for the Default entry is simply the REG\_SZ name of the Control Panel item.</span></span> <span data-ttu-id="10195-118">L’entrée par défaut peut être utile pour identifier l’entrée GUID, mais elle est facultative.</span><span class="sxs-lookup"><span data-stu-id="10195-118">The Default entry can be useful to identify the GUID entry, but it is optional.</span></span>

### <a name="step-3"></a><span data-ttu-id="10195-119">Étape 3 :</span><span class="sxs-lookup"><span data-stu-id="10195-119">Step 3:</span></span>

<span data-ttu-id="10195-120">En utilisant le GUID comme nom, ajoutez une sous-clé et ses entrées au registre comme suit.</span><span class="sxs-lookup"><span data-stu-id="10195-120">Using the GUID as a name, add a subkey and its entries to the registry as follows.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         (Default) = My Settings
         LocalizedString = @%ProgramFiles%\MyCorp\MyApp.exe,-9
         InfoTip = @%ProgramFiles%\MyCorp\MyApp.exe,-5
         System.ApplicationName = MyCorporation.MySettings
         System.ControlPanel.Category = 1,8
         System.Software.TasksFileUrl = %ProgramFiles%\MyCorp\MyApp\MyTaskLinks.xml
```

-   <span data-ttu-id="10195-121">**Par défaut**.</span><span class="sxs-lookup"><span data-stu-id="10195-121">**Default**.</span></span> <span data-ttu-id="10195-122">PRIX \_ SZ</span><span class="sxs-lookup"><span data-stu-id="10195-122">REG\_SZ.</span></span> <span data-ttu-id="10195-123">Nom complet de l’élément du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="10195-123">The display name for the Control Panel item.</span></span>
-   <span data-ttu-id="10195-124">**LocalizedString**.</span><span class="sxs-lookup"><span data-stu-id="10195-124">**LocalizedString**.</span></span> <span data-ttu-id="10195-125">facultatif.</span><span class="sxs-lookup"><span data-stu-id="10195-125">Optional.</span></span> <span data-ttu-id="10195-126">REG \_ SZ ou reg \_ expand \_ sz.</span><span class="sxs-lookup"><span data-stu-id="10195-126">REG\_SZ or REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="10195-127">Nom du module et ID de la table de chaînes du nom localisé de l’élément du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="10195-127">The module name and string table ID of the localized name of the Control Panel item.</span></span> <span data-ttu-id="10195-128">Le format est un signe « at » (@) suivi du nom du fichier. exe ou. dll qui contient la table de chaînes de l’interface utilisateur multilingue (MUI).</span><span class="sxs-lookup"><span data-stu-id="10195-128">The format is an "at" sign (@) followed by the name of the .exe or .dll that contains the Multilingual User Interface (MUI) string table.</span></span> <span data-ttu-id="10195-129">Les variables d’environnement peuvent être utilisées comme substituts pour une partie du chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="10195-129">Environment variables can be used as a substitute for a part of the path.</span></span> <span data-ttu-id="10195-130">Le chemin d’accès et le nom de fichier sont suivis d’une virgule (,) et d’un trait d’Union (-), suivi de l’ID dans la table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="10195-130">The path and file name is followed by a comma (,) and a hyphen (-), followed by the ID in the string table.</span></span>

    <span data-ttu-id="10195-131">Si le module n’a pas de table de chaînes, cette entrée peut simplement être la chaîne de nom complet.</span><span class="sxs-lookup"><span data-stu-id="10195-131">If the module does not have a string table, then this entry can simply be the display name string.</span></span> <span data-ttu-id="10195-132">Si vous utilisez uniquement la chaîne de nom complet plutôt qu’une table de chaînes, le nom ne s’ajuste pas à la langue d’affichage actuelle.</span><span class="sxs-lookup"><span data-stu-id="10195-132">If you use only the display name string rather than a string table, the name does not adjust to the current display language.</span></span>

-   <span data-ttu-id="10195-133">**Info-bulle**.</span><span class="sxs-lookup"><span data-stu-id="10195-133">**InfoTip**.</span></span> <span data-ttu-id="10195-134">REG \_ SZ ou reg \_ expand \_ sz.</span><span class="sxs-lookup"><span data-stu-id="10195-134">REG\_SZ or REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="10195-135">Description de l’élément du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="10195-135">A description of the Control Panel item.</span></span> <span data-ttu-id="10195-136">Ces informations sont affichées dans une info-bulle qui s’affiche lorsque la souris pointe sur l’icône de l’élément.</span><span class="sxs-lookup"><span data-stu-id="10195-136">This information is shown in an InfoTip that is displayed when the mouse hovers over the item's icon.</span></span> <span data-ttu-id="10195-137">La syntaxe est la même que celle utilisée pour LocalizedString, y compris la possibilité de fournir simplement une chaîne plutôt qu’une référence de table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="10195-137">The syntax is the same as that used for LocalizedString, including the option of simply providing a string rather than a string table reference.</span></span>
-   <span data-ttu-id="10195-138">**System. ApplicationName**.</span><span class="sxs-lookup"><span data-stu-id="10195-138">**System.ApplicationName**.</span></span> <span data-ttu-id="10195-139">PRIX \_ SZ</span><span class="sxs-lookup"><span data-stu-id="10195-139">REG\_SZ.</span></span> <span data-ttu-id="10195-140">Nom canonique de l'élément.</span><span class="sxs-lookup"><span data-stu-id="10195-140">The canonical name of the item.</span></span> <span data-ttu-id="10195-141">La commande de formulaire `control.exe /name System.ApplicationName` ouvre l’élément, par exemple `control.exe /name MyCorporation.MySettings` .</span><span class="sxs-lookup"><span data-stu-id="10195-141">The command of form `control.exe /name System.ApplicationName` opens the item; for example, `control.exe /name MyCorporation.MySettings`.</span></span> <span data-ttu-id="10195-142">Pour plus d’informations sur l’utilisation de Control.exe, consultez [exécution des éléments du panneau de configuration](executing-control-panel-items.md) .</span><span class="sxs-lookup"><span data-stu-id="10195-142">See [Executing Control Panel Items](executing-control-panel-items.md) for more information on the use of Control.exe.</span></span>
-   <span data-ttu-id="10195-143">**System. ControlPanel. Category**.</span><span class="sxs-lookup"><span data-stu-id="10195-143">**System.ControlPanel.Category**.</span></span> <span data-ttu-id="10195-144">PRIX \_ SZ</span><span class="sxs-lookup"><span data-stu-id="10195-144">REG\_SZ.</span></span> <span data-ttu-id="10195-145">Valeur qui déclare les catégories du panneau de configuration où l’élément apparaît.</span><span class="sxs-lookup"><span data-stu-id="10195-145">A value that declares the Control Panel categories where the item appears.</span></span> <span data-ttu-id="10195-146">Plusieurs catégories sont séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="10195-146">Multiple categories are separated by commas.</span></span> <span data-ttu-id="10195-147">Dans le cas de l’exemple ci-dessus, l’entrée indique que l’élément **mes paramètres** doit apparaître à la fois dans les catégories **apparence et personnalisation** et **programmes** .</span><span class="sxs-lookup"><span data-stu-id="10195-147">In the case of the example above, the entry specifies that the **My Settings** item should appear in both the **Appearance and Personalization** and **Programs** categories.</span></span> <span data-ttu-id="10195-148">Consultez [assignation de catégories du panneau de configuration](assigning-control-panel-categories.md) pour connaître les valeurs de catégorie possibles.</span><span class="sxs-lookup"><span data-stu-id="10195-148">See [Assigning Control Panel Categories](assigning-control-panel-categories.md) for possible category values.</span></span>
-   <span data-ttu-id="10195-149">**System. Software. TasksFileUrl**.</span><span class="sxs-lookup"><span data-stu-id="10195-149">**System.Software.TasksFileUrl**.</span></span> <span data-ttu-id="10195-150">REG \_ SZ ou reg \_ expand \_ sz.</span><span class="sxs-lookup"><span data-stu-id="10195-150">REG\_SZ or REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="10195-151">Chemin d’accès du fichier XML qui définit les [liens de tâche](creating-searchable-task-links.md).</span><span class="sxs-lookup"><span data-stu-id="10195-151">The path of the XML file that defines [task links](creating-searchable-task-links.md).</span></span> <span data-ttu-id="10195-152">Il peut s’agir d’un chemin d’accès direct à un fichier, comme indiqué dans l’exemple, ou d’une ressource incorporée spécifiée comme nom de module et ID de ressource, par exemple « % ProgramFiles% \\ champ MyCorp \\ MyApp \\MyApp.exe,-31 ».</span><span class="sxs-lookup"><span data-stu-id="10195-152">This can be a direct file path as shown in the example, or an embedded resource specified as a module name and resource ID such as "%ProgramFiles%\\MyCorp\\MyApp\\MyApp.exe,-31".</span></span>

### <a name="step-4"></a><span data-ttu-id="10195-153">Étape 4 :</span><span class="sxs-lookup"><span data-stu-id="10195-153">Step 4:</span></span>

<span data-ttu-id="10195-154">Sous la même sous-clé GUID, ajoutez la sous-clé suivante au registre pour fournir le chemin d’accès du fichier qui contient l’icône et l’ID de ressource de l’image dans ce fichier.</span><span class="sxs-lookup"><span data-stu-id="10195-154">Under that same GUID subkey, add the following subkey to the registry to provide the path of the file that contains the icon and the resource ID of the image within that file.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         DefaultIcon
            (Default) = %ProgramFiles%\MyCorp\MyApp.exe,-2
```

<span data-ttu-id="10195-155">Notez que, bien que la syntaxe soit similaire aux entrées LocalizedString et info-bulle présentées précédemment, aucun caractère « @ » n’est utilisé comme préfixe dans l' \_ entrée reg SZ ou reg \_ expand \_ SZ qui spécifie le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="10195-155">Note that while the syntax is otherwise similar to the LocalizedString and InfoTip entries discussed earlier, no '@' character is used as a prefix in the REG\_SZ or REG\_EXPAND\_SZ entry that specifies the path.</span></span>

### <a name="step-5"></a><span data-ttu-id="10195-156">Étape 5 :</span><span class="sxs-lookup"><span data-stu-id="10195-156">Step 5:</span></span>

<span data-ttu-id="10195-157">Ajoutez les informations suivantes au registre pour fournir la commande appelée par le système lorsque l’utilisateur ouvre le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="10195-157">Add the following information to the registry to provide the command that is called by the system when the user opens the Control Panel.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         Shell
            Open
               Command
                  (Default) = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp.exe /Settings
```

## <a name="related-topics"></a><span data-ttu-id="10195-158">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="10195-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10195-159">Inscription des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="10195-159">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="10195-160">Comment inscrire les éléments du panneau de configuration de la DLL</span><span class="sxs-lookup"><span data-stu-id="10195-160">How To Register DLL Control Panel Items</span></span>](how-to-register-dll-control-panel-item-registration-.md)
</dt> </dl>

 

 



