---
title: Ajout d’icônes et de menus contextuels avec des extensions de Shell
description: Vous pouvez améliorer l’expérience de vos utilisateurs avec Microsoft Windows Desktop Search (WDS) et votre gestionnaire de protocole en implémentant des extensions de Shell.
ms.assetid: 899f3fd1-1ae9-45fe-ae6d-26d4f07bf6e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adbd6b0f4c647c47e11d14aea5e5af748a59ba53
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2020
ms.locfileid: "104198762"
---
# <a name="adding-icons-and-context-menus-with-shell-extensions"></a><span data-ttu-id="3e5f7-103">Ajout d’icônes et de menus contextuels avec des extensions de Shell</span><span class="sxs-lookup"><span data-stu-id="3e5f7-103">Adding Icons and Context Menus with Shell Extensions</span></span>

> [!NOTE]
> <span data-ttu-id="3e5f7-104">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="3e5f7-105">Dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="3e5f7-106">Vous pouvez améliorer l’expérience de vos utilisateurs avec Microsoft Windows Desktop Search (WDS) et votre gestionnaire de protocole en implémentant des extensions de Shell.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-106">You can improve your users' experience with Microsoft Windows Desktop Search (WDS) and your protocol handler by implementing Shell extensions.</span></span> <span data-ttu-id="3e5f7-107">Sans extension supplémentaire, le gestionnaire de protocole que vous créez n’inclut pas les expériences utilisateur suivantes :</span><span class="sxs-lookup"><span data-stu-id="3e5f7-107">Without further extension, the protocol handler you create will not include the following user experiences:</span></span>

-   <span data-ttu-id="3e5f7-108">WDS n’affiche pas d’icônes spécifiques pour vos résultats.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-108">WDS will not display specific icons for your results.</span></span>
-   <span data-ttu-id="3e5f7-109">Lorsque les utilisateurs double-cliquent sur un élément, l’interface utilisateur ne répond pas à l’événement.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-109">When users double-click an item, the user interface will not respond to the event.</span></span>
-   <span data-ttu-id="3e5f7-110">Quand les utilisateurs cliquent avec le bouton droit sur un élément, le menu contextuel ne prend en charge aucune opération pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-110">When users right-click an item, the context menu will not support any operations for the item.</span></span>

<span data-ttu-id="3e5f7-111">Les implémentations minimales de **IPersist** et **IPersistFolder** sont requises par **IShellFolder**, et une implémentation minimale de **IShellFolder** est requise pour **IContextMenu** et **IExtractIcon**, les deux interfaces qui offrent une expérience utilisateur plus transparente.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-111">Minimal implementations of **IPersist** and **IPersistFolder** are required by **IShellFolder**, and a minimal implementation of **IShellFolder** is required for **IContextMenu** and **IExtractIcon**, the two interfaces that provide a more seamless user experience.</span></span>

 

## <a name="ipersist"></a><span data-ttu-id="3e5f7-112">IPersist</span><span class="sxs-lookup"><span data-stu-id="3e5f7-112">IPersist</span></span>

<span data-ttu-id="3e5f7-113">L’interface **IPersist** définit la méthode unique **GetClassID**, conçue pour fournir le CLSID d’un objet qui peut être stocké de manière permanente dans le système.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-113">The **IPersist** interface defines the single method **GetClassID**, which is designed to supply the CLSID of an object that can be stored persistently in the system.</span></span>



| <span data-ttu-id="3e5f7-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="3e5f7-114">Method</span></span>       | <span data-ttu-id="3e5f7-115">Description</span><span class="sxs-lookup"><span data-stu-id="3e5f7-115">Description</span></span>                                 |
|--------------|---------------------------------------------|
| <span data-ttu-id="3e5f7-116">GetClassID ()</span><span class="sxs-lookup"><span data-stu-id="3e5f7-116">GetClassID()</span></span> | <span data-ttu-id="3e5f7-117">Retourne l’ClassID du gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="3e5f7-117">Returns the ClassID of the protocol handler</span></span> |



 

> [!Note]
>
> <span data-ttu-id="3e5f7-118">Le même CLSID doit être implémenté pour **IPersist**, **IPersistFolder** et **IShellFolder**.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-118">The same CLSID should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

 

## <a name="ipersistfolder"></a><span data-ttu-id="3e5f7-119">IPersistFolder</span><span class="sxs-lookup"><span data-stu-id="3e5f7-119">IPersistFolder</span></span>

<span data-ttu-id="3e5f7-120">L’interface **IPersistFolder** est utilisée pour initialiser les objets de dossier de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-120">The **IPersistFolder** interface is used to initialize Shell folder objects.</span></span> <span data-ttu-id="3e5f7-121">L’implémentation de cette interface, dérivée de **IPersist**, est la manière dont le dossier est indiqué à l’emplacement où il se trouve dans l’espace de noms Shell.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-121">Implementation of this interface, which is derived from **IPersist**, is how the folder is told where it is in the Shell namespace.</span></span>



