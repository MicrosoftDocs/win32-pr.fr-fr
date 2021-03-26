---
description: Le shell Windows fournit un ensemble puissant d’objets Automation qui vous permettent de programmer l’interpréteur de commandes avec Microsoft Visual Basic et des langages de script tels que Microsoft JScript (compatible avec la spécification du langage ECMA 262) et Microsoft Visual Basic Scripting Edition (VBScript). Vous pouvez utiliser ces objets pour accéder à la plupart des fonctionnalités et boîtes de dialogue de l’interpréteur de commandes. Par exemple, vous pouvez accéder au système de fichiers, lancer des programmes et modifier les paramètres système.
title: Objets Shell scriptable
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09455fad-a769-42ef-83ba-b745ac819bf3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4c39e7e58a9715598056fb74aa154ed8a850f523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973606"
---
# <a name="scriptable-shell-objects"></a><span data-ttu-id="8c1f3-105">Objets Shell scriptable</span><span class="sxs-lookup"><span data-stu-id="8c1f3-105">Scriptable Shell Objects</span></span>

<span data-ttu-id="8c1f3-106">Le shell Windows fournit un ensemble puissant d’objets Automation qui vous permettent de programmer l’interpréteur de commandes avec Microsoft Visual Basic et des langages de script tels que Microsoft JScript (compatible avec la spécification du langage ECMA 262) et Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="8c1f3-106">The Windows Shell provides a powerful set of automation objects that enable you to program the Shell with Microsoft Visual Basic and scripting languages such as Microsoft JScript (compatible with ECMA 262 language specification) and Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="8c1f3-107">Vous pouvez utiliser ces objets pour accéder à la plupart des fonctionnalités et boîtes de dialogue de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-107">You can use these objects to access many of the Shell's features and dialog boxes.</span></span> <span data-ttu-id="8c1f3-108">Par exemple, vous pouvez accéder au système de fichiers, lancer des programmes et modifier les paramètres système.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-108">For example, you can access the file system, launch programs, and change system settings.</span></span>

<span data-ttu-id="8c1f3-109">Cette section présente les objets Shell scriptables.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-109">This section introduces the scriptable Shell objects.</span></span>

