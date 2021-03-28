---
description: 'Cette rubrique est organisée comme suit :'
title: Choix d’une méthode de menu contextuel statique ou dynamique
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 44227BCF-D35E-4a9e-B4E6-D50E6AFBAEDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 70c6cb74e2c9a432bfdae2f26da1fdbebfc5f00b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034821"
---
# <a name="choosing-a-static-or-dynamic-shortcut-menu-method"></a><span data-ttu-id="fa700-103">Choix d’une méthode de menu contextuel statique ou dynamique</span><span class="sxs-lookup"><span data-stu-id="fa700-103">Choosing a Static or Dynamic Shortcut Menu Method</span></span>

<span data-ttu-id="fa700-104">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="fa700-104">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="fa700-105">Choisir une méthode de verbe</span><span class="sxs-lookup"><span data-stu-id="fa700-105">Choose a Verb Method</span></span>](#choose-a-verb-method)
    -   [<span data-ttu-id="fa700-106">Méthodes Verb statiques</span><span class="sxs-lookup"><span data-stu-id="fa700-106">Static Verb Methods</span></span>](#static-verb-methods)
    -   [<span data-ttu-id="fa700-107">Méthodes de verbe dynamique préférées</span><span class="sxs-lookup"><span data-stu-id="fa700-107">Preferred Dynamic Verb Methods</span></span>](#preferred-dynamic-verb-methods)
    -   [<span data-ttu-id="fa700-108">Méthodes de verbe dynamique déconseillées</span><span class="sxs-lookup"><span data-stu-id="fa700-108">Discouraged Dynamic Verb Methods</span></span>](#discouraged-dynamic-verb-methods)
-   [<span data-ttu-id="fa700-109">Étendre un menu contextuel</span><span class="sxs-lookup"><span data-stu-id="fa700-109">Extend a Shortcut Menu</span></span>](#extend-a-shortcut-menu)
-   [<span data-ttu-id="fa700-110">Prise en charge des méthodes de verbe par système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="fa700-110">Support for Verb Methods by Operating System</span></span>](#support-for-verb-methods-by-operating-system)
-   [<span data-ttu-id="fa700-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fa700-111">Related topics</span></span>](#related-topics)

## <a name="choose-a-verb-method"></a><span data-ttu-id="fa700-112">Choisir une méthode de verbe</span><span class="sxs-lookup"><span data-stu-id="fa700-112">Choose a Verb Method</span></span>

<span data-ttu-id="fa700-113">Il est vivement recommandé d’implémenter un menu contextuel à l’aide de l’une des méthodes de verbe statique.</span><span class="sxs-lookup"><span data-stu-id="fa700-113">It is strongly encouraged that you implement a shortcut menu using one of the static verb methods.</span></span>

### <a name="static-verb-methods"></a><span data-ttu-id="fa700-114">Méthodes Verb statiques</span><span class="sxs-lookup"><span data-stu-id="fa700-114">Static Verb Methods</span></span>

<span data-ttu-id="fa700-115">Les verbes statiques sont les verbes les plus simples à implémenter, mais ils fournissent toujours des fonctionnalités riches.</span><span class="sxs-lookup"><span data-stu-id="fa700-115">Static verbs are the simplest verbs to implement, but they still provide rich functionality.</span></span> <span data-ttu-id="fa700-116">Choisissez toujours la méthode de menu contextuel la plus simple qui répond à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="fa700-116">Always chose the simplest shortcut menu method that meets your needs.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fa700-117">Verbe statique</span><span class="sxs-lookup"><span data-stu-id="fa700-117">Static Verb</span></span></th>
<th><span data-ttu-id="fa700-118">Description</span><span class="sxs-lookup"><span data-stu-id="fa700-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fa700-119"><a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> avec paramètres de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="fa700-119"><a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> with command line parameters</span></span></td>
<td><span data-ttu-id="fa700-120">Il s’agit des méthodes les plus simples et les plus familières pour implémenter un verbe statique.</span><span class="sxs-lookup"><span data-stu-id="fa700-120">This is the simplest and most familiar means of implementing a static verb.</span></span> <span data-ttu-id="fa700-121">Un processus est appelé via un appel à la fonction <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> avec les fichiers sélectionnés et tous les paramètres facultatifs passés comme ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="fa700-121">A process is invoked through a call to the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> function with the selected files and any optional parameters passed as the command line.</span></span> <span data-ttu-id="fa700-122">Cela ouvre le fichier ou le dossier.</span><span class="sxs-lookup"><span data-stu-id="fa700-122">This opens the file or folder.</span></span><br/> <span data-ttu-id="fa700-123">Cette méthode présente les limitations suivantes :</span><span class="sxs-lookup"><span data-stu-id="fa700-123">This method has the following limitations:</span></span>
<ul>
<li><span data-ttu-id="fa700-124">La longueur de la ligne de commande est limitée à 2000 caractères, ce qui limite le nombre d’éléments que le verbe peut gérer.</span><span class="sxs-lookup"><span data-stu-id="fa700-124">The command-line length is limited to 2000 characters, which limits the number of items that the verb can handle.</span></span></li>
<li><span data-ttu-id="fa700-125">Peut uniquement être utilisé avec les éléments du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="fa700-125">Can only be used with file system items.</span></span></li>
<li><span data-ttu-id="fa700-126">N’active pas la réutilisation d’un processus déjà en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="fa700-126">Does not enable re-use of an already running process.</span></span></li>
<li><span data-ttu-id="fa700-127">Requiert l’installation d’un exécutable pour gérer le verbe.</span><span class="sxs-lookup"><span data-stu-id="fa700-127">Requires that an executable be installed to handle the verb.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa700-128"><strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"> <strong>IDropTarget</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa700-128"><strong>DropTarget</strong>/<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a></span></span></td>
<td><span data-ttu-id="fa700-129">Une activation de verbe basée sur COM signifie que prend en charge l’activation en mode in-proc ou hors processus.</span><span class="sxs-lookup"><span data-stu-id="fa700-129">A COM-based verb activation means that supports in-proc or out-of-proc activation.</span></span> <span data-ttu-id="fa700-130"><strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> prend également en charge la réutilisation d’un gestionnaire déjà en cours d’exécution lorsque l’interface <strong>IDropTarget</strong> est implémentée par un serveur local.</span><span class="sxs-lookup"><span data-stu-id="fa700-130"><strong>DropTarget</strong>/<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> also supports re-use of an already running handler when the <strong>IDropTarget</strong> interface is implemented by a local server.</span></span> <span data-ttu-id="fa700-131">Il exprime également parfaitement les éléments via l’objet de données marshalés et fournit une référence à l’appel de la chaîne de site afin que vous puissiez interagir avec le demandeur via le service <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="fa700-131">It also perfectly expresses the items via the marshaled data object and provides a reference to the invoking site chain so that you can interact with the invoker through the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa700-132">Windows 7 et versions ultérieures : <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"> <strong>IExecuteCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa700-132">Windows 7 and later: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a></span></span></td>
<td><span data-ttu-id="fa700-133">La méthode d’implémentation la plus directe.</span><span class="sxs-lookup"><span data-stu-id="fa700-133">The most direct implementation method.</span></span> <span data-ttu-id="fa700-134">Étant donné qu’il s’agit d’une méthode d’appel COM (par exemple, DropTarget), cette interface prend en charge l’activation in-proc et out-of-process.</span><span class="sxs-lookup"><span data-stu-id="fa700-134">Because this is a COM-based invoke method (like DropTarget) this interface supports in-proc and out-of-proc activation.</span></span> <span data-ttu-id="fa700-135">Le verbe implémente <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> et <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a>, et éventuellement <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="fa700-135">The verb implements <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a>, and optionally <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a>.</span></span> <span data-ttu-id="fa700-136">Les éléments sont passés directement en tant que tableau d’éléments d’interpréteur de commandes et davantage de paramètres du demandeur sont disponibles pour l’implémentation du verbe, y compris le point d’appel, l’état du clavier, etc.</span><span class="sxs-lookup"><span data-stu-id="fa700-136">The items are passed directly as a Shell item array and more of the parameters from the invoker are available to the verb implementation, including the invoke point, keyboard state, and so forth.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa700-137">Windows 7 et versions ultérieures :<strong>ExplorerCommand</strong> /  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa700-137">Windows 7 and later:<strong>ExplorerCommand</strong>/ <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></span></span></td>
<td><span data-ttu-id="fa700-138">Active les sources de données qui fournissent leurs commandes de module de commande via <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> pour utiliser ces commandes comme verbes dans un menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="fa700-138">Enables data sources that provide their command module commands through <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="fa700-139">Étant donné que cette interface prend en charge uniquement l’activation in-process, il est recommandé d’utiliser des sources de données Shell qui doivent partager l’implémentation entre les commandes et les menus contextuels.</span><span class="sxs-lookup"><span data-stu-id="fa700-139">Because this interface supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="fa700-140">[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) est un hybride entre un verbe statique et dynamique.</span><span class="sxs-lookup"><span data-stu-id="fa700-140">[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) is a hybrid between a static and dynamic verb.</span></span> <span data-ttu-id="fa700-141">**IExplorerCommand** a été déclaré dans Windows Vista, mais sa capacité à implémenter un verbe dans un menu contextuel est une nouveauté de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fa700-141">**IExplorerCommand** was declared in Windows Vista, but its ability to implement a verb in a shortcut menu is new to Windows 7.</span></span>

 

<span data-ttu-id="fa700-142">Pour plus d’informations sur les requêtes [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) et Shell pour les attributs d’association de fichiers, consultez [types perçus et inscription d’application](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="fa700-142">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="preferred-dynamic-verb-methods"></a><span data-ttu-id="fa700-143">Méthodes de verbe dynamique préférées</span><span class="sxs-lookup"><span data-stu-id="fa700-143">Preferred Dynamic Verb Methods</span></span>

<span data-ttu-id="fa700-144">Les méthodes de verbe dynamique suivantes sont préférées :</span><span class="sxs-lookup"><span data-stu-id="fa700-144">The following dynamic verb methods are preferred:</span></span>



| <span data-ttu-id="fa700-145">Type de verbe</span><span class="sxs-lookup"><span data-stu-id="fa700-145">Verb Type</span></span>                                                                                 | <span data-ttu-id="fa700-146">Description</span><span class="sxs-lookup"><span data-stu-id="fa700-146">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa700-147">Verbe statique (listé dans le tableau précédent) + syntaxe de requête avancée (AQS)</span><span class="sxs-lookup"><span data-stu-id="fa700-147">Static verb (listed in the previous table) + Advanced Query Syntax (AQS)</span></span>                  | <span data-ttu-id="fa700-148">Ce choix obtient la visibilité des verbes dynamiques.</span><span class="sxs-lookup"><span data-stu-id="fa700-148">This choice gets dynamic verb visibility.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="fa700-149">Windows 7 et versions ultérieures : [ **IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)</span><span class="sxs-lookup"><span data-stu-id="fa700-149">Windows 7 and later: [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)</span></span>                         | <span data-ttu-id="fa700-150">Ce choix permet une implémentation courante des verbes et des commandes de l’Explorateur qui s’affichent dans le module de commande dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="fa700-150">This choice enables a common implementation of verbs and explorer commands that are displayed in the command module in Windows Explorer.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="fa700-151">Windows 7 et versions ultérieures : [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + verbe statique</span><span class="sxs-lookup"><span data-stu-id="fa700-151">Windows 7 and later: [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + static verb</span></span> | <span data-ttu-id="fa700-152">Ce choix obtient également la visibilité des verbes dynamiques.</span><span class="sxs-lookup"><span data-stu-id="fa700-152">This choice also gets dynamic verb visibility.</span></span> <span data-ttu-id="fa700-153">Il s’agit d’un modèle hybride dans lequel un simple gestionnaire in-process est utilisé pour calculer si un verbe statique donné doit être affiche.</span><span class="sxs-lookup"><span data-stu-id="fa700-153">It is a hybrid model where a simple in-process handler is used to compute if a given static verb should be displyed.</span></span> <span data-ttu-id="fa700-154">Cela peut être appliqué à toutes les méthodes d’implémentation de verbe statique pour obtenir un comportement dynamique et réduire l’exposition de la logique in-process.</span><span class="sxs-lookup"><span data-stu-id="fa700-154">This can be applied to all of the static verb implementation methods to achieve dynamic behavior and minimize the exposure of the in-process logic.</span></span> <span data-ttu-id="fa700-155">[**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) présente l’avantage de s’exécuter sur un thread d’arrière-plan, ce qui évite les blocages de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fa700-155">[**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) has the advantage of running on a background thread, and thereby avoids UI hangs.</span></span> <span data-ttu-id="fa700-156">Elle est beaucoup plus simple que [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="fa700-156">It is considerably simpler than [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> |



 

### <a name="discouraged-dynamic-verb-methods"></a><span data-ttu-id="fa700-157">Méthodes de verbe dynamique déconseillées</span><span class="sxs-lookup"><span data-stu-id="fa700-157">Discouraged Dynamic Verb Methods</span></span>

<span data-ttu-id="fa700-158">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) est la méthode la plus simple, mais également la plus compliquée à implémenter.</span><span class="sxs-lookup"><span data-stu-id="fa700-158">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated method to implement.</span></span> <span data-ttu-id="fa700-159">Il est basé sur des objets COM in-process qui s’exécutent sur le thread de l’appelant, qui est généralement l’Explorateur Windows, mais peut être n’importe quelle application hébergeant les éléments.</span><span class="sxs-lookup"><span data-stu-id="fa700-159">It is based on in-process COM objects that run on the thread of the caller, which usually Windows Explorer but can be any application hosting the items.</span></span> <span data-ttu-id="fa700-160">**IContextMenu** prend en charge la visibilité des verbes, le classement et le dessin personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fa700-160">**IContextMenu** supports verb visibility, ordering, and custom drawing.</span></span> <span data-ttu-id="fa700-161">Certaines de ces fonctionnalités ont été ajoutées aux fonctionnalités de verbe statique, telles qu’une icône à associer à une commande, et [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) pour gérer la visibilité.</span><span class="sxs-lookup"><span data-stu-id="fa700-161">Some of these features have been added to the static verb features, such as an icon to be associated with a command, and [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) to deal with visibility.</span></span>

<span data-ttu-id="fa700-162">Si vous devez étendre le menu contextuel d’un type de fichier en inscrivant un verbe dynamique pour le type de fichier, suivez les instructions fournies dans [Personnalisation d’un menu contextuel à l’aide de verbes dynamiques](shortcut-menu-using-dynamic-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="fa700-162">If you must extend the shortcut menu for a file type by registering a dynamic verb for the file type, then follow the instructions provided in [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

## <a name="extend-a-shortcut-menu"></a><span data-ttu-id="fa700-163">Étendre un menu contextuel</span><span class="sxs-lookup"><span data-stu-id="fa700-163">Extend a Shortcut Menu</span></span>

<span data-ttu-id="fa700-164">Une fois que vous avez choisi une méthode de verbe, vous pouvez étendre un menu contextuel pour un type de fichier en inscrivant un verbe statique pour le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fa700-164">After you choose a verb method you can extend a shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="fa700-165">Pour plus d’informations, consultez [création de gestionnaires de menus contextuels](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="fa700-165">For more information, see [Creating Context Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="support-for-verb-methods-by-operating-system"></a><span data-ttu-id="fa700-166">Prise en charge des méthodes de verbe par système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="fa700-166">Support for Verb Methods by Operating System</span></span>

<span data-ttu-id="fa700-167">La prise en charge des méthodes d’appel de verbe par système d’exploitation est répertoriée dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fa700-167">Support for verb invocation methods by operating system are listed in the following table.</span></span>



|                      |            |               |                      |
|----------------------|------------|---------------|----------------------|
|                      | <span data-ttu-id="fa700-168">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fa700-168">Windows XP</span></span> | <span data-ttu-id="fa700-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa700-169">Windows Vista</span></span> | <span data-ttu-id="fa700-170">Windows 7 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="fa700-170">Windows 7 and beyond</span></span> |
| <span data-ttu-id="fa700-171">CreateProcess</span><span class="sxs-lookup"><span data-stu-id="fa700-171">CreateProcess</span></span>        | <span data-ttu-id="fa700-172">X</span><span class="sxs-lookup"><span data-stu-id="fa700-172">X</span></span>          | <span data-ttu-id="fa700-173">X</span><span class="sxs-lookup"><span data-stu-id="fa700-173">X</span></span>             | <span data-ttu-id="fa700-174">X</span><span class="sxs-lookup"><span data-stu-id="fa700-174">X</span></span>                    |
| <span data-ttu-id="fa700-175">DDE</span><span class="sxs-lookup"><span data-stu-id="fa700-175">DDE</span></span>                  | <span data-ttu-id="fa700-176">X</span><span class="sxs-lookup"><span data-stu-id="fa700-176">X</span></span>          | <span data-ttu-id="fa700-177">X</span><span class="sxs-lookup"><span data-stu-id="fa700-177">X</span></span>             | <span data-ttu-id="fa700-178">X</span><span class="sxs-lookup"><span data-stu-id="fa700-178">X</span></span>                    |
| <span data-ttu-id="fa700-179">DropTarget</span><span class="sxs-lookup"><span data-stu-id="fa700-179">DropTarget</span></span>           | <span data-ttu-id="fa700-180">X</span><span class="sxs-lookup"><span data-stu-id="fa700-180">X</span></span>          | <span data-ttu-id="fa700-181">X</span><span class="sxs-lookup"><span data-stu-id="fa700-181">X</span></span>             | <span data-ttu-id="fa700-182">X</span><span class="sxs-lookup"><span data-stu-id="fa700-182">X</span></span>                    |
| <span data-ttu-id="fa700-183">ExecuteCommand</span><span class="sxs-lookup"><span data-stu-id="fa700-183">ExecuteCommand</span></span>       |            | <span data-ttu-id="fa700-184">X</span><span class="sxs-lookup"><span data-stu-id="fa700-184">X</span></span>             | <span data-ttu-id="fa700-185">X</span><span class="sxs-lookup"><span data-stu-id="fa700-185">X</span></span>                    |
| <span data-ttu-id="fa700-186">ExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="fa700-186">ExplorerCommand</span></span>      |            |               | <span data-ttu-id="fa700-187">X</span><span class="sxs-lookup"><span data-stu-id="fa700-187">X</span></span>                    |
| <span data-ttu-id="fa700-188">ExplorerCommandState</span><span class="sxs-lookup"><span data-stu-id="fa700-188">ExplorerCommandState</span></span> |            |               | <span data-ttu-id="fa700-189">X</span><span class="sxs-lookup"><span data-stu-id="fa700-189">X</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="fa700-190">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fa700-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa700-191">Meilleures pratiques pour les gestionnaires de menus contextuels et les verbes de sélection multiple</span><span class="sxs-lookup"><span data-stu-id="fa700-191">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="fa700-192">Création de gestionnaires de menu contextuel</span><span class="sxs-lookup"><span data-stu-id="fa700-192">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
</dt> <dt>

[<span data-ttu-id="fa700-193">Personnalisation d’un menu contextuel à l’aide de verbes dynamiques</span><span class="sxs-lookup"><span data-stu-id="fa700-193">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="fa700-194">Menus contextuels (menu contextuel) et gestionnaires de menus contextuels</span><span class="sxs-lookup"><span data-stu-id="fa700-194">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="fa700-195">Référence du menu contextuel</span><span class="sxs-lookup"><span data-stu-id="fa700-195">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> <dt>

[<span data-ttu-id="fa700-196">Verbes et associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="fa700-196">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> </dl>

 

 
