---
description: Les gestionnaires de menus contextuels, également appelés gestionnaires de menus contextuels ou gestionnaires de verbes, sont un type de gestionnaire de type de fichier. Comme tous les gestionnaires de ce type, il s’agit d’objets COM (Component Object Model) en cours d’implémentation en tant que dll.
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: Création de gestionnaires de menu contextuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b7091483726c322a8ae18bace883af126d404
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2021
ms.locfileid: "103869309"
---
# <a name="creating-shortcut-menu-handlers"></a><span data-ttu-id="470cc-104">Création de gestionnaires de menu contextuel</span><span class="sxs-lookup"><span data-stu-id="470cc-104">Creating Shortcut Menu Handlers</span></span>

<span data-ttu-id="470cc-105">Les gestionnaires de menus contextuels, également appelés gestionnaires de menus contextuels ou gestionnaires de verbes, sont un type de gestionnaire de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="470cc-105">Shortcut menu handlers, also known as context menu handlers or verb handlers, are a type of file type handler.</span></span> <span data-ttu-id="470cc-106">Comme tous les gestionnaires de ce type, il s’agit d’objets COM (Component Object Model) en cours d’implémentation en tant que dll.</span><span class="sxs-lookup"><span data-stu-id="470cc-106">Like all such handlers, they are in-process Component Object Model (COM) objects implemented as DLLs.</span></span>

> [!Note]  
> <span data-ttu-id="470cc-107">Des considérations spéciales sont à prendre en compte pour Windows 64 bits lors de l’enregistrement de gestionnaires qui fonctionnent dans le contexte d’applications 32 bits : quand les verbes de Shell sont appelés dans le contexte d’une application 32 bits, le sous-système WOW64 redirige l’accès au système de fichiers vers certains chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="470cc-107">There are special considerations for 64-bit Windows when registering handlers that work in the context of 32-bit applications: when Shell verbs are invoked in the context of a 32-bit application, the WOW64 subsystem redirects file system access to some paths.</span></span> <span data-ttu-id="470cc-108">Si votre gestionnaire. exe est stocké dans l’un de ces chemins d’accès, il n’est pas accessible dans ce contexte.</span><span class="sxs-lookup"><span data-stu-id="470cc-108">If your .exe handler is stored in one of those paths, it is not accessible in this context.</span></span> <span data-ttu-id="470cc-109">Par conséquent, pour une solution de contournement, stockez votre fichier. exe dans un chemin d’accès qui n’est pas redirigé, ou stockez une version stub de votre fichier. exe qui lance la version réelle.</span><span class="sxs-lookup"><span data-stu-id="470cc-109">Therefore, as a work around, either store your .exe in a path that does not get redirected, or store a stub version of your .exe that launches the real version.</span></span>

 

