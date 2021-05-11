---
description: Les gestionnaires de menus contextuels, également appelés gestionnaires de menus contextuels ou gestionnaires de verbes, sont un type de gestionnaire de type de fichier. Comme tous les gestionnaires de ce type, il s’agit d’objets COM (Component Object Model) en cours d’implémentation en tant que dll.
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: Création de gestionnaires de menu contextuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8e102833453566f42d058ff82061f34ebc65691
ms.sourcegitcommit: 9655f82be96b11258276fdefff14423c30552fbb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/11/2021
ms.locfileid: "109740570"
---
# <a name="creating-shortcut-menu-handlers"></a><span data-ttu-id="1e943-104">Création de gestionnaires de menu contextuel</span><span class="sxs-lookup"><span data-stu-id="1e943-104">Creating Shortcut Menu Handlers</span></span>

<span data-ttu-id="1e943-105">Les gestionnaires de menus contextuels, également appelés gestionnaires de menus contextuels ou gestionnaires de verbes, sont un type de gestionnaire de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="1e943-105">Shortcut menu handlers, also known as context menu handlers or verb handlers, are a type of file type handler.</span></span> <span data-ttu-id="1e943-106">Ces gestionnaires peuvent être impelmented de manière à ce qu’ils se chargent dans leur propre processus ou dans l’Explorateur, ou dans d’autres processus tiers.</span><span class="sxs-lookup"><span data-stu-id="1e943-106">These handlers may be impelmented in a way that causes them to load in their own process or in the explorer, or other 3rd party processes.</span></span> <span data-ttu-id="1e943-107">Soyez vigilant lors de la création de gestionnaires in-process, car ils peuvent nuire au processus qui les charge.</span><span class="sxs-lookup"><span data-stu-id="1e943-107">Take care when creating in-process handlers as they can cause harm to the process that loads them.</span></span>

> [!Note]  
> <span data-ttu-id="1e943-108">Il existe des considérations spéciales pour les versions 64 bits de Windows lors de l’enregistrement de gestionnaires qui fonctionnent dans le contexte d’applications 32 bits : lorsqu’ils sont appelés dans le contexte d’une application de bits différents, le sous-système WOW64 redirige l’accès au système de fichiers vers certains chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="1e943-108">There are special considerations for 64-bit based versions of Windows when registering handlers that work in the context of 32-bit applications: when invoked in the context of an application of different bitness, the WOW64 subsystem redirects file system access to some paths.</span></span> <span data-ttu-id="1e943-109">Si votre gestionnaire. exe est stocké dans l’un de ces chemins d’accès, il n’est pas accessible dans ce contexte.</span><span class="sxs-lookup"><span data-stu-id="1e943-109">If your .exe handler is stored in one of those paths, it is not accessible in this context.</span></span> <span data-ttu-id="1e943-110">Par conséquent, pour une solution de contournement, stockez votre fichier. exe dans un chemin d’accès qui n’est pas redirigé, ou stockez une version stub de votre fichier. exe qui lance la version réelle.</span><span class="sxs-lookup"><span data-stu-id="1e943-110">Therefore, as a work around, either store your .exe in a path that does not get redirected, or store a stub version of your .exe that launches the real version.</span></span>

