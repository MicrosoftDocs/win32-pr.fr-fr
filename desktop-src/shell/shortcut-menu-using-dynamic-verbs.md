---
description: Les gestionnaires de menus contextuels sont également appelés gestionnaires de menus contextuels ou gestionnaires de verbes. Un gestionnaire de menu contextuel est un type de gestionnaire de type de fichier.
ms.assetid: 7FC65C6F-3798-404c-B359-2BC75D3F54E7
title: Personnalisation d’un menu contextuel à l’aide de verbes dynamiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b24f035e84f0bde6dccde09f1ed94fefce421b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973463"
---
# <a name="customizing-a-shortcut-menu-using-dynamic-verbs"></a><span data-ttu-id="73489-104">Personnalisation d’un menu contextuel à l’aide de verbes dynamiques</span><span class="sxs-lookup"><span data-stu-id="73489-104">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>

<span data-ttu-id="73489-105">Les gestionnaires de menus contextuels sont également appelés gestionnaires de menus contextuels ou gestionnaires de verbes.</span><span class="sxs-lookup"><span data-stu-id="73489-105">Shortcut menu handlers are also known as context menu handlers or verb handlers.</span></span> <span data-ttu-id="73489-106">Un gestionnaire de menu contextuel est un type de gestionnaire de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="73489-106">A shortcut menu handler is a type of file type handler.</span></span>