<span data-ttu-id="470cc-110">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="470cc-110">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="470cc-111">Verbes canoniques</span><span class="sxs-lookup"><span data-stu-id="470cc-111">Canonical Verbs</span></span>](#canonical-verbs)
-   [<span data-ttu-id="470cc-112">Verbes étendus</span><span class="sxs-lookup"><span data-stu-id="470cc-112">Extended Verbs</span></span>](#extended-verbs)
-   [<span data-ttu-id="470cc-113">Personnalisation d’un menu contextuel à l’aide de verbes statiques</span><span class="sxs-lookup"><span data-stu-id="470cc-113">Customizing a Shortcut Menu Using Static Verbs</span></span>](#customizing-a-shortcut-menu-using-static-verbs)
    -   [<span data-ttu-id="470cc-114">Activation de votre gestionnaire à l’aide de l’interface IDropTarget</span><span class="sxs-lookup"><span data-stu-id="470cc-114">Activating Your Handler Using the IDropTarget Interface</span></span>](#activating-your-handler-using-the-idroptarget-interface)
    -   [<span data-ttu-id="470cc-115">Spécification de la position et de l’ordre des verbes statiques</span><span class="sxs-lookup"><span data-stu-id="470cc-115">Specifying the Position and Order of Static Verbs</span></span>](#specifying-the-position-and-order-of-static-verbs)
    -   [<span data-ttu-id="470cc-116">Positionnement des verbes en haut ou en bas du menu</span><span class="sxs-lookup"><span data-stu-id="470cc-116">Positioning Verbs at the Top or Bottom of the Menu</span></span>](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [<span data-ttu-id="470cc-117">Création de menus en cascade statiques</span><span class="sxs-lookup"><span data-stu-id="470cc-117">Creating Static Cascading Menus</span></span>](#creating-static-cascading-menus)
    -   [<span data-ttu-id="470cc-118">Obtention du comportement dynamique pour les verbes statiques à l’aide de la syntaxe de requête avancée</span><span class="sxs-lookup"><span data-stu-id="470cc-118">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [<span data-ttu-id="470cc-119">Déconseillé : Association de verbes à des commandes échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="470cc-119">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [<span data-ttu-id="470cc-120">Exécution des tâches d’implémentation de verbe</span><span class="sxs-lookup"><span data-stu-id="470cc-120">Completing Verb Implementation Tasks</span></span>](#completing-verb-implementation-tasks)
    -   [<span data-ttu-id="470cc-121">Personnalisation du menu contextuel pour les objets Shell prédéfinis</span><span class="sxs-lookup"><span data-stu-id="470cc-121">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [<span data-ttu-id="470cc-122">Extension d’un nouveau sous-menu</span><span class="sxs-lookup"><span data-stu-id="470cc-122">Extending a New Submenu</span></span>](#extending-a-new-submenu)
    -   [<span data-ttu-id="470cc-123">Suppression de verbes et contrôle de la visibilité</span><span class="sxs-lookup"><span data-stu-id="470cc-123">Suppressing Verbs and Controlling Visibility</span></span>](#suppressing-verbs-and-controlling-visibility)
    -   [<span data-ttu-id="470cc-124">Utilisation du modèle de sélection de verbe</span><span class="sxs-lookup"><span data-stu-id="470cc-124">Employing the Verb Selection Model</span></span>](#employing-the-verb-selection-model)
    -   [<span data-ttu-id="470cc-125">Utilisation des attributs d’élément</span><span class="sxs-lookup"><span data-stu-id="470cc-125">Using Item Attributes</span></span>](#using-item-attributes)
    -   [<span data-ttu-id="470cc-126">Implémentation de verbes personnalisés pour les dossiers via Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="470cc-126">Implementing Custom Verbs for Folders through Desktop.ini</span></span>](#implementing-custom-verbs-for-folders-through-desktopini)
-   [<span data-ttu-id="470cc-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="470cc-127">Related topics</span></span>](#related-topics)

## <a name="canonical-verbs"></a><span data-ttu-id="470cc-128">Verbes canoniques</span><span class="sxs-lookup"><span data-stu-id="470cc-128">Canonical Verbs</span></span>

<span data-ttu-id="470cc-129">Les applications sont généralement chargées de fournir des chaînes d’affichage localisées pour les verbes qu’elles définissent.</span><span class="sxs-lookup"><span data-stu-id="470cc-129">Applications are generally responsible for providing localized display strings for the verbs they define.</span></span> <span data-ttu-id="470cc-130">Toutefois, pour fournir un degré d’indépendance du langage, le système définit un ensemble standard de verbes couramment utilisés appelés verbes canoniques.</span><span class="sxs-lookup"><span data-stu-id="470cc-130">However, to provide a degree of language independence, the system defines a standard set of commonly used verbs called canonical verbs.</span></span> <span data-ttu-id="470cc-131">Un verbe canonique n’est jamais affiché à l’utilisateur et peut être utilisé avec n’importe quelle langue d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="470cc-131">A canonical verb is never displayed to the user, and can be used with any UI language.</span></span> <span data-ttu-id="470cc-132">Le système utilise le nom canonique pour générer automatiquement une chaîne d’affichage correctement localisée.</span><span class="sxs-lookup"><span data-stu-id="470cc-132">The system uses the canonical name to automatically generate a properly localized display string.</span></span> <span data-ttu-id="470cc-133">Par exemple, la chaîne d’affichage du verbe Open est définie sur **Open** sur un système en anglais et sur l’équivalent allemand sur un système allemand.</span><span class="sxs-lookup"><span data-stu-id="470cc-133">For instance, the open verb's display string is set to **Open** on an English system, and to the German equivalent on a German system.</span></span>



| <span data-ttu-id="470cc-134">Verbe canonique</span><span class="sxs-lookup"><span data-stu-id="470cc-134">Canonical verb</span></span> | <span data-ttu-id="470cc-135">Description</span><span class="sxs-lookup"><span data-stu-id="470cc-135">Description</span></span>                                                          |
|----------------|----------------------------------------------------------------------|
| <span data-ttu-id="470cc-136">Ouvrir</span><span class="sxs-lookup"><span data-stu-id="470cc-136">Open</span></span>           | <span data-ttu-id="470cc-137">Ouvre le fichier ou le dossier.</span><span class="sxs-lookup"><span data-stu-id="470cc-137">Opens the file or folder.</span></span>                                            |
| <span data-ttu-id="470cc-138">Opennew</span><span class="sxs-lookup"><span data-stu-id="470cc-138">Opennew</span></span>        | <span data-ttu-id="470cc-139">Ouvre le fichier ou le dossier dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="470cc-139">Opens the file or folder in a new window.</span></span>                            |
| <span data-ttu-id="470cc-140">Imprimer</span><span class="sxs-lookup"><span data-stu-id="470cc-140">Print</span></span>          | <span data-ttu-id="470cc-141">Imprime le fichier.</span><span class="sxs-lookup"><span data-stu-id="470cc-141">Prints the file.</span></span>                                                     |
| <span data-ttu-id="470cc-142">Printto</span><span class="sxs-lookup"><span data-stu-id="470cc-142">Printto</span></span>        | <span data-ttu-id="470cc-143">Permet à l’utilisateur d’imprimer un fichier en le faisant glisser vers un objet Printer.</span><span class="sxs-lookup"><span data-stu-id="470cc-143">Permits the user to print a file by dragging it to a printer object.</span></span> |
| <span data-ttu-id="470cc-144">Explorer</span><span class="sxs-lookup"><span data-stu-id="470cc-144">Explore</span></span>        | <span data-ttu-id="470cc-145">Ouvre l’Explorateur Windows avec le dossier sélectionné.</span><span class="sxs-lookup"><span data-stu-id="470cc-145">Opens Windows Explorer with the folder selected.</span></span>                     |
| <span data-ttu-id="470cc-146">Propriétés</span><span class="sxs-lookup"><span data-stu-id="470cc-146">Properties</span></span>     | <span data-ttu-id="470cc-147">Ouvre la feuille de propriétés de l’objet.</span><span class="sxs-lookup"><span data-stu-id="470cc-147">Opens the object's property sheet.</span></span>                                   |



 

> [!Note]  
> <span data-ttu-id="470cc-148">Le verbe **Printto** est également canonique, mais il n’est jamais affiché.</span><span class="sxs-lookup"><span data-stu-id="470cc-148">The **Printto** verb is also canonical, but it is never displayed.</span></span> <span data-ttu-id="470cc-149">Son inclusion permet à l’utilisateur d’imprimer un fichier en le faisant glisser vers un objet Printer.</span><span class="sxs-lookup"><span data-stu-id="470cc-149">Its inclusion enables the user to print a file by dragging it to a printer object.</span></span>

 

<span data-ttu-id="470cc-150">Les gestionnaires de menu contextuel peuvent fournir leurs propres verbes canoniques via [**IContextMenu :: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) avec **GC \_ VERBW** ou **GC \_ Verba**.</span><span class="sxs-lookup"><span data-stu-id="470cc-150">Shortcut menu handlers can provide their own canonical verbs through [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) with **GCS\_VERBW**, or **GCS\_VERBA**.</span></span> <span data-ttu-id="470cc-151">Le système utilise les verbes canoniques comme second paramètre (*lpOperation*) passé à [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), et est [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo). membre **lpVerb** passé à la méthode [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) .</span><span class="sxs-lookup"><span data-stu-id="470cc-151">The system will use the canonical verbs as the second parameter (*lpOperation*) passed to [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), and is the [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo).**lpVerb** member passed to the [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) method.</span></span>

## <a name="extended-verbs"></a><span data-ttu-id="470cc-152">Verbes étendus</span><span class="sxs-lookup"><span data-stu-id="470cc-152">Extended Verbs</span></span>

<span data-ttu-id="470cc-153">Quand l’utilisateur clique avec le bouton droit sur un objet, le menu contextuel affiche les verbes par défaut.</span><span class="sxs-lookup"><span data-stu-id="470cc-153">When the user right-clicks an object, the shortcut menu displays the default verbs.</span></span> <span data-ttu-id="470cc-154">Vous souhaiterez peut-être ajouter et prendre en charge des commandes dans certains menus contextuels qui ne s’affichent pas dans chaque menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="470cc-154">You might want to add and support commands on some shortcut menus that are not displayed on every shortcut menu.</span></span> <span data-ttu-id="470cc-155">Par exemple, vous pouvez avoir des commandes qui ne sont pas couramment utilisées ou qui sont destinées à des utilisateurs expérimentés.</span><span class="sxs-lookup"><span data-stu-id="470cc-155">For example, you could have commands that are not commonly used or that are intended for experienced users.</span></span> <span data-ttu-id="470cc-156">Pour cette raison, vous pouvez également définir un ou plusieurs verbes étendus.</span><span class="sxs-lookup"><span data-stu-id="470cc-156">For this reason, you can also define one or more extended verbs.</span></span> <span data-ttu-id="470cc-157">Ces verbes sont semblables aux verbes normaux, mais se distinguent des verbes normaux par leur mode d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="470cc-157">These verbs are similar to normal verbs, but are distinguished from normal verbs by the way they are registered.</span></span> <span data-ttu-id="470cc-158">Pour avoir accès à des verbes étendus, l’utilisateur doit cliquer avec le bouton droit sur un objet tout en appuyant sur la touche Maj.</span><span class="sxs-lookup"><span data-stu-id="470cc-158">To have access to extended verbs, the user must right-click an object while pressing the SHIFT key.</span></span> <span data-ttu-id="470cc-159">Lorsque l’utilisateur effectue cette action, les verbes étendus sont affichés en plus des verbes par défaut.</span><span class="sxs-lookup"><span data-stu-id="470cc-159">When the user does so, the extended verbs are displayed in addition to the default verbs.</span></span>

<span data-ttu-id="470cc-160">Vous pouvez utiliser le registre pour définir un ou plusieurs verbes étendus.</span><span class="sxs-lookup"><span data-stu-id="470cc-160">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="470cc-161">Les commandes associées s’affichent uniquement quand l’utilisateur clique avec le bouton droit sur un objet tout en appuyant sur la touche Maj.</span><span class="sxs-lookup"><span data-stu-id="470cc-161">The associated commands will be displayed only when the user right-clicks an object while also pressing the SHIFT key.</span></span> <span data-ttu-id="470cc-162">Pour définir un verbe comme étendu, ajoutez une valeur **\_ SZ** « étendue » à la sous-clé du verbe.</span><span class="sxs-lookup"><span data-stu-id="470cc-162">To define a verb as extended, add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="470cc-163">Aucune donnée ne doit être associée à la valeur.</span><span class="sxs-lookup"><span data-stu-id="470cc-163">The value should not have any data associated with it.</span></span>

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a><span data-ttu-id="470cc-164">Personnalisation d’un menu contextuel à l’aide de verbes statiques</span><span class="sxs-lookup"><span data-stu-id="470cc-164">Customizing a Shortcut Menu Using Static Verbs</span></span>

<span data-ttu-id="470cc-165">Après avoir [choisi un verbe statique ou dynamique pour votre menu contextuel](shortcut-choose-method.md) , vous pouvez étendre le menu contextuel d’un type de fichier en inscrivant un verbe statique pour le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="470cc-165">After [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md) you can extend the shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="470cc-166">Pour ce faire, ajoutez une sous-clé **Shell** sous la sous-clé pour le ProgID de l’application associée au type de fichier.</span><span class="sxs-lookup"><span data-stu-id="470cc-166">To do so, add a **Shell** subkey below the subkey for the ProgID of the application associated with the file type.</span></span> <span data-ttu-id="470cc-167">Si vous le souhaitez, vous pouvez définir un verbe par défaut pour le type de fichier en en faisant la valeur par défaut de la sous-clé **Shell** .</span><span class="sxs-lookup"><span data-stu-id="470cc-167">Optionally, you can define a default verb for the file type by making it the default value of the **Shell** subkey.</span></span>

<span data-ttu-id="470cc-168">Le verbe par défaut s’affiche en premier dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="470cc-168">The default verb is displayed first on the shortcut menu.</span></span> <span data-ttu-id="470cc-169">Son objectif est de fournir à l’interpréteur de commandes un verbe qu’il peut utiliser lorsque la fonction [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) est appelée, mais qu’aucun verbe n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="470cc-169">Its purpose is to provide the Shell with a verb it can use when the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) function is called, but no verb is specified.</span></span> <span data-ttu-id="470cc-170">L’interpréteur de commandes ne sélectionne pas nécessairement le verbe par défaut lorsque **ShellExecuteEx** est utilisé de cette manière.</span><span class="sxs-lookup"><span data-stu-id="470cc-170">The Shell does not necessarily select the default verb when **ShellExecuteEx** is used in this fashion.</span></span>

<span data-ttu-id="470cc-171">L’interpréteur de commandes utilise le premier verbe disponible dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="470cc-171">The Shell uses the first available verb in the following order:</span></span>

1.  <span data-ttu-id="470cc-172">Le verbe par défaut</span><span class="sxs-lookup"><span data-stu-id="470cc-172">The default verb</span></span>
2.  <span data-ttu-id="470cc-173">Premier verbe du Registre, si l’ordre du verbe est spécifié</span><span class="sxs-lookup"><span data-stu-id="470cc-173">The first verb in the registry, if the verb order is specified</span></span>
3.  <span data-ttu-id="470cc-174">Verbe **Open**</span><span class="sxs-lookup"><span data-stu-id="470cc-174">The **Open** verb</span></span>
4.  <span data-ttu-id="470cc-175">Le verbe **Open with**</span><span class="sxs-lookup"><span data-stu-id="470cc-175">The **Open With** verb</span></span>

<span data-ttu-id="470cc-176">Si aucun des verbes listés n’est disponible, l’opération échoue.</span><span class="sxs-lookup"><span data-stu-id="470cc-176">If none of the verbs listed is available, the operation fails.</span></span>

<span data-ttu-id="470cc-177">Créez une sous-clé pour chaque verbe que vous souhaitez ajouter sous la sous-clé Shell.</span><span class="sxs-lookup"><span data-stu-id="470cc-177">Create one subkey for each verb you want to add under the Shell subkey.</span></span> <span data-ttu-id="470cc-178">Chacune de ces sous-clés doit avoir une valeur **reg \_ SZ** définie sur la chaîne d’affichage du verbe (chaîne localisée).</span><span class="sxs-lookup"><span data-stu-id="470cc-178">Each of these subkeys must have a **REG\_SZ** value set to the verb's display string (localized string).</span></span> <span data-ttu-id="470cc-179">Pour chaque sous-clé de verbe, créez une sous-clé de commande avec la valeur par défaut définie sur la ligne de commande pour activer les éléments.</span><span class="sxs-lookup"><span data-stu-id="470cc-179">For each verb subkey, create a command subkey with the default value set to the command line for activating the items.</span></span> <span data-ttu-id="470cc-180">Pour les verbes canoniques, tels que **ouvrir** et **Imprimer**, vous pouvez omettre la chaîne d’affichage, car le système affiche automatiquement une chaîne correctement localisée.</span><span class="sxs-lookup"><span data-stu-id="470cc-180">For canonical verbs, such as **Open** and **Print**, you can omit the display string because the system automatically displays a properly localized string.</span></span> <span data-ttu-id="470cc-181">Pour les verbes non canoniques, si vous omettez la chaîne d’affichage, la chaîne de verbes est affichée.</span><span class="sxs-lookup"><span data-stu-id="470cc-181">For noncanonical verbs, if you omit the display string, the verb string is displayed.</span></span>

<span data-ttu-id="470cc-182">Dans l’exemple de Registre suivant, notez les points suivants :</span><span class="sxs-lookup"><span data-stu-id="470cc-182">In the following registry example, note that:</span></span>

-   <span data-ttu-id="470cc-183">Étant donné que **doit** n’est pas un verbe canonique, il est assigné à un nom complet, qui peut être sélectionné en appuyant sur la touche D.</span><span class="sxs-lookup"><span data-stu-id="470cc-183">Because **Doit** is not a canonical verb, it is assigned a display name, which can be selected by pressing the D key.</span></span>
-   <span data-ttu-id="470cc-184">Le verbe **Printto** n’apparaît pas dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="470cc-184">The **Printto** verb does not appear on the shortcut menu.</span></span> <span data-ttu-id="470cc-185">Toutefois, son inclusion dans le registre permet à l’utilisateur d’imprimer des fichiers en les supprimant sur une icône d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="470cc-185">However, its inclusion in the registry enables the user to print files by dropping them on a printer icon.</span></span>
-   <span data-ttu-id="470cc-186">Une sous-clé est affichée pour chaque verbe.</span><span class="sxs-lookup"><span data-stu-id="470cc-186">One subkey is shown for each verb.</span></span> <span data-ttu-id="470cc-187">**%1** représente le nom de fichier et **%2** le nom de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="470cc-187">**%1** represents the file name and **%2** the printer name.</span></span>

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

<span data-ttu-id="470cc-188">Le diagramme suivant illustre l’extension du menu contextuel conformément aux entrées de Registre ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="470cc-188">The following diagram illustrates the extension of the shortcut menu in accordance with the registry entries above.</span></span> <span data-ttu-id="470cc-189">Ce menu contextuel contient des verbes **ouvrir**, **exécuter** et **Imprimer** dans son menu **, avec le** verbe par défaut.</span><span class="sxs-lookup"><span data-stu-id="470cc-189">This shortcut menu has **Open**, **Do It**, and **Print** verbs on its menu, with **Do It** as the default verb.</span></span>

![capture d’écran du menu contextuel verbe par défaut do it](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a><span data-ttu-id="470cc-191">Activation de votre gestionnaire à l’aide de l’interface IDropTarget</span><span class="sxs-lookup"><span data-stu-id="470cc-191">Activating Your Handler Using the IDropTarget Interface</span></span>

<span data-ttu-id="470cc-192">Échange dynamique de données (DDE) est déconseillé ; Utilisez plutôt [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .</span><span class="sxs-lookup"><span data-stu-id="470cc-192">Dynamic Data Exchange (DDE) is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="470cc-193">**IDropTarget** est plus robuste et offre une meilleure prise en charge de l’activation, car il utilise l’activation com du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="470cc-193">**IDropTarget** is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="470cc-194">Dans le cas d’une sélection de plusieurs éléments, **IDropTarget** n’est pas soumis aux restrictions de taille de mémoire tampon trouvées dans DDE et dans [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="470cc-194">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="470cc-195">En outre, les éléments sont passés à l’application sous la forme d’un objet de données qui peut être converti en tableau d’éléments à l’aide de la fonction [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) .</span><span class="sxs-lookup"><span data-stu-id="470cc-195">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="470cc-196">Cela est plus simple et ne perd pas les informations d’espace de noms lorsque l’élément est converti en chemin d’accès pour les protocoles de ligne de commande ou DDE.</span><span class="sxs-lookup"><span data-stu-id="470cc-196">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="470cc-197">Pour plus d’informations sur les requêtes [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) et Shell pour les attributs d’association de fichiers, consultez [types perçus et inscription d’application](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="470cc-197">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="specifying-the-position-and-order-of-static-verbs"></a><span data-ttu-id="470cc-198">Spécification de la position et de l’ordre des verbes statiques</span><span class="sxs-lookup"><span data-stu-id="470cc-198">Specifying the Position and Order of Static Verbs</span></span>

<span data-ttu-id="470cc-199">Normalement, les verbes sont triés sur un menu contextuel en fonction de la façon dont ils sont énumérés. l’énumération est basée en premier sur l’ordre du tableau d’associations, puis sur l’ordre des éléments dans le tableau d’association, tel que défini par l’ordre de tri du Registre.</span><span class="sxs-lookup"><span data-stu-id="470cc-199">Normally verbs are ordered on a shortcut menu based on how they are enumerated; enumeration is based first on the order of the association array, and then on the order of the items in the association array, as defined by the sort order of the registry.</span></span>

<span data-ttu-id="470cc-200">Les verbes peuvent être classés en spécifiant la valeur par défaut de la sous-clé Shell pour l’entrée Association.</span><span class="sxs-lookup"><span data-stu-id="470cc-200">Verbs can be ordered by specifying the default value of the Shell subkey for the association entry.</span></span> <span data-ttu-id="470cc-201">Cette valeur par défaut peut inclure un seul élément, qui sera affiché à la position supérieure du menu contextuel, ou une liste d’éléments séparés par des espaces ou des virgules.</span><span class="sxs-lookup"><span data-stu-id="470cc-201">This default value can include a single item, which will be displayed at the top position of the shortcut menu, or a list of items separated by spaces or commas.</span></span> <span data-ttu-id="470cc-202">Dans ce dernier cas, le premier élément de la liste est l’élément par défaut et les autres verbes s’affichent immédiatement en dessous de celui-ci dans l’ordre spécifié.</span><span class="sxs-lookup"><span data-stu-id="470cc-202">In the latter case, the first item in the list is the default item, and the other verbs are displayed immediately below it in the order specified.</span></span>

<span data-ttu-id="470cc-203">Par exemple, l’entrée de Registre suivante produit des verbes de menu contextuel dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="470cc-203">For example, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="470cc-204">Afficher</span><span class="sxs-lookup"><span data-stu-id="470cc-204">Display</span></span>
2.  <span data-ttu-id="470cc-205">Gadgets</span><span class="sxs-lookup"><span data-stu-id="470cc-205">Gadgets</span></span>
3.  <span data-ttu-id="470cc-206">Personnalisation</span><span class="sxs-lookup"><span data-stu-id="470cc-206">Personalization</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell
         Display
         Gadgets
         Personalization
```

<span data-ttu-id="470cc-207">De même, l’entrée de Registre suivante produit des verbes de menu contextuel dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="470cc-207">Similarly, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="470cc-208">Personnalisation</span><span class="sxs-lookup"><span data-stu-id="470cc-208">Personalization</span></span>
2.  <span data-ttu-id="470cc-209">Gadgets</span><span class="sxs-lookup"><span data-stu-id="470cc-209">Gadgets</span></span>
3.  <span data-ttu-id="470cc-210">Afficher</span><span class="sxs-lookup"><span data-stu-id="470cc-210">Display</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a><span data-ttu-id="470cc-211">Positionnement des verbes en haut ou en bas du menu</span><span class="sxs-lookup"><span data-stu-id="470cc-211">Positioning Verbs at the Top or Bottom of the Menu</span></span>

<span data-ttu-id="470cc-212">L’attribut de Registre suivant peut être utilisé pour placer un verbe en haut ou en bas du menu.</span><span class="sxs-lookup"><span data-stu-id="470cc-212">The following registry attribute can be used to place a verb at the top or bottom of the menu.</span></span> <span data-ttu-id="470cc-213">S’il existe plusieurs verbes qui spécifient cet attribut, la dernière à le faire est prioritaire :</span><span class="sxs-lookup"><span data-stu-id="470cc-213">If there are multiple verbs that specify this attribute then the last one to do so gets priority:</span></span>

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a><span data-ttu-id="470cc-214">Création de menus en cascade statiques</span><span class="sxs-lookup"><span data-stu-id="470cc-214">Creating Static Cascading Menus</span></span>

<span data-ttu-id="470cc-215">Dans Windows 7 et versions ultérieures, l’implémentation des menus en cascade est prise en charge via les paramètres du Registre.</span><span class="sxs-lookup"><span data-stu-id="470cc-215">In Windows 7 and later, cascading menu implementation is supported through registry settings.</span></span> <span data-ttu-id="470cc-216">Avant Windows 7, la création de menus en cascade était possible uniquement via l’implémentation de l’interface [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="470cc-216">Prior to Windows 7, the creation of cascading menus was possible only through the implementation of the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span> <span data-ttu-id="470cc-217">Dans Windows 7 et versions ultérieures, vous devez recourir à des solutions basées sur du code COM uniquement lorsque les méthodes statiques sont insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="470cc-217">In Windows 7 and later, you should resort to COM code-based solutions only when the static methods are insufficient.</span></span>

<span data-ttu-id="470cc-218">La capture d’écran suivante fournit un exemple de menu en cascade.</span><span class="sxs-lookup"><span data-stu-id="470cc-218">The following screen shot provides an example of a cascading menu.</span></span>

![capture d’écran montrant un exemple de menu en cascade](images/file-assoc/filecascademenu2ndex.png)

<span data-ttu-id="470cc-220">Dans Windows 7 et versions ultérieures, il existe trois façons de créer des menus en cascade :</span><span class="sxs-lookup"><span data-stu-id="470cc-220">In Windows 7 and later, there are three ways to create cascading menus:</span></span>

-   [<span data-ttu-id="470cc-221">Création de menus en cascade avec l’entrée de Registre subcommandes</span><span class="sxs-lookup"><span data-stu-id="470cc-221">Creating Cascading Menus with the SubCommands Registry Entry</span></span>](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [<span data-ttu-id="470cc-222">Création de menus en cascade avec l’entrée de Registre ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="470cc-222">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [<span data-ttu-id="470cc-223">Création de menus en cascade avec l’interface IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="470cc-223">Creating Cascading Menus with the IExplorerCommand Interface</span></span>](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a><span data-ttu-id="470cc-224">Création de menus en cascade avec l’entrée de Registre subcommandes</span><span class="sxs-lookup"><span data-stu-id="470cc-224">Creating Cascading Menus with the SubCommands Registry Entry</span></span>

<span data-ttu-id="470cc-225">Dans Windows 7 et versions ultérieures, vous pouvez utiliser l’entrée de sous-commandes pour créer des menus en cascade à l’aide de la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="470cc-225">In Windows 7 and later, you can use the SubCommands entry to create cascading menus by using the following procedure.</span></span>

<span data-ttu-id="470cc-226">**Pour créer un menu en cascade à l’aide de l’entrée de sous-commandes**</span><span class="sxs-lookup"><span data-stu-id="470cc-226">**To create a cascading menu by using the SubCommands entry**</span></span>

1.  <span data-ttu-id="470cc-227">Créez une sous-clé sous **HKEY \_ classes \_ racine** \\ *ProgID* \\ **Shell** pour représenter votre menu en cascade.</span><span class="sxs-lookup"><span data-stu-id="470cc-227">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="470cc-228">Dans cet exemple, nous attribuons à cette sous-clé le nom *CascadeTest*.</span><span class="sxs-lookup"><span data-stu-id="470cc-228">In this example, we give this subkey the name *CascadeTest*.</span></span> <span data-ttu-id="470cc-229">Assurez-vous que la valeur par défaut de la sous-clé *CascadeTest* est vide et affichée sous la forme **(valeur non définie)**.</span><span class="sxs-lookup"><span data-stu-id="470cc-229">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  <span data-ttu-id="470cc-230">Dans votre sous-clé *CascadeTest* , ajoutez une entrée MUIVerb de type **reg \_ SZ** et affectez-lui le texte qui s’affichera comme nom dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="470cc-230">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="470cc-231">Dans cet exemple, nous lui attribuons le « menu Test cascade ».</span><span class="sxs-lookup"><span data-stu-id="470cc-231">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  <span data-ttu-id="470cc-232">Dans votre sous-clé *CascadeTest* , ajoutez une entrée de sous-commandes de type **reg \_ SZ** qui est affectée à la liste, demlimited par des points-virgules, des verbes qui doivent apparaître dans le menu, dans l’ordre d’apparition.</span><span class="sxs-lookup"><span data-stu-id="470cc-232">To your *CascadeTest* subkey, add a SubCommands entry of type **REG\_SZ** that is assigned list, demlimited by semi-colons, of the verbs that should appear on the menu, in the order of appearance.</span></span> <span data-ttu-id="470cc-233">Par exemple, nous attribuons ici un certain nombre de verbes fournis par le système :</span><span class="sxs-lookup"><span data-stu-id="470cc-233">For example, here we assign a number of system-provided verbs:</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  <span data-ttu-id="470cc-234">Dans le cas de verbes personnalisés, implémentez-les à l’aide de l’une des méthodes d’implémentation de verbe statique et répertoriez-les sous la sous-clé **CommandStore** comme indiqué dans cet exemple pour un verbe fictif *VerbName*:</span><span class="sxs-lookup"><span data-stu-id="470cc-234">In the case of custom verbs, implement them using any of the static verb implementation methods and list them under the **CommandStore** subkey as shown in this example for a fictional verb *VerbName*:</span></span>

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
> <span data-ttu-id="470cc-235">Cette méthode présente l’avantage que les verbes personnalisés peuvent être inscrits une seule fois et réutilisés en répertoriant le nom du verbe sous l’entrée sous-commandes.</span><span class="sxs-lookup"><span data-stu-id="470cc-235">This method has the advantage that the custom verbs can be registered once and reused by listing the verb name under the SubCommands entry.</span></span> <span data-ttu-id="470cc-236">Toutefois, l’application doit avoir l’autorisation de modifier le Registre sous **HKEY \_ local \_ machine**.</span><span class="sxs-lookup"><span data-stu-id="470cc-236">However, it requires the application to have permission to modify the registry under **HKEY\_LOCAL\_MACHINE**.</span></span>

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a><span data-ttu-id="470cc-237">Création de menus en cascade avec l’entrée de Registre ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="470cc-237">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>

<span data-ttu-id="470cc-238">Dans Windows 7 et versions ultérieures, vous pouvez utiliser l’entrée ExtendedSubCommandKey pour créer des menus en cascade étendus : des menus en cascade dans des menus en cascade.</span><span class="sxs-lookup"><span data-stu-id="470cc-238">In Windows 7 and later, you can use the ExtendedSubCommandKey entry to create extended cascading menus: cascading menus within cascading menus.</span></span>

<span data-ttu-id="470cc-239">La capture d’écran suivante est un exemple de menu en cascade étendu.</span><span class="sxs-lookup"><span data-stu-id="470cc-239">The following screen shot is an example of an extended cascading menu.</span></span>

![capture d’écran montrant le menu en cascade étendu pour les appareils](images/file-assoc/extendedsubcommandskey.png)

<span data-ttu-id="470cc-241">Étant donné que **HKEY \_ classes \_ root** est une combinaison de **HKEY \_ Current \_ User** et de **HKEY \_ local \_ machine**, vous pouvez enregistrer tous les verbes personnalisés sous la sous-clé de la sous-clé de la classe de logiciel de l' **\_ \_ utilisateur actuel** \\  \\  .</span><span class="sxs-lookup"><span data-stu-id="470cc-241">Because **HKEY\_CLASSES\_ROOT** is a combination of **HKEY\_CURRENT\_USER** and **HKEY\_LOCAL\_MACHINE**, you can register any custom verbs under the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span> <span data-ttu-id="470cc-242">Le principal avantage de cette approche est que les autorisations élevées ne sont pas requises.</span><span class="sxs-lookup"><span data-stu-id="470cc-242">The main advantage of doing so is that elevated permission is not required.</span></span> <span data-ttu-id="470cc-243">En outre, d’autres associations de fichiers peuvent réutiliser cet ensemble complet de verbes en spécifiant la même sous-clé ExtendedSubCommandsKey.</span><span class="sxs-lookup"><span data-stu-id="470cc-243">Also, other file associations can reuse this entire set of verbs by specifying the same ExtendedSubCommandsKey subkey.</span></span> <span data-ttu-id="470cc-244">Si vous n’avez pas besoin de réutiliser cet ensemble de verbes, vous pouvez répertorier les verbes sous le parent, mais vérifiez que la valeur par défaut du parent est vide.</span><span class="sxs-lookup"><span data-stu-id="470cc-244">If you do not need to reuse this set of verbs, you can list the verbs under the parent, but ensure that the Default value of the parent is empty.</span></span>

<span data-ttu-id="470cc-245">**Pour créer un menu en cascade à l’aide d’une entrée ExtendedSubCommandsKey**</span><span class="sxs-lookup"><span data-stu-id="470cc-245">**To create a cascading menu by using an ExtendedSubCommandsKey entry**</span></span>

1.  <span data-ttu-id="470cc-246">Créez une sous-clé sous **HKEY \_ classes \_ racine** \\ *ProgID* \\ **Shell** pour représenter votre menu en cascade.</span><span class="sxs-lookup"><span data-stu-id="470cc-246">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="470cc-247">Dans cet exemple, nous attribuons à cette sous-clé le nom *CascadeTest2*.</span><span class="sxs-lookup"><span data-stu-id="470cc-247">In this example, we give this subkey the name *CascadeTest2*.</span></span> <span data-ttu-id="470cc-248">Assurez-vous que la valeur par défaut de la sous-clé *CascadeTest* est vide et affichée sous la forme **(valeur non définie)**.</span><span class="sxs-lookup"><span data-stu-id="470cc-248">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  <span data-ttu-id="470cc-249">Dans votre sous-clé *CascadeTest* , ajoutez une entrée MUIVerb de type **reg \_ SZ** et affectez-lui le texte qui s’affichera comme nom dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="470cc-249">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="470cc-250">Dans cet exemple, nous lui attribuons le « menu Test cascade ».</span><span class="sxs-lookup"><span data-stu-id="470cc-250">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  <span data-ttu-id="470cc-251">Sous la sous-clé *CascadeTest* que vous avez créée, ajoutez une sous-clé **ExtendedSubCommandsKey** , puis ajoutez les sous-commandes du document (de type de **Registre \_ SZ** ), par exemple :</span><span class="sxs-lookup"><span data-stu-id="470cc-251">Under the *CascadeTest* subkey you have created, add an **ExtendedSubCommandsKey** subkey, and then add the document subcommands (of **REG\_SZ** type); for example:</span></span>

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

    <span data-ttu-id="470cc-252">Assurez-vous que la valeur par défaut de la sous-clé *menu de test cascade 2* est vide et affichée comme **(valeur non définie)**.</span><span class="sxs-lookup"><span data-stu-id="470cc-252">Ensure that the default value of the *Test Cascade Menu 2* subkey is empty, and shown as **(value not set)**.</span></span>

4.  <span data-ttu-id="470cc-253">Remplissez les sous-verbes à l’aide de l’une des implémentations de verbe statique suivantes.</span><span class="sxs-lookup"><span data-stu-id="470cc-253">Populate the subverbs using any of the following static verb implementations.</span></span> <span data-ttu-id="470cc-254">Notez que la sous-clé CommandFlags représente les valeurs EXPCMDFLAGS.</span><span class="sxs-lookup"><span data-stu-id="470cc-254">Note that the CommandFlags subkey represents EXPCMDFLAGS values.</span></span> <span data-ttu-id="470cc-255">Si vous souhaitez ajouter un séparateur avant ou après l’élément de menu cascade, utilisez ECF \_ SEPARATORBEFORE (0x20) ou ECF \_ SEPARATORAFTER (0x40).</span><span class="sxs-lookup"><span data-stu-id="470cc-255">If you want to add a separator before or after the cascade menu item, use ECF\_SEPARATORBEFORE (0x20) or ECF\_SEPARATORAFTER (0x40).</span></span> <span data-ttu-id="470cc-256">Pour obtenir une description de ces indicateurs Windows 7 et versions ultérieures, consultez [**IExplorerCommand :: GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span><span class="sxs-lookup"><span data-stu-id="470cc-256">For a description of these Windows 7 and later flags, see [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span></span> <span data-ttu-id="470cc-257">ECF \_ SEPARATORBEFORE fonctionne uniquement pour les éléments de menu de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="470cc-257">ECF\_SEPARATORBEFORE works only for the top level menu items.</span></span> <span data-ttu-id="470cc-258">MUIVerb est de type **reg \_ SZ** et CommandFlags est de type **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="470cc-258">MUIVerb is of type **REG\_SZ**, and CommandFlags is of type **REG\_DWORD**.</span></span>

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

<span data-ttu-id="470cc-259">La capture d’écran suivante illustre les exemples d’entrée de clé de Registre précédents.</span><span class="sxs-lookup"><span data-stu-id="470cc-259">The following screen shot is an illustration of the previous registry key entry examples.</span></span>

![capture d’écran montrant un exemple de menu en cascade montrant les choix du bloc-notes et de WordPad](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a><span data-ttu-id="470cc-261">Création de menus en cascade avec l’interface IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="470cc-261">Creating Cascading Menus with the IExplorerCommand Interface</span></span>

<span data-ttu-id="470cc-262">Vous pouvez également ajouter des verbes à un menu en cascade à l’aide de [**IExplorerCommand :: EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span><span class="sxs-lookup"><span data-stu-id="470cc-262">Another option for adding verbs to a cascading menu is through [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span></span> <span data-ttu-id="470cc-263">Cette méthode permet aux sources de données qui fournissent leurs commandes de module de commande via [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) d’utiliser ces commandes comme verbes dans un menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="470cc-263">This method enables data sources that provide their command module commands through [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="470cc-264">Dans Windows 7 et versions ultérieures, vous pouvez fournir la même implémentation de verbe à l’aide de [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) , comme vous pouvez le faire avec [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="470cc-264">In Windows 7 and later, you can provide the same verb implementation using [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) as you can with [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span>

<span data-ttu-id="470cc-265">Les deux captures d’écran suivantes illustrent l’utilisation des menus en cascade dans le dossier **appareils** .</span><span class="sxs-lookup"><span data-stu-id="470cc-265">The following two screen shots illustrate the use of cascading menus in the **Devices** folder.</span></span>

![Capture d’écran montrant un exemple de menu en cascade dans le dossier appareils.](images/file-assoc/filecascademenu.png)

<span data-ttu-id="470cc-267">La capture d’écran suivante illustre une autre implémentation d’un menu en cascade dans le dossier **appareils** .</span><span class="sxs-lookup"><span data-stu-id="470cc-267">The following screen shot illustrates another implementation of a cascading menu in the **Devices** folder.</span></span>

![capture d’écran montrant un exemple de menu en cascade dans le dossier appareils](images/file-assoc/cascadedevices2.png)

> [!Note]  
> <span data-ttu-id="470cc-269">Étant donné que [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) prend uniquement en charge l’activation in-process, il est recommandé d’utiliser des sources de données Shell qui doivent partager l’implémentation entre des commandes et des menus contextuels.</span><span class="sxs-lookup"><span data-stu-id="470cc-269">Because [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span>

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a><span data-ttu-id="470cc-270">Obtention du comportement dynamique pour les verbes statiques à l’aide de la syntaxe de requête avancée</span><span class="sxs-lookup"><span data-stu-id="470cc-270">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>

<span data-ttu-id="470cc-271">La syntaxe de requête avancée (AQS) peut exprimer une condition qui sera évaluée à l’aide des propriétés de l’élément pour lequel le verbe est instancié.</span><span class="sxs-lookup"><span data-stu-id="470cc-271">Advanced Query Syntax (AQS) can express a condition that will be evaluated using properties from the item that the verb is being instantiated for.</span></span> <span data-ttu-id="470cc-272">Ce système fonctionne uniquement avec les propriétés rapides.</span><span class="sxs-lookup"><span data-stu-id="470cc-272">This system works only with fast properties.</span></span> <span data-ttu-id="470cc-273">Il s’agit de propriétés que la source de données Shell signale comme rapide en ne retournant pas [\* \* \* \* SHCOLSTATE \_ Slow \* \*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) \* \* à partir de [**IShellFolder2 :: GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span><span class="sxs-lookup"><span data-stu-id="470cc-273">These are properties that the Shell data source reports as fast by not returning [\*\*\*\*SHCOLSTATE\_SLOW\*\*\*\*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) from [**IShellFolder2::GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span></span>

<span data-ttu-id="470cc-274">Windows 7 et versions ultérieures prennent en charge les valeurs canoniques qui évitent les problèmes sur les builds localisées.</span><span class="sxs-lookup"><span data-stu-id="470cc-274">Windows 7 and later support canonical values that avoid problems on localized builds.</span></span> <span data-ttu-id="470cc-275">La syntaxe canonique suivante est requise sur les builds localisées pour tirer parti de cette amélioration de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="470cc-275">The following canonical syntax is required on localized builds to take advantage of this Windows 7 enhancement.</span></span>

``` syntax
System.StructuredQueryType.Boolean#True
```

<span data-ttu-id="470cc-276">Dans l’exemple d’entrée de Registre suivant :</span><span class="sxs-lookup"><span data-stu-id="470cc-276">In the following example registry entry:</span></span>

-   <span data-ttu-id="470cc-277">La valeur **appliesTo** contrôle si le verbe est affiché ou masqué.</span><span class="sxs-lookup"><span data-stu-id="470cc-277">The **AppliesTo** value controls whether the verb is displayed or hidden.</span></span>
-   <span data-ttu-id="470cc-278">La valeur DefaultAppliesTo détermine le verbe par défaut.</span><span class="sxs-lookup"><span data-stu-id="470cc-278">The DefaultAppliesTo value controls which verb is the default.</span></span>
-   <span data-ttu-id="470cc-279">La valeur HasLUAShield détermine si un bouclier de contrôle de compte d’utilisateur (UAC) est affiché.</span><span class="sxs-lookup"><span data-stu-id="470cc-279">The HasLUAShield value controls whether a User Account Control (UAC) shield is displayed.</span></span>

<span data-ttu-id="470cc-280">Dans cet exemple, la valeur **DefaultAppliesTo** convertit ce verbe en valeur par défaut pour tous les fichiers avec le mot « exampleText1 » dans son nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="470cc-280">In this example the **DefaultAppliesTo** value makes this verb the default for any file with the word "exampleText1" in its file name.</span></span> <span data-ttu-id="470cc-281">La valeur **appliesTo** active le verbe pour tout fichier avec « exampleText1 » dans le nom.</span><span class="sxs-lookup"><span data-stu-id="470cc-281">The **AppliesTo** value enables the verb for any file with "exampleText1" in the name.</span></span> <span data-ttu-id="470cc-282">La valeur **HasLUAShield** affiche la protection des fichiers dont le nom contient « exampleText2 ».</span><span class="sxs-lookup"><span data-stu-id="470cc-282">The **HasLUAShield** value displays the shield for files with "exampleText2" in the name.</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

<span data-ttu-id="470cc-283">Ajoutez la sous-clé de **commande** et une valeur :</span><span class="sxs-lookup"><span data-stu-id="470cc-283">Add the **Command** subkey, and a value:</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

<span data-ttu-id="470cc-284">Dans le registre de Windows 7, consultez la section **HKEY \_ classes \_ root** \\ **Drive** comme exemple de verbes BitLocker qui utilisent l’approche suivante :</span><span class="sxs-lookup"><span data-stu-id="470cc-284">In the Windows 7 registry, see **HKEY\_CLASSES\_ROOT**\\**drive** as an example of bitlocker verbs that employ the following approach:</span></span>

-   <span data-ttu-id="470cc-285">AppliesTo = System. volume. BitlockerProtection : = 2</span><span class="sxs-lookup"><span data-stu-id="470cc-285">AppliesTo = System.Volume.BitlockerProtection:=2</span></span>
-   <span data-ttu-id="470cc-286">System. volume. BitlockerRequiresAdmin : = System. StructuredQueryType. Boolean \# true</span><span class="sxs-lookup"><span data-stu-id="470cc-286">System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean\#True</span></span>

<span data-ttu-id="470cc-287">Pour plus d’informations sur AQS, consultez [syntaxe de requête avancée](../search/-search-3x-advancedquerysyntax.md).</span><span class="sxs-lookup"><span data-stu-id="470cc-287">For more information about AQS, see [Advanced Query Syntax](../search/-search-3x-advancedquerysyntax.md).</span></span>

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a><span data-ttu-id="470cc-288">Déconseillé : Association de verbes à des commandes échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="470cc-288">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>

<span data-ttu-id="470cc-289">DDE est déconseillé. Utilisez plutôt [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .</span><span class="sxs-lookup"><span data-stu-id="470cc-289">DDE is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="470cc-290">DDE est déconseillé, car il s’appuie sur un message de fenêtre de diffusion pour découvrir le serveur DDE.</span><span class="sxs-lookup"><span data-stu-id="470cc-290">DDE is deprecated because it relies on a broadcast window message to discover the DDE server.</span></span> <span data-ttu-id="470cc-291">Un serveur DDE bloque le message de fenêtre de diffusion et bloque donc les conversations DDE pour d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="470cc-291">A DDE server hang stalls the broadcast window message and thus hangs DDE conversations for other applications.</span></span> <span data-ttu-id="470cc-292">Il est courant qu’une application bloquée unique provoque des blocages ultérieurs tout au bout de l’expérience de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="470cc-292">It is common for a single stuck application to cause subsequent hangs all across the user's experience.</span></span>

<span data-ttu-id="470cc-293">La méthode [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) est plus robuste et offre une meilleure prise en charge de l’activation, car elle utilise l’activation com du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="470cc-293">The [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) method is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="470cc-294">Dans le cas d’une sélection de plusieurs éléments, **IDropTarget** n’est pas soumis aux restrictions de taille de mémoire tampon trouvées dans DDE et dans [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="470cc-294">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="470cc-295">En outre, les éléments sont passés à l’application sous la forme d’un objet de données qui peut être converti en tableau d’éléments à l’aide de la fonction [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) .</span><span class="sxs-lookup"><span data-stu-id="470cc-295">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="470cc-296">Cela est plus simple et ne perd pas les informations d’espace de noms lorsque l’élément est converti en chemin d’accès pour les protocoles de ligne de commande ou DDE.</span><span class="sxs-lookup"><span data-stu-id="470cc-296">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="470cc-297">Pour plus d’informations sur les requêtes [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) et Shell pour les attributs d’association de fichiers, consultez [types perçus et inscription d’application](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="470cc-297">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

## <a name="completing-verb-implementation-tasks"></a><span data-ttu-id="470cc-298">Exécution des tâches d’implémentation de verbe</span><span class="sxs-lookup"><span data-stu-id="470cc-298">Completing Verb Implementation Tasks</span></span>

<span data-ttu-id="470cc-299">Les tâches suivantes pour implémenter des verbes sont pertinentes pour les implémentations de verbes statiques et dynamiques.</span><span class="sxs-lookup"><span data-stu-id="470cc-299">The following tasks for implementing verbs are relevant to both static and dynamic verb implementations.</span></span> <span data-ttu-id="470cc-300">Pour plus d’informations sur les verbes dynamiques, consultez [Personnalisation d’un menu contextuel à l’aide de verbes dynamiques](shortcut-menu-using-dynamic-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="470cc-300">For more information on dynamic verbs, see [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a><span data-ttu-id="470cc-301">Personnalisation du menu contextuel pour les objets Shell prédéfinis</span><span class="sxs-lookup"><span data-stu-id="470cc-301">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>

<span data-ttu-id="470cc-302">De nombreux objets Shell prédéfinis ont des menus contextuels qui peuvent être personnalisés.</span><span class="sxs-lookup"><span data-stu-id="470cc-302">Many predefined Shell objects have shortcut menus that can be customized.</span></span> <span data-ttu-id="470cc-303">Inscrivez la commande à peu près de la même façon que vous enregistrez des types de fichiers standard, mais utilisez le nom de l’objet prédéfini comme nom de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="470cc-303">Register the command in much the same way that you register typical file types, but use the name of the predefined object as the file type name.</span></span>

<span data-ttu-id="470cc-304">Une liste d’objets prédéfinis se trouve dans la section *objets Shell prédéfinis* de la [création de gestionnaires d’extension de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="470cc-304">A list of predefined objects is in the *Predefined Shell Objects* section of [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="470cc-305">Les objets Shell prédéfinis dont les menus contextuels peuvent être personnalisés en ajoutant des verbes dans le Registre sont marqués dans la table avec le mot verbe.</span><span class="sxs-lookup"><span data-stu-id="470cc-305">Those predefined Shell objects whose shortcut menus can be customized by adding verbs in the registry are marked in the table with the word Verb.</span></span>

### <a name="extending-a-new-submenu"></a><span data-ttu-id="470cc-306">Extension d’un nouveau sous-menu</span><span class="sxs-lookup"><span data-stu-id="470cc-306">Extending a New Submenu</span></span>

<span data-ttu-id="470cc-307">Quand un utilisateur ouvre le menu **fichier** dans l’Explorateur Windows, l’une des commandes affichées est **nouveau**.</span><span class="sxs-lookup"><span data-stu-id="470cc-307">When a user opens the **File** menu in Windows Explorer, one of the commands displayed is **New**.</span></span> <span data-ttu-id="470cc-308">La sélection de cette commande affiche un sous-menu.</span><span class="sxs-lookup"><span data-stu-id="470cc-308">Selecting this command displays a submenu.</span></span> <span data-ttu-id="470cc-309">Par défaut, le sous-menu contient deux commandes, **dossier** et **raccourci**, qui permettent aux utilisateurs de créer des sous-dossiers et des raccourcis.</span><span class="sxs-lookup"><span data-stu-id="470cc-309">By default, the submenu contains two commands, **Folder** and **Shortcut**, that enable users to create subfolders and shortcuts.</span></span> <span data-ttu-id="470cc-310">Ce sous-menu peut être étendu pour inclure des commandes de création de fichier pour n’importe quel type de fichier.</span><span class="sxs-lookup"><span data-stu-id="470cc-310">This submenu can be extended to include file creation commands for any file type.</span></span>

<span data-ttu-id="470cc-311">Pour ajouter une commande de création de fichier au sous-menu **nouveau** , les fichiers de votre application doivent avoir un type de fichier associé.</span><span class="sxs-lookup"><span data-stu-id="470cc-311">To add a file-creation command to the **New** submenu, your application's files must have an associated file type.</span></span> <span data-ttu-id="470cc-312">Incluez une sous-clé **ShellNew** sous le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="470cc-312">Include a **ShellNew** subkey under the file name.</span></span> <span data-ttu-id="470cc-313">Lorsque la **nouvelle** commande du menu **fichier** est sélectionnée, l’interpréteur de commandes ajoute le type de fichier au **nouveau** sous-menu.</span><span class="sxs-lookup"><span data-stu-id="470cc-313">When the **File** menu's **New** command is selected, the Shell adds the file type to the **New** submenu.</span></span> <span data-ttu-id="470cc-314">La chaîne d’affichage de la commande est la chaîne descriptive qui est assignée au ProgID du programme.</span><span class="sxs-lookup"><span data-stu-id="470cc-314">The command's display string is the descriptive string that is assigned to the program's ProgID.</span></span>

<span data-ttu-id="470cc-315">Pour spécifier la méthode de création de fichier, affectez une ou plusieurs valeurs de données à la sous-clé **ShellNew** .</span><span class="sxs-lookup"><span data-stu-id="470cc-315">To specify the file creation method, assign one or more data values to the **ShellNew** subkey.</span></span> <span data-ttu-id="470cc-316">Les valeurs disponibles sont répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="470cc-316">The available values are listed in the following table.</span></span>



| <span data-ttu-id="470cc-317">Valeur de la sous-clé ShellNew</span><span class="sxs-lookup"><span data-stu-id="470cc-317">ShellNew subkey value</span></span> | <span data-ttu-id="470cc-318">Description</span><span class="sxs-lookup"><span data-stu-id="470cc-318">Description</span></span>                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="470cc-319">Commande</span><span class="sxs-lookup"><span data-stu-id="470cc-319">Command</span></span>               | <span data-ttu-id="470cc-320">Exécute une application.</span><span class="sxs-lookup"><span data-stu-id="470cc-320">Executes an application.</span></span> <span data-ttu-id="470cc-321">Cette valeur **reg \_ SZ** spécifie le chemin d’accès de l’application à exécuter.</span><span class="sxs-lookup"><span data-stu-id="470cc-321">This **REG\_SZ** value specifies the path of the application to be executed.</span></span> <span data-ttu-id="470cc-322">Par exemple, vous pouvez le configurer pour lancer un Assistant.</span><span class="sxs-lookup"><span data-stu-id="470cc-322">For example, you could set it to launch a wizard.</span></span>                  |
| <span data-ttu-id="470cc-323">Données</span><span class="sxs-lookup"><span data-stu-id="470cc-323">Data</span></span>                  | <span data-ttu-id="470cc-324">Crée un fichier contenant les données spécifiées.</span><span class="sxs-lookup"><span data-stu-id="470cc-324">Creates a file containing specified data.</span></span> <span data-ttu-id="470cc-325">Cette valeur **reg \_ Binary** spécifie les données du fichier.</span><span class="sxs-lookup"><span data-stu-id="470cc-325">This **REG\_BINARY** value specifies the file's data.</span></span> <span data-ttu-id="470cc-326">Les **données** sont ignorées si **Nullfile** ou **filename** est spécifié.</span><span class="sxs-lookup"><span data-stu-id="470cc-326">**Data** is ignored if either **NullFile** or **FileName** is specified.</span></span> |
| <span data-ttu-id="470cc-327">FileName</span><span class="sxs-lookup"><span data-stu-id="470cc-327">FileName</span></span>              | <span data-ttu-id="470cc-328">Crée un fichier qui est une copie d’un fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="470cc-328">Creates a file that is a copy of a specified file.</span></span> <span data-ttu-id="470cc-329">Cette valeur **reg \_ SZ** spécifie le chemin d’accès complet du fichier à copier.</span><span class="sxs-lookup"><span data-stu-id="470cc-329">This **REG\_SZ** value specifies the fully qualified path of the file to be copied.</span></span>                                   |
| <span data-ttu-id="470cc-330">NullFile</span><span class="sxs-lookup"><span data-stu-id="470cc-330">NullFile</span></span>              | <span data-ttu-id="470cc-331">Crée un fichier vide.</span><span class="sxs-lookup"><span data-stu-id="470cc-331">Creates an empty file.</span></span> <span data-ttu-id="470cc-332">**Nullfile** n’a pas de valeur assignée.</span><span class="sxs-lookup"><span data-stu-id="470cc-332">**NullFile** has no assigned a value.</span></span> <span data-ttu-id="470cc-333">Si **Nullfile** est spécifié, les valeurs de registre des **données** et des **noms** de fichiers sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="470cc-333">If **NullFile** is specified, the **Data** and **FileName** registry values are ignored.</span></span>                    |



 

<span data-ttu-id="470cc-334">L’exemple de clé de Registre et la capture d’écran ci-dessous illustrent le **nouveau** sous-menu pour le type de fichier. MYP-ms.</span><span class="sxs-lookup"><span data-stu-id="470cc-334">The following registry key example and screen shot illustrate the **New** submenu for the .myp-ms file type.</span></span> <span data-ttu-id="470cc-335">Elle possède une commande, **MyProgram application**.</span><span class="sxs-lookup"><span data-stu-id="470cc-335">It has a command, **MyProgram Application**.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

<span data-ttu-id="470cc-336">La capture d’écran illustre le **nouveau** sous-menu.</span><span class="sxs-lookup"><span data-stu-id="470cc-336">The screen shot illustrates the **New** submenu.</span></span> <span data-ttu-id="470cc-337">Lorsqu’un utilisateur sélectionne **application MyProgram** dans le sous-menu **nouveau** , l’interpréteur de commandes crée un fichier nommé **New MyProgram application. MYP-ms** et le transmet à **MyProgram.exe**.</span><span class="sxs-lookup"><span data-stu-id="470cc-337">When a user selects **MyProgram Application** from the **New** submenu, the Shell creates a file named **New MyProgram Application.myp-ms** and passes it to **MyProgram.exe**.</span></span>

![capture d’écran de l’Explorateur Windows montrant une nouvelle commande « application MyProgram » dans le sous-menu « nouveau »](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a><span data-ttu-id="470cc-339">Création de gestionnaires de glisser-déplacer</span><span class="sxs-lookup"><span data-stu-id="470cc-339">Creating Drag-and-Drop Handlers</span></span>

<span data-ttu-id="470cc-340">La procédure de base pour l’implémentation d’un gestionnaire de glisser-déplacer est identique à celle des gestionnaires de menus contextuels conventionnels.</span><span class="sxs-lookup"><span data-stu-id="470cc-340">The basic procedure for implementing a drag-and-drop handler is the same as for conventional shortcut menu handlers.</span></span> <span data-ttu-id="470cc-341">Toutefois, les gestionnaires de menus contextuels utilisent normalement uniquement le pointeur [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) transmis à la méthode [**IShellExtInit :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) du gestionnaire pour extraire le nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="470cc-341">However, shortcut menu handlers normally use only the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer passed to the handler's [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method to extract the object's name.</span></span> <span data-ttu-id="470cc-342">Un gestionnaire de glisser-déplacer peut implémenter un gestionnaire de données plus sophistiqué pour modifier le comportement de l’objet déplacé.</span><span class="sxs-lookup"><span data-stu-id="470cc-342">A drag-and-drop handler could implement a more sophisticated data handler to modify the behavior of the dragged object.</span></span>

<span data-ttu-id="470cc-343">Quand un utilisateur clique avec le bouton droit sur un objet Shell pour faire glisser un objet, un menu contextuel s’affiche lorsque l’utilisateur tente de supprimer l’objet.</span><span class="sxs-lookup"><span data-stu-id="470cc-343">When a user right-clicks a Shell object to drag an object, a shortcut menu is displayed when the user attempts to drop the object.</span></span> <span data-ttu-id="470cc-344">La capture d’écran suivante illustre un menu contextuel de glisser-déplacer classique.</span><span class="sxs-lookup"><span data-stu-id="470cc-344">The following screen shot illustrates a typical drag-and-drop shortcut menu.</span></span>

![capture d’écran du menu contextuel glisser-déplacer](images/context-menu/context-dragdrop.png)

<span data-ttu-id="470cc-346">Un gestionnaire de glisser-déplacer est un gestionnaire de menu contextuel qui peut ajouter des éléments à ce menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="470cc-346">A drag-and-drop handler is a shortcut menu handler that can add items to this shortcut menu.</span></span> <span data-ttu-id="470cc-347">Les gestionnaires de glisser-déplacer sont généralement enregistrés sous la sous-clé suivante.</span><span class="sxs-lookup"><span data-stu-id="470cc-347">Drag-and-drop handlers are typically registered under the following subkey.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

<span data-ttu-id="470cc-348">Ajoutez une sous-clé sous la sous-clé **DragDropHandlers** nommée pour le gestionnaire de glisser-déplacer, puis définissez la valeur par défaut de la sous-clé sur la forme de chaîne du GUID de l’identificateur de classe (CLSID) du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="470cc-348">Add a subkey under the **DragDropHandlers** subkey named for the drag-and-drop handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span> <span data-ttu-id="470cc-349">L’exemple suivant active le gestionnaire de glisser-déplacer **MyDD** .</span><span class="sxs-lookup"><span data-stu-id="470cc-349">The following example enables the **MyDD** drag-and-drop handler.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a><span data-ttu-id="470cc-350">Suppression de verbes et contrôle de la visibilité</span><span class="sxs-lookup"><span data-stu-id="470cc-350">Suppressing Verbs and Controlling Visibility</span></span>

<span data-ttu-id="470cc-351">Vous pouvez utiliser les paramètres de stratégie Windows pour contrôler la visibilité des verbes.</span><span class="sxs-lookup"><span data-stu-id="470cc-351">You can use Windows policy settings to control verb visibility.</span></span> <span data-ttu-id="470cc-352">Les verbes peuvent être supprimés par le biais des paramètres de stratégie en ajoutant une valeur **SuppressionPolicy** ou une valeur Guid **SuppressionPolicyEx** à la sous-clé de Registre du verbe.</span><span class="sxs-lookup"><span data-stu-id="470cc-352">Verbs can be suppressed through policy settings by adding a **SuppressionPolicy** value, or a **SuppressionPolicyEx** GUID value to the verb's registry subkey.</span></span> <span data-ttu-id="470cc-353">Définissez la valeur de la sous-clé **SuppressionPolicy** sur l’ID de stratégie.</span><span class="sxs-lookup"><span data-stu-id="470cc-353">Set the value of the **SuppressionPolicy** subkey to the policy ID.</span></span> <span data-ttu-id="470cc-354">Si la stratégie est activée, le verbe et son entrée de menu contextuel associée sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="470cc-354">If the policy is turned on, the verb and its associated shortcut menu entry are suppressed.</span></span> <span data-ttu-id="470cc-355">Pour connaître les valeurs possibles de l’ID de stratégie, consultez l’énumération [**restrictions**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .</span><span class="sxs-lookup"><span data-stu-id="470cc-355">For possible policy ID values, see the [**RESTRICTIONS**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) enumeration.</span></span>

### <a name="employing-the-verb-selection-model"></a><span data-ttu-id="470cc-356">Utilisation du modèle de sélection de verbe</span><span class="sxs-lookup"><span data-stu-id="470cc-356">Employing the Verb Selection Model</span></span>

<span data-ttu-id="470cc-357">Les valeurs de Registre doivent être définies pour que les verbes gèrent les situations où un utilisateur peut sélectionner un seul élément, plusieurs éléments ou une sélection d’un élément.</span><span class="sxs-lookup"><span data-stu-id="470cc-357">Registry values must be set for verbs to handle situations where a user can select a single item, multiple items, or a selection from an item.</span></span> <span data-ttu-id="470cc-358">Un verbe requiert des valeurs de Registre distinctes pour chacune des trois situations prises en charge par le verbe.</span><span class="sxs-lookup"><span data-stu-id="470cc-358">A verb requires separate registry values for each of these three situations that the verb supports.</span></span> <span data-ttu-id="470cc-359">Les valeurs possibles pour le modèle de sélection de verbe sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="470cc-359">The possible values for the verb selection model are as follows:</span></span>

-   <span data-ttu-id="470cc-360">Spécifiez la valeur MultiSelectModel pour tous les verbes.</span><span class="sxs-lookup"><span data-stu-id="470cc-360">Specify the MultiSelectModel value for all verbs.</span></span> <span data-ttu-id="470cc-361">Si la valeur MultiSelectModel n’est pas spécifiée, elle est déduite du type d’implémentation de verbe que vous avez choisi.</span><span class="sxs-lookup"><span data-stu-id="470cc-361">If the MultiSelectModel value is not specified, it is inferred from the type of verb implementation you have chosen.</span></span> <span data-ttu-id="470cc-362">Pour les méthodes basées sur COM (par exemple, DropTarget et ExecuteCommand), le **lecteur** est supposé, et pour les autres méthodes, le **document** est supposé.</span><span class="sxs-lookup"><span data-stu-id="470cc-362">For COM-based methods (such as DropTarget and ExecuteCommand) **Player** is assumed, and for the other methods **Document** is assumed.</span></span>
-   <span data-ttu-id="470cc-363">Spécifiez **Single** pour les verbes qui prennent en charge une seule sélection.</span><span class="sxs-lookup"><span data-stu-id="470cc-363">Specify **Single** for verbs that support only a single selection.</span></span>
-   <span data-ttu-id="470cc-364">Spécifiez **Player** pour les verbes qui prennent en charge un nombre quelconque d’éléments.</span><span class="sxs-lookup"><span data-stu-id="470cc-364">Specify **Player** for verbs that support any number of items.</span></span>
-   <span data-ttu-id="470cc-365">Spécifiez **document** pour les verbes qui créent une fenêtre de niveau supérieur pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="470cc-365">Specify **Document** for verbs that create a top level window for each item.</span></span> <span data-ttu-id="470cc-366">Cela permet de limiter le nombre d’éléments activés et de ne pas manquer de ressources système si l’utilisateur ouvre un trop grand nombre de fenêtres.</span><span class="sxs-lookup"><span data-stu-id="470cc-366">Doing so limits the number of items activated and helps avoid running out of system resources if the user opens too many windows.</span></span>

<span data-ttu-id="470cc-367">Lorsque le nombre d’éléments sélectionnés ne correspond pas au modèle de sélection de verbe ou est supérieur aux limites par défaut indiquées dans le tableau suivant, le verbe ne s’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="470cc-367">When the number of items selected does not match the verb selection model or is greater than the default limits outlined in the following table, the verb fails to appear.</span></span>



| <span data-ttu-id="470cc-368">Type d’implémentation de verbe</span><span class="sxs-lookup"><span data-stu-id="470cc-368">Type of verb implementation</span></span> | <span data-ttu-id="470cc-369">Document</span><span class="sxs-lookup"><span data-stu-id="470cc-369">Document</span></span> | <span data-ttu-id="470cc-370">Lecteur</span><span class="sxs-lookup"><span data-stu-id="470cc-370">Player</span></span>    |
|-----------------------------|----------|-----------|
| <span data-ttu-id="470cc-371">Hérité</span><span class="sxs-lookup"><span data-stu-id="470cc-371">Legacy</span></span>                      | <span data-ttu-id="470cc-372">15 éléments</span><span class="sxs-lookup"><span data-stu-id="470cc-372">15 items</span></span> | <span data-ttu-id="470cc-373">100 éléments</span><span class="sxs-lookup"><span data-stu-id="470cc-373">100 items</span></span> |
| <span data-ttu-id="470cc-374">COM</span><span class="sxs-lookup"><span data-stu-id="470cc-374">COM</span></span>                         | <span data-ttu-id="470cc-375">15 éléments</span><span class="sxs-lookup"><span data-stu-id="470cc-375">15 items</span></span> | <span data-ttu-id="470cc-376">Aucune limite</span><span class="sxs-lookup"><span data-stu-id="470cc-376">No limit</span></span>  |



 

<span data-ttu-id="470cc-377">Voici des exemples d’entrées de Registre utilisant la valeur MultiSelectModel.</span><span class="sxs-lookup"><span data-stu-id="470cc-377">The following are example registry entries using the MultiSelectModel value.</span></span>

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

### <a name="using-item-attributes"></a><span data-ttu-id="470cc-378">Utilisation des attributs d’élément</span><span class="sxs-lookup"><span data-stu-id="470cc-378">Using Item Attributes</span></span>

<span data-ttu-id="470cc-379">Les valeurs d’indicateur [**SFGAO**](sfgao.md) des attributs d’environnement d’un élément peuvent être testées pour déterminer si le verbe doit être activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="470cc-379">The [**SFGAO**](sfgao.md) flag values of the Shell attributes for an item can be tested to determine whether the verb should be enabled or disabled.</span></span>

<span data-ttu-id="470cc-380">Pour utiliser cette fonctionnalité d’attribut, ajoutez les valeurs **reg \_ DWORD** suivantes sous le verbe :</span><span class="sxs-lookup"><span data-stu-id="470cc-380">To use this attribute feature, add the following the **REG\_DWORD** values under the verb:</span></span>

-   <span data-ttu-id="470cc-381">La valeur AttributeMask spécifie la valeur [**SFGAO**](sfgao.md) des valeurs de bit du masque avec lequel effectuer le test.</span><span class="sxs-lookup"><span data-stu-id="470cc-381">The AttributeMask value specifies the [**SFGAO**](sfgao.md) value of the bit values of the mask to test with.</span></span>
-   <span data-ttu-id="470cc-382">La valeur AttributeValue spécifie la valeur [**SFGAO**](sfgao.md) des bits qui sont testés.</span><span class="sxs-lookup"><span data-stu-id="470cc-382">The AttributeValue value specifies the [**SFGAO**](sfgao.md) value of the bits that are tested.</span></span>
-   <span data-ttu-id="470cc-383">Le ImpliedSelectionModel spécifie zéro pour les verbes d’élément, ou une valeur différente de zéro pour les verbes dans le menu contextuel d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="470cc-383">The ImpliedSelectionModel specifies zero for item verbs, or nonzero for verbs on the background shortcut menu.</span></span>

<span data-ttu-id="470cc-384">Dans l’exemple d’entrée de Registre suivant, AttributeMask est défini sur [**SFGAO \_ ReadOnly**](sfgao.md) (0x40000).</span><span class="sxs-lookup"><span data-stu-id="470cc-384">In the following example registry entry, the AttributeMask is set to [**SFGAO\_READONLY**](sfgao.md) (0x40000).</span></span>

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

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a><span data-ttu-id="470cc-385">Implémentation de verbes personnalisés pour les dossiers via Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="470cc-385">Implementing Custom Verbs for Folders through Desktop.ini</span></span>

<span data-ttu-id="470cc-386">Dans Windows 7 et versions ultérieures, vous pouvez ajouter des verbes à un dossier par le biais de Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="470cc-386">In Windows 7 and later, you can add verbs to a folder through Desktop.ini.</span></span> <span data-ttu-id="470cc-387">Pour plus d’informations sur les fichiers de Desktop.ini, consultez [Comment personnaliser des dossiers avec des Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="470cc-387">For more information about Desktop.ini files, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span>

> [!Note]  
> <span data-ttu-id="470cc-388">Desktop.ini fichiers doivent toujours être marqués comme étant  +  **masqués** par le système afin qu’ils ne soient pas affichés aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="470cc-388">Desktop.ini files should always be marked **System** + **Hidden** so they won't be displayed to users.</span></span>

 

<span data-ttu-id="470cc-389">**Pour ajouter des verbes personnalisés pour les dossiers à l’aide d’un fichier Desktop.ini, procédez comme suit :**</span><span class="sxs-lookup"><span data-stu-id="470cc-389">**To add custom verbs for folders through a Desktop.ini file, perform the following steps:**</span></span>

1.  <span data-ttu-id="470cc-390">Créez un dossier marqué **en lecture seule** ou **système**.</span><span class="sxs-lookup"><span data-stu-id="470cc-390">Create a folder that is marked **Read-only** or **System**.</span></span>
2.  <span data-ttu-id="470cc-391">Créez un fichier de Desktop.ini qui comprend un \[ . ShellClassInfo \] DirectoryClass = ProgID du dossier.</span><span class="sxs-lookup"><span data-stu-id="470cc-391">Create a Desktop.ini file that includes a \[.ShellClassInfo\] DirectoryClass=Folder ProgID.</span></span>
3.  <span data-ttu-id="470cc-392">Dans le registre, créez le dossier **\_ \_ racine** de l’identificateur de classe HKEY, \\  avec la valeur CanUseForDirectory.</span><span class="sxs-lookup"><span data-stu-id="470cc-392">In the registry create **HKEY\_CLASSES\_ROOT**\\**Folder ProgID** with a value of CanUseForDirectory.</span></span> <span data-ttu-id="470cc-393">La valeur CanUseForDirectory évite l’utilisation abusive des ProgID qui sont définis pour ne pas participer à l’implémentation de verbes personnalisés pour les dossiers par le biais de Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="470cc-393">The CanUseForDirectory value avoids the misuse of ProgIDs that are set not to participate in implementing custom verbs for folders through Desktop.ini.</span></span>
4.  <span data-ttu-id="470cc-394">Ajoutez des verbes dans la sous-clé du **dossier** ProgID, par exemple :</span><span class="sxs-lookup"><span data-stu-id="470cc-394">Add verbs under the **Folder** ProgID subkey, for example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> <span data-ttu-id="470cc-395">Ces verbes peuvent être le verbe par défaut. dans ce cas, le double-clic sur le dossier active le verbe.</span><span class="sxs-lookup"><span data-stu-id="470cc-395">These verbs can be the default verb, in which case double-clicking the folder activates the verb.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="470cc-396">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="470cc-396">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="470cc-397">Meilleures pratiques pour les gestionnaires de menus contextuels et les verbes de sélection multiple</span><span class="sxs-lookup"><span data-stu-id="470cc-397">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="470cc-398">Choix d’un verbe statique ou dynamique pour votre menu contextuel</span><span class="sxs-lookup"><span data-stu-id="470cc-398">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="470cc-399">Personnalisation d’un menu contextuel à l’aide de verbes dynamiques</span><span class="sxs-lookup"><span data-stu-id="470cc-399">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="470cc-400">Menus contextuels (menu contextuel) et gestionnaires de menus contextuels</span><span class="sxs-lookup"><span data-stu-id="470cc-400">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="470cc-401">Verbes et associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="470cc-401">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="470cc-402">Référence du menu contextuel</span><span class="sxs-lookup"><span data-stu-id="470cc-402">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 