-   [<span data-ttu-id="8c1f3-110">Versions de Shell</span><span class="sxs-lookup"><span data-stu-id="8c1f3-110">Shell Versions</span></span>](#shell-versions)
-   [<span data-ttu-id="8c1f3-111">Instanciation d’objets Shell</span><span class="sxs-lookup"><span data-stu-id="8c1f3-111">Instantiating Shell Objects</span></span>](#instantiating-shell-objects)
    -   [<span data-ttu-id="8c1f3-112">Liaison tardive</span><span class="sxs-lookup"><span data-stu-id="8c1f3-112">Late Binding</span></span>](#late-binding)
    -   [<span data-ttu-id="8c1f3-113">Élément objet HTML</span><span class="sxs-lookup"><span data-stu-id="8c1f3-113">HTML OBJECT Element</span></span>](#html-object-element)
-   [<span data-ttu-id="8c1f3-114">Objet Shell</span><span class="sxs-lookup"><span data-stu-id="8c1f3-114">Shell Object</span></span>](#shell-object)
    -   [<span data-ttu-id="8c1f3-115">Sécurité</span><span class="sxs-lookup"><span data-stu-id="8c1f3-115">Security</span></span>](#security)
-   [<span data-ttu-id="8c1f3-116">Objets de dossier</span><span class="sxs-lookup"><span data-stu-id="8c1f3-116">Folder Objects</span></span>](#folder-objects)

## <a name="shell-versions"></a><span data-ttu-id="8c1f3-117">Versions de Shell</span><span class="sxs-lookup"><span data-stu-id="8c1f3-117">Shell Versions</span></span>

<span data-ttu-id="8c1f3-118">La plupart des objets Shell sont disponibles dans la [version 4,71](versions.md) de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-118">Many of the Shell objects became available in [version 4.71](versions.md) of the Shell.</span></span> <span data-ttu-id="8c1f3-119">D’autres sont disponibles dans la version 5,00 et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-119">Others are available in version 5.00 and later.</span></span> <span data-ttu-id="8c1f3-120">La version 5,00 est devenue disponible avec Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-120">Version 5.00 became available with Windows 2000.</span></span> <span data-ttu-id="8c1f3-121">Le tableau suivant répertorie chaque objet Shell sous la version du Shell dans lequel l’objet est devenu disponible.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-121">The following table lists each Shell object under the version of the Shell in which the object became available.</span></span>



| <span data-ttu-id="8c1f3-122">Version 4,71</span><span class="sxs-lookup"><span data-stu-id="8c1f3-122">Version 4.71</span></span>                                            | <span data-ttu-id="8c1f3-123">Version 5,00</span><span class="sxs-lookup"><span data-stu-id="8c1f3-123">Version 5.00</span></span>                                          |
|---------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="8c1f3-124">**Dossier**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-124">**Folder**</span></span>](folder.md)                                | [<span data-ttu-id="8c1f3-125">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-125">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)     |
| [<span data-ttu-id="8c1f3-126">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-126">**FolderItemVerb**</span></span>](folderitemverb.md)                | [<span data-ttu-id="8c1f3-127">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-127">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)   |
| [<span data-ttu-id="8c1f3-128">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-128">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | [<span data-ttu-id="8c1f3-129">**Dossier2**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-129">**Folder2**</span></span>](folder2-object.md)                     |
| [<span data-ttu-id="8c1f3-130">**Shell**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-130">**Shell**</span></span>](shell.md)                                  | [<span data-ttu-id="8c1f3-131">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-131">**FolderItem**</span></span>](folderitem.md)                      |
| [<span data-ttu-id="8c1f3-132">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-132">**ShellFolderView**</span></span>](shellfolderview.md)              | [<span data-ttu-id="8c1f3-133">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-133">**FolderItems**</span></span>](folderitems.md)                    |
| [<span data-ttu-id="8c1f3-134">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-134">**ShellUIHelper**</span></span>](shelluihelper.md)                  | [<span data-ttu-id="8c1f3-135">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-135">**FolderItems2**</span></span>](folderitems2-object.md)           |
| [<span data-ttu-id="8c1f3-136">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-136">**ShellWindows**</span></span>](shellwindows.md)                    | [<span data-ttu-id="8c1f3-137">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-137">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)     |
| [<span data-ttu-id="8c1f3-138">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-138">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | [<span data-ttu-id="8c1f3-139">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-139">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)     |
|                                                         | [<span data-ttu-id="8c1f3-140">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-140">**ShellFolderItem**</span></span>](shellfolderitem-object.md)     |
|                                                         | [<span data-ttu-id="8c1f3-141">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-141">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md) |
|                                                         | [<span data-ttu-id="8c1f3-142">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-142">**ShellLinkObject**</span></span>](shelllinkobject-object.md)     |



 

## <a name="instantiating-shell-objects"></a><span data-ttu-id="8c1f3-143">Instanciation d’objets Shell</span><span class="sxs-lookup"><span data-stu-id="8c1f3-143">Instantiating Shell Objects</span></span>

<span data-ttu-id="8c1f3-144">Pour instancier les objets Shell dans Visual Basic applications avec une liaison précoce, ajoutez des références aux bibliothèques suivantes dans votre projet :</span><span class="sxs-lookup"><span data-stu-id="8c1f3-144">To instantiate the Shell objects in Visual Basic applications with early binding, add references to the following libraries in your project:</span></span>

-   <span data-ttu-id="8c1f3-145">Contrôles Microsoft Internet (SHDocVw)</span><span class="sxs-lookup"><span data-stu-id="8c1f3-145">Microsoft Internet Controls (SHDocVw)</span></span>
-   <span data-ttu-id="8c1f3-146">Microsoft Shell Controls and Automation (shell32)</span><span class="sxs-lookup"><span data-stu-id="8c1f3-146">Microsoft Shell Controls and Automation (Shell32)</span></span>

### <a name="late-binding"></a><span data-ttu-id="8c1f3-147">Liaison tardive</span><span class="sxs-lookup"><span data-stu-id="8c1f3-147">Late Binding</span></span>

<span data-ttu-id="8c1f3-148">Vous pouvez également instancier un grand nombre d’objets Shell avec une liaison tardive.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-148">You can also instantiate many of the Shell objects with late binding.</span></span> <span data-ttu-id="8c1f3-149">Cette approche fonctionne dans les applications Visual Basic et dans le script.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-149">This approach works in Visual Basic applications and in script.</span></span> <span data-ttu-id="8c1f3-150">L’exemple suivant montre comment instancier l’objet [**Shell**](shell.md) dans JScript.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-150">The following example shows how to instantiate the [**Shell**](shell.md) object in JScript.</span></span>


```
<SCRIPT LANGUAGE="JScript">
<!--
    function fnCreateShell()    
    {
        // Instantiate the Shell object and invoke its FileRun method.
        var oShell = new ActiveXObject("shell.application");
        oshell.FileRun;
    }
-->
</SCRIPT>
```



<span data-ttu-id="8c1f3-151">L’exemple suivant montre comment instancier l’objet [**Folder**](folder.md) dans VBScript.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-151">The following example shows how to instantiate the [**Folder**](folder.md) object in VBScript.</span></span>


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnCreateFolder()
        dim oShell    
        dim oFolder
        dim sDir

        sDir = "C:\SomePath" 
        set oShell = CreateObject("shell.application")
        set oFolder = oShell.NameSpace(sDir)  
    end function
-->  
</SCRIPT>
```



<span data-ttu-id="8c1f3-152">Dans l’exemple précédent, *sDir* est le chemin d’accès à l’objet [**Folder**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="8c1f3-152">In the preceding example, *sDir* is the path to the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="8c1f3-153">Notez que les valeurs d’énumération [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) ne sont pas disponibles dans le script.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-153">Note that the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span>

<span data-ttu-id="8c1f3-154">Le ProgID de chacun des objets Shell est indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-154">The ProgID for each of the Shell objects is shown in the following table.</span></span>



| <span data-ttu-id="8c1f3-155">Object</span><span class="sxs-lookup"><span data-stu-id="8c1f3-155">Object</span></span>                                                  | <span data-ttu-id="8c1f3-156">ProgID</span><span class="sxs-lookup"><span data-stu-id="8c1f3-156">ProgID</span></span>                                                                                  |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c1f3-157">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-157">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="8c1f3-158">Microsoft. DiskQuota. 1</span><span class="sxs-lookup"><span data-stu-id="8c1f3-158">Microsoft.DiskQuota.1</span></span>                                                                   |
| [<span data-ttu-id="8c1f3-159">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-159">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="8c1f3-160">Liaison tardive impossible</span><span class="sxs-lookup"><span data-stu-id="8c1f3-160">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="8c1f3-161">**Dossier**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-161">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="8c1f3-162">Shell. Shell \_ application. Namespace ("...")</span><span class="sxs-lookup"><span data-stu-id="8c1f3-162">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="8c1f3-163">**Dossier2**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-163">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="8c1f3-164">Shell. Shell \_ application. Namespace ("...")</span><span class="sxs-lookup"><span data-stu-id="8c1f3-164">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="8c1f3-165">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-165">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="8c1f3-166">Shell. Shell \_ application. Namespace ("..."). Self ou dossier. Items. Item ou Folder. ParseName</span><span class="sxs-lookup"><span data-stu-id="8c1f3-166">shell.Shell\_Application.NameSpace("...").Self or Folder.Items.Item or Folder.ParseName</span></span> |
| [<span data-ttu-id="8c1f3-167">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-167">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="8c1f3-168">Dossier. Items</span><span class="sxs-lookup"><span data-stu-id="8c1f3-168">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="8c1f3-169">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-169">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="8c1f3-170">Dossier. Items</span><span class="sxs-lookup"><span data-stu-id="8c1f3-170">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="8c1f3-171">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-171">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="8c1f3-172">Shell. NameSpace ("..."). Self. verbes. Item ()</span><span class="sxs-lookup"><span data-stu-id="8c1f3-172">Shell.NameSpace("...").Self.Verbs.Item()</span></span>                                                |
| [<span data-ttu-id="8c1f3-173">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-173">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="8c1f3-174">FolderItem. Verbs ou Shell. NameSpace ("..."). Self. verbes</span><span class="sxs-lookup"><span data-stu-id="8c1f3-174">FolderItem.Verbs or Shell.NameSpace("...").Self.Verbs</span></span>                                   |
| [<span data-ttu-id="8c1f3-175">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-175">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="8c1f3-176">Shell. \_Application Shell</span><span class="sxs-lookup"><span data-stu-id="8c1f3-176">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="8c1f3-177">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-177">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="8c1f3-178">Shell. NameSpace ("..."). Self. GetLink ou Shell. NameSpace ("..."). Items (). GetLink</span><span class="sxs-lookup"><span data-stu-id="8c1f3-178">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="8c1f3-179">**Shell**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-179">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="8c1f3-180">Shell. \_Application Shell</span><span class="sxs-lookup"><span data-stu-id="8c1f3-180">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="8c1f3-181">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-181">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="8c1f3-182">Shell. NameSpace ("..."). Self ou Shell. NameSpace ("..."). Items ()</span><span class="sxs-lookup"><span data-stu-id="8c1f3-182">Shell.NameSpace("...").Self or Shell.NameSpace("...").Items()</span></span>                           |
| [<span data-ttu-id="8c1f3-183">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-183">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="8c1f3-184">Liaison tardive impossible</span><span class="sxs-lookup"><span data-stu-id="8c1f3-184">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="8c1f3-185">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-185">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="8c1f3-186">Liaison tardive impossible</span><span class="sxs-lookup"><span data-stu-id="8c1f3-186">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="8c1f3-187">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-187">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="8c1f3-188">Shell. NameSpace ("..."). Self. GetLink ou Shell. NameSpace ("..."). Items (). GetLink</span><span class="sxs-lookup"><span data-stu-id="8c1f3-188">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="8c1f3-189">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-189">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="8c1f3-190">Liaison tardive impossible</span><span class="sxs-lookup"><span data-stu-id="8c1f3-190">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="8c1f3-191">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-191">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="8c1f3-192">Shell. Shell \_ Windows ou ShellWindows. \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="8c1f3-192">shell.Shell\_Windows or ShellWindows.\_NewEnum</span></span>                                          |
| [<span data-ttu-id="8c1f3-193">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-193">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="8c1f3-194">Liaison tardive impossible</span><span class="sxs-lookup"><span data-stu-id="8c1f3-194">Cannot late bind</span></span>                                                                        |



 

### <a name="html-object-element"></a><span data-ttu-id="8c1f3-195">Élément objet HTML</span><span class="sxs-lookup"><span data-stu-id="8c1f3-195">HTML OBJECT Element</span></span>

<span data-ttu-id="8c1f3-196">Vous pouvez également utiliser l’élément [**Object**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) pour instancier des objets Shell sur une page html.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-196">You can also use the [**OBJECT**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) element to instantiate Shell objects on an HTML page.</span></span> <span data-ttu-id="8c1f3-197">Pour ce faire, définissez l’attribut **ID** de l’élément **Object** sur le nom de la variable que vous allez utiliser dans vos scripts, puis identifiez l’objet à l’aide de son numéro d’inscription (ClassID).</span><span class="sxs-lookup"><span data-stu-id="8c1f3-197">To do this, set the **OBJECT** element's **ID** attribute to the variable name you will use in your scripts, and identify the object using its registered number (CLASSID).</span></span> <span data-ttu-id="8c1f3-198">Le code HTML suivant crée une instance de l’objet [**ShellFolderItem**](shellfolderitem-object.md) à l’aide de l’élément **objet** .</span><span class="sxs-lookup"><span data-stu-id="8c1f3-198">The following HTML creates an instance of the [**ShellFolderItem**](shellfolderitem-object.md) object using the **OBJECT** element.</span></span>


```
<OBJECT ID="oShFolderItem" 
    NAME="Shell Folder Item Object"
    CLASSID="clsid:2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e">
</OBJECT>
```



<span data-ttu-id="8c1f3-199">Le tableau suivant répertorie chaque objet Shell et son CLASSID respectif.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-199">The following table lists each Shell object and its respective CLASSID.</span></span>



|                                                         |                                      |
|---------------------------------------------------------|--------------------------------------|
| [<span data-ttu-id="8c1f3-200">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-200">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="8c1f3-201">7988B571-EC89-11cf-9C00-00AA00A14F56</span><span class="sxs-lookup"><span data-stu-id="8c1f3-201">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="8c1f3-202">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-202">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="8c1f3-203">7988B571-EC89-11cf-9C00-00AA00A14F56</span><span class="sxs-lookup"><span data-stu-id="8c1f3-203">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="8c1f3-204">**Dossier**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-204">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="8c1f3-205">BBCBDE60-C3FF-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="8c1f3-205">BBCBDE60-C3FF-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="8c1f3-206">**Dossier2**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-206">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="8c1f3-207">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span><span class="sxs-lookup"><span data-stu-id="8c1f3-207">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span></span> |
| [<span data-ttu-id="8c1f3-208">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-208">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="8c1f3-209">744129E0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="8c1f3-209">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="8c1f3-210">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-210">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="8c1f3-211">744129E0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="8c1f3-211">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="8c1f3-212">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-212">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="8c1f3-213">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span><span class="sxs-lookup"><span data-stu-id="8c1f3-213">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span></span> |
| [<span data-ttu-id="8c1f3-214">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-214">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="8c1f3-215">08EC3E00-50B0-11CF-960C-0080C7F4EE85</span><span class="sxs-lookup"><span data-stu-id="8c1f3-215">08EC3E00-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="8c1f3-216">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-216">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="8c1f3-217">1F8352C0-50B0-11CF-960C-0080C7F4EE85</span><span class="sxs-lookup"><span data-stu-id="8c1f3-217">1F8352C0-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="8c1f3-218">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-218">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="8c1f3-219">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span><span class="sxs-lookup"><span data-stu-id="8c1f3-219">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span></span> |
| [<span data-ttu-id="8c1f3-220">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-220">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="8c1f3-221">317EE249-F12E-11d2-B1E4-00C04F8EEB3E</span><span class="sxs-lookup"><span data-stu-id="8c1f3-221">317EE249-F12E-11d2-B1E4-00C04F8EEB3E</span></span> |
| [<span data-ttu-id="8c1f3-222">**Shell**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-222">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="8c1f3-223">13709620-C279-11CE-A49E-444553540000</span><span class="sxs-lookup"><span data-stu-id="8c1f3-223">13709620-C279-11CE-A49E-444553540000</span></span> |
| [<span data-ttu-id="8c1f3-224">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-224">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="8c1f3-225">2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e</span><span class="sxs-lookup"><span data-stu-id="8c1f3-225">2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e</span></span> |
| [<span data-ttu-id="8c1f3-226">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-226">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="8c1f3-227">62112AA1-EBE4-11cf-A5FB-0020AFE7292D</span><span class="sxs-lookup"><span data-stu-id="8c1f3-227">62112AA1-EBE4-11cf-A5FB-0020AFE7292D</span></span> |
| [<span data-ttu-id="8c1f3-228">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-228">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="8c1f3-229">4a3df050-23bd-11d2-939f-00a0c91eedba</span><span class="sxs-lookup"><span data-stu-id="8c1f3-229">4a3df050-23bd-11d2-939f-00a0c91eedba</span></span> |
| [<span data-ttu-id="8c1f3-230">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-230">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="8c1f3-231">11219420-1768-11d1-95BE-00609797EA4F</span><span class="sxs-lookup"><span data-stu-id="8c1f3-231">11219420-1768-11d1-95BE-00609797EA4F</span></span> |
| [<span data-ttu-id="8c1f3-232">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-232">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="8c1f3-233">64AB4BB7-111E-11D1-8F79-00C04FC2FBE1</span><span class="sxs-lookup"><span data-stu-id="8c1f3-233">64AB4BB7-111E-11D1-8F79-00C04FC2FBE1</span></span> |
| [<span data-ttu-id="8c1f3-234">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-234">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="8c1f3-235">9BA05972-F6A8-11CF-A442-00A0C90A8F39</span><span class="sxs-lookup"><span data-stu-id="8c1f3-235">9BA05972-F6A8-11CF-A442-00A0C90A8F39</span></span> |
| [<span data-ttu-id="8c1f3-236">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="8c1f3-236">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="8c1f3-237">1820FED0-473E-11D0-A96C-00C04FD705A2</span><span class="sxs-lookup"><span data-stu-id="8c1f3-237">1820FED0-473E-11D0-A96C-00C04FD705A2</span></span> |



 

## <a name="shell-object"></a><span data-ttu-id="8c1f3-238">Objet Shell</span><span class="sxs-lookup"><span data-stu-id="8c1f3-238">Shell Object</span></span>

<span data-ttu-id="8c1f3-239">L’objet [**Shell**](shell.md) représente les objets dans l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-239">The [**Shell**](shell.md) object represents the objects in the Shell.</span></span> <span data-ttu-id="8c1f3-240">Vous pouvez utiliser les méthodes exposées par l’objet Shell pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8c1f3-240">You can use the methods exposed by the Shell object to:</span></span>

-   <span data-ttu-id="8c1f3-241">Ouvrir, Explorer et parcourir les dossiers.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-241">Open, explore, and browse for folders.</span></span>
-   <span data-ttu-id="8c1f3-242">Réduction, restauration, mise en cascade ou vignette des fenêtres ouvertes.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-242">Minimize, restore, cascade, or tile open windows.</span></span>
-   <span data-ttu-id="8c1f3-243">Lancez les applications du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-243">Launch Control Panel applications.</span></span>
-   <span data-ttu-id="8c1f3-244">Affiche les boîtes de dialogue système.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-244">Display system dialog boxes.</span></span>

<span data-ttu-id="8c1f3-245">Les utilisateurs sont peut-être plus familiarisés avec les commandes auxquelles ils accèdent à partir du menu **Démarrer** et du menu contextuel de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-245">Users are perhaps most familiar with the commands they access from the **Start** menu and the taskbar's shortcut menu.</span></span> <span data-ttu-id="8c1f3-246">Le menu contextuel de la barre des tâches s’affiche lorsque les utilisateurs cliquent avec le bouton droit sur la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-246">The taskbar's shortcut menu appears when users right-click the taskbar.</span></span> <span data-ttu-id="8c1f3-247">L’application HTML (HTA) suivante génère une page de démarrage avec des boutons qui implémentent un grand nombre des méthodes de l’objet [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="8c1f3-247">The following HTML Application (HTA) produces a start page with buttons that implement many of the [**Shell**](shell.md) object's methods.</span></span> <span data-ttu-id="8c1f3-248">Certaines de ces méthodes implémentent des fonctionnalités dans le menu **Démarrer** et le menu contextuel de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-248">Some of these methods implement features on the **Start** menu and the taskbar's shortcut menu.</span></span>


```
<HTML>
<HEAD>
    <TITLE>Start Page</TITLE>
    
    <OBJECT ID="oShell"
        CLASSID="clsid:13709620-C279-11CE-A49E-444553540000">
    </OBJECT>
    
    <STYLE>
        INPUT {width: 200} 
    </STYLE>  
    
    <SCRIPT LANGUAGE="VBScript">
    <!--
        function fnStart(sMethod)
            select case sMethod
              case 0    
                  'Minimizes all windows on the desktop
                oshell.Shell_MinimizeAll
              case 1  
                  'Displays the Run dialog box
                oshell.FileRun
              case 2  
                  'Displays the Shut Down Windows dialog box
                oshell.Shell_ShutdownWindows
              case 3  
                  'Displays the Find dialog box
                oshell.Shell_FindFilesr
              case 4  
                  'Displays the Date/Time dialog box
                oshell.Shell_SetTime 
              case 5  
                  'Displays the Internet Properties dialog box
                oshell.Shell_ControlPanelItem "INETCPL.cpl"
              case 6  
                  'Explores the My Documents folder
                oshell.Shell_Explore "C:\My Documents"
              case 7  
                  'Enables user to select folder from Program Files
                oshell.Shell_BrowseForFolder 0, "My Programs", 0, "C:\Program Files" 
              case 8  
                  'Opens the Favorites folder
                oshell.Shell_Open "C:\WINDOWS\Favorites"
              case 9  
                  'Displays the Taskbar Properties dialog box
                oshell.Shell_TrayProperties
            end select  
        end function      
    -->
    </SCRIPT>
</HEAD>

<BODY>
    <H1>Start...</H1>
    <INPUT type="button" value="Edit Taskbar Properties" onclick="fnStart(9)"><br>
    <INPUT type="button" value="Open Favorites Folder" onclick="fnStart(8)"><br>
    <INPUT type="button" value="Browse Program Files" onclick="fnStart(7)"><br>
    <INPUT type="button" value="Explore My Documents" onclick="fnStart(6)"><br>
    <INPUT type="button" value="Modify Internet Properties" onclick="fnStart(5)"><br>
    <INPUT type="button" value="Set System Time" onclick="fnStart(4)"><br>
    <INPUT type="button" value="Find a File or Folder" onclick="fnStart(3)"><br>
    <INPUT type="button" value="Shut Down Windows" onclick="fnStart(2)"><br>
    <INPUT type="button" value="Run" onclick="fnStart(1)">     
    <INPUT type="button" value="Minimize All Windows" onclick="fnStart(0)">     
</BODY>
</HTML>
```



### <a name="security"></a><span data-ttu-id="8c1f3-249">Sécurité</span><span class="sxs-lookup"><span data-stu-id="8c1f3-249">Security</span></span>

<span data-ttu-id="8c1f3-250">En tant qu’application, une HTA s’exécute sous un modèle de sécurité différent de celui d’une page Web.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-250">As an application, an HTA runs under a different security model than a webpage.</span></span> <span data-ttu-id="8c1f3-251">Pour interagir avec une page Web qui implémente les fonctionnalités des objets Shell, les utilisateurs doivent activer l’option **initialiser et générer un script des contrôles ActiveX non marqués comme sécurisés** pour la zone de sécurité dans laquelle ils visualisent la page.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-251">To interact with a webpage that implements the functionality of the Shell objects, users must enable the **Initialize and script ActiveX Controls not marked as safe** option for the security zone in which they are viewing the page.</span></span>

## <a name="folder-objects"></a><span data-ttu-id="8c1f3-252">Objets de dossier</span><span class="sxs-lookup"><span data-stu-id="8c1f3-252">Folder Objects</span></span>

<span data-ttu-id="8c1f3-253">L’objet [**Folder**](folder.md) représente un dossier shell.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-253">The [**Folder**](folder.md) object represents a Shell folder.</span></span> <span data-ttu-id="8c1f3-254">Vous pouvez utiliser les méthodes exposées par l’objet Folder pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8c1f3-254">You can use the methods exposed by the Folder object to:</span></span>

-   <span data-ttu-id="8c1f3-255">Obtenir des informations sur un dossier.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-255">Get information about a folder.</span></span>
-   <span data-ttu-id="8c1f3-256">Créer des sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-256">Create subfolders.</span></span>
-   <span data-ttu-id="8c1f3-257">Copier et déplacer des objets de fichier dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-257">Copy and move file objects into the folder.</span></span>

<span data-ttu-id="8c1f3-258">L’objet [**FolderItem**](folderitem.md) représente un élément dans un dossier shell.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-258">The [**FolderItem**](folderitem.md) object represents an item in a Shell folder.</span></span> <span data-ttu-id="8c1f3-259">Ses propriétés vous permettent de récupérer des informations sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-259">Its properties enable you to retrieve information about the item.</span></span> <span data-ttu-id="8c1f3-260">Vous pouvez utiliser les méthodes exposées par cet objet pour exécuter les verbes d’un élément, ou pour récupérer des informations sur l’objet [**FolderItemVerbs**](folderitemverbs.md) d’un élément.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-260">You can use the methods exposed by this object to run an item's verbs, or to retrieve information about an item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span>

<span data-ttu-id="8c1f3-261">L’objet [**FolderItems**](folderitems.md) représente une collection d’éléments dans un dossier shell.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-261">The [**FolderItems**](folderitems.md) object represents a collection of items in a Shell folder.</span></span> <span data-ttu-id="8c1f3-262">Ses méthodes et propriétés vous permettent de récupérer des informations sur la collection.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-262">Its methods and properties enable you to retrieve information about the collection.</span></span>

<span data-ttu-id="8c1f3-263">L’exemple de Visual Basic suivant montre la relation entre plusieurs objets de dossier et comment ils peuvent être utilisés ensemble.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-263">The following Visual Basic example shows the relationship between several of the folder objects and how they can be used together.</span></span> <span data-ttu-id="8c1f3-264">Quand l’utilisateur clique sur le bouton de commande appelé **cmdGetPath**, le programme affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner un dossier dans **poste de travail**, où ssfDRIVES est la valeur d’énumération [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) pour **poste de travail**.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-264">When the user clicks the command button called **cmdGetPath**, the program displays a dialog box that enables the user to select a folder from **My Computer**, where ssfDRIVES is the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration value for **My Computer**.</span></span> <span data-ttu-id="8c1f3-265">Quand l’utilisateur choisit un dossier, son chemin d’accès est affiché dans la zone de texte appelée **txtPath**.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-265">When the user chooses a folder, the folder's path is displayed in the text box called **txtPath**.</span></span>


```
Private Sub cmdGetPath_Click()
    Dim oShell As New Shell
    Dim oFolder As Folder
    Dim oFolderItem As FolderItem
 
    Set oFolder = oshell.Shell_BrowseForFolder(Me.hWnd, "Select a Folder", 0, ssfDrives)
   
    Set oFolderItem = oFolderItems.Item

    txtPath.Text = oFolderItem.Path
End Sub
```



<span data-ttu-id="8c1f3-266">Dans VBScript, cette fonction est légèrement différente, car les valeurs d’énumération [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) ne sont pas disponibles dans le script.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-266">In VBScript, this function is slightly different because the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span> <span data-ttu-id="8c1f3-267">L’exemple suivant illustre l’équivalent en VBScript de l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="8c1f3-267">The following example shows the VBScript equivalent of the previous example.</span></span>


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnGetMyPathVB() 
        dim oShell
        dim oFolder
        dim oFolderItem
        
        set oShell = CreateObject("shell.application")      
        set oFolder = oshell.Shell_BrowseForFolder(0, "Choose a Folder", 0)             
        set oFolderItem = oFolder.Items.Item         
        
        document.all.item("myPath").innerText = oFolderItem.Path                                
    end function
-->
</SCRIPT>
```



<span data-ttu-id="8c1f3-268">Dans l’exemple JScript suivant, qui est une traduction directe de l’exemple VBScript précédent, notez la manière dont les parenthèses vides « () » sont utilisées pour appeler les [**méthodes Items et**](folder-items.md) [**Item**](folderitems-item.md) .</span><span class="sxs-lookup"><span data-stu-id="8c1f3-268">In the following JScript example, which is a direct translation of the preceding VBScript example, note how the empty parentheses '()' are used to invoke the [**Items**](folder-items.md) and [**Item**](folderitems-item.md) methods.</span></span>


```
<SCRIPT LANGUAGE="JavaScript">
<!--
    function fnGetMyPathJ() 
    {       
        var oShell = new ActiveXObject("shell.application");
                    
        var oFolder = new Object;                   
        oFolder = oshell.Shell_BrowseForFolder(0, "Choose a folder", 0);
                                
        var oFolderItem = new Object;       
        oFolderItem = oFolder.Items().Item();                               
        
        document.all.item("myPath").innerText = oFolderItem.Path;
    }    
-->
</SCRIPT>
```



 

 
