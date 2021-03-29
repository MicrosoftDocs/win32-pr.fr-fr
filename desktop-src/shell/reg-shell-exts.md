---
description: Un objet de gestionnaire d’extensions d’interpréteur de commandes doit être inscrit pour que l’interpréteur de commandes puisse l’utiliser. Cette rubrique est une discussion générale sur l’enregistrement d’un gestionnaire d’extensions de Shell.
ms.assetid: e4b98c18-746b-4909-8821-f25de9d15373
title: Inscription des gestionnaires d’extensions de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca50bfaff984884b74ecc8572d4af9d96c55d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973474"
---
# <a name="registering-shell-extension-handlers"></a><span data-ttu-id="de53f-104">Inscription des gestionnaires d’extensions de Shell</span><span class="sxs-lookup"><span data-stu-id="de53f-104">Registering Shell Extension Handlers</span></span>

<span data-ttu-id="de53f-105">Un objet de gestionnaire d’extensions d’interpréteur de commandes doit être inscrit pour que l’interpréteur de commandes puisse l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="de53f-105">A Shell extension handler object must be registered before the Shell can use it.</span></span> <span data-ttu-id="de53f-106">Cette rubrique est une discussion générale sur l’enregistrement d’un gestionnaire d’extensions de Shell.</span><span class="sxs-lookup"><span data-stu-id="de53f-106">This topic is a general discussion of how to register a Shell extension handler.</span></span>

<span data-ttu-id="de53f-107">Chaque fois que vous créez ou modifiez un gestionnaire d’extensions de Shell, il est important d’informer le système que vous avez apporté une modification.</span><span class="sxs-lookup"><span data-stu-id="de53f-107">Any time you create or change a Shell extension handler, it is important to notify the system that you have made a change.</span></span> <span data-ttu-id="de53f-108">Pour ce faire, appelez [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), en spécifiant l’événement **\_ ASSOCCHANGED SHCNE** .</span><span class="sxs-lookup"><span data-stu-id="de53f-108">Do so by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specifying the **SHCNE\_ASSOCCHANGED** event.</span></span> <span data-ttu-id="de53f-109">Si vous n’appelez pas **SHChangeNotify**, la modification peut ne pas être reconnue tant que le système n’est pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="de53f-109">If you do not call **SHChangeNotify**, the change might not be recognized until the system is rebooted.</span></span>

