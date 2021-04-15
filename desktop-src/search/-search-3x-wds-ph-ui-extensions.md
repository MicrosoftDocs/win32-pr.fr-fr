---
description: Pour vous assurer que vos données sont indexées et présentées correctement à l’utilisateur pendant les recherches, vous devez implémenter des magasins de données Shell (également appelés extensions d’espace de noms de Shell) et des gestionnaires de type de fichier (également appelés extensions d’interpréteur de commandes, gestionnaires d’extension ou gestionnaires d’extension de Shell).
ms.assetid: 38cebb3c-51bf-439c-8d4e-445344f6cb66
title: Ajout d’icônes, d’aperçus et de menus contextuels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501006227f6192b7d81a2a88ba915c368a9cc398
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525533"
---
# <a name="adding-icons-previews-and-shortcut-menus"></a><span data-ttu-id="a0f2c-103">Ajout d’icônes, d’aperçus et de menus contextuels</span><span class="sxs-lookup"><span data-stu-id="a0f2c-103">Adding Icons, Previews and Shortcut Menus</span></span>

<span data-ttu-id="a0f2c-104">Pour vous assurer que vos données sont indexées et présentées correctement à l’utilisateur pendant les recherches, vous devez implémenter des magasins de données Shell (également appelés [extensions d’espace de noms de Shell](../shell/nse-works.md)) et des gestionnaires de type de fichier (également appelés extensions d’interpréteur de commandes, gestionnaires d' [extension](../shell/handlers.md)ou gestionnaires d’extension de Shell).</span><span class="sxs-lookup"><span data-stu-id="a0f2c-104">To ensure that your data is indexed and presented correctly to the user during searches, you need to implement Shell data stores (also known as [Shell Namespace Extensions](../shell/nse-works.md)), and file type handlers (also known as Shell extensions, [extension handlers](../shell/handlers.md), or Shell extension handlers).</span></span>

<span data-ttu-id="a0f2c-105">Cette rubrique décrit les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="a0f2c-105">This topic describes the following interfaces:</span></span>

-   [<span data-ttu-id="a0f2c-106">Implémentation de gestionnaires de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="a0f2c-106">Implementing File Type Handlers</span></span>](#implementing-file-type-handlers)
    -   [<span data-ttu-id="a0f2c-107">IPersist</span><span class="sxs-lookup"><span data-stu-id="a0f2c-107">IPersist</span></span>](#ipersist)
    -   [<span data-ttu-id="a0f2c-108">IPersistFolder</span><span class="sxs-lookup"><span data-stu-id="a0f2c-108">IPersistFolder</span></span>](#ipersistfolder)
    -   [<span data-ttu-id="a0f2c-109">IShellFolder</span><span class="sxs-lookup"><span data-stu-id="a0f2c-109">IShellFolder</span></span>](#ishellfolder)
    -   [<span data-ttu-id="a0f2c-110">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="a0f2c-110">IContextMenu</span></span>](#icontextmenu)
    -   [<span data-ttu-id="a0f2c-111">IExtractIcon</span><span class="sxs-lookup"><span data-stu-id="a0f2c-111">IExtractIcon</span></span>](#iextracticon)
    -   [<span data-ttu-id="a0f2c-112">IPreviewHandler</span><span class="sxs-lookup"><span data-stu-id="a0f2c-112">IPreviewHandler</span></span>](#ipreviewhandler)
-   [<span data-ttu-id="a0f2c-113">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="a0f2c-113">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="a0f2c-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0f2c-114">Related topics</span></span>](#related-topics)

## <a name="implementing-file-type-handlers"></a><span data-ttu-id="a0f2c-115">Implémentation de gestionnaires de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="a0f2c-115">Implementing File Type Handlers</span></span>

<span data-ttu-id="a0f2c-116">Ces extensions de Shell ou gestionnaires de type de fichier fournissent à vos utilisateurs les expériences d’environnement suivantes :</span><span class="sxs-lookup"><span data-stu-id="a0f2c-116">These Shell extensions or file type handlers provide your users with the following Shell experiences:</span></span>

-   <span data-ttu-id="a0f2c-117">La vue résultats affiche une icône spécifique pour votre type d’élément.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-117">The results view displays a specific icon for your item type.</span></span>
-   <span data-ttu-id="a0f2c-118">La vue résultats affiche un aperçu de l’élément lorsque l’utilisateur sélectionne l’élément.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-118">The results view displays a preview of the item when the user selects the item.</span></span>
-   <span data-ttu-id="a0f2c-119">Les utilisateurs peuvent double-cliquer sur des éléments pour initier des événements tels que l’ouverture du fichier.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-119">Users can double-click items to initiate events such as opening the file.</span></span>
-   <span data-ttu-id="a0f2c-120">Les utilisateurs peuvent cliquer avec le bouton droit sur les éléments pour accéder à un menu contextuel (contexte).</span><span class="sxs-lookup"><span data-stu-id="a0f2c-120">Users can right-click items to access a shortcut (context) menu.</span></span>
-   <span data-ttu-id="a0f2c-121">Les utilisateurs peuvent glisser-déplacer des éléments.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-121">Users can drag-and-drop items.</span></span>

<span data-ttu-id="a0f2c-122">Comme tous les objets COM (Component Object Model), les gestionnaires de types de fichiers doivent implémenter une interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) et une fabrique de classe.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-122">Like all Component Object Model (COM) objects, file type handlers must implement an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface and a class factory.</span></span>

<span data-ttu-id="a0f2c-123">Dans Windows XP ou version antérieure, les gestionnaires doivent également implémenter :</span><span class="sxs-lookup"><span data-stu-id="a0f2c-123">In Windows XP or earlier, handlers should also implement:</span></span>

-   <span data-ttu-id="a0f2c-124">L' [interface IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile)</span><span class="sxs-lookup"><span data-stu-id="a0f2c-124">Either [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile)</span></span>
-   <span data-ttu-id="a0f2c-125">Ou [interface IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)</span><span class="sxs-lookup"><span data-stu-id="a0f2c-125">Or [IShellExtInit Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)</span></span>

<span data-ttu-id="a0f2c-126">Dans Windows Vista, l’interface [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) et l' [interface IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) ont été remplacées par les trois interfaces suivantes pour que Shell Initialise le gestionnaire :</span><span class="sxs-lookup"><span data-stu-id="a0f2c-126">In Windows Vista, [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [IShellExtInit Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) were replaced by the following three interfaces for Shell to initialize the handler:</span></span>

-   [<span data-ttu-id="a0f2c-127">IInitializeWithStream, interface</span><span class="sxs-lookup"><span data-stu-id="a0f2c-127">IInitializeWithStream Interface</span></span>](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [<span data-ttu-id="a0f2c-128">Interface IInitializeWithItem</span><span class="sxs-lookup"><span data-stu-id="a0f2c-128">IInitializeWithItem Interface</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [<span data-ttu-id="a0f2c-129">Interface IInitializeWithFile</span><span class="sxs-lookup"><span data-stu-id="a0f2c-129">IInitializeWithFile Interface</span></span>](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)

<span data-ttu-id="a0f2c-130">Pour fournir une expérience utilisateur raisonnable, vous devez fournir un magasin de données Shell avec votre gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-130">To provide a reasonable user experience you must provide a Shell data store with your protocol handler.</span></span> <span data-ttu-id="a0f2c-131">Ce magasin de données sert alors de « fabrique » pour les gestionnaires d’icônes, les gestionnaires de menus contextuels, les gestionnaires d’aperçus, etc.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-131">That data store then serves as the "factory" for icon handlers, shortcut menu handlers, preview handlers, and so forth.</span></span> <span data-ttu-id="a0f2c-132">Les implémentations minimales de l’interface [IPersist](/windows/desktop/api/objidl/nn-objidl-ipersist) et de l' [interface IPersistFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) sont requises par l' [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), et une implémentation minimale de l’interface IShellFolder est requise pour [IContextMenu](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) et [IExtractIcon](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).</span><span class="sxs-lookup"><span data-stu-id="a0f2c-132">Minimal implementations of [IPersist Interface](/windows/desktop/api/objidl/nn-objidl-ipersist) and [IPersistFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) are required by [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), and a minimal implementation of IShellFolder Interface is required for the [IContextMenu](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) and [IExtractIcon](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).</span></span>

> [!Note]  
> <span data-ttu-id="a0f2c-133">Le même identificateur de classe (CLSID) doit être implémenté pour **IPersist**, **IPersistFolder** et **IShellFolder**.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-133">The same class identifier (CLSID) should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

<span data-ttu-id="a0f2c-134">Pour plus d’informations sur la création d’un magasin de données Shell pour prendre en charge un gestionnaire de protocole, consultez [implémentation des interfaces d’objets de dossier de base](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a0f2c-134">For more information about creating a Shell data store to support a protocol handler, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

### <a name="ipersist"></a><span data-ttu-id="a0f2c-135">IPersist</span><span class="sxs-lookup"><span data-stu-id="a0f2c-135">IPersist</span></span>

<span data-ttu-id="a0f2c-136">L’interface **IPersist** définit la méthode unique **GetClassID**, conçue pour fournir le CLSID d’un objet qui peut être stocké de manière permanente dans le système.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-136">The **IPersist** interface defines the single method **GetClassID**, which is designed to supply the CLSID of an object that can be stored persistently in the system.</span></span>



| <span data-ttu-id="a0f2c-137">Méthode</span><span class="sxs-lookup"><span data-stu-id="a0f2c-137">Method</span></span>     | <span data-ttu-id="a0f2c-138">Description</span><span class="sxs-lookup"><span data-stu-id="a0f2c-138">Description</span></span>                                      |
|------------|--------------------------------------------------|
| <span data-ttu-id="a0f2c-139">GetClassID</span><span class="sxs-lookup"><span data-stu-id="a0f2c-139">GetClassID</span></span> | <span data-ttu-id="a0f2c-140">Retourne le CLSID de l’objet de magasin de données Shell</span><span class="sxs-lookup"><span data-stu-id="a0f2c-140">Returns the CLSID of the Shell data store object</span></span> |



 

### <a name="ipersistfolder"></a><span data-ttu-id="a0f2c-141">IPersistFolder</span><span class="sxs-lookup"><span data-stu-id="a0f2c-141">IPersistFolder</span></span>

<span data-ttu-id="a0f2c-142">L’interface **IPersistFolder** est utilisée pour initialiser les objets de dossier de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-142">The **IPersistFolder** interface is used to initialize Shell folder objects.</span></span> <span data-ttu-id="a0f2c-143">L’implémentation de cette interface, dérivée de **IPersist**, est la manière dont le dossier est indiqué à l’emplacement où il se trouve dans l’espace de noms Shell.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-143">Implementation of this interface, which is derived from **IPersist**, is how the folder is told where it is in the Shell namespace.</span></span> <span data-ttu-id="a0f2c-144">Vous n’utilisez pas cette interface directement.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-144">You do not use this interface directly.</span></span> <span data-ttu-id="a0f2c-145">Elle est utilisée par l’implémentation du système de fichiers de la [méthode IShellFolder :: BindToObject](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) lors de l’initialisation d’un objet de dossier de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-145">It is used by the file system implementation of [IShellFolder::BindToObject Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) when it initializes a Shell folder object.</span></span>



| <span data-ttu-id="a0f2c-146">Méthode</span><span class="sxs-lookup"><span data-stu-id="a0f2c-146">Method</span></span>     | <span data-ttu-id="a0f2c-147">Description</span><span class="sxs-lookup"><span data-stu-id="a0f2c-147">Description</span></span>                                                                                            |
|------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f2c-148">Initialiser</span><span class="sxs-lookup"><span data-stu-id="a0f2c-148">Initialize</span></span> | <span data-ttu-id="a0f2c-149">Demande à un objet de dossier de Shell de s’initialiser en fonction des informations transmises et des retours \_ OK</span><span class="sxs-lookup"><span data-stu-id="a0f2c-149">Instructs a Shell folder object to initialize itself based on the information passed and returns S\_OK</span></span> |



 

### <a name="ishellfolder"></a><span data-ttu-id="a0f2c-150">IShellFolder</span><span class="sxs-lookup"><span data-stu-id="a0f2c-150">IShellFolder</span></span>

<span data-ttu-id="a0f2c-151">L’interface d' [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) est utilisée pour gérer les dossiers, et une implémentation partielle est nécessaire pour que les interfaces d’icône et de contexte implémentées pour un gestionnaire de protocole se comportent correctement dans l’interface utilisateur des résultats de la recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-151">The [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface is used to manage folders, and a partial implementation is required so that the icon and context interfaces implemented for a protocol handler will behave correctly in the Windows Search results user interface.</span></span> <span data-ttu-id="a0f2c-152">La plupart des fonctionnalités requises sont exposées par le biais de la méthode **GetUIObjectOf** .</span><span class="sxs-lookup"><span data-stu-id="a0f2c-152">Most of the functionality required is exposed through the **GetUIObjectOf** method.</span></span> <span data-ttu-id="a0f2c-153">Cette méthode permet à un complément d’interroger les interfaces **IExtractIcon** et **IContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="a0f2c-153">This method enables an add-in to query for the **IExtractIcon** and **IContextMenu** interfaces.</span></span>

<span data-ttu-id="a0f2c-154">L’interface d' [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) utilise PIDL à la place des URL.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-154">The [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface uses PIDLs instead of URLs.</span></span> <span data-ttu-id="a0f2c-155">Contrairement aux spécifications d’un magasin de données Shell complet, les compléments peuvent utiliser une structure IDL simple qui contient uniquement l’URL.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-155">In contrast to the requirements of a complete Shell data store, add-ins can use a simple IDL structure that contains only the URL.</span></span>

<span data-ttu-id="a0f2c-156">Les méthodes suivantes de l' [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) doivent être implémentées.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-156">The following methods of [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) must be implemented.</span></span> <span data-ttu-id="a0f2c-157">Cinq de ces méthodes nécessitent une implémentation minimale.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-157">Five of these methods require minimal implementation.</span></span>



| <span data-ttu-id="a0f2c-158">Méthode</span><span class="sxs-lookup"><span data-stu-id="a0f2c-158">Method</span></span>           | <span data-ttu-id="a0f2c-159">Description</span><span class="sxs-lookup"><span data-stu-id="a0f2c-159">Description</span></span>                                                                                                                                                                                                                                                                   |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f2c-160">BindToObject</span><span class="sxs-lookup"><span data-stu-id="a0f2c-160">BindToObject</span></span>     | <span data-ttu-id="a0f2c-161">Retourne E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="a0f2c-161">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="a0f2c-162">BindToStorage</span><span class="sxs-lookup"><span data-stu-id="a0f2c-162">BindToStorage</span></span>    | <span data-ttu-id="a0f2c-163">Retourne E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="a0f2c-163">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="a0f2c-164">CreateViewObject</span><span class="sxs-lookup"><span data-stu-id="a0f2c-164">CreateViewObject</span></span> | <span data-ttu-id="a0f2c-165">Retourne E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="a0f2c-165">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="a0f2c-166">SetNameOf</span><span class="sxs-lookup"><span data-stu-id="a0f2c-166">SetNameOf</span></span>        | <span data-ttu-id="a0f2c-167">Retourne E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="a0f2c-167">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="a0f2c-168">ParseDisplayName</span><span class="sxs-lookup"><span data-stu-id="a0f2c-168">ParseDisplayName</span></span> | <span data-ttu-id="a0f2c-169">Convertit une URL en structure PIDL</span><span class="sxs-lookup"><span data-stu-id="a0f2c-169">Converts a URL to the PIDL structure</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="a0f2c-170">CompareIDs</span><span class="sxs-lookup"><span data-stu-id="a0f2c-170">CompareIDs</span></span>       | <span data-ttu-id="a0f2c-171">Compare deux valeurs PIDL</span><span class="sxs-lookup"><span data-stu-id="a0f2c-171">Compares two PIDL values</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="a0f2c-172">GetDisplayNameOf</span><span class="sxs-lookup"><span data-stu-id="a0f2c-172">GetDisplayNameOf</span></span> | <span data-ttu-id="a0f2c-173">Retourne l’URL d’un PIDL</span><span class="sxs-lookup"><span data-stu-id="a0f2c-173">Returns the URL for a PIDL</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="a0f2c-174">GetUIObjectOf</span><span class="sxs-lookup"><span data-stu-id="a0f2c-174">GetUIObjectOf</span></span>    | <span data-ttu-id="a0f2c-175">Cette méthode est semblable à la [méthode IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="a0f2c-175">This method is similar to the [IUnknown::QueryInterface Method](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="a0f2c-176">Si une icône est demandée, l’appelant demande l’IID \_ IExtractIcon ; si un menu contextuel est demandé, l’appelant demande l’IID \_ IContextMenu</span><span class="sxs-lookup"><span data-stu-id="a0f2c-176">If an icon is requested, the caller requests the IID\_IExtractIcon; if a shortcut menu is requested, the caller requests the IID\_IContextMenu</span></span> |



 

<span data-ttu-id="a0f2c-177">**IShellFolder** n’est pas utilisé pour énumérer des dossiers.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-177">**IShellFolder** is not used to enumerate folders.</span></span> <span data-ttu-id="a0f2c-178">Cela signifie que le nom complet d’un dossier sera l’URL physique.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-178">This means that the display name of a folder will be the physical URL.</span></span> <span data-ttu-id="a0f2c-179">Cela peut changer à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-179">This may change in the future.</span></span>

### <a name="icontextmenu"></a><span data-ttu-id="a0f2c-180">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="a0f2c-180">IContextMenu</span></span>

<span data-ttu-id="a0f2c-181">Lorsque Windows Search affiche les résultats à l’utilisateur, l’utilisateur peut cliquer avec le bouton droit sur un élément et afficher un menu contextuel défini par votre interface **IContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="a0f2c-181">When Windows Search displays results to the user, the user can right-click an item and see a shortcut menu defined by your **IContextMenu** interface.</span></span> <span data-ttu-id="a0f2c-182">Les menus contextuels sont également appelés menus contextuels.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-182">Shortcut menus are also known as context menus.</span></span>

<span data-ttu-id="a0f2c-183">L’action par défaut dans le menu contextuel est la même que celle effectuée lors d’un double-clic sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-183">The default action on the context menu is the same action taken when the item is double-clicked.</span></span> <span data-ttu-id="a0f2c-184">Sans les interfaces **IShellFolder** ou **IContextMenu** correspondantes pour l’élément, le comportement par défaut d’un événement de double-clic consiste à transmettre l’URL en tant qu’argument à la fonction [ShellExecute](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="a0f2c-184">Without the corresponding **IShellFolder** or **IContextMenu** interfaces for the item, the default behavior for a double-click event is to pass the URL as an argument to the [ShellExecute Function](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) function.</span></span>

<span data-ttu-id="a0f2c-185">Pour plus d’informations sur la création de gestionnaires de menus contextuels et sur les [Exemples : extensions de Shell pour les gestionnaires de protocole](-search-3x-wds-ph-ui-samplecode.md) pour l’exemple de code, consultez Création de gestionnaires de [menus](../shell/context-menu-handlers.md) contextuels.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-185">Refer to [Creating Context Menu Handlers](../shell/context-menu-handlers.md) for more information on creating shortcut menu handlers, and [Sample: Shell Extensions for Protocol Handlers](-search-3x-wds-ph-ui-samplecode.md) for sample code.</span></span>

### <a name="iextracticon"></a><span data-ttu-id="a0f2c-186">IExtractIcon</span><span class="sxs-lookup"><span data-stu-id="a0f2c-186">IExtractIcon</span></span>

<span data-ttu-id="a0f2c-187">**IExtractIcon** récupère une icône pour l’interface utilisateur de recherche Windows en fonction de l’URL figurant dans le PIDL fourni par votre gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-187">**IExtractIcon** retrieves an icon for the Windows Search user interface based on the URL in the PIDL provided by your protocol handler.</span></span>

<span data-ttu-id="a0f2c-188">Pour plus d’informations sur la création de gestionnaires d’icône et d' [Exemples : extensions de Shell pour les gestionnaires de protocole](-search-3x-wds-ph-ui-samplecode.md) pour l’exemple de code, consultez [création de gestionnaires d’icône](../shell/how-to-create-icon-handlers.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f2c-188">Refer to [Creating Icon Handlers](../shell/how-to-create-icon-handlers.md) for more information on creating icon handlers and [Sample: Shell Extensions for Protocol Handlers](-search-3x-wds-ph-ui-samplecode.md) for sample code.</span></span>

### <a name="ipreviewhandler"></a><span data-ttu-id="a0f2c-189">IPreviewHandler</span><span class="sxs-lookup"><span data-stu-id="a0f2c-189">IPreviewHandler</span></span>

<span data-ttu-id="a0f2c-190">Le [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) affiche un aperçu complet d’un élément sélectionné dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-190">The [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) renders a rich preview of a selected item in Windows Explorer.</span></span> <span data-ttu-id="a0f2c-191">Les versions préliminaires sont disponibles dans Windows Search 4,0 ou dans Windows Vista avec Windows Desktop Search 3. x.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-191">Previews are available in Windows Search 4.0, or in Windows Vista with Windows Desktop Search 3.x.</span></span>

<span data-ttu-id="a0f2c-192">Pour créer un gestionnaire d’aperçus personnalisé :</span><span class="sxs-lookup"><span data-stu-id="a0f2c-192">To create a custom preview handler:</span></span>

1.  <span data-ttu-id="a0f2c-193">Implémentez un [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) qui prend un [IStream](/windows/win32/api/objidl/nn-objidl-istream), en suivant les instructions fournies dans les [gestionnaires d’aperçus](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="a0f2c-193">Implement an [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) that takes an [IStream](/windows/win32/api/objidl/nn-objidl-istream), following the guidelines provided in [Preview Handlers](../shell/preview-handlers.md).</span></span>
2.  <span data-ttu-id="a0f2c-194">Inscrire votre gestionnaire d’aperçus :</span><span class="sxs-lookup"><span data-stu-id="a0f2c-194">Register your preview handler:</span></span>

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx\{8895b1c6-b41f-4c1c-a562-0d564250836f}
       @ = {<Your_PreviewHandler_GUID>}
    ```

3.  <span data-ttu-id="a0f2c-195">Effectuez les deux étapes suivantes pour implémenter un dossier Shell pour votre URL :</span><span class="sxs-lookup"><span data-stu-id="a0f2c-195">Complete the following two steps to implement a Shell folder for your URL:</span></span>
    1.  <span data-ttu-id="a0f2c-196">Dans la [méthode IShellFolder :: GetUIObjectOf](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof), gérez [IQueryAssociations](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) et retournez votre Association pour vos éléments de Shell, comme illustré dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-196">In [IShellFolder::GetUIObjectOf Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof), handle [IQueryAssociations](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) and return your association for your Shell items, as shown in the following code sample.</span></span>

        ```
        CComPtr<IQueryAssociations> spqa;
        AssocCreate(CLSID_QueryAssociations, __uuidof(IQueryAssociations), &spqa);
        spqa->Init(0, L"Your_Object_Type", NULL, NULL);
        spqa->QueryInterface(riid, ppvReturn);
        ```

        

    2.  <span data-ttu-id="a0f2c-197">Une fois que l’interpréteur de commandes interroge votre dossier Shell pour obtenir le flux de données pour initialiser le gestionnaire d’aperçus, accédez à votre méthode de [méthode IShellFolder :: BindToObject](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) , gérez IID IID \_ et renvoyez un [IStream](/windows/win32/api/objidl/nn-objidl-istream) à votre URL.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-197">After the Shell queries your Shell folder for the data stream to initialize the preview handler, go to your [IShellFolder::BindToObject Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) method, handle IID\_IStream and return an [IStream](/windows/win32/api/objidl/nn-objidl-istream) to your URL.</span></span>

<span data-ttu-id="a0f2c-198">Pour réutiliser un gestionnaire d’aperçus existant pour votre type de fichier, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="a0f2c-198">To reuse an existing preview handler for your file type, follow these two steps:</span></span>

1.  <span data-ttu-id="a0f2c-199">Inscrivez ce gestionnaire d’aperçus pour votre type de fichier à l’aide du CLSID du gestionnaire d’aperçus existant à la place de <votre \_ \_ GUID PreviewHandler>.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-199">Register that preview handler for your file type using the CLSID of the existing preview handler in place of <Your\_PreviewHandler\_GUID>.</span></span>
2.  <span data-ttu-id="a0f2c-200">Implémentez un dossier shell.</span><span class="sxs-lookup"><span data-stu-id="a0f2c-200">Implement a Shell folder.</span></span>

<span data-ttu-id="a0f2c-201">Pour plus d’informations sur la création de gestionnaires d’aperçus, consultez [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) et les [gestionnaires d’aperçus](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="a0f2c-201">For more information on creating preview handlers, see [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) and [Preview Handlers](../shell/preview-handlers.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a0f2c-202">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="a0f2c-202">Additional Resources</span></span>

-   <span data-ttu-id="a0f2c-203">Pour obtenir une vue d’ensemble du processus d’indexation, consultez [processus d’indexation](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a0f2c-203">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="a0f2c-204">Pour plus d’informations sur la création de gestionnaires, consultez [inscription d’extensions de Shell](../shell/reg-shell-exts.md), création de gestionnaires d’extensions de [Shell](../shell/handlers.md), [menu contextuel](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), [extensions d’espace de noms de Shell](../shell/nse-works.md) et gestionnaires d' [Aperçu](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="a0f2c-204">For information about creating handlers, see [Registering Shell Extensions](../shell/reg-shell-exts.md), [Creating Shell Extension Handlers](../shell/handlers.md), [Context Menu](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), [Shell Namespace Extensions](../shell/nse-works.md) and [Preview Handlers](../shell/preview-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0f2c-205">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0f2c-205">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a0f2c-206">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="a0f2c-206">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a0f2c-207">Développement de gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="a0f2c-207">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="a0f2c-208">Fonctionnement des gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="a0f2c-208">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="a0f2c-209">Notification de l’index des modifications</span><span class="sxs-lookup"><span data-stu-id="a0f2c-209">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="a0f2c-210">Exemple de code : extensions de Shell pour les gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="a0f2c-210">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="a0f2c-211">Installation et inscription de gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="a0f2c-211">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[<span data-ttu-id="a0f2c-212">Création d’un connecteur de recherche pour un gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="a0f2c-212">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[<span data-ttu-id="a0f2c-213">Débogage de gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="a0f2c-213">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