<span data-ttu-id="73489-107">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="73489-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="73489-108">À propos des verbes statiques et dynamiques</span><span class="sxs-lookup"><span data-stu-id="73489-108">About Static and Dynamic Verbs</span></span>](#about-static-and-dynamic-verbs)
-   [<span data-ttu-id="73489-109">Fonctionnement des gestionnaires de menus contextuels avec les verbes dynamiques</span><span class="sxs-lookup"><span data-stu-id="73489-109">How Shortcut Menu Handlers Work with Dynamic Verbs</span></span>](#how-shortcut-menu-handlers-work-with-dynamic-verbs)
-   [<span data-ttu-id="73489-110">Éviter les collisions dues à des noms de verbe non qualifiés</span><span class="sxs-lookup"><span data-stu-id="73489-110">Avoiding Collisions Due to Unqualified Verb Names</span></span>](#avoiding-collisions-due-to-unqualified-verb-names)
-   [<span data-ttu-id="73489-111">Inscription d’un gestionnaire de menu contextuel avec un verbe dynamique</span><span class="sxs-lookup"><span data-stu-id="73489-111">Registering a Shortcut Menu Handler with a Dynamic Verb</span></span>](#registering-a-shortcut-menu-handler-with-a-dynamic-verb)
-   [<span data-ttu-id="73489-112">Implémentation de l’interface IContextMenu</span><span class="sxs-lookup"><span data-stu-id="73489-112">Implementing the IContextMenu Interface</span></span>](#implementing-the-icontextmenu-interface)
    -   [<span data-ttu-id="73489-113">IContextMenu :: GetCommandString, méthode</span><span class="sxs-lookup"><span data-stu-id="73489-113">IContextMenu::GetCommandString Method</span></span>](#icontextmenugetcommandstring-method)
    -   [<span data-ttu-id="73489-114">IContextMenu :: commande InvokeCommand, méthode</span><span class="sxs-lookup"><span data-stu-id="73489-114">IContextMenu::InvokeCommand Method</span></span>](#icontextmenuinvokecommand-method)
    -   [<span data-ttu-id="73489-115">IContextMenu :: QueryContextMenu, méthode</span><span class="sxs-lookup"><span data-stu-id="73489-115">IContextMenu::QueryContextMenu Method</span></span>](#icontextmenuquerycontextmenu-method)
-   [<span data-ttu-id="73489-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="73489-116">Related topics</span></span>](#related-topics)

## <a name="about-static-and-dynamic-verbs"></a><span data-ttu-id="73489-117">À propos des verbes statiques et dynamiques</span><span class="sxs-lookup"><span data-stu-id="73489-117">About Static and Dynamic Verbs</span></span>

<span data-ttu-id="73489-118">Nous vous encourageons vivement à implémenter un menu contextuel à l’aide d’une des méthodes de verbe statiques.</span><span class="sxs-lookup"><span data-stu-id="73489-118">We strongly encourage you to implement a shortcut menu using one of the static verb methods.</span></span> <span data-ttu-id="73489-119">Nous vous recommandons de suivre les instructions fournies dans la section « personnalisation d’un menu contextuel à l’aide de verbes statiques » de [création de gestionnaires de menu contextuel](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="73489-119">We recommend that you follow the instructions provided in the "Customizing a Shortcut Menu using Static Verbs" section of [Creating Context Menu Handlers](context-menu-handlers.md).</span></span> <span data-ttu-id="73489-120">Pour obtenir le comportement dynamique pour les verbes statiques dans Windows 7 et versions ultérieures, consultez « obtention du comportement dynamique pour les verbes statiques » dans [création de gestionnaires de menus contextuels](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="73489-120">To get dynamic behavior for static verbs in Windows 7 and later, see "Getting Dynamic Behavior for Static Verbs" in [Creating Context Menu Handlers](context-menu-handlers.md).</span></span> <span data-ttu-id="73489-121">Pour plus d’informations sur l’implémentation d’un verbe statique et sur les verbes dynamiques à éviter, consultez [choix d’un verbe statique ou dynamique pour votre menu contextuel](shortcut-choose-method.md).</span><span class="sxs-lookup"><span data-stu-id="73489-121">For details on static verb implementation, and which dynamic verbs to avoid, see [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md).</span></span>

<span data-ttu-id="73489-122">Si vous devez étendre le menu contextuel d’un type de fichier en inscrivant un verbe dynamique pour le type de fichier, suivez les instructions fournies plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="73489-122">If you must extend the shortcut menu for a file type by registering a dynamic verb for the file type, then follow the instructions provided later in this topic.</span></span>

> [!Note]  
> <span data-ttu-id="73489-123">Des considérations spéciales sont à prendre en compte pour Windows 64 bits lors de l’enregistrement de gestionnaires qui fonctionnent dans le contexte d’applications 32 bits : quand les verbes de Shell sont appelés dans le contexte d’une application 32 bits, le sous-système WOW64 redirige l’accès au système de fichiers vers certains chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="73489-123">There are special considerations for 64-bit Windows when registering handlers that work in the context of 32-bit applications: when Shell verbs are invoked in the context of a 32-bit application, the WOW64 subsystem redirects file system access to some paths.</span></span> <span data-ttu-id="73489-124">Si votre gestionnaire. exe est stocké dans l’un de ces chemins d’accès, il n’est pas accessible dans ce contexte.</span><span class="sxs-lookup"><span data-stu-id="73489-124">If your .exe handler is stored in one of those paths, it is not accessible in this context.</span></span> <span data-ttu-id="73489-125">Par conséquent, pour une solution de contournement, stockez votre fichier. exe dans un chemin d’accès qui n’est pas redirigé, ou stockez une version stub de votre fichier. exe qui lance la version réelle.</span><span class="sxs-lookup"><span data-stu-id="73489-125">Therefore, as a work around, either store your .exe in a path that does not get redirected, or store a stub version of your .exe that launches the real version.</span></span>

 

## <a name="how-shortcut-menu-handlers-work-with-dynamic-verbs"></a><span data-ttu-id="73489-126">Fonctionnement des gestionnaires de menus contextuels avec les verbes dynamiques</span><span class="sxs-lookup"><span data-stu-id="73489-126">How Shortcut Menu Handlers Work with Dynamic Verbs</span></span>

<span data-ttu-id="73489-127">En plus de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), les gestionnaires de menus contextuels exportent les interfaces supplémentaires suivantes pour gérer la messagerie nécessaire pour implémenter les éléments de menu owner-drawn :</span><span class="sxs-lookup"><span data-stu-id="73489-127">In addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), shortcut menu handlers export the following additional interfaces to handle the messaging needed to implement owner-drawn menu items:</span></span>

-   <span data-ttu-id="73489-128">[**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="73489-128">[**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (mandatory)</span></span>
-   <span data-ttu-id="73489-129">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="73489-129">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (mandatory)</span></span>
-   <span data-ttu-id="73489-130">[**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (facultatif)</span><span class="sxs-lookup"><span data-stu-id="73489-130">[**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (optional)</span></span>
-   <span data-ttu-id="73489-131">[**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (facultatif)</span><span class="sxs-lookup"><span data-stu-id="73489-131">[**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (optional)</span></span>

<span data-ttu-id="73489-132">Pour plus d’informations sur les éléments de menu owner-drawn, consultez la section *creating Owner-Drawn menu items* dans [using menus](../menurc/using-menus.md).</span><span class="sxs-lookup"><span data-stu-id="73489-132">For more information on owner-drawn menu items, see the *Creating Owner-Drawn Menu Items* section in [Using Menus](../menurc/using-menus.md).</span></span>

<span data-ttu-id="73489-133">L’interpréteur de commandes utilise l’interface [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) pour initialiser le gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="73489-133">Shell uses the [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface to initialize the handler.</span></span> <span data-ttu-id="73489-134">Lorsque l’interpréteur de commandes appelle [**IShellExtInit :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), il passe un objet de données avec le nom de l’objet et un pointeur vers une liste d’identificateurs d’éléments (PIDL) du dossier qui contient le fichier.</span><span class="sxs-lookup"><span data-stu-id="73489-134">When the Shell calls [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), it passes in a data object with the object's name and a pointer to an item identifier list (PIDL) of the folder that contains the file.</span></span> <span data-ttu-id="73489-135">Le paramètre *hkeyProgID* est l’emplacement du Registre sous lequel le handle du menu contextuel est inscrit.</span><span class="sxs-lookup"><span data-stu-id="73489-135">The *hkeyProgID* parameter is the registry location under which the shortcut menu handle is registered.</span></span> <span data-ttu-id="73489-136">La méthode **IShellExtInit :: Initialize** doit extraire le nom de fichier de l’objet de données et stocker le nom et le pointeur du dossier vers une liste d’identificateurs d’éléments (PIDL) pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="73489-136">The **IShellExtInit::Initialize** method must extract the file name from the data object and store the name and the folder's pointer to an item identifier list (PIDL) for later use.</span></span> <span data-ttu-id="73489-137">Pour plus d’informations sur l’initialisation du gestionnaire, consultez [implémentation de IShellExtInit](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="73489-137">For more information on handler initialization, see [Implementing IShellExtInit](handlers.md).</span></span>

<span data-ttu-id="73489-138">Lorsque les verbes sont présentés dans un menu contextuel, ils sont d’abord découverts, puis présentés à l’utilisateur et enfin appelés.</span><span class="sxs-lookup"><span data-stu-id="73489-138">When verbs are presented in a shortcut menu, they are first discovered, then presented to the user, and finally invoked.</span></span> <span data-ttu-id="73489-139">La liste suivante décrit ces trois étapes plus en détail :</span><span class="sxs-lookup"><span data-stu-id="73489-139">The following list describes these three steps in more detail:</span></span>

1.  <span data-ttu-id="73489-140">L’interpréteur de commandes appelle [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), qui retourne un jeu de verbes qui peut être basé sur l’état des éléments ou du système.</span><span class="sxs-lookup"><span data-stu-id="73489-140">The Shell calls [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), which returns a set of verbs that can be based on the state of the items or the system.</span></span>
2.  <span data-ttu-id="73489-141">Le système transmet un handle **HMENU** que la méthode peut utiliser pour ajouter des éléments au menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="73489-141">The system passes in an **HMENU** handle that the method can use to add items to the shortcut menu.</span></span>
3.  <span data-ttu-id="73489-142">Si l’utilisateur clique sur l’un des éléments du gestionnaire, le shell appelle [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span><span class="sxs-lookup"><span data-stu-id="73489-142">If the user clicks one of the handler's items, the Shell calls [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span> <span data-ttu-id="73489-143">Le gestionnaire peut ensuite exécuter la commande appropriée.</span><span class="sxs-lookup"><span data-stu-id="73489-143">The handler can then execute the appropriate command.</span></span>

## <a name="avoiding-collisions-due-to-unqualified-verb-names"></a><span data-ttu-id="73489-144">Éviter les collisions dues à des noms de verbe non qualifiés</span><span class="sxs-lookup"><span data-stu-id="73489-144">Avoiding Collisions Due to Unqualified Verb Names</span></span>

<span data-ttu-id="73489-145">Étant donné que les verbes sont inscrits par type, le même nom de verbe peut être utilisé pour les verbes sur différents éléments.</span><span class="sxs-lookup"><span data-stu-id="73489-145">Because verbs are registered per type, the same verb name can be used for verbs on different items.</span></span> <span data-ttu-id="73489-146">Cela permet aux applications de faire référence à des verbes communs indépendants du type d’élément.</span><span class="sxs-lookup"><span data-stu-id="73489-146">Doing so enables applications to refer to common verbs independent of the item type.</span></span> <span data-ttu-id="73489-147">Bien que cette fonctionnalité soit utile, l’utilisation de noms non qualifiés peut entraîner des collisions entre plusieurs éditeurs de logiciels indépendants (ISV) qui choisissent le même nom de verbe.</span><span class="sxs-lookup"><span data-stu-id="73489-147">While this functionality is useful, the use of unqualified names can result in collisions with multiple independent software vendors (ISVs) that choose the same verb name.</span></span> <span data-ttu-id="73489-148">Pour éviter cela, préfixez toujours les verbes avec le nom ISV comme suit :</span><span class="sxs-lookup"><span data-stu-id="73489-148">To avoid this, always prefix verbs with the ISV name as follows:</span></span>

`ISV_Name.verb`

<span data-ttu-id="73489-149">Utilisez toujours un ProgID spécifique à l’application.</span><span class="sxs-lookup"><span data-stu-id="73489-149">Always use an application specific ProgID.</span></span> <span data-ttu-id="73489-150">L’adoption de la Convention de mappage de l’extension de nom de fichier à un ProgID fourni par un ISV évite les collisions potentielles.</span><span class="sxs-lookup"><span data-stu-id="73489-150">Adopting the convention of mapping the file name extension to an ISV provided ProgID avoids potential collisions.</span></span> <span data-ttu-id="73489-151">Toutefois, étant donné que certains types d’éléments n’utilisent pas ce mappage, il est nécessaire de nommer les noms uniques des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="73489-151">However, because some item types do not use this mapping, there is a need for vendor-unique names.</span></span> <span data-ttu-id="73489-152">Lorsque vous ajoutez un verbe à un ProgID existant qui peut déjà être inscrit dans ce verbe, vous devez d’abord supprimer la clé de registre de l’ancien verbe avant d’ajouter votre propre verbe.</span><span class="sxs-lookup"><span data-stu-id="73489-152">When adding a verb to an existing ProgID that might already have that verb registered, you must first remove the registry key for the old verb before adding your own verb.</span></span> <span data-ttu-id="73489-153">Vous devez le faire pour éviter de fusionner les informations de verbe à partir des deux verbes.</span><span class="sxs-lookup"><span data-stu-id="73489-153">You must do so to avoid merging the verb information from the two verbs.</span></span> <span data-ttu-id="73489-154">Dans le cas contraire, cela entraîne un comportement imprévisible.</span><span class="sxs-lookup"><span data-stu-id="73489-154">Failure to do so results in unpredictable behavior.</span></span>

## <a name="registering-a-shortcut-menu-handler-with-a-dynamic-verb"></a><span data-ttu-id="73489-155">Inscription d’un gestionnaire de menu contextuel avec un verbe dynamique</span><span class="sxs-lookup"><span data-stu-id="73489-155">Registering a Shortcut Menu Handler with a Dynamic Verb</span></span>

<span data-ttu-id="73489-156">Les gestionnaires de menus contextuels sont associés à un type de fichier ou à un dossier.</span><span class="sxs-lookup"><span data-stu-id="73489-156">Shortcut menu handlers are associated with either a file type or a folder.</span></span> <span data-ttu-id="73489-157">Pour les types de fichiers, le gestionnaire est inscrit sous la sous-clé suivante.</span><span class="sxs-lookup"><span data-stu-id="73489-157">For file types, the handler is registered under the following subkey.</span></span>

```
HKEY_CLASSES_ROOT
   Program ID
      shellex
         ContextMenuHandlers
```

<span data-ttu-id="73489-158">Pour associer un gestionnaire de menu contextuel à un type de fichier ou à un dossier, commencez par créer une sous-clé sous la sous-clé **ContextMenuHandlers** .</span><span class="sxs-lookup"><span data-stu-id="73489-158">To associate a shortcut menu handler with either a file type or a folder, first create a subkey under the **ContextMenuHandlers** subkey.</span></span> <span data-ttu-id="73489-159">Nommez la sous-clé du gestionnaire et définissez la valeur par défaut de la sous-clé sur la forme de chaîne du GUID de l’identificateur de classe (CLSID) du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="73489-159">Name the subkey for the handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span>

<span data-ttu-id="73489-160">Ensuite, pour associer un gestionnaire de menu contextuel à différents genres de dossiers, inscrivez le gestionnaire de la même façon que vous le feriez pour un type de fichier, mais sous la sous-clé *FolderType* comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="73489-160">Then to associate a shortcut menu handler with different kinds of folders, register the handler the same way you would for a file type, but under the *FolderType* subkey as shown in the following example.</span></span>

```
HKEY_CLASSES_ROOT
   FolderType
      shellex
         ContextMenuHandlers
```

<span data-ttu-id="73489-161">Pour plus d’informations sur les types de dossiers pour lesquels vous pouvez enregistrer des gestionnaires, consultez [inscription des gestionnaires d’extensions de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="73489-161">For more information about about which folder types you can register handlers for, see [Registering Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="73489-162">Si un menu contextuel est associé à un type de fichier, double-cliquez sur un objet pour lancer normalement la commande par défaut et la méthode [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) du gestionnaire n’est pas appelée.</span><span class="sxs-lookup"><span data-stu-id="73489-162">If a file type has a shortcut menu associated with it, then double-clicking an object normally launches the default command, and the handler's [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) method is not called.</span></span> <span data-ttu-id="73489-163">Pour spécifier que la méthode **IContextMenu :: QueryContextMenu** du gestionnaire doit être appelée lors d’un double-clic sur un objet, créez une sous-clé sous la sous-clé **CLSID** du gestionnaire, comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="73489-163">To specify that the handler's **IContextMenu::QueryContextMenu** method should be called when an object is double-clicked, create a subkey under the handler's **CLSID** subkey as shown here.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {00000000-1111-2222-3333-444444444444}
         shellex
            MayChangeDefaultMenu
```

<span data-ttu-id="73489-164">Quand vous double-cliquez sur un objet associé au gestionnaire, [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) est appelé avec l’indicateur **CMF \_ DEFAULTONLY** défini dans le paramètre *uFlags* .</span><span class="sxs-lookup"><span data-stu-id="73489-164">When an object associated with the handler is double-clicked, [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) is called with the **CMF\_DEFAULTONLY** flag set in the *uFlags* parameter.</span></span>

<span data-ttu-id="73489-165">Les gestionnaires de menus contextuels ne doivent définir la sous-clé **MayChangeDefaultMenu** que s’ils peuvent avoir besoin de modifier le verbe par défaut du menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="73489-165">Shortcut menu handlers should set the **MayChangeDefaultMenu** subkey only if they might need to change the shortcut menu's default verb.</span></span> <span data-ttu-id="73489-166">La définition de cette sous-clé force le système à charger la DLL du gestionnaire lors d’un double-clic sur un élément associé.</span><span class="sxs-lookup"><span data-stu-id="73489-166">Setting this subkey forces the system to load the handler's DLL when an associated item is double-clicked.</span></span> <span data-ttu-id="73489-167">Si votre gestionnaire ne modifie pas le verbe par défaut, vous ne devez pas définir cette sous-clé, car cela amène le système à charger votre DLL inutilement.</span><span class="sxs-lookup"><span data-stu-id="73489-167">If your handler does not change the default verb, you should not set this subkey because doing so causes the system to load your DLL unnecessarily.</span></span>

<span data-ttu-id="73489-168">L’exemple suivant illustre les entrées de Registre qui activent un gestionnaire de menu contextuel pour un type de fichier. MYP.</span><span class="sxs-lookup"><span data-stu-id="73489-168">The following example illustrates registry entries that enable a shortcut menu handler for an .myp file type.</span></span> <span data-ttu-id="73489-169">La sous-clé **CLSID** du gestionnaire comprend une sous-clé **MayChangeDefaultMenu** pour garantir que le gestionnaire est appelé lorsque l’utilisateur double-clique sur un objet connexe.</span><span class="sxs-lookup"><span data-stu-id="73489-169">The handler's **CLSID** subkey includes a **MayChangeDefaultMenu** subkey to guarantee that the handler is called when the user double-clicks a related object.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
         shellex
            MayChangeDefaultMenu
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         ContextMenuHandler
            MyCommand = {00000000-1111-2222-3333-444444444444}
```

## <a name="implementing-the-icontextmenu-interface"></a><span data-ttu-id="73489-170">Implémentation de l’interface IContextMenu</span><span class="sxs-lookup"><span data-stu-id="73489-170">Implementing the IContextMenu Interface</span></span>

<span data-ttu-id="73489-171">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) est la méthode la plus simple, mais également la plus compliquée à implémenter.</span><span class="sxs-lookup"><span data-stu-id="73489-171">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated method to implement.</span></span> <span data-ttu-id="73489-172">Nous vous recommandons vivement d’implémenter un verbe à l’aide de l’une des méthodes Verb statiques.</span><span class="sxs-lookup"><span data-stu-id="73489-172">We strongly recommend that you implement a verb by using one of the static verb methods.</span></span> <span data-ttu-id="73489-173">Pour plus d’informations, consultez [choix d’un verbe statique ou dynamique pour votre menu contextuel](shortcut-choose-method.md).</span><span class="sxs-lookup"><span data-stu-id="73489-173">For more information, see [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md).</span></span> <span data-ttu-id="73489-174">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) a trois méthodes, **GetCommandString**, **commande InvokeCommand** et **QueryContextMenu**, qui sont décrites ici en détail.</span><span class="sxs-lookup"><span data-stu-id="73489-174">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) has three methods, **GetCommandString**, **InvokeCommand**, and **QueryContextMenu**, which are discussed here in detail.</span></span>

### <a name="icontextmenugetcommandstring-method"></a><span data-ttu-id="73489-175">IContextMenu :: GetCommandString, méthode</span><span class="sxs-lookup"><span data-stu-id="73489-175">IContextMenu::GetCommandString Method</span></span>

<span data-ttu-id="73489-176">La méthode [**IContextMenu :: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) du gestionnaire est utilisée pour retourner le nom canonique d’un verbe.</span><span class="sxs-lookup"><span data-stu-id="73489-176">The handler's [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) method is used to return the canonical name for a verb.</span></span> <span data-ttu-id="73489-177">Cette méthode est facultative.</span><span class="sxs-lookup"><span data-stu-id="73489-177">This method is optional.</span></span> <span data-ttu-id="73489-178">Dans Windows XP et les versions antérieures de Windows, lorsque l’Explorateur Windows a une barre d’État, cette méthode est utilisée pour récupérer le texte d’aide qui s’affiche dans la barre d’État pour un élément de menu.</span><span class="sxs-lookup"><span data-stu-id="73489-178">In Windows XP and earlier versions of Windows, when Windows Explorer has a Status bar, this method is used to retrieve the help text that is displayed in the Status bar for a menu item.</span></span>

<span data-ttu-id="73489-179">Le paramètre *idCmd* contient le décalage de l’identificateur de la commande qui a été définie lors de l’appel de [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="73489-179">The *idCmd* parameter holds the identifier offset of the command that was defined when [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) was called.</span></span> <span data-ttu-id="73489-180">Si une chaîne d’aide est demandée, *uFlags* est défini sur **GC \_ HELPTEXTW**.</span><span class="sxs-lookup"><span data-stu-id="73489-180">If a help string is requested, *uFlags* will be set to **GCS\_HELPTEXTW**.</span></span> <span data-ttu-id="73489-181">Copiez la chaîne d’aide dans la mémoire tampon *pszName* , en la convertissant en **PWSTR**.</span><span class="sxs-lookup"><span data-stu-id="73489-181">Copy the help string to the *pszName* buffer, casting it to a **PWSTR**.</span></span> <span data-ttu-id="73489-182">La chaîne de verbe est demandée en affectant à *uFlags* la valeur **GC \_ VERBW**.</span><span class="sxs-lookup"><span data-stu-id="73489-182">The verb string is requested by setting *uFlags* to **GCS\_VERBW**.</span></span> <span data-ttu-id="73489-183">Copiez la chaîne appropriée dans *pszName*, tout comme avec la chaîne d’aide.</span><span class="sxs-lookup"><span data-stu-id="73489-183">Copy the appropriate string to *pszName*, just as with the help string.</span></span> <span data-ttu-id="73489-184">Les indicateurs **GC \_ Validate** et **GC \_ VALIDATEW** ne sont pas utilisés par les gestionnaires de menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="73489-184">The **GCS\_VALIDATEA** and **GCS\_VALIDATEW** flags are not used by shortcut menu handlers.</span></span>

<span data-ttu-id="73489-185">L’exemple suivant illustre une implémentation simple de [**IContextMenu :: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) qui correspond à l’exemple [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) donné dans la section [IContextMenu :: QueryContextMenu](#icontextmenuquerycontextmenu-method) de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="73489-185">The following example shows a simple implementation of [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) that corresponds to the [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) example given in the [IContextMenu::QueryContextMenu Method](#icontextmenuquerycontextmenu-method) section of this topic.</span></span> <span data-ttu-id="73489-186">Étant donné que le gestionnaire ajoute un seul élément de menu, il n’existe qu’un seul jeu de chaînes qui peut être retourné.</span><span class="sxs-lookup"><span data-stu-id="73489-186">Because the handler adds only one menu item, there is only one set of strings that can be returned.</span></span> <span data-ttu-id="73489-187">La méthode teste si *idCmd* est valide et, si c’est le cas, retourne la chaîne demandée.</span><span class="sxs-lookup"><span data-stu-id="73489-187">The method tests whether *idCmd* is valid and, if it is, returns the requested string.</span></span>

<span data-ttu-id="73489-188">La fonction [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) est utilisée pour copier la chaîne demandée dans *pszName* afin de garantir que la chaîne copiée ne dépasse pas la taille de la mémoire tampon spécifiée par *cchName*.</span><span class="sxs-lookup"><span data-stu-id="73489-188">The [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) function is used to copy the requested string to *pszName* to ensure that the copied string does not exceed the size of the buffer specified by *cchName*.</span></span> <span data-ttu-id="73489-189">Cet exemple implémente uniquement la prise en charge des valeurs Unicode de *uFlags*, car seules celles-ci ont été utilisées dans l’Explorateur Windows depuis Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="73489-189">This example only implements support for the Unicode values of *uFlags*, because only those have been used in Windows Explorer since Windows 2000.</span></span>


```C++
IFACEMETHODIMP CMenuExtension::GetCommandString(UINT idCommand, 
                                                UINT uFlags, 
                                                UINT *pReserved, 
                                                PSTR pszName, 
                                                UINT cchName)
{
    HRESULT hr = E_INVALIDARG;

    if (idCommand == IDM_DISPLAY)
    {
        switch (uFlags)
        {
            case GCS_HELPTEXTW:
                // Only useful for pre-Vista versions of Windows that 
                // have a Status bar.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"Display File Name");
                break; 

            case GCS_VERBW:
                // GCS_VERBW is an optional feature that enables a caller
                // to discover the canonical name for the verb passed in
                // through idCommand.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"DisplayFileName");
                break; 
        }
    }
    return hr;
}
```



### <a name="icontextmenuinvokecommand-method"></a><span data-ttu-id="73489-190">IContextMenu :: commande InvokeCommand, méthode</span><span class="sxs-lookup"><span data-stu-id="73489-190">IContextMenu::InvokeCommand Method</span></span>

<span data-ttu-id="73489-191">Cette méthode est appelée lorsqu’un utilisateur clique sur un élément de menu pour indiquer au gestionnaire d’exécuter la commande associée.</span><span class="sxs-lookup"><span data-stu-id="73489-191">This method is called when a user clicks a menu item to tell the handler to run the associated command.</span></span> <span data-ttu-id="73489-192">Le paramètre *Pici* pointe vers une structure qui contient les informations requises.</span><span class="sxs-lookup"><span data-stu-id="73489-192">The *pici* parameter points to a structure that contains the information required.</span></span>

<span data-ttu-id="73489-193">Bien que *Pici* soit déclaré dans shlobj. h comme une structure [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) , dans la pratique, il pointe souvent vers une structure [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) .</span><span class="sxs-lookup"><span data-stu-id="73489-193">Although *pici* is declared in Shlobj.h as a [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) structure, in practice it often points to a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure.</span></span> <span data-ttu-id="73489-194">Cette structure est une version étendue de **CMINVOKECOMMANDINFO** et a plusieurs membres supplémentaires qui permettent de passer des chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="73489-194">This structure is an extended version of **CMINVOKECOMMANDINFO** and has several additional members that make it possible to pass Unicode strings.</span></span>

<span data-ttu-id="73489-195">Vérifiez le membre **cbSize** de *Pici* pour déterminer la structure qui a été transmise.</span><span class="sxs-lookup"><span data-stu-id="73489-195">Check the **cbSize** member of *pici* to determine which structure was passed in.</span></span> <span data-ttu-id="73489-196">S’il s’agit d’une structure [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) et que l’indicateur **\_ \_ Unicode de masque Cmic** est défini pour le membre **fmask** , castez *Pici* en **CMINVOKECOMMANDINFOEX**.</span><span class="sxs-lookup"><span data-stu-id="73489-196">If it is a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure and the **fMask** member has the **CMIC\_MASK\_UNICODE** flag set, cast *pici* to **CMINVOKECOMMANDINFOEX**.</span></span> <span data-ttu-id="73489-197">Cela permet à votre application d’utiliser les informations Unicode contenues dans les cinq derniers membres de la structure.</span><span class="sxs-lookup"><span data-stu-id="73489-197">This enables your application to use the Unicode information contained in the last five members of the structure.</span></span>

<span data-ttu-id="73489-198">Le membre **lpVerb** ou **lpVerbW** de la structure est utilisé pour identifier la commande à exécuter.</span><span class="sxs-lookup"><span data-stu-id="73489-198">The structure's **lpVerb** or **lpVerbW** member is used to identify the command to be executed.</span></span> <span data-ttu-id="73489-199">Les commandes sont identifiées de l’une des deux manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="73489-199">Commands are identified in one of the following two ways:</span></span>

-   <span data-ttu-id="73489-200">Par la chaîne du verbe de la commande</span><span class="sxs-lookup"><span data-stu-id="73489-200">By the command's verb string</span></span>
-   <span data-ttu-id="73489-201">Par le décalage de l’identificateur de la commande</span><span class="sxs-lookup"><span data-stu-id="73489-201">By the command's identifier offset</span></span>

<span data-ttu-id="73489-202">Pour faire la distinction entre ces deux cas, vérifiez le mot de poids fort de **lpVerb** pour le cas ANSI ou **lpVerbW** pour la casse Unicode.</span><span class="sxs-lookup"><span data-stu-id="73489-202">To distinguish between these two cases, check the high-order word of **lpVerb** for the ANSI case or **lpVerbW** for the Unicode case.</span></span> <span data-ttu-id="73489-203">Si le mot de poids fort est différent de zéro, **lpVerb** ou **lpVerbW** contient une chaîne de verbe.</span><span class="sxs-lookup"><span data-stu-id="73489-203">If the high-order word is nonzero, **lpVerb** or **lpVerbW** holds a verb string.</span></span> <span data-ttu-id="73489-204">Si le mot de poids fort est égal à zéro, le décalage de la commande se trouve dans le mot de poids faible de **lpVerb**.</span><span class="sxs-lookup"><span data-stu-id="73489-204">If the high-order word is zero, the command offset is in the low-order word of **lpVerb**.</span></span>

<span data-ttu-id="73489-205">L’exemple suivant illustre une implémentation simple de [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) qui correspond aux exemples [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) et [**IContextMenu :: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) fournis avant et après cette section.</span><span class="sxs-lookup"><span data-stu-id="73489-205">The following example shows a simple implementation of [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) that corresponds to the [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) and [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) examples given before and after this section.</span></span> <span data-ttu-id="73489-206">La méthode détermine d’abord la structure qui est passée.</span><span class="sxs-lookup"><span data-stu-id="73489-206">The method first determines which structure is being passed in.</span></span> <span data-ttu-id="73489-207">Elle détermine ensuite si la commande est identifiée par son décalage ou son verbe.</span><span class="sxs-lookup"><span data-stu-id="73489-207">It then determines whether the command is identified by its offset or its verb.</span></span> <span data-ttu-id="73489-208">Si **lpVerb** ou **lpVerbW** contient un verbe ou un offset valide, la méthode affiche une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="73489-208">If **lpVerb** or **lpVerbW** holds a valid verb or offset, the method displays a message box.</span></span>


```C++
STDMETHODIMP CShellExtension::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    BOOL fEx = FALSE;
    BOOL fUnicode = FALSE;

    if(lpcmi->cbSize == sizeof(CMINVOKECOMMANDINFOEX))
    {
        fEx = TRUE;
        if((lpcmi->fMask & CMIC_MASK_UNICODE))
        {
            fUnicode = TRUE;
        }
    }

    if( !fUnicode && HIWORD(lpcmi->lpVerb))
    {
        if(StrCmpIA(lpcmi->lpVerb, m_pszVerb))
        {
            return E_FAIL;
        }
    }

    else if( fUnicode && HIWORD(((CMINVOKECOMMANDINFOEX *) lpcmi)->lpVerbW))
    {
        if(StrCmpIW(((CMINVOKECOMMANDINFOEX *)lpcmi)->lpVerbW, m_pwszVerb))
        {
            return E_FAIL;
        }
    }

    else if(LOWORD(lpcmi->lpVerb) != IDM_DISPLAY)
    {
        return E_FAIL;
    }

    else
    {
        MessageBox(lpcmi->hwnd,
                   "The File Name",
                   "File Name",
                   MB_OK|MB_ICONINFORMATION);
    }

    return S_OK;
}
```



### <a name="icontextmenuquerycontextmenu-method"></a><span data-ttu-id="73489-209">IContextMenu :: QueryContextMenu, méthode</span><span class="sxs-lookup"><span data-stu-id="73489-209">IContextMenu::QueryContextMenu Method</span></span>

<span data-ttu-id="73489-210">L’interpréteur de commandes appelle [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) pour permettre au gestionnaire de menu contextuel d’ajouter ses éléments de menu au menu.</span><span class="sxs-lookup"><span data-stu-id="73489-210">The Shell calls [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) to enable the shortcut menu handler to add its menu items to the menu.</span></span> <span data-ttu-id="73489-211">Il passe le handle **HMENU** dans le paramètre *HMENU* .</span><span class="sxs-lookup"><span data-stu-id="73489-211">It passes in the **HMENU** handle in the *hmenu* parameter.</span></span> <span data-ttu-id="73489-212">Le paramètre *indexMenu* est défini sur l’index à utiliser pour le premier élément de menu à ajouter.</span><span class="sxs-lookup"><span data-stu-id="73489-212">The *indexMenu* parameter is set to the index to be used for the first menu item that is to be added.</span></span>

<span data-ttu-id="73489-213">Tous les éléments de menu ajoutés par le gestionnaire doivent avoir des identificateurs qui se trouvent entre les valeurs des paramètres *idCmdFirst* et *idCmdLast* .</span><span class="sxs-lookup"><span data-stu-id="73489-213">Any menu items that are added by the handler must have identifiers that fall between the values in the *idCmdFirst* and *idCmdLast* parameters.</span></span> <span data-ttu-id="73489-214">En règle générale, le premier identificateur de commande est défini sur *idCmdFirst*, qui est incrémenté d’une unité (1) pour chaque commande supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="73489-214">Typically, the first command identifier is set to *idCmdFirst*, which is incremented by one (1) for each additional command.</span></span> <span data-ttu-id="73489-215">Cette pratique vous permet d’éviter de dépasser les *idCmdLast* et d’optimiser le nombre d’identificateurs disponibles au cas où l’interpréteur de commandes appellera plus d’un gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="73489-215">This practice helps you avoid exceeding *idCmdLast* and maximizes the number of available identifiers in case the Shell calls more than one handler.</span></span>

<span data-ttu-id="73489-216">Le *décalage de commande* d’un identificateur d’élément correspond à la différence entre l’identificateur et la valeur dans *idCmdFirst*.</span><span class="sxs-lookup"><span data-stu-id="73489-216">An item identifier's *command offset* is the difference between the identifier and the value in *idCmdFirst*.</span></span> <span data-ttu-id="73489-217">Stockez le décalage de chaque élément que votre gestionnaire ajoute au menu contextuel, car l’interpréteur de commandes peut l’utiliser pour identifier l’élément s’il appelle ensuite [**IContextMenu :: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) ou [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span><span class="sxs-lookup"><span data-stu-id="73489-217">Store the offset of each item that your handler adds to the shortcut menu because the Shell might use it to identify the item if it subsequently calls [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) or [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span>

<span data-ttu-id="73489-218">Vous devez également affecter un [verbe](launch.md) à chaque commande que vous ajoutez.</span><span class="sxs-lookup"><span data-stu-id="73489-218">You should also assign a [verb](launch.md) to each command you add.</span></span> <span data-ttu-id="73489-219">Un verbe est une chaîne qui peut être utilisée à la place de l’offset pour identifier la commande lorsque [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) est appelé.</span><span class="sxs-lookup"><span data-stu-id="73489-219">A verb is a string that can be used instead of the offset to identify the command when [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) is called.</span></span> <span data-ttu-id="73489-220">Il est également utilisé par des fonctions telles que [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) pour exécuter des commandes de menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="73489-220">It is also used by functions such as [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to execute shortcut menu commands.</span></span>

<span data-ttu-id="73489-221">Il existe trois indicateurs qui peuvent être transmis via le paramètre *uFlags* qui sont pertinents pour les gestionnaires de menus contextuels.</span><span class="sxs-lookup"><span data-stu-id="73489-221">There are three flags that can be passed in through the *uFlags* parameter that are relevant to shortcut menu handlers.</span></span> <span data-ttu-id="73489-222">Ils sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="73489-222">They are described in the following table.</span></span>



| <span data-ttu-id="73489-223">Indicateur</span><span class="sxs-lookup"><span data-stu-id="73489-223">Flag</span></span>             | <span data-ttu-id="73489-224">Description</span><span class="sxs-lookup"><span data-stu-id="73489-224">Description</span></span>                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73489-225">CMF \_ DEFAULTONLY</span><span class="sxs-lookup"><span data-stu-id="73489-225">CMF\_DEFAULTONLY</span></span> | <span data-ttu-id="73489-226">L’utilisateur a sélectionné la commande par défaut, généralement en double-cliquant sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="73489-226">The user has selected the default command, usually by double-clicking the object.</span></span> <span data-ttu-id="73489-227">[**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) doit retourner le contrôle à l’interpréteur de commandes sans modifier le menu.</span><span class="sxs-lookup"><span data-stu-id="73489-227">[**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) should return control to the Shell without modifying the menu.</span></span> |
| <span data-ttu-id="73489-228">CMF \_ NOdéfaut</span><span class="sxs-lookup"><span data-stu-id="73489-228">CMF\_NODEFAULT</span></span>   | <span data-ttu-id="73489-229">Aucun élément dans le menu ne doit être l’élément par défaut.</span><span class="sxs-lookup"><span data-stu-id="73489-229">No item in the menu should be the default item.</span></span> <span data-ttu-id="73489-230">La méthode doit ajouter ses commandes au menu.</span><span class="sxs-lookup"><span data-stu-id="73489-230">The method should add its commands to the menu.</span></span>                                                                                                                          |
| <span data-ttu-id="73489-231">CMF \_ normal</span><span class="sxs-lookup"><span data-stu-id="73489-231">CMF\_NORMAL</span></span>      | <span data-ttu-id="73489-232">Le menu contextuel s’affiche normalement.</span><span class="sxs-lookup"><span data-stu-id="73489-232">The shortcut menu will be displayed normally.</span></span> <span data-ttu-id="73489-233">La méthode doit ajouter ses commandes au menu.</span><span class="sxs-lookup"><span data-stu-id="73489-233">The method should add its commands to the menu.</span></span>                                                                                                                            |



 

<span data-ttu-id="73489-234">Utilisez [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) ou [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) pour ajouter des éléments de menu à la liste.</span><span class="sxs-lookup"><span data-stu-id="73489-234">Use either [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) or [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) to add menu items to the list.</span></span> <span data-ttu-id="73489-235">Ensuite, retournez une valeur **HRESULT** avec la gravité définie sur **gravité \_ réussite**.</span><span class="sxs-lookup"><span data-stu-id="73489-235">Then return an **HRESULT** value with the severity set to **SEVERITY\_SUCCESS**.</span></span> <span data-ttu-id="73489-236">Définissez la valeur de code sur le décalage de l’identificateur de commande le plus grand qui a été assigné, plus un (1).</span><span class="sxs-lookup"><span data-stu-id="73489-236">Set the code value to the offset of the largest command identifier that was assigned, plus one (1).</span></span> <span data-ttu-id="73489-237">Par exemple, supposons que *idCmdFirst* a la valeur 5 et que vous ajoutez trois éléments au menu avec des identificateurs de commande 5, 7 et 8.</span><span class="sxs-lookup"><span data-stu-id="73489-237">For example, assume that *idCmdFirst* is set to 5 and you add three items to the menu with command identifiers of 5, 7, and 8.</span></span> <span data-ttu-id="73489-238">La valeur de retour doit être `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)` .</span><span class="sxs-lookup"><span data-stu-id="73489-238">The return value should be `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)`.</span></span>

<span data-ttu-id="73489-239">L’exemple suivant illustre une implémentation simple de [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) qui insère une seule commande.</span><span class="sxs-lookup"><span data-stu-id="73489-239">The following example shows a simple implementation of [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) that inserts a single command.</span></span> <span data-ttu-id="73489-240">Le décalage de l’identificateur de la commande est l' \_ affichage IDM, qui est défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="73489-240">The identifier offset for the command is IDM\_DISPLAY, which is set to zero.</span></span> <span data-ttu-id="73489-241">Les variables **m \_ pszVerb** et **m \_ pwszVerb** sont des variables privées utilisées pour stocker la chaîne de verbe indépendante du langage associée à la fois dans les formats ANSI et Unicode.</span><span class="sxs-lookup"><span data-stu-id="73489-241">The **m\_pszVerb** and **m\_pwszVerb** variables are private variables used to store the associated language-independent verb string in both ANSI and Unicode formats.</span></span>


```C++
#define IDM_DISPLAY 0

STDMETHODIMP CMenuExtension::QueryContextMenu(HMENU hMenu,
                                              UINT indexMenu,
                                              UINT idCmdFirst,
                                              UINT idCmdLast,
                                              UINT uFlags)
{
    HRESULT hr;
    
    if(!(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu(hMenu, 
                   indexMenu, 
                   MF_STRING | MF_BYPOSITION, 
                   idCmdFirst + IDM_DISPLAY, 
                   "&Display File Name");

    
        
        hr = StringCbCopyA(m_pszVerb, sizeof(m_pszVerb), "display");
        hr = StringCbCopyW(m_pwszVerb, sizeof(m_pwszVerb), L"display");

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_DISPLAY + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));
}
```



<span data-ttu-id="73489-242">Pour d’autres tâches d’implémentation de verbe, consultez [création de gestionnaires de menus contextuels](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="73489-242">For other verb implementation tasks, see [Creating Context Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="73489-243">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="73489-243">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73489-244">Menus contextuels (menu contextuel) et gestionnaires de menus contextuels</span><span class="sxs-lookup"><span data-stu-id="73489-244">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="73489-245">Verbes et associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="73489-245">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="73489-246">Choix d’un verbe statique ou dynamique pour votre menu contextuel</span><span class="sxs-lookup"><span data-stu-id="73489-246">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="73489-247">Meilleures pratiques pour les gestionnaires de menus contextuels et les verbes de sélection multiple</span><span class="sxs-lookup"><span data-stu-id="73489-247">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="73489-248">Création de gestionnaires de menu contextuel</span><span class="sxs-lookup"><span data-stu-id="73489-248">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
</dt> <dt>

[<span data-ttu-id="73489-249">Référence du menu contextuel</span><span class="sxs-lookup"><span data-stu-id="73489-249">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 