| <span data-ttu-id="3e5f7-122">Méthode</span><span class="sxs-lookup"><span data-stu-id="3e5f7-122">Method</span></span>       | <span data-ttu-id="3e5f7-123">Description</span><span class="sxs-lookup"><span data-stu-id="3e5f7-123">Description</span></span>                                                                                            |
|--------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5f7-124">Initialize ()</span><span class="sxs-lookup"><span data-stu-id="3e5f7-124">Initialize()</span></span> | <span data-ttu-id="3e5f7-125">Demande à un objet de dossier de Shell de s’initialiser en fonction des informations transmises et des retours \_ OK</span><span class="sxs-lookup"><span data-stu-id="3e5f7-125">Instructs a Shell folder object to initialize itself based on the information passed and returns S\_OK</span></span> |



 

> [!Note]
>
> <span data-ttu-id="3e5f7-126">Le même CLSID doit être implémenté pour **IPersist**, **IPersistFolder** et **IShellFolder**.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-126">The same CLSID should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

<span data-ttu-id="3e5f7-127">Vous n’utilisez pas cette interface directement.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-127">You do not use this interface directly.</span></span> <span data-ttu-id="3e5f7-128">Elle est utilisée par l’implémentation du système de fichiers de l’interface IShellFolder :: BindToObject lors de l’initialisation d’un objet de dossier de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-128">It is used by the file system implementation of the IShellFolder::BindToObject interface when it initializes a Shell folder object.</span></span>

 

## <a name="ishellfolder"></a><span data-ttu-id="3e5f7-129">IShellFolder</span><span class="sxs-lookup"><span data-stu-id="3e5f7-129">IShellFolder</span></span>

<span data-ttu-id="3e5f7-130">L’interface **IShellFolder** est utilisée pour gérer les dossiers, et une implémentation partielle est nécessaire pour que les interfaces d’icône et de contexte implémentées pour un gestionnaire de protocole se comportent correctement dans l’interface utilisateur des résultats de la recherche Windows Desktop.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-130">The **IShellFolder** interface is used to manage folders, and a partial implementation is required so that the icon and context interfaces implemented for a protocol handler will behave correctly in the Windows Desktop Search results user interface.</span></span> <span data-ttu-id="3e5f7-131">La plupart des fonctionnalités requises sont exposées par le biais de la méthode **GetUIObjectOf** .</span><span class="sxs-lookup"><span data-stu-id="3e5f7-131">Most of the functionality required is exposed through the **GetUIObjectOf** method.</span></span> <span data-ttu-id="3e5f7-132">Cette méthode permet à un complément d’interroger les interfaces **IExtractIcon** et **IContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="3e5f7-132">This method enables an add-in to query for the **IExtractIcon** and **IContextMenu** interfaces.</span></span>

<span data-ttu-id="3e5f7-133">L’interface **IShellFolder** utilise PIDL à la place des URL.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-133">The **IShellFolder** interface uses PIDLs instead of URLs.</span></span> <span data-ttu-id="3e5f7-134">Contrairement aux spécifications d’une extension d’espace de noms complète, les compléments peuvent utiliser une structure IDL simple qui contient uniquement l’URL.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-134">In contrast to the requirements of a complete Namespace extension, add-ins can use a simple IDL structure that contains only the URL.</span></span>

<span data-ttu-id="3e5f7-135">Les méthodes suivantes de **IShellFolder** doivent être implémentées.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-135">The following methods of **IShellFolder** must be implemented.</span></span> <span data-ttu-id="3e5f7-136">Notez que cinq de ces méthodes nécessitent une implémentation minimale.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-136">Note that five of these methods require minimal implementation.</span></span>



| <span data-ttu-id="3e5f7-137">Méthode</span><span class="sxs-lookup"><span data-stu-id="3e5f7-137">Method</span></span>             | <span data-ttu-id="3e5f7-138">Description</span><span class="sxs-lookup"><span data-stu-id="3e5f7-138">Description</span></span>                                                                                                                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5f7-139">BindToObject()</span><span class="sxs-lookup"><span data-stu-id="3e5f7-139">BindToObject()</span></span>     | <span data-ttu-id="3e5f7-140">Retourne E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="3e5f7-140">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="3e5f7-141">BindToStorage()</span><span class="sxs-lookup"><span data-stu-id="3e5f7-141">BindToStorage()</span></span>    | <span data-ttu-id="3e5f7-142">Retourne E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="3e5f7-142">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="3e5f7-143">CreateViewObject()</span><span class="sxs-lookup"><span data-stu-id="3e5f7-143">CreateViewObject()</span></span> | <span data-ttu-id="3e5f7-144">Retourne E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="3e5f7-144">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="3e5f7-145">SetNameOf()</span><span class="sxs-lookup"><span data-stu-id="3e5f7-145">SetNameOf()</span></span>        | <span data-ttu-id="3e5f7-146">Retourne E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="3e5f7-146">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="3e5f7-147">ParseDisplayName()</span><span class="sxs-lookup"><span data-stu-id="3e5f7-147">ParseDisplayName()</span></span> | <span data-ttu-id="3e5f7-148">Convertit une URL en structure PIDL</span><span class="sxs-lookup"><span data-stu-id="3e5f7-148">Converts a URL to the PIDL structure</span></span>                                                                                                                                                                        |
| <span data-ttu-id="3e5f7-149">CompareIDs()</span><span class="sxs-lookup"><span data-stu-id="3e5f7-149">CompareIDs()</span></span>       | <span data-ttu-id="3e5f7-150">Compare deux valeurs PIDL</span><span class="sxs-lookup"><span data-stu-id="3e5f7-150">Compares two PIDL values</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="3e5f7-151">GetDisplayNameOf()</span><span class="sxs-lookup"><span data-stu-id="3e5f7-151">GetDisplayNameOf()</span></span> | <span data-ttu-id="3e5f7-152">Retourne l’URL d’un PIDL</span><span class="sxs-lookup"><span data-stu-id="3e5f7-152">Returns the URL for a PIDL</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="3e5f7-153">GetUIObjectOf()</span><span class="sxs-lookup"><span data-stu-id="3e5f7-153">GetUIObjectOf()</span></span>    | <span data-ttu-id="3e5f7-154">Cette méthode est similaire à la méthode QueryInterface OLE COM.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-154">This method is similar to the OLE COM QueryInterface method.</span></span> <span data-ttu-id="3e5f7-155">Si une icône est demandée, l’appelant demande l’IID \_ IExtractIcon ; si un menu contextuel est demandé, l’appelant demande l' \_ IID IContextMenu.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-155">If an icon is requested, the caller requests the IID\_IExtractIcon; if a context menu is requested, the caller requests the IID\_IContextMenu.</span></span> |



 