<span data-ttu-id="1e943-111">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="1e943-111">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="1e943-112">Verbes canoniques</span><span class="sxs-lookup"><span data-stu-id="1e943-112">Canonical Verbs</span></span>](#canonical-verbs)
-   [<span data-ttu-id="1e943-113">Verbes étendus</span><span class="sxs-lookup"><span data-stu-id="1e943-113">Extended Verbs</span></span>](#extended-verbs)
-   [<span data-ttu-id="1e943-114">Verbes d’accès par programme uniquement</span><span class="sxs-lookup"><span data-stu-id="1e943-114">Programmatic Access Only Verbs</span></span>](#programmaticaccessonly-verbs)
-   [<span data-ttu-id="1e943-115">Personnalisation d’un menu contextuel à l’aide de verbes statiques</span><span class="sxs-lookup"><span data-stu-id="1e943-115">Customizing a Shortcut Menu Using Static Verbs</span></span>](#customizing-a-shortcut-menu-using-static-verbs)
    -   [<span data-ttu-id="1e943-116">Activation de votre gestionnaire à l’aide de l’interface IDropTarget</span><span class="sxs-lookup"><span data-stu-id="1e943-116">Activating Your Handler Using the IDropTarget Interface</span></span>](#activating-your-handler-using-the-idroptarget-interface)
    -   [<span data-ttu-id="1e943-117">Spécification de la position et de l’ordre des verbes statiques</span><span class="sxs-lookup"><span data-stu-id="1e943-117">Specifying the Position and Order of Static Verbs</span></span>](#specifying-the-position-and-order-of-static-verbs)
    -   [<span data-ttu-id="1e943-118">Positionnement des verbes en haut ou en bas du menu</span><span class="sxs-lookup"><span data-stu-id="1e943-118">Positioning Verbs at the Top or Bottom of the Menu</span></span>](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [<span data-ttu-id="1e943-119">Création de menus en cascade statiques</span><span class="sxs-lookup"><span data-stu-id="1e943-119">Creating Static Cascading Menus</span></span>](#creating-static-cascading-menus)
    -   [<span data-ttu-id="1e943-120">Obtention du comportement dynamique pour les verbes statiques à l’aide de la syntaxe de requête avancée</span><span class="sxs-lookup"><span data-stu-id="1e943-120">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [<span data-ttu-id="1e943-121">Déconseillé : Association de verbes à des commandes échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="1e943-121">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [<span data-ttu-id="1e943-122">Exécution des tâches d’implémentation de verbe</span><span class="sxs-lookup"><span data-stu-id="1e943-122">Completing Verb Implementation Tasks</span></span>](#completing-verb-implementation-tasks)
    -   [<span data-ttu-id="1e943-123">Personnalisation du menu contextuel pour les objets Shell prédéfinis</span><span class="sxs-lookup"><span data-stu-id="1e943-123">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [<span data-ttu-id="1e943-124">Extension d’un nouveau sous-menu</span><span class="sxs-lookup"><span data-stu-id="1e943-124">Extending a New Submenu</span></span>](#extending-a-new-submenu)
    -   [<span data-ttu-id="1e943-125">Suppression de verbes et contrôle de la visibilité</span><span class="sxs-lookup"><span data-stu-id="1e943-125">Suppressing Verbs and Controlling Visibility</span></span>](#suppressing-verbs-and-controlling-visibility)
    -   [<span data-ttu-id="1e943-126">Utilisation du modèle de sélection de verbe</span><span class="sxs-lookup"><span data-stu-id="1e943-126">Employing the Verb Selection Model</span></span>](#employing-the-verb-selection-model)
    -   [<span data-ttu-id="1e943-127">Utilisation des attributs d’élément</span><span class="sxs-lookup"><span data-stu-id="1e943-127">Using Item Attributes</span></span>](#using-item-attributes)
    -   [<span data-ttu-id="1e943-128">Implémentation de verbes personnalisés pour les dossiers via Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="1e943-128">Implementing Custom Verbs for Folders through Desktop.ini</span></span>](#implementing-custom-verbs-for-folders-through-desktopini)
-   [<span data-ttu-id="1e943-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1e943-129">Related topics</span></span>](#related-topics)

## <a name="canonical-verbs"></a><span data-ttu-id="1e943-130">Verbes canoniques</span><span class="sxs-lookup"><span data-stu-id="1e943-130">Canonical Verbs</span></span>

<span data-ttu-id="1e943-131">Les applications sont généralement chargées de fournir des chaînes d’affichage localisées pour les verbes qu’elles définissent.</span><span class="sxs-lookup"><span data-stu-id="1e943-131">Applications are generally responsible for providing localized display strings for the verbs they define.</span></span> <span data-ttu-id="1e943-132">Toutefois, pour fournir un degré d’indépendance du langage, le système définit un ensemble standard de verbes couramment utilisés appelés verbes canoniques.</span><span class="sxs-lookup"><span data-stu-id="1e943-132">However, to provide a degree of language independence, the system defines a standard set of commonly used verbs called canonical verbs.</span></span> <span data-ttu-id="1e943-133">Un verbe canonique n’est jamais affiché à l’utilisateur et peut être utilisé avec n’importe quelle langue d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1e943-133">A canonical verb is never displayed to the user, and can be used with any UI language.</span></span> <span data-ttu-id="1e943-134">Le système utilise le nom canonique pour générer automatiquement une chaîne d’affichage correctement localisée.</span><span class="sxs-lookup"><span data-stu-id="1e943-134">The system uses the canonical name to automatically generate a properly localized display string.</span></span> <span data-ttu-id="1e943-135">Par exemple, la chaîne d’affichage du verbe Open est définie sur **Open** sur un système en anglais et sur l’équivalent allemand sur un système allemand.</span><span class="sxs-lookup"><span data-stu-id="1e943-135">For instance, the open verb's display string is set to **Open** on an English system, and to the German equivalent on a German system.</span></span>


| <span data-ttu-id="1e943-136">Verbe canonique</span><span class="sxs-lookup"><span data-stu-id="1e943-136">Canonical verb</span></span> | <span data-ttu-id="1e943-137">Description</span><span class="sxs-lookup"><span data-stu-id="1e943-137">Description</span></span>                                                          |
|----------------|----------------------------------------------------------------------|
| <span data-ttu-id="1e943-138">Ouvrir</span><span class="sxs-lookup"><span data-stu-id="1e943-138">Open</span></span>           | <span data-ttu-id="1e943-139">Ouvre le fichier ou le dossier.</span><span class="sxs-lookup"><span data-stu-id="1e943-139">Opens the file or folder.</span></span>                                            |
| <span data-ttu-id="1e943-140">Opennew</span><span class="sxs-lookup"><span data-stu-id="1e943-140">Opennew</span></span>        | <span data-ttu-id="1e943-141">Ouvre le fichier ou le dossier dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1e943-141">Opens the file or folder in a new window.</span></span>                            |
| <span data-ttu-id="1e943-142">Impression</span><span class="sxs-lookup"><span data-stu-id="1e943-142">Print</span></span>          | <span data-ttu-id="1e943-143">Imprime le fichier.</span><span class="sxs-lookup"><span data-stu-id="1e943-143">Prints the file.</span></span>                                                     |
| <span data-ttu-id="1e943-144">Printto</span><span class="sxs-lookup"><span data-stu-id="1e943-144">Printto</span></span>        | <span data-ttu-id="1e943-145">Permet à l’utilisateur d’imprimer un fichier en le faisant glisser vers un objet Printer.</span><span class="sxs-lookup"><span data-stu-id="1e943-145">Permits the user to print a file by dragging it to a printer object.</span></span> |
| <span data-ttu-id="1e943-146">Explorer</span><span class="sxs-lookup"><span data-stu-id="1e943-146">Explore</span></span>        | <span data-ttu-id="1e943-147">Ouvre l’Explorateur Windows avec le dossier sélectionné.</span><span class="sxs-lookup"><span data-stu-id="1e943-147">Opens Windows Explorer with the folder selected.</span></span>                     |
| <span data-ttu-id="1e943-148">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1e943-148">Properties</span></span>     | <span data-ttu-id="1e943-149">Ouvre la feuille de propriétés de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1e943-149">Opens the object's property sheet.</span></span>                                   |

> [!Note]  
> <span data-ttu-id="1e943-150">Le verbe **Printto** est également canonique, mais il n’est jamais affiché.</span><span class="sxs-lookup"><span data-stu-id="1e943-150">The **Printto** verb is also canonical, but it is never displayed.</span></span> <span data-ttu-id="1e943-151">Son inclusion permet à l’utilisateur d’imprimer un fichier en le faisant glisser vers un objet Printer.</span><span class="sxs-lookup"><span data-stu-id="1e943-151">Its inclusion enables the user to print a file by dragging it to a printer object.</span></span>

<span data-ttu-id="1e943-152">Les gestionnaires de menu contextuel peuvent fournir leurs propres verbes canoniques via [**IContextMenu :: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) avec **GC \_ VERBW** ou **GC \_ Verba**.</span><span class="sxs-lookup"><span data-stu-id="1e943-152">Shortcut menu handlers can provide their own canonical verbs through [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) with **GCS\_VERBW**, or **GCS\_VERBA**.</span></span> <span data-ttu-id="1e943-153">Le système utilise les verbes canoniques comme second paramètre (*lpOperation*) passé à [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), et est [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo). membre **lpVerb** passé à la méthode [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) .</span><span class="sxs-lookup"><span data-stu-id="1e943-153">The system will use the canonical verbs as the second parameter (*lpOperation*) passed to [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), and is the [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo).**lpVerb** member passed to the [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) method.</span></span>

## <a name="extended-verbs"></a><span data-ttu-id="1e943-154">Verbes étendus</span><span class="sxs-lookup"><span data-stu-id="1e943-154">Extended Verbs</span></span>

<span data-ttu-id="1e943-155">Quand l’utilisateur clique avec le bouton droit sur un objet, le menu contextuel affiche les verbes par défaut.</span><span class="sxs-lookup"><span data-stu-id="1e943-155">When the user right-clicks an object, the shortcut menu displays the default verbs.</span></span> <span data-ttu-id="1e943-156">Vous souhaiterez peut-être ajouter et prendre en charge des commandes dans certains menus contextuels qui ne s’affichent pas dans chaque menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="1e943-156">You might want to add and support commands on some shortcut menus that are not displayed on every shortcut menu.</span></span> <span data-ttu-id="1e943-157">Par exemple, vous pouvez avoir des commandes qui ne sont pas couramment utilisées ou qui sont destinées à des utilisateurs expérimentés.</span><span class="sxs-lookup"><span data-stu-id="1e943-157">For example, you could have commands that are not commonly used or that are intended for experienced users.</span></span> <span data-ttu-id="1e943-158">Pour cette raison, vous pouvez également définir un ou plusieurs verbes étendus.</span><span class="sxs-lookup"><span data-stu-id="1e943-158">For this reason, you can also define one or more extended verbs.</span></span> <span data-ttu-id="1e943-159">Ces verbes sont semblables aux verbes normaux, mais se distinguent des verbes normaux par leur mode d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1e943-159">These verbs are similar to normal verbs, but are distinguished from normal verbs by the way they are registered.</span></span> <span data-ttu-id="1e943-160">Pour avoir accès à des verbes étendus, l’utilisateur doit cliquer avec le bouton droit sur un objet tout en appuyant sur la touche Maj.</span><span class="sxs-lookup"><span data-stu-id="1e943-160">To have access to extended verbs, the user must right-click an object while pressing the SHIFT key.</span></span> <span data-ttu-id="1e943-161">Lorsque l’utilisateur effectue cette action, les verbes étendus sont affichés en plus des verbes par défaut.</span><span class="sxs-lookup"><span data-stu-id="1e943-161">When the user does so, the extended verbs are displayed in addition to the default verbs.</span></span>

<span data-ttu-id="1e943-162">Vous pouvez utiliser le registre pour définir un ou plusieurs verbes étendus.</span><span class="sxs-lookup"><span data-stu-id="1e943-162">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="1e943-163">Les commandes associées s’affichent uniquement quand l’utilisateur clique avec le bouton droit sur un objet tout en appuyant sur la touche Maj.</span><span class="sxs-lookup"><span data-stu-id="1e943-163">The associated commands will be displayed only when the user right-clicks an object while also pressing the SHIFT key.</span></span> <span data-ttu-id="1e943-164">Pour définir un verbe comme étendu, ajoutez une valeur **\_ SZ** « étendue » à la sous-clé du verbe.</span><span class="sxs-lookup"><span data-stu-id="1e943-164">To define a verb as extended, add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="1e943-165">Aucune donnée ne doit être associée à la valeur.</span><span class="sxs-lookup"><span data-stu-id="1e943-165">The value should not have any data associated with it.</span></span>

## <a name="programmatic-access-only"></a><span data-ttu-id="1e943-166">Accès par programme uniquement</span><span class="sxs-lookup"><span data-stu-id="1e943-166">Programmatic Access Only</span></span>

<span data-ttu-id="1e943-167">Ces verbes ne sont jamais affichés dans un menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="1e943-167">These verbs are never displayed in a context menu.</span></span> <span data-ttu-id="1e943-168">Ils sont accessibles à l’aide de [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) et en spécifiant le champ **LpVerb** du paramètre *pExecInfo* (un objet [SHELLEXECUTEINFO](/windows/win32/api/shellapi/ns-shellapi-shellexecuteinfoa) ).</span><span class="sxs-lookup"><span data-stu-id="1e943-168">These can be accessed by using [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) and specifying the **lpVerb** field of the *pExecInfo* parameter (a [SHELLEXECUTEINFO](/windows/win32/api/shellapi/ns-shellapi-shellexecuteinfoa) object).</span></span> <span data-ttu-id="1e943-169">Pour définir un verbe comme accès par programme uniquement, ajoutez une valeur de **reg \_ SZ** « ProgrammaticAccessOnly » à la sous-clé du verbe.</span><span class="sxs-lookup"><span data-stu-id="1e943-169">To define a verb as programmatic access only, add a "ProgrammaticAccessOnly" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="1e943-170">Aucune donnée ne doit être associée à la valeur.</span><span class="sxs-lookup"><span data-stu-id="1e943-170">The value should not have any data associated with it.</span></span>

<span data-ttu-id="1e943-171">Vous pouvez utiliser le registre pour définir un ou plusieurs verbes étendus.</span><span class="sxs-lookup"><span data-stu-id="1e943-171">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="1e943-172">Les commandes associées s’affichent uniquement quand l’utilisateur clique avec le bouton droit sur un objet tout en appuyant sur la touche Maj.</span><span class="sxs-lookup"><span data-stu-id="1e943-172">The associated commands will be displayed only when the user right-clicks an object while also pressing the SHIFT key.</span></span> <span data-ttu-id="1e943-173">Pour définir un verbe comme étendu, ajoutez une valeur **\_ SZ** « étendue » à la sous-clé du verbe.</span><span class="sxs-lookup"><span data-stu-id="1e943-173">To define a verb as extended, add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="1e943-174">Aucune donnée ne doit être associée à la valeur.</span><span class="sxs-lookup"><span data-stu-id="1e943-174">The value should not have any data associated with it.</span></span>

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a><span data-ttu-id="1e943-175">Personnalisation d’un menu contextuel à l’aide de verbes statiques</span><span class="sxs-lookup"><span data-stu-id="1e943-175">Customizing a Shortcut Menu Using Static Verbs</span></span>

<span data-ttu-id="1e943-176">Après avoir [choisi un verbe statique ou dynamique pour votre menu contextuel](shortcut-choose-method.md) , vous pouvez étendre le menu contextuel d’un type de fichier en inscrivant un verbe statique pour le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="1e943-176">After [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md) you can extend the shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="1e943-177">Pour ce faire, ajoutez une sous-clé **Shell** sous la sous-clé pour le ProgID de l’application associée au type de fichier.</span><span class="sxs-lookup"><span data-stu-id="1e943-177">To do so, add a **Shell** subkey below the subkey for the ProgID of the application associated with the file type.</span></span> <span data-ttu-id="1e943-178">Si vous le souhaitez, vous pouvez définir un verbe par défaut pour le type de fichier en en faisant la valeur par défaut de la sous-clé **Shell** .</span><span class="sxs-lookup"><span data-stu-id="1e943-178">Optionally, you can define a default verb for the file type by making it the default value of the **Shell** subkey.</span></span>

<span data-ttu-id="1e943-179">Le verbe par défaut s’affiche en premier dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="1e943-179">The default verb is displayed first on the shortcut menu.</span></span> <span data-ttu-id="1e943-180">Son objectif est de fournir à l’interpréteur de commandes un verbe qu’il peut utiliser lorsque la fonction [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) est appelée, mais qu’aucun verbe n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="1e943-180">Its purpose is to provide the Shell with a verb it can use when the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) function is called, but no verb is specified.</span></span> <span data-ttu-id="1e943-181">L’interpréteur de commandes ne sélectionne pas nécessairement le verbe par défaut lorsque **ShellExecuteEx** est utilisé de cette manière.</span><span class="sxs-lookup"><span data-stu-id="1e943-181">The Shell does not necessarily select the default verb when **ShellExecuteEx** is used in this fashion.</span></span>

<span data-ttu-id="1e943-182">L’interpréteur de commandes utilise le premier verbe disponible dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="1e943-182">The Shell uses the first available verb in the following order:</span></span>

1.  <span data-ttu-id="1e943-183">Le verbe par défaut</span><span class="sxs-lookup"><span data-stu-id="1e943-183">The default verb</span></span>
2.  <span data-ttu-id="1e943-184">Premier verbe du Registre, si l’ordre du verbe est spécifié</span><span class="sxs-lookup"><span data-stu-id="1e943-184">The first verb in the registry, if the verb order is specified</span></span>
3.  <span data-ttu-id="1e943-185">Verbe **Open**</span><span class="sxs-lookup"><span data-stu-id="1e943-185">The **Open** verb</span></span>
4.  <span data-ttu-id="1e943-186">Le verbe **Open with**</span><span class="sxs-lookup"><span data-stu-id="1e943-186">The **Open With** verb</span></span>

<span data-ttu-id="1e943-187">Si aucun des verbes listés n’est disponible, l’opération échoue.</span><span class="sxs-lookup"><span data-stu-id="1e943-187">If none of the verbs listed is available, the operation fails.</span></span>

<span data-ttu-id="1e943-188">Créez une sous-clé pour chaque verbe que vous souhaitez ajouter sous la sous-clé Shell.</span><span class="sxs-lookup"><span data-stu-id="1e943-188">Create one subkey for each verb you want to add under the Shell subkey.</span></span> <span data-ttu-id="1e943-189">Chacune de ces sous-clés doit avoir une valeur **reg \_ SZ** définie sur la chaîne d’affichage du verbe (chaîne localisée).</span><span class="sxs-lookup"><span data-stu-id="1e943-189">Each of these subkeys must have a **REG\_SZ** value set to the verb's display string (localized string).</span></span> <span data-ttu-id="1e943-190">Pour chaque sous-clé de verbe, créez une sous-clé de commande avec la valeur par défaut définie sur la ligne de commande pour activer les éléments.</span><span class="sxs-lookup"><span data-stu-id="1e943-190">For each verb subkey, create a command subkey with the default value set to the command line for activating the items.</span></span> <span data-ttu-id="1e943-191">Pour les verbes canoniques, tels que **ouvrir** et **Imprimer**, vous pouvez omettre la chaîne d’affichage, car le système affiche automatiquement une chaîne correctement localisée.</span><span class="sxs-lookup"><span data-stu-id="1e943-191">For canonical verbs, such as **Open** and **Print**, you can omit the display string because the system automatically displays a properly localized string.</span></span> <span data-ttu-id="1e943-192">Pour les verbes non canoniques, si vous omettez la chaîne d’affichage, la chaîne de verbes est affichée.</span><span class="sxs-lookup"><span data-stu-id="1e943-192">For noncanonical verbs, if you omit the display string, the verb string is displayed.</span></span>

<span data-ttu-id="1e943-193">Dans l’exemple de Registre suivant, notez les points suivants :</span><span class="sxs-lookup"><span data-stu-id="1e943-193">In the following registry example, note that:</span></span>

-   <span data-ttu-id="1e943-194">Étant donné que **doit** n’est pas un verbe canonique, il est assigné à un nom complet, qui peut être sélectionné en appuyant sur la touche D.</span><span class="sxs-lookup"><span data-stu-id="1e943-194">Because **Doit** is not a canonical verb, it is assigned a display name, which can be selected by pressing the D key.</span></span>
-   <span data-ttu-id="1e943-195">Le verbe **Printto** n’apparaît pas dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="1e943-195">The **Printto** verb does not appear on the shortcut menu.</span></span> <span data-ttu-id="1e943-196">Toutefois, son inclusion dans le registre permet à l’utilisateur d’imprimer des fichiers en les supprimant sur une icône d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="1e943-196">However, its inclusion in the registry enables the user to print files by dropping them on a printer icon.</span></span>
-   <span data-ttu-id="1e943-197">Une sous-clé est affichée pour chaque verbe.</span><span class="sxs-lookup"><span data-stu-id="1e943-197">One subkey is shown for each verb.</span></span> <span data-ttu-id="1e943-198">**%1** représente le nom de fichier et **%2** le nom de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="1e943-198">**%1** represents the file name and **%2** the printer name.</span></span>

```
HKEY_CLASSES_ROOT
   .myp-ms
      (Default) = MyProgram.1
      MyProgram.1
         (Default) = My Program Application
         Shell
            (Default) = doit
            doit
               (Default) = &Do It
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            open
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            print
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1"
            printto
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1" "%2"
```

<span data-ttu-id="1e943-199">Le diagramme suivant illustre l’extension du menu contextuel conformément aux entrées de Registre ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="1e943-199">The following diagram illustrates the extension of the shortcut menu in accordance with the registry entries above.</span></span> <span data-ttu-id="1e943-200">Ce menu contextuel contient des verbes **ouvrir**, **exécuter** et **Imprimer** dans son menu **, avec le** verbe par défaut.</span><span class="sxs-lookup"><span data-stu-id="1e943-200">This shortcut menu has **Open**, **Do It**, and **Print** verbs on its menu, with **Do It** as the default verb.</span></span>

![capture d’écran du menu contextuel verbe par défaut do it](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a><span data-ttu-id="1e943-202">Activation de votre gestionnaire à l’aide de l’interface IDropTarget</span><span class="sxs-lookup"><span data-stu-id="1e943-202">Activating Your Handler Using the IDropTarget Interface</span></span>

<span data-ttu-id="1e943-203">Échange dynamique de données (DDE) est déconseillé ; Utilisez plutôt [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .</span><span class="sxs-lookup"><span data-stu-id="1e943-203">Dynamic Data Exchange (DDE) is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="1e943-204">**IDropTarget** est plus robuste et offre une meilleure prise en charge de l’activation, car il utilise l’activation com du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="1e943-204">**IDropTarget** is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="1e943-205">Dans le cas d’une sélection de plusieurs éléments, **IDropTarget** n’est pas soumis aux restrictions de taille de mémoire tampon trouvées dans DDE et dans [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="1e943-205">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="1e943-206">En outre, les éléments sont passés à l’application sous la forme d’un objet de données qui peut être converti en tableau d’éléments à l’aide de la fonction [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) .</span><span class="sxs-lookup"><span data-stu-id="1e943-206">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="1e943-207">Cela est plus simple et ne perd pas les informations d’espace de noms lorsque l’élément est converti en chemin d’accès pour les protocoles de ligne de commande ou DDE.</span><span class="sxs-lookup"><span data-stu-id="1e943-207">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="1e943-208">Pour plus d’informations sur les requêtes [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) et Shell pour les attributs d’association de fichiers, consultez [types perçus et inscription d’application](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="1e943-208">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="specifying-the-position-and-order-of-static-verbs"></a><span data-ttu-id="1e943-209">Spécification de la position et de l’ordre des verbes statiques</span><span class="sxs-lookup"><span data-stu-id="1e943-209">Specifying the Position and Order of Static Verbs</span></span>

<span data-ttu-id="1e943-210">Normalement, les verbes sont triés sur un menu contextuel en fonction de la façon dont ils sont énumérés. l’énumération est basée en premier sur l’ordre du tableau d’associations, puis sur l’ordre des éléments dans le tableau d’association, tel que défini par l’ordre de tri du Registre.</span><span class="sxs-lookup"><span data-stu-id="1e943-210">Normally verbs are ordered on a shortcut menu based on how they are enumerated; enumeration is based first on the order of the association array, and then on the order of the items in the association array, as defined by the sort order of the registry.</span></span>

<span data-ttu-id="1e943-211">Les verbes peuvent être classés en spécifiant la valeur par défaut de la sous-clé Shell pour l’entrée Association.</span><span class="sxs-lookup"><span data-stu-id="1e943-211">Verbs can be ordered by specifying the default value of the Shell subkey for the association entry.</span></span> <span data-ttu-id="1e943-212">Cette valeur par défaut peut inclure un seul élément, qui sera affiché à la position supérieure du menu contextuel, ou une liste d’éléments séparés par des espaces ou des virgules.</span><span class="sxs-lookup"><span data-stu-id="1e943-212">This default value can include a single item, which will be displayed at the top position of the shortcut menu, or a list of items separated by spaces or commas.</span></span> <span data-ttu-id="1e943-213">Dans ce dernier cas, le premier élément de la liste est l’élément par défaut et les autres verbes s’affichent immédiatement en dessous de celui-ci dans l’ordre spécifié.</span><span class="sxs-lookup"><span data-stu-id="1e943-213">In the latter case, the first item in the list is the default item, and the other verbs are displayed immediately below it in the order specified.</span></span>

<span data-ttu-id="1e943-214">Par exemple, l’entrée de Registre suivante produit des verbes de menu contextuel dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="1e943-214">For example, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="1e943-215">Affichage</span><span class="sxs-lookup"><span data-stu-id="1e943-215">Display</span></span>
2.  <span data-ttu-id="1e943-216">Gadgets</span><span class="sxs-lookup"><span data-stu-id="1e943-216">Gadgets</span></span>
3.  <span data-ttu-id="1e943-217">Personnalisation</span><span class="sxs-lookup"><span data-stu-id="1e943-217">Personalization</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell
         Display
         Gadgets
         Personalization
```

<span data-ttu-id="1e943-218">De même, l’entrée de Registre suivante produit des verbes de menu contextuel dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="1e943-218">Similarly, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="1e943-219">Personnalisation</span><span class="sxs-lookup"><span data-stu-id="1e943-219">Personalization</span></span>
2.  <span data-ttu-id="1e943-220">Gadgets</span><span class="sxs-lookup"><span data-stu-id="1e943-220">Gadgets</span></span>
3.  <span data-ttu-id="1e943-221">Affichage</span><span class="sxs-lookup"><span data-stu-id="1e943-221">Display</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a><span data-ttu-id="1e943-222">Positionnement des verbes en haut ou en bas du menu</span><span class="sxs-lookup"><span data-stu-id="1e943-222">Positioning Verbs at the Top or Bottom of the Menu</span></span>

<span data-ttu-id="1e943-223">L’attribut de Registre suivant peut être utilisé pour placer un verbe en haut ou en bas du menu.</span><span class="sxs-lookup"><span data-stu-id="1e943-223">The following registry attribute can be used to place a verb at the top or bottom of the menu.</span></span> <span data-ttu-id="1e943-224">S’il existe plusieurs verbes qui spécifient cet attribut, la dernière à le faire est prioritaire :</span><span class="sxs-lookup"><span data-stu-id="1e943-224">If there are multiple verbs that specify this attribute then the last one to do so gets priority:</span></span>

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a><span data-ttu-id="1e943-225">Création de menus en cascade statiques</span><span class="sxs-lookup"><span data-stu-id="1e943-225">Creating Static Cascading Menus</span></span>

<span data-ttu-id="1e943-226">Dans Windows 7 et versions ultérieures, l’implémentation des menus en cascade est prise en charge via les paramètres du Registre.</span><span class="sxs-lookup"><span data-stu-id="1e943-226">In Windows 7 and later, cascading menu implementation is supported through registry settings.</span></span> <span data-ttu-id="1e943-227">Avant Windows 7, la création de menus en cascade était possible uniquement via l’implémentation de l’interface [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="1e943-227">Prior to Windows 7, the creation of cascading menus was possible only through the implementation of the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span> <span data-ttu-id="1e943-228">Dans Windows 7 et versions ultérieures, vous devez recourir à des solutions basées sur du code COM uniquement lorsque les méthodes statiques sont insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="1e943-228">In Windows 7 and later, you should resort to COM code-based solutions only when the static methods are insufficient.</span></span>

<span data-ttu-id="1e943-229">La capture d’écran suivante fournit un exemple de menu en cascade.</span><span class="sxs-lookup"><span data-stu-id="1e943-229">The following screen shot provides an example of a cascading menu.</span></span>

![capture d’écran montrant un exemple de menu en cascade](images/file-assoc/filecascademenu2ndex.png)

<span data-ttu-id="1e943-231">Dans Windows 7 et versions ultérieures, il existe trois façons de créer des menus en cascade :</span><span class="sxs-lookup"><span data-stu-id="1e943-231">In Windows 7 and later, there are three ways to create cascading menus:</span></span>

-   [<span data-ttu-id="1e943-232">Création de menus en cascade avec l’entrée de Registre subcommandes</span><span class="sxs-lookup"><span data-stu-id="1e943-232">Creating Cascading Menus with the SubCommands Registry Entry</span></span>](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [<span data-ttu-id="1e943-233">Création de menus en cascade avec l’entrée de Registre ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="1e943-233">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [<span data-ttu-id="1e943-234">Création de menus en cascade avec l’interface IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="1e943-234">Creating Cascading Menus with the IExplorerCommand Interface</span></span>](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a><span data-ttu-id="1e943-235">Création de menus en cascade avec l’entrée de Registre subcommandes</span><span class="sxs-lookup"><span data-stu-id="1e943-235">Creating Cascading Menus with the SubCommands Registry Entry</span></span>

<span data-ttu-id="1e943-236">Dans Windows 7 et versions ultérieures, vous pouvez utiliser l’entrée de sous-commandes pour créer des menus en cascade à l’aide de la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="1e943-236">In Windows 7 and later, you can use the SubCommands entry to create cascading menus by using the following procedure.</span></span>

<span data-ttu-id="1e943-237">**Pour créer un menu en cascade à l’aide de l’entrée de sous-commandes**</span><span class="sxs-lookup"><span data-stu-id="1e943-237">**To create a cascading menu by using the SubCommands entry**</span></span>

1.  <span data-ttu-id="1e943-238">Créez une sous-clé sous **HKEY \_ classes \_ racine** \\ *ProgID* \\ **Shell** pour représenter votre menu en cascade.</span><span class="sxs-lookup"><span data-stu-id="1e943-238">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="1e943-239">Dans cet exemple, nous attribuons à cette sous-clé le nom *CascadeTest*.</span><span class="sxs-lookup"><span data-stu-id="1e943-239">In this example, we give this subkey the name *CascadeTest*.</span></span> <span data-ttu-id="1e943-240">Assurez-vous que la valeur par défaut de la sous-clé *CascadeTest* est vide et affichée sous la forme **(valeur non définie)**.</span><span class="sxs-lookup"><span data-stu-id="1e943-240">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  <span data-ttu-id="1e943-241">Dans votre sous-clé *CascadeTest* , ajoutez une entrée MUIVerb de type **reg \_ SZ** et affectez-lui le texte qui s’affichera comme nom dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="1e943-241">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="1e943-242">Dans cet exemple, nous lui attribuons le « menu Test cascade ».</span><span class="sxs-lookup"><span data-stu-id="1e943-242">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  <span data-ttu-id="1e943-243">Dans votre sous-clé *CascadeTest* , ajoutez une entrée de sous-commandes de type **reg \_ SZ** qui est affectée à la liste, demlimited par des points-virgules, des verbes qui doivent apparaître dans le menu, dans l’ordre d’apparition.</span><span class="sxs-lookup"><span data-stu-id="1e943-243">To your *CascadeTest* subkey, add a SubCommands entry of type **REG\_SZ** that is assigned list, demlimited by semi-colons, of the verbs that should appear on the menu, in the order of appearance.</span></span> <span data-ttu-id="1e943-244">Par exemple, nous attribuons ici un certain nombre de verbes fournis par le système :</span><span class="sxs-lookup"><span data-stu-id="1e943-244">For example, here we assign a number of system-provided verbs:</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  <span data-ttu-id="1e943-245">Dans le cas de verbes personnalisés, implémentez-les à l’aide de l’une des méthodes d’implémentation de verbe statique et répertoriez-les sous la sous-clé **CommandStore** comme indiqué dans cet exemple pour un verbe fictif *VerbName*:</span><span class="sxs-lookup"><span data-stu-id="1e943-245">In the case of custom verbs, implement them using any of the static verb implementation methods and list them under the **CommandStore** subkey as shown in this example for a fictional verb *VerbName*:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      CommandStore
                         Shell
                            VerbName
                            command
                               (Default) = notepad.exe %1
    ```

> [!Note]  
> <span data-ttu-id="1e943-246">Cette méthode présente l’avantage que les verbes personnalisés peuvent être inscrits une seule fois et réutilisés en répertoriant le nom du verbe sous l’entrée sous-commandes.</span><span class="sxs-lookup"><span data-stu-id="1e943-246">This method has the advantage that the custom verbs can be registered once and reused by listing the verb name under the SubCommands entry.</span></span> <span data-ttu-id="1e943-247">Toutefois, l’application doit avoir l’autorisation de modifier le Registre sous **HKEY \_ local \_ machine**.</span><span class="sxs-lookup"><span data-stu-id="1e943-247">However, it requires the application to have permission to modify the registry under **HKEY\_LOCAL\_MACHINE**.</span></span>

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a><span data-ttu-id="1e943-248">Création de menus en cascade avec l’entrée de Registre ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="1e943-248">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>

<span data-ttu-id="1e943-249">Dans Windows 7 et versions ultérieures, vous pouvez utiliser l’entrée ExtendedSubCommandKey pour créer des menus en cascade étendus : des menus en cascade dans des menus en cascade.</span><span class="sxs-lookup"><span data-stu-id="1e943-249">In Windows 7 and later, you can use the ExtendedSubCommandKey entry to create extended cascading menus: cascading menus within cascading menus.</span></span>

<span data-ttu-id="1e943-250">La capture d’écran suivante est un exemple de menu en cascade étendu.</span><span class="sxs-lookup"><span data-stu-id="1e943-250">The following screen shot is an example of an extended cascading menu.</span></span>

![capture d’écran montrant le menu en cascade étendu pour les appareils](images/file-assoc/extendedsubcommandskey.png)

<span data-ttu-id="1e943-252">Étant donné que **HKEY \_ classes \_ root** est une combinaison de **HKEY \_ Current \_ User** et de **HKEY \_ local \_ machine**, vous pouvez enregistrer tous les verbes personnalisés sous la sous-clé de la sous-clé de la classe de logiciel de l' **\_ \_ utilisateur actuel** \\  \\  .</span><span class="sxs-lookup"><span data-stu-id="1e943-252">Because **HKEY\_CLASSES\_ROOT** is a combination of **HKEY\_CURRENT\_USER** and **HKEY\_LOCAL\_MACHINE**, you can register any custom verbs under the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span> <span data-ttu-id="1e943-253">Le principal avantage de cette approche est que les autorisations élevées ne sont pas requises.</span><span class="sxs-lookup"><span data-stu-id="1e943-253">The main advantage of doing so is that elevated permission is not required.</span></span> <span data-ttu-id="1e943-254">En outre, d’autres associations de fichiers peuvent réutiliser cet ensemble complet de verbes en spécifiant la même sous-clé ExtendedSubCommandsKey.</span><span class="sxs-lookup"><span data-stu-id="1e943-254">Also, other file associations can reuse this entire set of verbs by specifying the same ExtendedSubCommandsKey subkey.</span></span> <span data-ttu-id="1e943-255">Si vous n’avez pas besoin de réutiliser cet ensemble de verbes, vous pouvez répertorier les verbes sous le parent, mais vérifiez que la valeur par défaut du parent est vide.</span><span class="sxs-lookup"><span data-stu-id="1e943-255">If you do not need to reuse this set of verbs, you can list the verbs under the parent, but ensure that the Default value of the parent is empty.</span></span>

<span data-ttu-id="1e943-256">**Pour créer un menu en cascade à l’aide d’une entrée ExtendedSubCommandsKey**</span><span class="sxs-lookup"><span data-stu-id="1e943-256">**To create a cascading menu by using an ExtendedSubCommandsKey entry**</span></span>

1.  <span data-ttu-id="1e943-257">Créez une sous-clé sous **HKEY \_ classes \_ racine** \\ *ProgID* \\ **Shell** pour représenter votre menu en cascade.</span><span class="sxs-lookup"><span data-stu-id="1e943-257">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="1e943-258">Dans cet exemple, nous attribuons à cette sous-clé le nom *CascadeTest2*.</span><span class="sxs-lookup"><span data-stu-id="1e943-258">In this example, we give this subkey the name *CascadeTest2*.</span></span> <span data-ttu-id="1e943-259">Assurez-vous que la valeur par défaut de la sous-clé *CascadeTest* est vide et affichée sous la forme **(valeur non définie)**.</span><span class="sxs-lookup"><span data-stu-id="1e943-259">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  <span data-ttu-id="1e943-260">Dans votre sous-clé *CascadeTest* , ajoutez une entrée MUIVerb de type **reg \_ SZ** et affectez-lui le texte qui s’affichera comme nom dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="1e943-260">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="1e943-261">Dans cet exemple, nous lui attribuons le « menu Test cascade ».</span><span class="sxs-lookup"><span data-stu-id="1e943-261">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  <span data-ttu-id="1e943-262">Sous la sous-clé *CascadeTest* que vous avez créée, ajoutez une sous-clé **ExtendedSubCommandsKey** , puis ajoutez les sous-commandes du document (de type de **Registre \_ SZ** ), par exemple :</span><span class="sxs-lookup"><span data-stu-id="1e943-262">Under the *CascadeTest* subkey you have created, add an **ExtendedSubCommandsKey** subkey, and then add the document subcommands (of **REG\_SZ** type); for example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       txtfile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Layout
                   Properties
                   Select all
    ```

    <span data-ttu-id="1e943-263">Assurez-vous que la valeur par défaut de la sous-clé *menu de test cascade 2* est vide et affichée comme **(valeur non définie)**.</span><span class="sxs-lookup"><span data-stu-id="1e943-263">Ensure that the default value of the *Test Cascade Menu 2* subkey is empty, and shown as **(value not set)**.</span></span>

4.  <span data-ttu-id="1e943-264">Remplissez les sous-verbes à l’aide de l’une des implémentations de verbe statique suivantes.</span><span class="sxs-lookup"><span data-stu-id="1e943-264">Populate the subverbs using any of the following static verb implementations.</span></span> <span data-ttu-id="1e943-265">Notez que la sous-clé CommandFlags représente les valeurs EXPCMDFLAGS.</span><span class="sxs-lookup"><span data-stu-id="1e943-265">Note that the CommandFlags subkey represents EXPCMDFLAGS values.</span></span> <span data-ttu-id="1e943-266">Si vous souhaitez ajouter un séparateur avant ou après l’élément de menu cascade, utilisez ECF \_ SEPARATORBEFORE (0x20) ou ECF \_ SEPARATORAFTER (0x40).</span><span class="sxs-lookup"><span data-stu-id="1e943-266">If you want to add a separator before or after the cascade menu item, use ECF\_SEPARATORBEFORE (0x20) or ECF\_SEPARATORAFTER (0x40).</span></span> <span data-ttu-id="1e943-267">Pour obtenir une description de ces indicateurs Windows 7 et versions ultérieures, consultez [**IExplorerCommand :: GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span><span class="sxs-lookup"><span data-stu-id="1e943-267">For a description of these Windows 7 and later flags, see [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span></span> <span data-ttu-id="1e943-268">ECF \_ SEPARATORBEFORE fonctionne uniquement pour les éléments de menu de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="1e943-268">ECF\_SEPARATORBEFORE works only for the top level menu items.</span></span> <span data-ttu-id="1e943-269">MUIVerb est de type **reg \_ SZ** et CommandFlags est de type **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="1e943-269">MUIVerb is of type **REG\_SZ**, and CommandFlags is of type **REG\_DWORD**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       txtile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Shell
                      cmd1
                         MUIVerb = Notepad
                         command
                            (Default) = %SystemRoot%\system32\notepad.exe %1
                      cmd2
                         MUIVerb = Wordpad
                         CommandFlags = 0x20
                         command
                            (Default) = "C:\Program Files\Windows NT\Accessories\wordpad.exe" %1
    ```

<span data-ttu-id="1e943-270">La capture d’écran suivante illustre les exemples d’entrée de clé de Registre précédents.</span><span class="sxs-lookup"><span data-stu-id="1e943-270">The following screen shot is an illustration of the previous registry key entry examples.</span></span>

![capture d’écran montrant un exemple de menu en cascade montrant les choix du bloc-notes et de WordPad](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a><span data-ttu-id="1e943-272">Création de menus en cascade avec l’interface IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="1e943-272">Creating Cascading Menus with the IExplorerCommand Interface</span></span>

<span data-ttu-id="1e943-273">Vous pouvez également ajouter des verbes à un menu en cascade à l’aide de [**IExplorerCommand :: EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span><span class="sxs-lookup"><span data-stu-id="1e943-273">Another option for adding verbs to a cascading menu is through [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span></span> <span data-ttu-id="1e943-274">Cette méthode permet aux sources de données qui fournissent leurs commandes de module de commande via [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) d’utiliser ces commandes comme verbes dans un menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="1e943-274">This method enables data sources that provide their command module commands through [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="1e943-275">Dans Windows 7 et versions ultérieures, vous pouvez fournir la même implémentation de verbe à l’aide de [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) , comme vous pouvez le faire avec [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="1e943-275">In Windows 7 and later, you can provide the same verb implementation using [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) as you can with [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span>

<span data-ttu-id="1e943-276">Les deux captures d’écran suivantes illustrent l’utilisation des menus en cascade dans le dossier **appareils** .</span><span class="sxs-lookup"><span data-stu-id="1e943-276">The following two screen shots illustrate the use of cascading menus in the **Devices** folder.</span></span>

![Capture d’écran montrant un exemple de menu en cascade dans le dossier appareils.](images/file-assoc/filecascademenu.png)

<span data-ttu-id="1e943-278">La capture d’écran suivante illustre une autre implémentation d’un menu en cascade dans le dossier **appareils** .</span><span class="sxs-lookup"><span data-stu-id="1e943-278">The following screen shot illustrates another implementation of a cascading menu in the **Devices** folder.</span></span>

![capture d’écran montrant un exemple de menu en cascade dans le dossier appareils](images/file-assoc/cascadedevices2.png)

> [!Note]  
> <span data-ttu-id="1e943-280">Étant donné que [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) prend uniquement en charge l’activation in-process, il est recommandé d’utiliser des sources de données Shell qui doivent partager l’implémentation entre des commandes et des menus contextuels.</span><span class="sxs-lookup"><span data-stu-id="1e943-280">Because [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span>

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a><span data-ttu-id="1e943-281">Obtention du comportement dynamique pour les verbes statiques à l’aide de la syntaxe de requête avancée</span><span class="sxs-lookup"><span data-stu-id="1e943-281">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>

<span data-ttu-id="1e943-282">La syntaxe de requête avancée (AQS) peut exprimer une condition qui sera évaluée à l’aide des propriétés de l’élément pour lequel le verbe est instancié.</span><span class="sxs-lookup"><span data-stu-id="1e943-282">Advanced Query Syntax (AQS) can express a condition that will be evaluated using properties from the item that the verb is being instantiated for.</span></span> <span data-ttu-id="1e943-283">Ce système fonctionne uniquement avec les propriétés rapides.</span><span class="sxs-lookup"><span data-stu-id="1e943-283">This system works only with fast properties.</span></span> <span data-ttu-id="1e943-284">Il s’agit de propriétés que la source de données Shell signale comme rapide en ne retournant pas [\* \* \* \* SHCOLSTATE \_ Slow \* \*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) \* \* à partir de [**IShellFolder2 :: GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span><span class="sxs-lookup"><span data-stu-id="1e943-284">These are properties that the Shell data source reports as fast by not returning [\*\*\*\*SHCOLSTATE\_SLOW\*\*\*\*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) from [**IShellFolder2::GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span></span>

<span data-ttu-id="1e943-285">Windows 7 et versions ultérieures prennent en charge les valeurs canoniques qui évitent les problèmes sur les builds localisées.</span><span class="sxs-lookup"><span data-stu-id="1e943-285">Windows 7 and later support canonical values that avoid problems on localized builds.</span></span> <span data-ttu-id="1e943-286">La syntaxe canonique suivante est requise sur les builds localisées pour tirer parti de cette amélioration de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1e943-286">The following canonical syntax is required on localized builds to take advantage of this Windows 7 enhancement.</span></span>

``` syntax
System.StructuredQueryType.Boolean#True
```

<span data-ttu-id="1e943-287">Dans l’exemple d’entrée de Registre suivant :</span><span class="sxs-lookup"><span data-stu-id="1e943-287">In the following example registry entry:</span></span>

-   <span data-ttu-id="1e943-288">La valeur **appliesTo** contrôle si le verbe est affiché ou masqué.</span><span class="sxs-lookup"><span data-stu-id="1e943-288">The **AppliesTo** value controls whether the verb is displayed or hidden.</span></span>
-   <span data-ttu-id="1e943-289">La valeur DefaultAppliesTo détermine le verbe par défaut.</span><span class="sxs-lookup"><span data-stu-id="1e943-289">The DefaultAppliesTo value controls which verb is the default.</span></span>
-   <span data-ttu-id="1e943-290">La valeur HasLUAShield détermine si un bouclier de contrôle de compte d’utilisateur (UAC) est affiché.</span><span class="sxs-lookup"><span data-stu-id="1e943-290">The HasLUAShield value controls whether a User Account Control (UAC) shield is displayed.</span></span>

<span data-ttu-id="1e943-291">Dans cet exemple, la valeur **DefaultAppliesTo** convertit ce verbe en valeur par défaut pour tous les fichiers avec le mot « exampleText1 » dans son nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="1e943-291">In this example the **DefaultAppliesTo** value makes this verb the default for any file with the word "exampleText1" in its file name.</span></span> <span data-ttu-id="1e943-292">La valeur **appliesTo** active le verbe pour tout fichier avec « exampleText1 » dans le nom.</span><span class="sxs-lookup"><span data-stu-id="1e943-292">The **AppliesTo** value enables the verb for any file with "exampleText1" in the name.</span></span> <span data-ttu-id="1e943-293">La valeur **HasLUAShield** affiche la protection des fichiers dont le nom contient « exampleText2 ».</span><span class="sxs-lookup"><span data-stu-id="1e943-293">The **HasLUAShield** value displays the shield for files with "exampleText2" in the name.</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

<span data-ttu-id="1e943-294">Ajoutez la sous-clé de **commande** et une valeur :</span><span class="sxs-lookup"><span data-stu-id="1e943-294">Add the **Command** subkey, and a value:</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

<span data-ttu-id="1e943-295">Dans le registre de Windows 7, consultez la section **HKEY \_ classes \_ root** \\ **Drive** comme exemple de verbes BitLocker qui utilisent l’approche suivante :</span><span class="sxs-lookup"><span data-stu-id="1e943-295">In the Windows 7 registry, see **HKEY\_CLASSES\_ROOT**\\**drive** as an example of bitlocker verbs that employ the following approach:</span></span>

-   <span data-ttu-id="1e943-296">AppliesTo = System. volume. BitlockerProtection : = 2</span><span class="sxs-lookup"><span data-stu-id="1e943-296">AppliesTo = System.Volume.BitlockerProtection:=2</span></span>
-   <span data-ttu-id="1e943-297">System. volume. BitlockerRequiresAdmin : = System. StructuredQueryType. Boolean \# true</span><span class="sxs-lookup"><span data-stu-id="1e943-297">System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean\#True</span></span>

<span data-ttu-id="1e943-298">Pour plus d’informations sur AQS, consultez [syntaxe de requête avancée](../search/-search-3x-advancedquerysyntax.md).</span><span class="sxs-lookup"><span data-stu-id="1e943-298">For more information about AQS, see [Advanced Query Syntax](../search/-search-3x-advancedquerysyntax.md).</span></span>

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a><span data-ttu-id="1e943-299">Déconseillé : Association de verbes à des commandes échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="1e943-299">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>

<span data-ttu-id="1e943-300">DDE est déconseillé. Utilisez plutôt [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .</span><span class="sxs-lookup"><span data-stu-id="1e943-300">DDE is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="1e943-301">DDE est déconseillé, car il s’appuie sur un message de fenêtre de diffusion pour découvrir le serveur DDE.</span><span class="sxs-lookup"><span data-stu-id="1e943-301">DDE is deprecated because it relies on a broadcast window message to discover the DDE server.</span></span> <span data-ttu-id="1e943-302">Un serveur DDE bloque le message de fenêtre de diffusion et bloque donc les conversations DDE pour d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="1e943-302">A DDE server hang stalls the broadcast window message and thus hangs DDE conversations for other applications.</span></span> <span data-ttu-id="1e943-303">Il est courant qu’une application bloquée unique provoque des blocages ultérieurs tout au bout de l’expérience de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1e943-303">It is common for a single stuck application to cause subsequent hangs all across the user's experience.</span></span>

<span data-ttu-id="1e943-304">La méthode [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) est plus robuste et offre une meilleure prise en charge de l’activation, car elle utilise l’activation com du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="1e943-304">The [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) method is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="1e943-305">Dans le cas d’une sélection de plusieurs éléments, **IDropTarget** n’est pas soumis aux restrictions de taille de mémoire tampon trouvées dans DDE et dans [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="1e943-305">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="1e943-306">En outre, les éléments sont passés à l’application sous la forme d’un objet de données qui peut être converti en tableau d’éléments à l’aide de la fonction [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) .</span><span class="sxs-lookup"><span data-stu-id="1e943-306">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="1e943-307">Cela est plus simple et ne perd pas les informations d’espace de noms lorsque l’élément est converti en chemin d’accès pour les protocoles de ligne de commande ou DDE.</span><span class="sxs-lookup"><span data-stu-id="1e943-307">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="1e943-308">Pour plus d’informations sur les requêtes [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) et Shell pour les attributs d’association de fichiers, consultez [types perçus et inscription d’application](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="1e943-308">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

## <a name="completing-verb-implementation-tasks"></a><span data-ttu-id="1e943-309">Exécution des tâches d’implémentation de verbe</span><span class="sxs-lookup"><span data-stu-id="1e943-309">Completing Verb Implementation Tasks</span></span>

<span data-ttu-id="1e943-310">Les tâches suivantes pour implémenter des verbes sont pertinentes pour les implémentations de verbes statiques et dynamiques.</span><span class="sxs-lookup"><span data-stu-id="1e943-310">The following tasks for implementing verbs are relevant to both static and dynamic verb implementations.</span></span> <span data-ttu-id="1e943-311">Pour plus d’informations sur les verbes dynamiques, consultez [Personnalisation d’un menu contextuel à l’aide de verbes dynamiques](shortcut-menu-using-dynamic-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="1e943-311">For more information on dynamic verbs, see [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a><span data-ttu-id="1e943-312">Personnalisation du menu contextuel pour les objets Shell prédéfinis</span><span class="sxs-lookup"><span data-stu-id="1e943-312">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>

<span data-ttu-id="1e943-313">De nombreux objets Shell prédéfinis ont des menus contextuels qui peuvent être personnalisés.</span><span class="sxs-lookup"><span data-stu-id="1e943-313">Many predefined Shell objects have shortcut menus that can be customized.</span></span> <span data-ttu-id="1e943-314">Inscrivez la commande à peu près de la même façon que vous enregistrez des types de fichiers standard, mais utilisez le nom de l’objet prédéfini comme nom de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="1e943-314">Register the command in much the same way that you register typical file types, but use the name of the predefined object as the file type name.</span></span>

<span data-ttu-id="1e943-315">Une liste d’objets prédéfinis se trouve dans la section *objets Shell prédéfinis* de la [création de gestionnaires d’extension de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="1e943-315">A list of predefined objects is in the *Predefined Shell Objects* section of [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="1e943-316">Les objets Shell prédéfinis dont les menus contextuels peuvent être personnalisés en ajoutant des verbes dans le Registre sont marqués dans la table avec le mot verbe.</span><span class="sxs-lookup"><span data-stu-id="1e943-316">Those predefined Shell objects whose shortcut menus can be customized by adding verbs in the registry are marked in the table with the word Verb.</span></span>

### <a name="extending-a-new-submenu"></a><span data-ttu-id="1e943-317">Extension d’un nouveau sous-menu</span><span class="sxs-lookup"><span data-stu-id="1e943-317">Extending a New Submenu</span></span>

<span data-ttu-id="1e943-318">Quand un utilisateur ouvre le menu **fichier** dans l’Explorateur Windows, l’une des commandes affichées est **nouveau**.</span><span class="sxs-lookup"><span data-stu-id="1e943-318">When a user opens the **File** menu in Windows Explorer, one of the commands displayed is **New**.</span></span> <span data-ttu-id="1e943-319">La sélection de cette commande affiche un sous-menu.</span><span class="sxs-lookup"><span data-stu-id="1e943-319">Selecting this command displays a submenu.</span></span> <span data-ttu-id="1e943-320">Par défaut, le sous-menu contient deux commandes, **dossier** et **raccourci**, qui permettent aux utilisateurs de créer des sous-dossiers et des raccourcis.</span><span class="sxs-lookup"><span data-stu-id="1e943-320">By default, the submenu contains two commands, **Folder** and **Shortcut**, that enable users to create subfolders and shortcuts.</span></span> <span data-ttu-id="1e943-321">Ce sous-menu peut être étendu pour inclure des commandes de création de fichier pour n’importe quel type de fichier.</span><span class="sxs-lookup"><span data-stu-id="1e943-321">This submenu can be extended to include file creation commands for any file type.</span></span>

<span data-ttu-id="1e943-322">Pour ajouter une commande de création de fichier au sous-menu **nouveau** , les fichiers de votre application doivent avoir un type de fichier associé.</span><span class="sxs-lookup"><span data-stu-id="1e943-322">To add a file-creation command to the **New** submenu, your application's files must have an associated file type.</span></span> <span data-ttu-id="1e943-323">Incluez une sous-clé **ShellNew** sous le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="1e943-323">Include a **ShellNew** subkey under the file name.</span></span> <span data-ttu-id="1e943-324">Lorsque la **nouvelle** commande du menu **fichier** est sélectionnée, l’interpréteur de commandes ajoute le type de fichier au **nouveau** sous-menu.</span><span class="sxs-lookup"><span data-stu-id="1e943-324">When the **File** menu's **New** command is selected, the Shell adds the file type to the **New** submenu.</span></span> <span data-ttu-id="1e943-325">La chaîne d’affichage de la commande est la chaîne descriptive qui est assignée au ProgID du programme.</span><span class="sxs-lookup"><span data-stu-id="1e943-325">The command's display string is the descriptive string that is assigned to the program's ProgID.</span></span>

<span data-ttu-id="1e943-326">Pour spécifier la méthode de création de fichier, affectez une ou plusieurs valeurs de données à la sous-clé **ShellNew** .</span><span class="sxs-lookup"><span data-stu-id="1e943-326">To specify the file creation method, assign one or more data values to the **ShellNew** subkey.</span></span> <span data-ttu-id="1e943-327">Les valeurs disponibles sont répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1e943-327">The available values are listed in the following table.</span></span>



| <span data-ttu-id="1e943-328">Valeur de la sous-clé ShellNew</span><span class="sxs-lookup"><span data-stu-id="1e943-328">ShellNew subkey value</span></span> | <span data-ttu-id="1e943-329">Description</span><span class="sxs-lookup"><span data-stu-id="1e943-329">Description</span></span>                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e943-330">Commande</span><span class="sxs-lookup"><span data-stu-id="1e943-330">Command</span></span>               | <span data-ttu-id="1e943-331">Exécute une application.</span><span class="sxs-lookup"><span data-stu-id="1e943-331">Executes an application.</span></span> <span data-ttu-id="1e943-332">Cette valeur **reg \_ SZ** spécifie le chemin d’accès de l’application à exécuter.</span><span class="sxs-lookup"><span data-stu-id="1e943-332">This **REG\_SZ** value specifies the path of the application to be executed.</span></span> <span data-ttu-id="1e943-333">Par exemple, vous pouvez le configurer pour lancer un Assistant.</span><span class="sxs-lookup"><span data-stu-id="1e943-333">For example, you could set it to launch a wizard.</span></span>                  |
| <span data-ttu-id="1e943-334">Données</span><span class="sxs-lookup"><span data-stu-id="1e943-334">Data</span></span>                  | <span data-ttu-id="1e943-335">Crée un fichier contenant les données spécifiées.</span><span class="sxs-lookup"><span data-stu-id="1e943-335">Creates a file containing specified data.</span></span> <span data-ttu-id="1e943-336">Cette valeur **reg \_ Binary** spécifie les données du fichier.</span><span class="sxs-lookup"><span data-stu-id="1e943-336">This **REG\_BINARY** value specifies the file's data.</span></span> <span data-ttu-id="1e943-337">Les **données** sont ignorées si **Nullfile** ou **filename** est spécifié.</span><span class="sxs-lookup"><span data-stu-id="1e943-337">**Data** is ignored if either **NullFile** or **FileName** is specified.</span></span> |
| <span data-ttu-id="1e943-338">FileName</span><span class="sxs-lookup"><span data-stu-id="1e943-338">FileName</span></span>              | <span data-ttu-id="1e943-339">Crée un fichier qui est une copie d’un fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="1e943-339">Creates a file that is a copy of a specified file.</span></span> <span data-ttu-id="1e943-340">Cette valeur **reg \_ SZ** spécifie le chemin d’accès complet du fichier à copier.</span><span class="sxs-lookup"><span data-stu-id="1e943-340">This **REG\_SZ** value specifies the fully qualified path of the file to be copied.</span></span>                                   |
| <span data-ttu-id="1e943-341">NullFile</span><span class="sxs-lookup"><span data-stu-id="1e943-341">NullFile</span></span>              | <span data-ttu-id="1e943-342">Crée un fichier vide.</span><span class="sxs-lookup"><span data-stu-id="1e943-342">Creates an empty file.</span></span> <span data-ttu-id="1e943-343">**Nullfile** n’a pas de valeur assignée.</span><span class="sxs-lookup"><span data-stu-id="1e943-343">**NullFile** has no assigned a value.</span></span> <span data-ttu-id="1e943-344">Si **Nullfile** est spécifié, les valeurs de registre des **données** et des **noms** de fichiers sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="1e943-344">If **NullFile** is specified, the **Data** and **FileName** registry values are ignored.</span></span>                    |



 

<span data-ttu-id="1e943-345">L’exemple de clé de Registre et la capture d’écran ci-dessous illustrent le **nouveau** sous-menu pour le type de fichier. MYP-ms.</span><span class="sxs-lookup"><span data-stu-id="1e943-345">The following registry key example and screen shot illustrate the **New** submenu for the .myp-ms file type.</span></span> <span data-ttu-id="1e943-346">Elle possède une commande, **MyProgram application**.</span><span class="sxs-lookup"><span data-stu-id="1e943-346">It has a command, **MyProgram Application**.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

<span data-ttu-id="1e943-347">La capture d’écran illustre le **nouveau** sous-menu.</span><span class="sxs-lookup"><span data-stu-id="1e943-347">The screen shot illustrates the **New** submenu.</span></span> <span data-ttu-id="1e943-348">Lorsqu’un utilisateur sélectionne **application MyProgram** dans le sous-menu **nouveau** , l’interpréteur de commandes crée un fichier nommé **New MyProgram application. MYP-ms** et le transmet à **MyProgram.exe**.</span><span class="sxs-lookup"><span data-stu-id="1e943-348">When a user selects **MyProgram Application** from the **New** submenu, the Shell creates a file named **New MyProgram Application.myp-ms** and passes it to **MyProgram.exe**.</span></span>

![capture d’écran de l’Explorateur Windows montrant une nouvelle commande « application MyProgram » dans le sous-menu « nouveau »](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a><span data-ttu-id="1e943-350">Création de gestionnaires de glisser-déplacer</span><span class="sxs-lookup"><span data-stu-id="1e943-350">Creating Drag-and-Drop Handlers</span></span>

<span data-ttu-id="1e943-351">La procédure de base pour l’implémentation d’un gestionnaire de glisser-déplacer est identique à celle des gestionnaires de menus contextuels conventionnels.</span><span class="sxs-lookup"><span data-stu-id="1e943-351">The basic procedure for implementing a drag-and-drop handler is the same as for conventional shortcut menu handlers.</span></span> <span data-ttu-id="1e943-352">Toutefois, les gestionnaires de menus contextuels utilisent normalement uniquement le pointeur [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) transmis à la méthode [**IShellExtInit :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) du gestionnaire pour extraire le nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1e943-352">However, shortcut menu handlers normally use only the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer passed to the handler's [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method to extract the object's name.</span></span> <span data-ttu-id="1e943-353">Un gestionnaire de glisser-déplacer peut implémenter un gestionnaire de données plus sophistiqué pour modifier le comportement de l’objet déplacé.</span><span class="sxs-lookup"><span data-stu-id="1e943-353">A drag-and-drop handler could implement a more sophisticated data handler to modify the behavior of the dragged object.</span></span>

<span data-ttu-id="1e943-354">Quand un utilisateur clique avec le bouton droit sur un objet Shell pour faire glisser un objet, un menu contextuel s’affiche lorsque l’utilisateur tente de supprimer l’objet.</span><span class="sxs-lookup"><span data-stu-id="1e943-354">When a user right-clicks a Shell object to drag an object, a shortcut menu is displayed when the user attempts to drop the object.</span></span> <span data-ttu-id="1e943-355">La capture d’écran suivante illustre un menu contextuel de glisser-déplacer classique.</span><span class="sxs-lookup"><span data-stu-id="1e943-355">The following screen shot illustrates a typical drag-and-drop shortcut menu.</span></span>

![capture d’écran du menu contextuel glisser-déplacer](images/context-menu/context-dragdrop.png)

<span data-ttu-id="1e943-357">Un gestionnaire de glisser-déplacer est un gestionnaire de menu contextuel qui peut ajouter des éléments à ce menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="1e943-357">A drag-and-drop handler is a shortcut menu handler that can add items to this shortcut menu.</span></span> <span data-ttu-id="1e943-358">Les gestionnaires de glisser-déplacer sont généralement enregistrés sous la sous-clé suivante.</span><span class="sxs-lookup"><span data-stu-id="1e943-358">Drag-and-drop handlers are typically registered under the following subkey.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

<span data-ttu-id="1e943-359">Ajoutez une sous-clé sous la sous-clé **DragDropHandlers** nommée pour le gestionnaire de glisser-déplacer, puis définissez la valeur par défaut de la sous-clé sur la forme de chaîne du GUID de l’identificateur de classe (CLSID) du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="1e943-359">Add a subkey under the **DragDropHandlers** subkey named for the drag-and-drop handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span> <span data-ttu-id="1e943-360">L’exemple suivant active le gestionnaire de glisser-déplacer **MyDD** .</span><span class="sxs-lookup"><span data-stu-id="1e943-360">The following example enables the **MyDD** drag-and-drop handler.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a><span data-ttu-id="1e943-361">Suppression de verbes et contrôle de la visibilité</span><span class="sxs-lookup"><span data-stu-id="1e943-361">Suppressing Verbs and Controlling Visibility</span></span>

<span data-ttu-id="1e943-362">Vous pouvez utiliser les paramètres de stratégie Windows pour contrôler la visibilité des verbes.</span><span class="sxs-lookup"><span data-stu-id="1e943-362">You can use Windows policy settings to control verb visibility.</span></span> <span data-ttu-id="1e943-363">Les verbes peuvent être supprimés par le biais des paramètres de stratégie en ajoutant une valeur **SuppressionPolicy** ou une valeur Guid **SuppressionPolicyEx** à la sous-clé de Registre du verbe.</span><span class="sxs-lookup"><span data-stu-id="1e943-363">Verbs can be suppressed through policy settings by adding a **SuppressionPolicy** value, or a **SuppressionPolicyEx** GUID value to the verb's registry subkey.</span></span> <span data-ttu-id="1e943-364">Définissez la valeur de la sous-clé **SuppressionPolicy** sur l’ID de stratégie.</span><span class="sxs-lookup"><span data-stu-id="1e943-364">Set the value of the **SuppressionPolicy** subkey to the policy ID.</span></span> <span data-ttu-id="1e943-365">Si la stratégie est activée, le verbe et son entrée de menu contextuel associée sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="1e943-365">If the policy is turned on, the verb and its associated shortcut menu entry are suppressed.</span></span> <span data-ttu-id="1e943-366">Pour connaître les valeurs possibles de l’ID de stratégie, consultez l’énumération [**restrictions**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .</span><span class="sxs-lookup"><span data-stu-id="1e943-366">For possible policy ID values, see the [**RESTRICTIONS**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) enumeration.</span></span>

### <a name="employing-the-verb-selection-model"></a><span data-ttu-id="1e943-367">Utilisation du modèle de sélection de verbe</span><span class="sxs-lookup"><span data-stu-id="1e943-367">Employing the Verb Selection Model</span></span>

<span data-ttu-id="1e943-368">Les valeurs de Registre doivent être définies pour que les verbes gèrent les situations où un utilisateur peut sélectionner un seul élément, plusieurs éléments ou une sélection d’un élément.</span><span class="sxs-lookup"><span data-stu-id="1e943-368">Registry values must be set for verbs to handle situations where a user can select a single item, multiple items, or a selection from an item.</span></span> <span data-ttu-id="1e943-369">Un verbe requiert des valeurs de Registre distinctes pour chacune des trois situations prises en charge par le verbe.</span><span class="sxs-lookup"><span data-stu-id="1e943-369">A verb requires separate registry values for each of these three situations that the verb supports.</span></span> <span data-ttu-id="1e943-370">Les valeurs possibles pour le modèle de sélection de verbe sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1e943-370">The possible values for the verb selection model are as follows:</span></span>

-   <span data-ttu-id="1e943-371">Spécifiez la valeur MultiSelectModel pour tous les verbes.</span><span class="sxs-lookup"><span data-stu-id="1e943-371">Specify the MultiSelectModel value for all verbs.</span></span> <span data-ttu-id="1e943-372">Si la valeur MultiSelectModel n’est pas spécifiée, elle est déduite du type d’implémentation de verbe que vous avez choisi.</span><span class="sxs-lookup"><span data-stu-id="1e943-372">If the MultiSelectModel value is not specified, it is inferred from the type of verb implementation you have chosen.</span></span> <span data-ttu-id="1e943-373">Pour les méthodes basées sur COM (par exemple, DropTarget et ExecuteCommand), le **lecteur** est supposé, et pour les autres méthodes, le **document** est supposé.</span><span class="sxs-lookup"><span data-stu-id="1e943-373">For COM-based methods (such as DropTarget and ExecuteCommand) **Player** is assumed, and for the other methods **Document** is assumed.</span></span>
-   <span data-ttu-id="1e943-374">Spécifiez **Single** pour les verbes qui prennent en charge une seule sélection.</span><span class="sxs-lookup"><span data-stu-id="1e943-374">Specify **Single** for verbs that support only a single selection.</span></span>
-   <span data-ttu-id="1e943-375">Spécifiez **Player** pour les verbes qui prennent en charge un nombre quelconque d’éléments.</span><span class="sxs-lookup"><span data-stu-id="1e943-375">Specify **Player** for verbs that support any number of items.</span></span>
-   <span data-ttu-id="1e943-376">Spécifiez **document** pour les verbes qui créent une fenêtre de niveau supérieur pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="1e943-376">Specify **Document** for verbs that create a top level window for each item.</span></span> <span data-ttu-id="1e943-377">Cela permet de limiter le nombre d’éléments activés et de ne pas manquer de ressources système si l’utilisateur ouvre un trop grand nombre de fenêtres.</span><span class="sxs-lookup"><span data-stu-id="1e943-377">Doing so limits the number of items activated and helps avoid running out of system resources if the user opens too many windows.</span></span>

<span data-ttu-id="1e943-378">Lorsque le nombre d’éléments sélectionnés ne correspond pas au modèle de sélection de verbe ou est supérieur aux limites par défaut indiquées dans le tableau suivant, le verbe ne s’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="1e943-378">When the number of items selected does not match the verb selection model or is greater than the default limits outlined in the following table, the verb fails to appear.</span></span>



| <span data-ttu-id="1e943-379">Type d’implémentation de verbe</span><span class="sxs-lookup"><span data-stu-id="1e943-379">Type of verb implementation</span></span> | <span data-ttu-id="1e943-380">Document</span><span class="sxs-lookup"><span data-stu-id="1e943-380">Document</span></span> | <span data-ttu-id="1e943-381">Lecteur</span><span class="sxs-lookup"><span data-stu-id="1e943-381">Player</span></span>    |
|-----------------------------|----------|-----------|
| <span data-ttu-id="1e943-382">Hérité</span><span class="sxs-lookup"><span data-stu-id="1e943-382">Legacy</span></span>                      | <span data-ttu-id="1e943-383">15 éléments</span><span class="sxs-lookup"><span data-stu-id="1e943-383">15 items</span></span> | <span data-ttu-id="1e943-384">100 éléments</span><span class="sxs-lookup"><span data-stu-id="1e943-384">100 items</span></span> |
| <span data-ttu-id="1e943-385">COM</span><span class="sxs-lookup"><span data-stu-id="1e943-385">COM</span></span>                         | <span data-ttu-id="1e943-386">15 éléments</span><span class="sxs-lookup"><span data-stu-id="1e943-386">15 items</span></span> | <span data-ttu-id="1e943-387">Aucune limite</span><span class="sxs-lookup"><span data-stu-id="1e943-387">No limit</span></span>  |



 

<span data-ttu-id="1e943-388">Voici des exemples d’entrées de Registre utilisant la valeur MultiSelectModel.</span><span class="sxs-lookup"><span data-stu-id="1e943-388">The following are example registry entries using the MultiSelectModel value.</span></span>

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

### <a name="using-item-attributes"></a><span data-ttu-id="1e943-389">Utilisation des attributs d’élément</span><span class="sxs-lookup"><span data-stu-id="1e943-389">Using Item Attributes</span></span>

<span data-ttu-id="1e943-390">Les valeurs d’indicateur [**SFGAO**](sfgao.md) des attributs d’environnement d’un élément peuvent être testées pour déterminer si le verbe doit être activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="1e943-390">The [**SFGAO**](sfgao.md) flag values of the Shell attributes for an item can be tested to determine whether the verb should be enabled or disabled.</span></span>

<span data-ttu-id="1e943-391">Pour utiliser cette fonctionnalité d’attribut, ajoutez les valeurs **reg \_ DWORD** suivantes sous le verbe :</span><span class="sxs-lookup"><span data-stu-id="1e943-391">To use this attribute feature, add the following the **REG\_DWORD** values under the verb:</span></span>

-   <span data-ttu-id="1e943-392">La valeur AttributeMask spécifie la valeur [**SFGAO**](sfgao.md) des valeurs de bit du masque avec lequel effectuer le test.</span><span class="sxs-lookup"><span data-stu-id="1e943-392">The AttributeMask value specifies the [**SFGAO**](sfgao.md) value of the bit values of the mask to test with.</span></span>
-   <span data-ttu-id="1e943-393">La valeur AttributeValue spécifie la valeur [**SFGAO**](sfgao.md) des bits qui sont testés.</span><span class="sxs-lookup"><span data-stu-id="1e943-393">The AttributeValue value specifies the [**SFGAO**](sfgao.md) value of the bits that are tested.</span></span>
-   <span data-ttu-id="1e943-394">Le ImpliedSelectionModel spécifie zéro pour les verbes d’élément, ou une valeur différente de zéro pour les verbes dans le menu contextuel d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="1e943-394">The ImpliedSelectionModel specifies zero for item verbs, or nonzero for verbs on the background shortcut menu.</span></span>

<span data-ttu-id="1e943-395">Dans l’exemple d’entrée de Registre suivant, AttributeMask est défini sur [**SFGAO \_ ReadOnly**](sfgao.md) (0x40000).</span><span class="sxs-lookup"><span data-stu-id="1e943-395">In the following example registry entry, the AttributeMask is set to [**SFGAO\_READONLY**](sfgao.md) (0x40000).</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a><span data-ttu-id="1e943-396">Implémentation de verbes personnalisés pour les dossiers via Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="1e943-396">Implementing Custom Verbs for Folders through Desktop.ini</span></span>

<span data-ttu-id="1e943-397">Dans Windows 7 et versions ultérieures, vous pouvez ajouter des verbes à un dossier par le biais de Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="1e943-397">In Windows 7 and later, you can add verbs to a folder through Desktop.ini.</span></span> <span data-ttu-id="1e943-398">Pour plus d’informations sur les fichiers de Desktop.ini, consultez [Comment personnaliser des dossiers avec des Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="1e943-398">For more information about Desktop.ini files, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span>

> [!Note]  
> <span data-ttu-id="1e943-399">Desktop.ini fichiers doivent toujours être marqués comme étant  +  **masqués** par le système afin qu’ils ne soient pas affichés aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1e943-399">Desktop.ini files should always be marked **System** + **Hidden** so they won't be displayed to users.</span></span>

 

<span data-ttu-id="1e943-400">**Pour ajouter des verbes personnalisés pour les dossiers à l’aide d’un fichier Desktop.ini, procédez comme suit :**</span><span class="sxs-lookup"><span data-stu-id="1e943-400">**To add custom verbs for folders through a Desktop.ini file, perform the following steps:**</span></span>

1.  <span data-ttu-id="1e943-401">Créez un dossier marqué **en lecture seule** ou **système**.</span><span class="sxs-lookup"><span data-stu-id="1e943-401">Create a folder that is marked **Read-only** or **System**.</span></span>
2.  <span data-ttu-id="1e943-402">Créez un fichier de Desktop.ini qui comprend un \[ . ShellClassInfo \] DirectoryClass = ProgID du dossier.</span><span class="sxs-lookup"><span data-stu-id="1e943-402">Create a Desktop.ini file that includes a \[.ShellClassInfo\] DirectoryClass=Folder ProgID.</span></span>
3.  <span data-ttu-id="1e943-403">Dans le registre, créez le dossier **\_ \_ racine** de l’identificateur de classe HKEY, \\  avec la valeur CanUseForDirectory.</span><span class="sxs-lookup"><span data-stu-id="1e943-403">In the registry create **HKEY\_CLASSES\_ROOT**\\**Folder ProgID** with a value of CanUseForDirectory.</span></span> <span data-ttu-id="1e943-404">La valeur CanUseForDirectory évite l’utilisation abusive des ProgID qui sont définis pour ne pas participer à l’implémentation de verbes personnalisés pour les dossiers par le biais de Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="1e943-404">The CanUseForDirectory value avoids the misuse of ProgIDs that are set not to participate in implementing custom verbs for folders through Desktop.ini.</span></span>
4.  <span data-ttu-id="1e943-405">Ajoutez des verbes dans la sous-clé du **dossier** ProgID, par exemple :</span><span class="sxs-lookup"><span data-stu-id="1e943-405">Add verbs under the **Folder** ProgID subkey, for example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> <span data-ttu-id="1e943-406">Ces verbes peuvent être le verbe par défaut. dans ce cas, le double-clic sur le dossier active le verbe.</span><span class="sxs-lookup"><span data-stu-id="1e943-406">These verbs can be the default verb, in which case double-clicking the folder activates the verb.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1e943-407">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1e943-407">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e943-408">Meilleures pratiques pour les gestionnaires de menus contextuels et les verbes de sélection multiple</span><span class="sxs-lookup"><span data-stu-id="1e943-408">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="1e943-409">Choix d’un verbe statique ou dynamique pour votre menu contextuel</span><span class="sxs-lookup"><span data-stu-id="1e943-409">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="1e943-410">Personnalisation d’un menu contextuel à l’aide de verbes dynamiques</span><span class="sxs-lookup"><span data-stu-id="1e943-410">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="1e943-411">Menus contextuels (menu contextuel) et gestionnaires de menus contextuels</span><span class="sxs-lookup"><span data-stu-id="1e943-411">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="1e943-412">Verbes et associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="1e943-412">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="1e943-413">Référence du menu contextuel</span><span class="sxs-lookup"><span data-stu-id="1e943-413">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 