<span data-ttu-id="de53f-110">Certains facteurs supplémentaires s’appliquent aux systèmes Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="de53f-110">There are some additional factors that apply to Windows 2000 systems.</span></span> <span data-ttu-id="de53f-111">Pour plus d’informations, consultez la section [inscription du gestionnaire d’extensions de Shell sur les systèmes Windows 2000](#registering-shell-extension-handlers) .</span><span class="sxs-lookup"><span data-stu-id="de53f-111">For details, see the [Registering Shell Extension Handlers on Windows 2000 Systems](#registering-shell-extension-handlers) section.</span></span>

<span data-ttu-id="de53f-112">Comme pour tous les objets COM (Component Object Model), vous devez créer un GUID pour le gestionnaire à l’aide d’un outil tel que Guidgen.exe, fourni avec le kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="de53f-112">As with all Component Object Model (COM) objects, you must create a GUID for the handler using a tool such as Guidgen.exe, which is provided with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="de53f-113">Créez une sous-clé sous le CLSID **\_ \_ racine des classes HKEY** \\  dont le nom est le format de chaîne de ce GUID.</span><span class="sxs-lookup"><span data-stu-id="de53f-113">Create a subkey under **HKEY\_CLASSES\_ROOT**\\**CLSID** whose name is the string form of that GUID.</span></span> <span data-ttu-id="de53f-114">Étant donné que les gestionnaires d’extensions de Shell sont des serveurs in-process, vous devez également créer une sous-clé **InprocServer32** sous la sous-clé de GUID avec la valeur (par défaut) définie sur le chemin d’accès de la dll du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="de53f-114">Because Shell extension handlers are in-process servers, you also must create an **InprocServer32** subkey under that GUID subkey with the (Default) value set to the path of the handler's DLL.</span></span> <span data-ttu-id="de53f-115">Utilisez le modèle de thread cloisonné.</span><span class="sxs-lookup"><span data-stu-id="de53f-115">Use the apartment threading model.</span></span> <span data-ttu-id="de53f-116">En voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="de53f-116">An example is shown here:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {00021500-0000-0000-C000-000000000046}
         InprocServer32
            (Default) = %windir%\System32\Example.dll
            ThreadingModel = Apartment
```

<span data-ttu-id="de53f-117">Chaque fois que l’interpréteur de commandes prend une mesure qui peut impliquer un gestionnaire d’extensions de Shell, il vérifie la sous-clé de registre appropriée.</span><span class="sxs-lookup"><span data-stu-id="de53f-117">Any time the Shell takes an action that can involve a Shell extension handler, it checks the appropriate registry subkey.</span></span> <span data-ttu-id="de53f-118">Sous-clé sous laquelle un gestionnaire d’extensions est inscrit contrôle quand il sera appelé.</span><span class="sxs-lookup"><span data-stu-id="de53f-118">The subkey under which an extension handler is registered controls when it will be called.</span></span> <span data-ttu-id="de53f-119">Par exemple, il est courant d’avoir un gestionnaire de menu contextuel appelé lorsque l’interpréteur de commandes affiche un menu contextuel pour un membre d’un [type de fichier](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="de53f-119">For instance, it is a common practice to have a shortcut menu handler called when the Shell displays a shortcut menu for a member of a [file type](fa-file-types.md).</span></span> <span data-ttu-id="de53f-120">Dans ce cas, le gestionnaire doit être inscrit sous la sous-clé **ProgID** du type de fichier.</span><span class="sxs-lookup"><span data-stu-id="de53f-120">In this case, the handler must be registered under the file type's **ProgID** subkey.</span></span>

<span data-ttu-id="de53f-121">Cette rubrique traite des sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="de53f-121">This topic discusses the following subjects:</span></span>

-   [<span data-ttu-id="de53f-122">Noms de gestionnaires</span><span class="sxs-lookup"><span data-stu-id="de53f-122">Handler Names</span></span>](#handler-names)
-   [<span data-ttu-id="de53f-123">Objets Shell prédéfinis</span><span class="sxs-lookup"><span data-stu-id="de53f-123">Predefined Shell Objects</span></span>](#predefined-shell-objects)
-   [<span data-ttu-id="de53f-124">Exemple d’inscription d’un gestionnaire d’extensions</span><span class="sxs-lookup"><span data-stu-id="de53f-124">Example of an Extension Handler Registration</span></span>](#example-of-an-extension-handler-registration)
    -   [<span data-ttu-id="de53f-125">Inscription des gestionnaires d’extensions de Shell</span><span class="sxs-lookup"><span data-stu-id="de53f-125">Registering Shell Extension Handlers</span></span>](#registering-shell-extension-handlers)
-   [<span data-ttu-id="de53f-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="de53f-126">Related topics</span></span>](#related-topics)

## <a name="handler-names"></a><span data-ttu-id="de53f-127">Noms de gestionnaires</span><span class="sxs-lookup"><span data-stu-id="de53f-127">Handler Names</span></span>

<span data-ttu-id="de53f-128">Pour activer un gestionnaire d’extensions de Shell, créez une sous-clé avec le nom de la sous-clé du gestionnaire (voir ci-dessous) sous la sous-clé **shellex** du **ProgID** (pour les types de fichiers) ou du nom du type d’objet Shell (pour les [ \_ \_ objets Shell prédéfinis](handlers.md)).</span><span class="sxs-lookup"><span data-stu-id="de53f-128">To enable a Shell extension handler, create a subkey with the handler subkey name (see below) under the **ShellEx** subkey of either the **ProgID** (for file types) or the Shell object type name (for [predefined\_shell\_objects](handlers.md)).</span></span>

<span data-ttu-id="de53f-129">Par exemple, si vous souhaitez inscrire un gestionnaire d’extension de menu contextuel pour MyProgram. 1, commencez par créer la sous-clé suivante :</span><span class="sxs-lookup"><span data-stu-id="de53f-129">For example, if you wanted to register a shortcut menu extension handler for MyProgram.1, you begin by creating the following subkey:</span></span>

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

<span data-ttu-id="de53f-130">Pour les gestionnaires suivants, créez une sous-clé sous la sous-clé « nom de la sous-clé du gestionnaire » nommée comme version de chaîne de l’identificateur de classe (CLSID) de l’extension de Shell.</span><span class="sxs-lookup"><span data-stu-id="de53f-130">For the following handlers, create a subkey underneath the "Handler Subkey name" subkey named as the string version of the class identifier (CLSID) of the Shell extension.</span></span> <span data-ttu-id="de53f-131">Plusieurs extensions peuvent être inscrites sous le nom de la sous-clé du gestionnaire en créant plusieurs sous-clés.</span><span class="sxs-lookup"><span data-stu-id="de53f-131">Multiple extensions can be registered under the handler subkey name by creating multiple subkeys.</span></span>



| <span data-ttu-id="de53f-132">Handler</span><span class="sxs-lookup"><span data-stu-id="de53f-132">Handler</span></span>                 | <span data-ttu-id="de53f-133">Interface</span><span class="sxs-lookup"><span data-stu-id="de53f-133">Interface</span></span>          | <span data-ttu-id="de53f-134">Nom de la sous-clé du gestionnaire</span><span class="sxs-lookup"><span data-stu-id="de53f-134">Handler Subkey Name</span></span>       |
|-------------------------|--------------------|---------------------------|
| <span data-ttu-id="de53f-135">Gestionnaire de fournisseur de colonne</span><span class="sxs-lookup"><span data-stu-id="de53f-135">Column provider handler</span></span> | <span data-ttu-id="de53f-136">IColumnProvider</span><span class="sxs-lookup"><span data-stu-id="de53f-136">IColumnProvider</span></span>    | <span data-ttu-id="de53f-137">**ColumnHandlers**</span><span class="sxs-lookup"><span data-stu-id="de53f-137">**ColumnHandlers**</span></span>        |
| <span data-ttu-id="de53f-138">Gestionnaire de menu contextuel</span><span class="sxs-lookup"><span data-stu-id="de53f-138">Shortcut menu handler</span></span>   | <span data-ttu-id="de53f-139">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="de53f-139">IContextMenu</span></span>       | <span data-ttu-id="de53f-140">**ContextMenuHandlers**</span><span class="sxs-lookup"><span data-stu-id="de53f-140">**ContextMenuHandlers**</span></span>   |
| <span data-ttu-id="de53f-141">Gestionnaire CopyHook</span><span class="sxs-lookup"><span data-stu-id="de53f-141">Copyhook handler</span></span>        | <span data-ttu-id="de53f-142">ICopyHook</span><span class="sxs-lookup"><span data-stu-id="de53f-142">ICopyHook</span></span>          | <span data-ttu-id="de53f-143">**CopyHookHandlers**</span><span class="sxs-lookup"><span data-stu-id="de53f-143">**CopyHookHandlers**</span></span>      |
| <span data-ttu-id="de53f-144">Gestionnaire de glisser-déplacer</span><span class="sxs-lookup"><span data-stu-id="de53f-144">Drag-and-drop handler</span></span>   | <span data-ttu-id="de53f-145">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="de53f-145">IContextMenu</span></span>       | <span data-ttu-id="de53f-146">**DragDropHandlers**</span><span class="sxs-lookup"><span data-stu-id="de53f-146">**DragDropHandlers**</span></span>      |
| <span data-ttu-id="de53f-147">Gestionnaire de feuille de propriétés</span><span class="sxs-lookup"><span data-stu-id="de53f-147">Property sheet handler</span></span>  | <span data-ttu-id="de53f-148">IShellPropSheetExt</span><span class="sxs-lookup"><span data-stu-id="de53f-148">IShellPropSheetExt</span></span> | <span data-ttu-id="de53f-149">**PropertySheetHandlers**</span><span class="sxs-lookup"><span data-stu-id="de53f-149">**PropertySheetHandlers**</span></span> |



 

<span data-ttu-id="de53f-150">Pour les gestionnaires suivants, la valeur par défaut de la clé « nom de la sous-clé du gestionnaire » est la version de chaîne du CLSID de l’extension de Shell.</span><span class="sxs-lookup"><span data-stu-id="de53f-150">For the following handlers, the default value of the "Handler Subkey Name" key is the string version of the CLSID of the Shell extension.</span></span> <span data-ttu-id="de53f-151">Une seule extension peut être inscrite pour ces gestionnaires.</span><span class="sxs-lookup"><span data-stu-id="de53f-151">Only one extension can be registered for these handlers.</span></span>



| <span data-ttu-id="de53f-152">Handler</span><span class="sxs-lookup"><span data-stu-id="de53f-152">Handler</span></span>                 | <span data-ttu-id="de53f-153">Interface</span><span class="sxs-lookup"><span data-stu-id="de53f-153">Interface</span></span>            | <span data-ttu-id="de53f-154">Nom de la sous-clé du gestionnaire</span><span class="sxs-lookup"><span data-stu-id="de53f-154">Handler Subkey Name</span></span>                        |
|-------------------------|----------------------|--------------------------------------------|
| <span data-ttu-id="de53f-155">Gestionnaire de données</span><span class="sxs-lookup"><span data-stu-id="de53f-155">Data handler</span></span>            | <span data-ttu-id="de53f-156">IDataObject</span><span class="sxs-lookup"><span data-stu-id="de53f-156">IDataObject</span></span>          | <span data-ttu-id="de53f-157">**DataHandler**</span><span class="sxs-lookup"><span data-stu-id="de53f-157">**DataHandler**</span></span>                            |
| <span data-ttu-id="de53f-158">Supprimer le gestionnaire</span><span class="sxs-lookup"><span data-stu-id="de53f-158">Drop handler</span></span>            | <span data-ttu-id="de53f-159">IDropTarget</span><span class="sxs-lookup"><span data-stu-id="de53f-159">IDropTarget</span></span>          | <span data-ttu-id="de53f-160">**DropHandler**</span><span class="sxs-lookup"><span data-stu-id="de53f-160">**DropHandler**</span></span>                            |
| <span data-ttu-id="de53f-161">Gestionnaire d’icône</span><span class="sxs-lookup"><span data-stu-id="de53f-161">Icon handler</span></span>            | <span data-ttu-id="de53f-162">IExtractIconA/W</span><span class="sxs-lookup"><span data-stu-id="de53f-162">IExtractIconA/W</span></span>      | <span data-ttu-id="de53f-163">**IconHandler**</span><span class="sxs-lookup"><span data-stu-id="de53f-163">**IconHandler**</span></span>                            |
| <span data-ttu-id="de53f-164">Gestionnaire d’images miniatures</span><span class="sxs-lookup"><span data-stu-id="de53f-164">Thumbnail image handler</span></span> | <span data-ttu-id="de53f-165">IThumbnailProvider</span><span class="sxs-lookup"><span data-stu-id="de53f-165">IThumbnailProvider</span></span>   | <span data-ttu-id="de53f-166">**{E357FCCD-A995-4576-B01F-234630154E96}**</span><span class="sxs-lookup"><span data-stu-id="de53f-166">**{E357FCCD-A995-4576-B01F-234630154E96}**</span></span> |
| <span data-ttu-id="de53f-167">Gestionnaire d'info-bulle</span><span class="sxs-lookup"><span data-stu-id="de53f-167">Infotip handler</span></span>         | <span data-ttu-id="de53f-168">IQueryInfo</span><span class="sxs-lookup"><span data-stu-id="de53f-168">IQueryInfo</span></span>           | <span data-ttu-id="de53f-169">**{00021500-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="de53f-169">**{00021500-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="de53f-170">Lien de Shell (ANSI)</span><span class="sxs-lookup"><span data-stu-id="de53f-170">Shell link (ANSI)</span></span>       | <span data-ttu-id="de53f-171">IShellLinkA</span><span class="sxs-lookup"><span data-stu-id="de53f-171">IShellLinkA</span></span>          | <span data-ttu-id="de53f-172">**{000214EE-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="de53f-172">**{000214EE-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="de53f-173">Lien de Shell (UNICODE)</span><span class="sxs-lookup"><span data-stu-id="de53f-173">Shell link (UNICODE)</span></span>    | <span data-ttu-id="de53f-174">IShellLinkW</span><span class="sxs-lookup"><span data-stu-id="de53f-174">IShellLinkW</span></span>          | <span data-ttu-id="de53f-175">**{000214F9-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="de53f-175">**{000214F9-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="de53f-176">Stockage structuré</span><span class="sxs-lookup"><span data-stu-id="de53f-176">Structured storage</span></span>      | <span data-ttu-id="de53f-177">IStorage</span><span class="sxs-lookup"><span data-stu-id="de53f-177">IStorage</span></span>             | <span data-ttu-id="de53f-178">**{0000000B-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="de53f-178">**{0000000B-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="de53f-179">Métadonnées</span><span class="sxs-lookup"><span data-stu-id="de53f-179">Metadata</span></span>                | <span data-ttu-id="de53f-180">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="de53f-180">IPropertySetStorage</span></span>  | <span data-ttu-id="de53f-181">**PropertyHandler**</span><span class="sxs-lookup"><span data-stu-id="de53f-181">**PropertyHandler**</span></span>                        |
| <span data-ttu-id="de53f-182">Épingler au menu Démarrer</span><span class="sxs-lookup"><span data-stu-id="de53f-182">Pin to Start Menu</span></span>       | <span data-ttu-id="de53f-183">IStartMenuPinnedList</span><span class="sxs-lookup"><span data-stu-id="de53f-183">IStartMenuPinnedList</span></span> | <span data-ttu-id="de53f-184">**{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}**</span><span class="sxs-lookup"><span data-stu-id="de53f-184">**{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}**</span></span> |
| <span data-ttu-id="de53f-185">Épingler à la barre des tâches</span><span class="sxs-lookup"><span data-stu-id="de53f-185">Pin to Taskbar</span></span>          |                      | <span data-ttu-id="de53f-186">**{90AA3A4E-1CBA-4233-B8BB-535773D48449}**</span><span class="sxs-lookup"><span data-stu-id="de53f-186">**{90AA3A4E-1CBA-4233-B8BB-535773D48449}**</span></span> |



 

<span data-ttu-id="de53f-187">Les sous-clés spécifiées pour ajouter **Épingler au menu Démarrer** et **Épingler à la barre des tâches** dans le menu contextuel d’un élément ne sont nécessaires que pour les types de fichiers qui incluent l’entrée [IsShortCut](./links.md) .</span><span class="sxs-lookup"><span data-stu-id="de53f-187">The subkeys specified to add **Pin to Start Menu** and **Pin to Taskbar** to an item's shortcut menu are only required for file types that include the [IsShortCut](./links.md) entry.</span></span>

## <a name="predefined-shell-objects"></a><span data-ttu-id="de53f-188">Objets Shell prédéfinis</span><span class="sxs-lookup"><span data-stu-id="de53f-188">Predefined Shell Objects</span></span>

<span data-ttu-id="de53f-189">L’interpréteur de commandes définit des objets supplémentaires sous la **\_ \_ racine HKEY classes** qui peuvent être étendus de la même façon que les types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="de53f-189">The Shell defines additional objects under **HKEY\_CLASSES\_ROOT** which can be extended in the same way as file types.</span></span> <span data-ttu-id="de53f-190">Par exemple, pour ajouter un gestionnaire de feuille de propriétés pour tous les fichiers, vous pouvez vous inscrire sous la sous-clé **PropertySheetHandlers** .</span><span class="sxs-lookup"><span data-stu-id="de53f-190">For example, to add a property sheet handler for all files, you can register under the **PropertySheetHandlers** subkey.</span></span>

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

<span data-ttu-id="de53f-191">Le tableau suivant indique les différentes sous-clés de la **\_ \_ racine de la classe HKEY** sous lesquelles les gestionnaires d’extension peuvent être inscrits.</span><span class="sxs-lookup"><span data-stu-id="de53f-191">The following table gives the various subkeys of **HKEY\_CLASSES\_ROOT** under which extension handlers can be registered.</span></span> <span data-ttu-id="de53f-192">Notez que de nombreux gestionnaires d’extension ne peuvent pas être enregistrés sous toutes les sous-clés répertoriées.</span><span class="sxs-lookup"><span data-stu-id="de53f-192">Note that many extension handlers cannot be registered under all of the listed subkeys.</span></span> <span data-ttu-id="de53f-193">Pour plus d’informations, consultez la documentation du gestionnaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="de53f-193">For further details, see the specific handler's documentation.</span></span>



| <span data-ttu-id="de53f-194">Sous-clé</span><span class="sxs-lookup"><span data-stu-id="de53f-194">Subkey</span></span>                    | <span data-ttu-id="de53f-195">Description</span><span class="sxs-lookup"><span data-stu-id="de53f-195">Description</span></span>                                                          | <span data-ttu-id="de53f-196">Gestionnaires possibles</span><span class="sxs-lookup"><span data-stu-id="de53f-196">Possible Handlers</span></span>                                |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="de53f-197">\**\** _</span><span class="sxs-lookup"><span data-stu-id="de53f-197">\**\** _</span></span>                    | <span data-ttu-id="de53f-198">Tous les fichiers</span><span class="sxs-lookup"><span data-stu-id="de53f-198">All files</span></span>                                                            | <span data-ttu-id="de53f-199">Menu contextuel, feuille de propriétés, verbes (voir ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="de53f-199">Shortcut Menu, Property Sheet, Verbs (see below)</span></span> |
| <span data-ttu-id="de53f-200">_ *AllFileSystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="de53f-200">_ *AllFileSystemObjects*\*</span></span>  | <span data-ttu-id="de53f-201">Tous les fichiers et dossiers de fichiers</span><span class="sxs-lookup"><span data-stu-id="de53f-201">All files and file folders</span></span>                                           | <span data-ttu-id="de53f-202">Menu contextuel, feuille de propriétés, verbes</span><span class="sxs-lookup"><span data-stu-id="de53f-202">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="de53f-203">**Folder**</span><span class="sxs-lookup"><span data-stu-id="de53f-203">**Folder**</span></span>                | <span data-ttu-id="de53f-204">Tous les dossiers</span><span class="sxs-lookup"><span data-stu-id="de53f-204">All folders</span></span>                                                          | <span data-ttu-id="de53f-205">Menu contextuel, feuille de propriétés, verbes</span><span class="sxs-lookup"><span data-stu-id="de53f-205">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="de53f-206">**Directory**</span><span class="sxs-lookup"><span data-stu-id="de53f-206">**Directory**</span></span>             | <span data-ttu-id="de53f-207">Dossiers de fichiers</span><span class="sxs-lookup"><span data-stu-id="de53f-207">File folders</span></span>                                                         | <span data-ttu-id="de53f-208">Menu contextuel, feuille de propriétés, verbes</span><span class="sxs-lookup"><span data-stu-id="de53f-208">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="de53f-209">**\\Arrière-plan du répertoire**</span><span class="sxs-lookup"><span data-stu-id="de53f-209">**Directory\\Background**</span></span> | <span data-ttu-id="de53f-210">Arrière-plan du dossier de fichiers</span><span class="sxs-lookup"><span data-stu-id="de53f-210">File folder background</span></span>                                               | <span data-ttu-id="de53f-211">Menu contextuel uniquement</span><span class="sxs-lookup"><span data-stu-id="de53f-211">Shortcut Menu only</span></span>                               |
| <span data-ttu-id="de53f-212">**DesktopBackground**</span><span class="sxs-lookup"><span data-stu-id="de53f-212">**DesktopBackground**</span></span>     | <span data-ttu-id="de53f-213">Arrière-plan du Bureau (Windows 7 et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="de53f-213">Desktop background (Windows 7 and higher)</span></span>                            | <span data-ttu-id="de53f-214">Menu contextuel, verbes</span><span class="sxs-lookup"><span data-stu-id="de53f-214">Shortcut Menu, Verbs</span></span>                             |
| <span data-ttu-id="de53f-215">**Lecteur**</span><span class="sxs-lookup"><span data-stu-id="de53f-215">**Drive**</span></span>                 | <span data-ttu-id="de53f-216">Tous les lecteurs dans MyComputer, tels que « C : \\ »</span><span class="sxs-lookup"><span data-stu-id="de53f-216">All drives in MyComputer, such as "C:\\"</span></span>                             | <span data-ttu-id="de53f-217">Menu contextuel, feuille de propriétés, verbes</span><span class="sxs-lookup"><span data-stu-id="de53f-217">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="de53f-218">**Réseau**</span><span class="sxs-lookup"><span data-stu-id="de53f-218">**Network**</span></span>               | <span data-ttu-id="de53f-219">Tout le réseau (sous Favoris réseau)</span><span class="sxs-lookup"><span data-stu-id="de53f-219">Entire network (under My Network Places)</span></span>                             | <span data-ttu-id="de53f-220">Menu contextuel, feuille de propriétés, verbes</span><span class="sxs-lookup"><span data-stu-id="de53f-220">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="de53f-221">**Type de réseau \\\\\#**</span><span class="sxs-lookup"><span data-stu-id="de53f-221">**Network\\Type\\\#**</span></span>     | <span data-ttu-id="de53f-222">Tous les objets de type \# (voir ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="de53f-222">All objects of type \# (see below)</span></span>                                   | <span data-ttu-id="de53f-223">Menu contextuel, feuille de propriétés, verbes</span><span class="sxs-lookup"><span data-stu-id="de53f-223">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="de53f-224">**NetShare**</span><span class="sxs-lookup"><span data-stu-id="de53f-224">**NetShare**</span></span>              | <span data-ttu-id="de53f-225">Tous les partages réseau</span><span class="sxs-lookup"><span data-stu-id="de53f-225">All network shares</span></span>                                                   | <span data-ttu-id="de53f-226">Menu contextuel, feuille de propriétés, verbes</span><span class="sxs-lookup"><span data-stu-id="de53f-226">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="de53f-227">**Serveur netserver**</span><span class="sxs-lookup"><span data-stu-id="de53f-227">**NetServer**</span></span>             | <span data-ttu-id="de53f-228">Tous les serveurs réseau</span><span class="sxs-lookup"><span data-stu-id="de53f-228">All network servers</span></span>                                                  | <span data-ttu-id="de53f-229">Menu contextuel, feuille de propriétés, verbes</span><span class="sxs-lookup"><span data-stu-id="de53f-229">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="de53f-230">*\_nom du fournisseur réseau \_*</span><span class="sxs-lookup"><span data-stu-id="de53f-230">*network\_provider\_name*</span></span> | <span data-ttu-id="de53f-231">Tous les objets fournis par le fournisseur réseau «*\_ \_ nom du fournisseur réseau*»</span><span class="sxs-lookup"><span data-stu-id="de53f-231">All objects provided by network provider "*network\_provider\_name*"</span></span> | <span data-ttu-id="de53f-232">Menu contextuel, feuille de propriétés, verbes</span><span class="sxs-lookup"><span data-stu-id="de53f-232">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="de53f-233">**Imprimantes**</span><span class="sxs-lookup"><span data-stu-id="de53f-233">**Printers**</span></span>              | <span data-ttu-id="de53f-234">Toutes les imprimantes</span><span class="sxs-lookup"><span data-stu-id="de53f-234">All printers</span></span>                                                         | <span data-ttu-id="de53f-235">Menu contextuel, feuille de propriétés</span><span class="sxs-lookup"><span data-stu-id="de53f-235">Shortcut Menu, Property Sheet</span></span>                    |
| <span data-ttu-id="de53f-236">**AudioCD**</span><span class="sxs-lookup"><span data-stu-id="de53f-236">**AudioCD**</span></span>               | <span data-ttu-id="de53f-237">CD audio dans le lecteur CD</span><span class="sxs-lookup"><span data-stu-id="de53f-237">Audio CD in CD drive</span></span>                                                 | <span data-ttu-id="de53f-238">Verbes uniquement</span><span class="sxs-lookup"><span data-stu-id="de53f-238">Verbs only</span></span>                                       |
| <span data-ttu-id="de53f-239">**DVD**</span><span class="sxs-lookup"><span data-stu-id="de53f-239">**DVD**</span></span>                   | <span data-ttu-id="de53f-240">Lecteur de DVD (Windows 2000)</span><span class="sxs-lookup"><span data-stu-id="de53f-240">DVD drive (Windows 2000)</span></span>                                             | <span data-ttu-id="de53f-241">Menu contextuel, feuille de propriétés, verbes</span><span class="sxs-lookup"><span data-stu-id="de53f-241">Shortcut Menu, Property Sheet, Verbs</span></span>             |



 

### <a name="notes"></a><span data-ttu-id="de53f-242">Notes</span><span class="sxs-lookup"><span data-stu-id="de53f-242">Notes</span></span>

-   <span data-ttu-id="de53f-243">Le menu contextuel de l’arrière-plan du dossier de fichiers est accessible en cliquant avec le bouton droit dans un dossier de fichiers, mais pas sur le contenu du dossier.</span><span class="sxs-lookup"><span data-stu-id="de53f-243">The file folder background shortcut menu is accessed by right-clicking within a file folder, but not over any of the folder's contents.</span></span>
-   <span data-ttu-id="de53f-244">Les « verbes » sont des commandes spéciales **inscrites sous le \_ \_** verbe de Shell de la \\ *sous-clé* de l' \\ **interpréteur** de commandes \\ .</span><span class="sxs-lookup"><span data-stu-id="de53f-244">"Verbs" are special commands registered under **HKEY\_CLASSES\_ROOT**\\*Subkey*\\**Shell**\\**Verb**.</span></span>
-   <span data-ttu-id="de53f-245">Pour le type de **réseau** \\  \\ **\#** , « \# » est un code de type de fournisseur réseau au format décimal.</span><span class="sxs-lookup"><span data-stu-id="de53f-245">For **Network**\\**Type**\\**\#**, "\#" is a network provider type code in decimal.</span></span> <span data-ttu-id="de53f-246">Le code du type de fournisseur réseau est le mot de poids fort d’un type de réseau.</span><span class="sxs-lookup"><span data-stu-id="de53f-246">The network provider type code is the high word of a network type.</span></span> <span data-ttu-id="de53f-247">La liste des types de réseau est fournie dans le fichier d’en-tête Winnetwk. h ( \_ valeurs net WNNC \_ \* ).</span><span class="sxs-lookup"><span data-stu-id="de53f-247">The list of network types is given in the Winnetwk.h header file (WNNC\_NET\_\* values).</span></span> <span data-ttu-id="de53f-248">Par exemple, WNNC \_ NET \_ Shiva est 0x00330000. par conséquent, la sous-clé de type correspondante serait de type **HKEY \_ classes \_ racine** de \\  \\ **type** \\ **51**.</span><span class="sxs-lookup"><span data-stu-id="de53f-248">For example, WNNC\_NET\_SHIVA is 0x00330000, so the corresponding type subkey would be **HKEY\_CLASSES\_ROOT**\\**Network**\\**Type**\\**51**.</span></span>
-   <span data-ttu-id="de53f-249">«*\_ \_ nom du fournisseur réseau*» est un nom de fournisseur réseau spécifié par [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), avec les espaces convertis en traits de soulignement.</span><span class="sxs-lookup"><span data-stu-id="de53f-249">"*network\_provider\_name*" is a network provider name as specified by [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), with the spaces converted into underscores.</span></span> <span data-ttu-id="de53f-250">Par exemple, si le fournisseur réseau de réseau Microsoft est installé, son nom de fournisseur est « Microsoft Windows Network » et le *\_ \_ nom du fournisseur réseau* correspondant est **Microsoft \_ Windows \_ Network**.</span><span class="sxs-lookup"><span data-stu-id="de53f-250">For example, if the Microsoft Networking network provider is installed, its provider name is "Microsoft Windows Network", and the corresponding *network\_provider\_name* is **Microsoft\_Windows\_Network**.</span></span>

## <a name="example-of-an-extension-handler-registration"></a><span data-ttu-id="de53f-251">Exemple d’inscription d’un gestionnaire d’extensions</span><span class="sxs-lookup"><span data-stu-id="de53f-251">Example of an Extension Handler Registration</span></span>

<span data-ttu-id="de53f-252">Pour activer un gestionnaire spécifique, créez une sous-clé sous la sous-clé de type de gestionnaire d’extension avec le nom du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="de53f-252">To enable a particular handler, create a subkey under the extension handler type subkey with the name of the handler.</span></span> <span data-ttu-id="de53f-253">L’interpréteur de commandes n’utilise pas le nom du gestionnaire, mais il doit être différent de tous les autres noms sous cette sous-clé de type.</span><span class="sxs-lookup"><span data-stu-id="de53f-253">The Shell does not use the handler's name, but it must be different from all other names under that type subkey.</span></span> <span data-ttu-id="de53f-254">Définissez la valeur par défaut de la sous-clé Name sur la forme de chaîne du GUID du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="de53f-254">Set the default value of the name subkey to the string form of the handler's GUID.</span></span>

<span data-ttu-id="de53f-255">L’exemple suivant illustre les entrées de Registre qui activent les gestionnaires d’extensions de menu contextuel et de feuille de propriétés, à l’aide d’un exemple de type de fichier. MYP.</span><span class="sxs-lookup"><span data-stu-id="de53f-255">The following example illustrates registry entries that enable shortcut menu and property sheet extension handlers, using an example .myp file type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
      {11111111-2222-3333-4444-555555555555}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      Shellex
         ContextMenuHandler
            MyCommand
               (Default) = {00000000-1111-2222-3333-444444444444}
         PropertySheetHandlers
            MyPropSheet
               (Default) = {11111111-2222-3333-4444-555555555555}
```

### <a name="registering-shell-extension-handlers"></a><span data-ttu-id="de53f-256">Inscription des gestionnaires d’extensions de Shell</span><span class="sxs-lookup"><span data-stu-id="de53f-256">Registering Shell Extension Handlers</span></span>

<span data-ttu-id="de53f-257">La procédure d’inscription décrite dans cette section doit être suivie pour tous les systèmes Windows.</span><span class="sxs-lookup"><span data-stu-id="de53f-257">The registration procedure discussed in this section must be followed for all Windows systems.</span></span> <span data-ttu-id="de53f-258">Toutefois, avec les systèmes ultérieurs, une étape supplémentaire peut être nécessaire.</span><span class="sxs-lookup"><span data-stu-id="de53f-258">However, with later systems, an additional step might be necessary.</span></span> <span data-ttu-id="de53f-259">Étant donné que ces versions ultérieures de Windows sont conçues pour être utilisées dans un environnement géré, l’accès au registre peut être limité administrativement, ce qui nécessite une approche quelque peu différente de celle décrite dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="de53f-259">Because these later versions of Windows are designed to be used in a managed environment, access to the registry could be administratively restricted, requiring a somewhat different approach to installation than described in the previous section.</span></span>

> [!Note]  
> <span data-ttu-id="de53f-260">Les programmes d’installation ne doivent généralement pas écrire directement dans le registre.</span><span class="sxs-lookup"><span data-stu-id="de53f-260">Setup programs should generally not write directly to the registry.</span></span> <span data-ttu-id="de53f-261">Au lieu de cela, le programme d’installation doit être effectué avec Windows Installer packages.</span><span class="sxs-lookup"><span data-stu-id="de53f-261">Instead, setup should be accomplished with Windows Installer packages.</span></span> <span data-ttu-id="de53f-262">Ces outils garantissent que les logiciels s’exécutent correctement et fournissent un accès à des fonctionnalités telles que l’inscription de classe par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="de53f-262">These tools ensure that software runs well and provides access to capabilities such as per-user class registration.</span></span>

 

<span data-ttu-id="de53f-263">Les gestionnaires d’extensions de Shell s’exécutent dans le processus de Shell.</span><span class="sxs-lookup"><span data-stu-id="de53f-263">Shell extension handlers run in the Shell process.</span></span> <span data-ttu-id="de53f-264">Étant donné qu’il s’agit d’un processus système, l’administrateur d’un système peut limiter les gestionnaires d’extension d’environnement à ceux d’une liste approuvée en définissant la valeur EnforceShellExtensionSecurity de la clé de l' **Explorateur** sur 1 comme indiqué ici :</span><span class="sxs-lookup"><span data-stu-id="de53f-264">Because it is a system process, the administrator of a system can limit Shell extension handlers to those on an approved list by setting the EnforceShellExtensionSecurity value of the **Explorer** key to 1 as shown here:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
                     EnforceShellExtensionSecurity = 1
```

<span data-ttu-id="de53f-265">Pour placer un gestionnaire d’extensions de Shell dans la liste approuvée, créez une valeur **reg \_ SZ** dont le nom correspond à la chaîne du GUID du gestionnaire sous la sous-clé **approuvée** .</span><span class="sxs-lookup"><span data-stu-id="de53f-265">To place a Shell extension handler on the approved list, create a **REG\_SZ** value whose name is the string form of the handler's GUID under the **Approved** subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
```

<span data-ttu-id="de53f-266">Par exemple, l’exemple suivant ajoute les gestionnaires *myCommand* et *MyPropSheet* à la liste approuvée.</span><span class="sxs-lookup"><span data-stu-id="de53f-266">For example, the following example adds the *MyCommand* and *MyPropSheet* handlers to the approved list.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
                     {00000000-1111-2222-3333-444444444444} = MyCommand
                     {11111111-2222-3333-4444-555555555555} = MyPropSheet
```

<span data-ttu-id="de53f-267">L’interpréteur de commandes n’utilise pas la valeur qui est assignée au GUID, mais il doit être configuré pour faciliter l’inspection du Registre.</span><span class="sxs-lookup"><span data-stu-id="de53f-267">The Shell does not use the value that is assigned to the GUID, but it should be set to make inspecting the registry easier.</span></span>

<span data-ttu-id="de53f-268">Votre application de configuration peut ajouter des valeurs à la sous-clé **approuvée** uniquement si la personne qui installe l’application dispose de privilèges suffisants.</span><span class="sxs-lookup"><span data-stu-id="de53f-268">Your setup application can add values to the **Approved** subkey only if the person installing the application has sufficient privileges.</span></span> <span data-ttu-id="de53f-269">Si la tentative d’ajout d’un gestionnaire d’extensions échoue, vous devez informer l’utilisateur que des privilèges d’administrateur sont nécessaires pour installer complètement l’application.</span><span class="sxs-lookup"><span data-stu-id="de53f-269">If the attempt to add an extension handler fails, you should inform the user that administrative privileges are required to fully install the application.</span></span> <span data-ttu-id="de53f-270">Si le gestionnaire est essentiel pour l’application, vous devez faire échouer le programme d’installation et demander à l’utilisateur de contacter un administrateur.</span><span class="sxs-lookup"><span data-stu-id="de53f-270">If the handler is essential to the application, you should fail the setup and notify the user to contact an administrator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de53f-271">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="de53f-271">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de53f-272">Initialisation des gestionnaires d’extensions de Shell</span><span class="sxs-lookup"><span data-stu-id="de53f-272">Initializing Shell Extension Handlers</span></span>](int-shell-exts.md)
</dt> </dl>

 

 