> [!Note]
>
> <span data-ttu-id="3e5f7-156">Le même CLSID doit être implémenté pour **IPersist**, **IPersistFolder** et **IShellFolder**.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-156">The same CLSID should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

<span data-ttu-id="3e5f7-157">**IShellFolder** n’est pas utilisé pour énumérer des dossiers.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-157">**IShellFolder** is not used to enumerate folders.</span></span> <span data-ttu-id="3e5f7-158">Cela signifie que le nom complet d’un dossier sera l’URL physique.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-158">This means that the display name of a folder will be the physical URL.</span></span> <span data-ttu-id="3e5f7-159">Cela peut changer à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-159">This may change in the future.</span></span>

 

## <a name="icontextmenu"></a><span data-ttu-id="3e5f7-160">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="3e5f7-160">IContextMenu</span></span>

<span data-ttu-id="3e5f7-161">Lorsque WDS affiche les résultats à l’utilisateur, l’utilisateur peut cliquer avec le bouton droit sur un élément et afficher un menu contextuel défini par votre interface **IContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="3e5f7-161">When WDS displays results to the user, the user can right-click an item and see a context menu defined by your **IContextMenu** interface.</span></span>

<span data-ttu-id="3e5f7-162">L’action par défaut dans le menu contextuel est la même que celle effectuée lors d’un double-clic sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-162">The default action on the context menu is the same action taken when the item is double-clicked.</span></span> <span data-ttu-id="3e5f7-163">Sans les interfaces **IShellFolder** ou **IContextMenu** correspondantes pour l’élément, le comportement par défaut d’un événement de double-clic consiste à passer l’URL en tant qu’argument à la fonction ShellExecute.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-163">Without the corresponding **IShellFolder** or **IContextMenu** interfaces for the item, the default behavior for a double-click event is to pass the URL as an argument to the ShellExecute function.</span></span>

 

## <a name="iextracticon"></a><span data-ttu-id="3e5f7-164">IExtractIcon</span><span class="sxs-lookup"><span data-stu-id="3e5f7-164">IExtractIcon</span></span>

<span data-ttu-id="3e5f7-165">**IExtractIcon** récupère une icône pour l’interface utilisateur WDS en fonction de l’URL figurant dans le PIDL fourni par votre gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-165">**IExtractIcon** retrieves an icon for the WDS user interface based on the URL in the PIDL provided by your protocol handler.</span></span>

 

## <a name="code-sample"></a><span data-ttu-id="3e5f7-166">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="3e5f7-166">Code Sample</span></span>

<span data-ttu-id="3e5f7-167">L' [exemple de code d’interface utilisateur du gestionnaire de protocole personnalisé](-search-2x-wds-ph-ui-samplecode.md) illustre une implémentation de **IShellFolder** et des interfaces de prise en charge, et prend en charge la manipulation du PIDL.</span><span class="sxs-lookup"><span data-stu-id="3e5f7-167">The [Custom Protocol Handler User Interface Sample Code](-search-2x-wds-ph-ui-samplecode.md) demonstrates an implementation of **IShellFolder** and supporting interfaces and includes support for manipulating the PIDLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e5f7-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3e5f7-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3e5f7-169">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="3e5f7-169">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3e5f7-170">Exemple de code d’interface utilisateur du gestionnaire de protocole personnalisé</span><span class="sxs-lookup"><span data-stu-id="3e5f7-170">Custom Protocol Handler User Interface Sample Code</span></span>](-search-2x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="3e5f7-171">Installation et inscription de gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="3e5f7-171">Installing and Registering Protocol Handlers</span></span>](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 




