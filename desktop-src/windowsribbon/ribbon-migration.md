---
title: Migration vers l’infrastructure de ruban Windows
description: Une application qui s’appuie sur des menus, des barres d’outils et des boîtes de dialogue traditionnels peut être migrée vers l’interface utilisateur riche, dynamique et basée sur le contexte du système de commandes de l’infrastructure de ruban Windows.
ms.assetid: 3a8ca41e-18b3-4c9d-865b-5f4c5fcf7ceb
keywords:
- Ruban Windows, migration vers
- Ruban, migration vers
- migration vers le ruban Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74822781f891815c6eb30d9e15a7f7efaa983fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463383"
---
# <a name="migrating-to-the-windows-ribbon-framework"></a><span data-ttu-id="4ffe6-106">Migration vers l’infrastructure de ruban Windows</span><span class="sxs-lookup"><span data-stu-id="4ffe6-106">Migrating to the Windows Ribbon Framework</span></span>

<span data-ttu-id="4ffe6-107">Une application qui s’appuie sur des menus, des barres d’outils et des boîtes de dialogue traditionnels peut être migrée vers l’interface utilisateur riche, dynamique et basée sur le contexte du système de commandes de l’infrastructure de ruban Windows.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-107">An application that relies on traditional menus, toolbars, and dialogs can be migrated to the rich, dynamic, and context-driven UI of the Windows Ribbon framework Command system.</span></span> <span data-ttu-id="4ffe6-108">Il s’agit d’un moyen simple et efficace de moderniser et de revitaliser l’application tout en améliorant également l’accessibilité, la convivialité et la détectabilité de ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-108">This is an easy and effective way to modernize and revitalize the application while also improving the accessibility, usability, and discoverability of its functionality.</span></span>

## <a name="introduction"></a><span data-ttu-id="4ffe6-109">Introduction</span><span class="sxs-lookup"><span data-stu-id="4ffe6-109">Introduction</span></span>

<span data-ttu-id="4ffe6-110">En général, la migration d’une application existante vers l’infrastructure du ruban implique les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="4ffe6-110">In general, migrating an existing application to the Ribbon framework involves the following:</span></span>

-   <span data-ttu-id="4ffe6-111">Conception d’une disposition de ruban et d’une organisation de contrôle qui expose les fonctionnalités de l’application existante et est suffisamment flexible pour prendre en charge les nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-111">Designing a Ribbon layout and control organization that exposes the functionality of the existing application and is flexible enough to support new functionality.</span></span>
-   <span data-ttu-id="4ffe6-112">Adaptation du code de l’application existante.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-112">Adapting the code of the existing application.</span></span>
-   <span data-ttu-id="4ffe6-113">Migration des ressources d’application existantes (chaînes et images) vers l’infrastructure du ruban.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-113">Migrating existing application resources (strings and images) to the Ribbon framework.</span></span>

> [!Note]  
> <span data-ttu-id="4ffe6-114">Les [instructions relatives à l’expérience utilisateur du ruban](https://msdn.microsoft.com/library/cc872782.aspx) doivent être examinées pour déterminer si l’application est un candidat approprié pour une interface ruban.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-114">The [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx) should be reviewed to determine if the application is a suitable candidate for a Ribbon UI.</span></span>

 

## <a name="design-the-ribbon-layout"></a><span data-ttu-id="4ffe6-115">Concevoir la disposition du ruban</span><span class="sxs-lookup"><span data-stu-id="4ffe6-115">Design the Ribbon Layout</span></span>

<span data-ttu-id="4ffe6-116">Les conceptions de l’interface utilisateur du ruban et les dispositions de contrôle potentielles peuvent être identifiées en effectuant les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4ffe6-116">Potential Ribbon UI designs and control layouts can be identified by performing these steps:</span></span>

1.  <span data-ttu-id="4ffe6-117">En effectuant l’inventaire de toutes les fonctionnalités existantes.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-117">Taking inventory of all existing functionality.</span></span>
2.  <span data-ttu-id="4ffe6-118">Conversion de cette fonctionnalité en commandes de ruban.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-118">Translating this functionality into Ribbon Commands.</span></span>
3.  <span data-ttu-id="4ffe6-119">Organisation des commandes en groupes logiques.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-119">Organizing the Commands into logical groups.</span></span>

### <a name="take-inventory"></a><span data-ttu-id="4ffe6-120">Effectuer un inventaire</span><span class="sxs-lookup"><span data-stu-id="4ffe6-120">Take Inventory</span></span>

<span data-ttu-id="4ffe6-121">Dans l’infrastructure du ruban, la fonctionnalité exposée par une application qui manipule l’État ou la vue d’un espace de travail ou d’un document est considérée comme une commande.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-121">In the Ribbon framework, the functionality exposed by an application that manipulates the state or the view of a workspace or document is considered a command.</span></span> <span data-ttu-id="4ffe6-122">Ce qui constitue une commande peut varier et dépend de la nature et du domaine de l’application existante.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-122">What constitutes a command may vary and depends on the nature and domain of the existing application.</span></span>

<span data-ttu-id="4ffe6-123">Le tableau suivant répertorie un ensemble de commandes de base pour une application hypothétique de modification de texte :</span><span class="sxs-lookup"><span data-stu-id="4ffe6-123">The following table lists a set of basic commands for a hypothetical text editing application:</span></span>



| <span data-ttu-id="4ffe6-124">Symbole</span><span class="sxs-lookup"><span data-stu-id="4ffe6-124">Symbol</span></span>           | <span data-ttu-id="4ffe6-125">id</span><span class="sxs-lookup"><span data-stu-id="4ffe6-125">ID</span></span>     | <span data-ttu-id="4ffe6-126">Description</span><span class="sxs-lookup"><span data-stu-id="4ffe6-126">Description</span></span>               |
|------------------|--------|---------------------------|
| <span data-ttu-id="4ffe6-127">fichier d’ID \_ \_ nouveau</span><span class="sxs-lookup"><span data-stu-id="4ffe6-127">ID\_FILE\_NEW</span></span>    | <span data-ttu-id="4ffe6-128">0xE100</span><span class="sxs-lookup"><span data-stu-id="4ffe6-128">0xE100</span></span> | <span data-ttu-id="4ffe6-129">Nouveau document</span><span class="sxs-lookup"><span data-stu-id="4ffe6-129">New document</span></span>              |
| <span data-ttu-id="4ffe6-130">\_enregistrement du fichier d’ID \_</span><span class="sxs-lookup"><span data-stu-id="4ffe6-130">ID\_FILE\_SAVE</span></span>   | <span data-ttu-id="4ffe6-131">0xE103</span><span class="sxs-lookup"><span data-stu-id="4ffe6-131">0xE103</span></span> | <span data-ttu-id="4ffe6-132">Enregistrer le document</span><span class="sxs-lookup"><span data-stu-id="4ffe6-132">Save document</span></span>             |
| <span data-ttu-id="4ffe6-133">\_enregistrement du fichier d’ID \_</span><span class="sxs-lookup"><span data-stu-id="4ffe6-133">ID\_FILE\_SAVEAS</span></span> | <span data-ttu-id="4ffe6-134">0xE104</span><span class="sxs-lookup"><span data-stu-id="4ffe6-134">0xE104</span></span> | <span data-ttu-id="4ffe6-135">Enregistrer sous... dialogue</span><span class="sxs-lookup"><span data-stu-id="4ffe6-135">Save As... (dialog)</span></span>       |
| <span data-ttu-id="4ffe6-136">fichier d’ID \_ \_ ouvert</span><span class="sxs-lookup"><span data-stu-id="4ffe6-136">ID\_FILE\_OPEN</span></span>   | <span data-ttu-id="4ffe6-137">0xE101</span><span class="sxs-lookup"><span data-stu-id="4ffe6-137">0xE101</span></span> | <span data-ttu-id="4ffe6-138">Ouvrir... dialogue</span><span class="sxs-lookup"><span data-stu-id="4ffe6-138">Open... (dialog)</span></span>          |
| <span data-ttu-id="4ffe6-139">\_sortie du fichier d’ID \_</span><span class="sxs-lookup"><span data-stu-id="4ffe6-139">ID\_FILE\_EXIT</span></span>   | <span data-ttu-id="4ffe6-140">0xE102</span><span class="sxs-lookup"><span data-stu-id="4ffe6-140">0xE102</span></span> | <span data-ttu-id="4ffe6-141">Quitter l’application</span><span class="sxs-lookup"><span data-stu-id="4ffe6-141">Exit the application</span></span>      |
| <span data-ttu-id="4ffe6-142">\_annuler la modification de l’ID \_</span><span class="sxs-lookup"><span data-stu-id="4ffe6-142">ID\_EDIT\_UNDO</span></span>   | <span data-ttu-id="4ffe6-143">0xE12B</span><span class="sxs-lookup"><span data-stu-id="4ffe6-143">0xE12B</span></span> | <span data-ttu-id="4ffe6-144">Annuler</span><span class="sxs-lookup"><span data-stu-id="4ffe6-144">Undo</span></span>                      |
| <span data-ttu-id="4ffe6-145">modifier l’ID \_ \_ couper</span><span class="sxs-lookup"><span data-stu-id="4ffe6-145">ID\_EDIT\_CUT</span></span>    | <span data-ttu-id="4ffe6-146">0xE123</span><span class="sxs-lookup"><span data-stu-id="4ffe6-146">0xE123</span></span> | <span data-ttu-id="4ffe6-147">Couper le texte sélectionné</span><span class="sxs-lookup"><span data-stu-id="4ffe6-147">Cut selected text</span></span>         |
| <span data-ttu-id="4ffe6-148">copier l’ID \_ \_</span><span class="sxs-lookup"><span data-stu-id="4ffe6-148">ID\_EDIT\_COPY</span></span>   | <span data-ttu-id="4ffe6-149">0xE122</span><span class="sxs-lookup"><span data-stu-id="4ffe6-149">0xE122</span></span> | <span data-ttu-id="4ffe6-150">Copier le texte sélectionné</span><span class="sxs-lookup"><span data-stu-id="4ffe6-150">Copy selected text</span></span>        |
| <span data-ttu-id="4ffe6-151">édition de l’ID- \_ \_ coller</span><span class="sxs-lookup"><span data-stu-id="4ffe6-151">ID\_EDIT\_PASTE</span></span>  | <span data-ttu-id="4ffe6-152">0xE125</span><span class="sxs-lookup"><span data-stu-id="4ffe6-152">0xE125</span></span> | <span data-ttu-id="4ffe6-153">Coller le texte à partir du presse-papiers</span><span class="sxs-lookup"><span data-stu-id="4ffe6-153">Paste text from clipboard</span></span> |
| <span data-ttu-id="4ffe6-154">modification d’ID \_ \_ Effacer</span><span class="sxs-lookup"><span data-stu-id="4ffe6-154">ID\_EDIT\_CLEAR</span></span>  | <span data-ttu-id="4ffe6-155">0xE120</span><span class="sxs-lookup"><span data-stu-id="4ffe6-155">0xE120</span></span> | <span data-ttu-id="4ffe6-156">Supprimer le texte sélectionné</span><span class="sxs-lookup"><span data-stu-id="4ffe6-156">Delete selected text</span></span>      |
| <span data-ttu-id="4ffe6-157">ZOOM de la vue d’ID \_ \_</span><span class="sxs-lookup"><span data-stu-id="4ffe6-157">ID\_VIEW\_ZOOM</span></span>   | <span data-ttu-id="4ffe6-158">1242</span><span class="sxs-lookup"><span data-stu-id="4ffe6-158">1242</span></span>   | <span data-ttu-id="4ffe6-159">Zoom... dialogue</span><span class="sxs-lookup"><span data-stu-id="4ffe6-159">Zoom... (dialog)</span></span>          |



 

<span data-ttu-id="4ffe6-160">Regardez au-delà des menus et des barres d’outils existants lors de la création d’un inventaire des commandes.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-160">Look beyond existing menus and toolbars when building an inventory of commands.</span></span> <span data-ttu-id="4ffe6-161">Prenez en compte toutes les façons dont un utilisateur peut interagir avec l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-161">Consider all the ways a user can interact with the workspace.</span></span> <span data-ttu-id="4ffe6-162">Même si toutes les commandes ne conviennent pas à l’inclusion dans le ruban, cet exercice peut très bien exposer des commandes qui ont été masquées par des couches d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-162">Even though not every command is suitable for inclusion in the Ribbon, this exercise may very well expose commands that were previously obscured by layers of UI.</span></span>

### <a name="translate"></a><span data-ttu-id="4ffe6-163">Translate</span><span class="sxs-lookup"><span data-stu-id="4ffe6-163">Translate</span></span>

<span data-ttu-id="4ffe6-164">Toutes les commandes ne doivent pas être représentées dans l’interface ruban.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-164">Not every command needs to be represented in the Ribbon UI.</span></span> <span data-ttu-id="4ffe6-165">Par exemple, en entrant du texte, en modifiant une sélection, en faisant défiler ou en déplaçant le point d’insertion avec les commandes de la souris toutes éligibles dans l’éditeur de texte hypothétique, toutefois, celles-ci ne conviennent pas à l’exposition dans une barre de commandes, car chacune implique une interaction directe avec l’interface utilisateur de l’application.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-165">For example, entering text, changing a selection, scrolling, or moving the insertion-point with the mouse all qualify as commands in the hypothetical text editor, however, these are not suitable to expose in a command bar as each involves a direct interaction with the UI of the application.</span></span>

<span data-ttu-id="4ffe6-166">À l’inverse, certaines fonctionnalités peuvent ne pas être considérées comme une commande dans le sens traditionnel.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-166">Conversely, some functionality may not be thought of as a command in the traditional sense.</span></span> <span data-ttu-id="4ffe6-167">Par exemple, au lieu d’être enfoui dans une boîte de dialogue, les réglages de marge de page de l’imprimante peuvent être représentés dans le ruban sous la forme d’un groupe de contrôles Spinner dans un onglet contextuel ou [en mode application](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="4ffe6-167">For example, instead of being buried in a dialog box, printer page-margin adjustments could be represented in the Ribbon as a group of Spinner controls in a contextual tab or [application mode](ribbon-applicationmodes.md).</span></span>

> [!Note]  
> <span data-ttu-id="4ffe6-168">Prenez note de l’ID numérique qui peut être assigné à chaque commande.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-168">Make note of the numeric ID that may be assigned to each command.</span></span> <span data-ttu-id="4ffe6-169">Certaines infrastructures d’interface utilisateur, telles que Microsoft Foundation Classes (MFC), définissent des ID pour les commandes telles que le menu fichier et Edition (0xE100 à 0xE200).</span><span class="sxs-lookup"><span data-stu-id="4ffe6-169">Some UI frameworks, such as Microsoft Foundation Classes (MFC), define IDs for commands such as the file and edit menu (0xE100 to 0xE200).</span></span>

 

### <a name="organize"></a><span data-ttu-id="4ffe6-170">Organiser</span><span class="sxs-lookup"><span data-stu-id="4ffe6-170">Organize</span></span>

<span data-ttu-id="4ffe6-171">Avant de tenter d’organiser l’inventaire des commandes, les recommandations relatives à l' [expérience utilisateur du ruban](https://msdn.microsoft.com/library/cc872782.aspx) doivent être examinées pour connaître les meilleures pratiques lors de l’implémentation d’une interface utilisateur du ruban.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-171">Before attempting to organize the command inventory, the [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx) should be reviewed for best practices when implementing a Ribbon UI.</span></span>

<span data-ttu-id="4ffe6-172">En général, les règles suivantes peuvent être appliquées à l’Organisation des commandes du ruban :</span><span class="sxs-lookup"><span data-stu-id="4ffe6-172">In general, the following rules can be applied to Ribbon Command organization:</span></span>

-   <span data-ttu-id="4ffe6-173">Les commandes qui opèrent sur le fichier ou l’application globale appartiennent très probablement au menu de l' [application](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="4ffe6-173">Commands that operate on the file or the overall application most likely belong in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>
-   <span data-ttu-id="4ffe6-174">Les commandes fréquemment utilisées, telles que couper, copier et coller (comme dans l’exemple de l’éditeur de texte), sont généralement placées sur un onglet de démarrage par défaut. Dans les applications plus complexes, elles peuvent être dupliquées ailleurs dans l’interface ruban.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-174">Frequently used Commands such as Cut, Copy, and Paste (as in the text editor example) are typically placed on a default home tab. In more complex applications, they may be duplicated elsewhere in the Ribbon UI.</span></span>
-   <span data-ttu-id="4ffe6-175">Les commandes importantes ou fréquemment utilisées peuvent garantir l’inclusion par défaut dans la [barre d’outils accès rapide](windowsribbon-controls-quickaccesstoolbar.md).</span><span class="sxs-lookup"><span data-stu-id="4ffe6-175">Important or frequently used Commands might warrant default inclusion in the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="4ffe6-176">L’infrastructure du ruban fournit également des contrôles ContextMenu et MiniToolbar via la vue ContextPopup.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-176">The Ribbon framework also provides ContextMenu and MiniToolbar controls through the ContextPopup View.</span></span> <span data-ttu-id="4ffe6-177">Ces fonctionnalités ne sont pas obligatoires, mais si votre application possède un ou plusieurs menus contextuels existants, la migration des commandes qu’elles contiennent peut permettre la réutilisation du code base existant avec une liaison automatique avec les ressources existantes.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-177">These features are not mandatory, but if your application has one or more existing context menus then migrating the commands they contain may allow the reuse of the existing codebase with automatic binding to existing resources.</span></span>

<span data-ttu-id="4ffe6-178">Étant donné que chaque application est différente, lisez les instructions et essayez de les appliquer dans la mesure du possible.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-178">Because every application is different, read the guidelines and try to apply them to the fullest extent possible.</span></span> <span data-ttu-id="4ffe6-179">L’un des objectifs de l’infrastructure du ruban est de fournir une expérience utilisateur familière et cohérente. cet objectif sera plus réalisable si les conceptions de nouvelles applications reflètent le plus possible les applications de ruban existantes.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-179">One of the goals of the Ribbon framework is to provide a familiar, consistent user experience and this goal will be more achievable if designs for new applications mirror existing Ribbon applications as much as possible.</span></span>

## <a name="adapt-your-code"></a><span data-ttu-id="4ffe6-180">Adapter votre code</span><span class="sxs-lookup"><span data-stu-id="4ffe6-180">Adapt Your Code</span></span>

<span data-ttu-id="4ffe6-181">Une fois que les commandes de ruban ont été identifiées et organisées en regroupements logiques, le nombre d’étapes impliquées dans l’incorporation de l’infrastructure du ruban dans le code d’application existant dépend de la complexité de l’application d’origine.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-181">Once the Ribbon Commands have been identified and organized into logical groupings, the number of steps involved when incorporating the Ribbon framework into existing application code depends on the complexity of the original application.</span></span> <span data-ttu-id="4ffe6-182">En général, il existe trois étapes de base :</span><span class="sxs-lookup"><span data-stu-id="4ffe6-182">In general, there are three basic steps:</span></span>

-   <span data-ttu-id="4ffe6-183">Créez le balisage du ruban en fonction de l’organisation de la commande et de la spécification de la disposition.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-183">Create the Ribbon markup based on the Command organization and layout specification.</span></span>
-   <span data-ttu-id="4ffe6-184">Remplacez les fonctionnalités de menu et de barre d’outils héritées par la fonctionnalité du ruban.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-184">Replace legacy menu and toolbar functionality with Ribbon functionality.</span></span>
-   <span data-ttu-id="4ffe6-185">Implémentez un adaptateur IUICommandHandler.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-185">Implement an IUICommandHandler adapter.</span></span>

### <a name="create-the-markup"></a><span data-ttu-id="4ffe6-186">Créer le balisage</span><span class="sxs-lookup"><span data-stu-id="4ffe6-186">Create The Markup</span></span>

<span data-ttu-id="4ffe6-187">La liste des commandes, ainsi que leur organisation et leur disposition, sont déclarées par le biais du fichier de balisage du ruban qui est consommé par le [compilateur de balisage du ruban](windowsribbon-intentcl.md).</span><span class="sxs-lookup"><span data-stu-id="4ffe6-187">The list of commands as well as their organization and layout are declared through the Ribbon markup file which is consumed by the [Ribbon markup compiler](windowsribbon-intentcl.md).</span></span>

> [!Note]  
> <span data-ttu-id="4ffe6-188">La plupart des étapes requises pour adapter une application existante sont similaires à celles requises pour démarrer une nouvelle application ruban.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-188">Many of the steps required to adapt an existing application are similar to those required to start a new Ribbon application.</span></span> <span data-ttu-id="4ffe6-189">Pour plus d’informations, consultez le didacticiel [création d’une application de ruban](windowsribbon-stepbystep.md) pour une nouvelle application ruban.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-189">For more information, see the [Creating a Ribbon Application](windowsribbon-stepbystep.md) tutorial for a new Ribbon application walkthrough.</span></span>

 

<span data-ttu-id="4ffe6-190">Il existe deux sections principales pour le balisage du ruban.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-190">There are two primary sections to the Ribbon markup.</span></span> <span data-ttu-id="4ffe6-191">La première section est un manifeste de commandes et les ressources associées (chaînes et images).</span><span class="sxs-lookup"><span data-stu-id="4ffe6-191">The first section is a manifest of Commands and their associated resources (strings and images).</span></span> <span data-ttu-id="4ffe6-192">La deuxième section spécifie la structure et le positionnement des contrôles sur le ruban.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-192">The second section specifies the structure and placement of controls on the Ribbon.</span></span>

<span data-ttu-id="4ffe6-193">Le balisage de l’éditeur de texte simple peut se présenter comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="4ffe6-193">The markup for the simple text editor might look something like the following example:</span></span>

> [!Note]  
> <span data-ttu-id="4ffe6-194">Les ressources de type image et chaîne sont traitées plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-194">Image and string resources are covered later in this article.</span></span>

 


```C++
<?xml version="1.0" encoding="utf-8"?>
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">

  <Application.Commands>
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" />
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" />
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" />
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" />
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" />
    <Command Name="cmdUndo" Id="0xE12B" Symbol="ID_CMD_UNDO" LabelTitle="Undo" />
    <Command Name="cmdCut" Id="0xE123" Symbol="ID_CMD_CUT" LabelTitle="Cut" />
    <Command Name="cmdCopy" Id="0xE122" Symbol="ID_CMD_COPY" LabelTitle="Copy" />
    <Command Name="cmdPaste" Id="0xE125" Symbol="ID_CMD_PASTE" LabelTitle="Paste" />
    <Command Name="cmdDelete" Id="0xE120" Symbol="ID_CMD_DELETE" LabelTitle="Delete" />
    <Command Name="cmdZoom" Id="1242" Symbol="ID_CMD_ZOOM" LabelTitle="Zoom" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.ApplicationMenu>
        <ApplicationMenu>
          <MenuGroup>
            <Button CommandName="cmdNew" />
            <Button CommandName="cmdOpen" />
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdSaveAs" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdExit" />
          </MenuGroup>
        </ApplicationMenu>
      </Ribbon.ApplicationMenu>
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar>
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdUndo" />
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
      <Ribbon.Tabs>
        <Tab>
          <Group CommandName="grpClipboard" SizeDefinition="FourButtons">
            <Button CommandName="cmdPaste" />
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdDelete" />
          </Group>
        </Tab>
        <Tab>
          <Group CommandName="grpView" SizeDefinition="OneButton">
            <Button CommandName="cmdZoom" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>

</Application>
```



<span data-ttu-id="4ffe6-195">Pour éviter de redéfinir des symboles définis par une infrastructure d’interface utilisateur telle que MFC, l’exemple précédent utilise des noms de symboles légèrement différents pour chaque commande (fichier d’ID \_ \_ nouveau et ID \_ cmd \_ New).</span><span class="sxs-lookup"><span data-stu-id="4ffe6-195">To avoid redefining symbols that are defined by a UI framework such as MFC, the previous example uses slightly different symbol names for each Command (ID\_FILE\_NEW versus ID\_CMD\_NEW).</span></span> <span data-ttu-id="4ffe6-196">Toutefois, l’ID numérique affecté à chaque commande doit rester le même.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-196">However, the numeric ID assigned to each Command must remain the same.</span></span>

<span data-ttu-id="4ffe6-197">Pour intégrer le fichier de balisage dans une application, configurez une étape de génération personnalisée pour exécuter le compilateur de balisage du ruban, UICC.exe.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-197">To integrate the markup file into an application, configure a custom build step to run the Ribbon markup compiler, UICC.exe.</span></span> <span data-ttu-id="4ffe6-198">L’en-tête et les fichiers de ressources qui en résultent sont ensuite incorporés dans le projet existant.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-198">The resulting header and resource files are then incorporated into the existing project.</span></span> <span data-ttu-id="4ffe6-199">Si l’exemple d’application de ruban de l’éditeur de texte est nommé « RibbonPad », une ligne de commande de génération personnalisée semblable à la suivante est requise :</span><span class="sxs-lookup"><span data-stu-id="4ffe6-199">If the example text editor Ribbon application is named "RibbonPad", a custom-build command line similar to the following is required:</span></span>


```
UICC.exe res\RibbonPad_ribbon.xml res\RibbonPad_ribbon.bin 
         /header:res\RibbonPad_ribbon.h /res:res\RibbonPad_ribbon.rc2
```



<span data-ttu-id="4ffe6-200">Le compilateur de balisage crée un fichier binaire, un fichier d’en-tête (H) et un fichier de ressources (RC).</span><span class="sxs-lookup"><span data-stu-id="4ffe6-200">The markup compiler creates a binary file, a header (H) file and a resource (RC) file.</span></span> <span data-ttu-id="4ffe6-201">Étant donné que l’application existante a probablement un fichier RC existant, incluez les fichiers. RC et RC générés dans ce fichier RC, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="4ffe6-201">Because the existing application likely has an existing RC file, include the generated H and RC files in that RC file, as shown in the following example:</span></span>


```C++
#ifndef APSTUDIO_INVOKED
/////////////////////////////////////////////////////////////////////////////
//
// Generated from the TEXTINCLUDE 3 resource.
//

#define _AFX_NO_SPLITTER_RESOURCES
#define _AFX_NO_OLE_RESOURCES
#define _AFX_NO_TRACKER_RESOURCES
#define _AFX_NO_PROPERTY_RESOURCES

#if !defined(AFX_RESOURCE_DLL) || defined(AFX_TARG_ENU)
LANGUAGE 9, 1
#pragma code_page(1252)

#include "res\RibbonPad_ribbon.h"  // Ribbon resources
#include "res\RibbonPad_ribbon.rc2"  // Ribbon resources

#include "res\RibbonPad.rc2"  // non-Microsoft Visual C++ edited resources
#include "afxres.rc"    // Standard components
#include "afxprint.rc"  // printing/print preview resources
#endif
#endif    // not APSTUDIO_INVOKED
```



### <a name="replace-legacy-menus-and-toolbars"></a><span data-ttu-id="4ffe6-202">Remplacer les menus et les barres d’outils hérités</span><span class="sxs-lookup"><span data-stu-id="4ffe6-202">Replace Legacy Menus and Toolbars</span></span>

<span data-ttu-id="4ffe6-203">Le remplacement des menus et barres d’outils standard par un ruban dans une application héritée requiert les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="4ffe6-203">Replacing standard menus and toolbars with a ribbon in a legacy application requires the following:</span></span>

1.  <span data-ttu-id="4ffe6-204">Supprimez les références de ressource de menu et de barre d’outils du fichier de ressources de l’application.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-204">Remove toolbar and menu resource references from the application's resource file.</span></span>
2.  <span data-ttu-id="4ffe6-205">Supprimez tout le code d’initialisation de la barre d’outils et de la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-205">Delete all toolbar and menu bar initialization code.</span></span>
3.  <span data-ttu-id="4ffe6-206">Supprimez tout code utilisé pour attacher une barre d’outils ou une barre de menus à la fenêtre de niveau supérieur de l’application.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-206">Delete any code used to attach a toolbar or menu bar to the top-level window of the application.</span></span>
4.  <span data-ttu-id="4ffe6-207">Instanciez l’infrastructure du ruban.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-207">Instantiate the Ribbon framework.</span></span>
5.  <span data-ttu-id="4ffe6-208">Attachez le ruban à la fenêtre de niveau supérieur de l’application.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-208">Attach the ribbon to the top-level window of the application.</span></span>
6.  <span data-ttu-id="4ffe6-209">Chargez le balisage compilé.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-209">Load the compiled markup.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4ffe6-210">La barre d’État et les tables de raccourcis clavier existantes doivent être conservées, car l’infrastructure du ruban ne remplace pas ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-210">Existing status bar and keyboard shortcut tables should be preserved as the Ribbon framework does not replace these features.</span></span>

 

<span data-ttu-id="4ffe6-211">L’exemple suivant montre comment initialiser l’infrastructure à l’aide de [**IUIFramework :: Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize):</span><span class="sxs-lookup"><span data-stu-id="4ffe6-211">The following example demonstrates how to initialize the framework using [**IUIFramework::Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize):</span></span>


```C++
int CMainFrame::OnCreate(LPCREATESTRUCT lpCreateStruct)
{
    if (CFrameWnd::OnCreate(lpCreateStruct) == -1)
        return -1;
    
    if (!m_RibbonBar.Create(this, WS_CHILD|WS_DISABLED|WS_VISIBLE|CBRS_TOP|CBRS_HIDE_INPLACE,0))
        return -1;      // fail to create

    if (!m_wndStatusBar.Create(this) || !m_wndStatusBar.SetIndicators(indicators,sizeof(indicators)/sizeof(UINT)))
        return -1;      // fail to create

    // Ribbon initialization
    InitRibbon(this, &m_spUIFramework);

    return 0;
}
```



<span data-ttu-id="4ffe6-212">L’exemple suivant montre comment utiliser [**IUIFramework :: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) pour charger le balisage compilé :</span><span class="sxs-lookup"><span data-stu-id="4ffe6-212">The following example demonstrates how to use [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) to load the compiled markup:</span></span>


```C++
HRESULT InitRibbon(CMainFrame* pMainFrame, IUnknown** ppFramework)
{
    // Create the IUIFramework instance.
    CComPtr<IUIFramework> spFramework;
    HRESULT hr = ::CoCreateInstance(CLSID_UIRibbonFramework, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&spFramework));
    if (FAILED(hr))
        return hr;
    
    // Instantiate the CApplication object.
    CComObject<CApplication>* pApplication;
    hr = CComObject<CApplication>::CreateInstance(&pApplication);   // Refcount is 0
    
    // Call AddRef on the CApplication object. The smart pointer will release the refcount when it is out of scope.
    CComPtr< CComObject<CApplication> > spApplication(pApplication);

    if (FAILED(hr))
        return hr;

    // Initialize and load the Ribbon.
    spApplication->Initialize(pMainFrame);

    hr = spFramework->Initialize(*pMainFrame, spApplication);
    if (FAILED(hr))
        return hr;

    hr = spFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
        return hr;

    // Return IUIFramework interface to the caller.
    hr = spFramework->QueryInterface(ppFramework);

    return hr;
}
```



<span data-ttu-id="4ffe6-213">La classe CApplication, référencée ci-dessus, doit implémenter une paire d’interfaces COM (Component Object Model) définies par l’infrastructure du ruban : [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) et [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler).</span><span class="sxs-lookup"><span data-stu-id="4ffe6-213">The CApplication class, referred to above, must implement a pair of Component Object Model (COM) interfaces defined by the Ribbon framework: [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) and [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler).</span></span>

<span data-ttu-id="4ffe6-214">[**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) fournit l’interface de rappel principale entre l’infrastructure et l’application (par exemple, la hauteur du ruban est communiquée par le biais de [**IUIApplication :: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)), tandis que les rappels pour les commandes individuelles sont fournis en réponse à [**IUIApplication :: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand).</span><span class="sxs-lookup"><span data-stu-id="4ffe6-214">[**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) provides the main callback interface between the framework and the application (for example, the height of the ribbon is communicated through [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)) while the callbacks for individual Commands are provided in response to [**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand).</span></span>

<span data-ttu-id="4ffe6-215">**Conseil :** Certaines infrastructures d’application, telles que MFC, requièrent que la hauteur de la barre de ruban soit prise en compte lors du rendu de l’espace de document de l’application.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-215">**Tip:** Some application frameworks, such as MFC, require that the height of the ribbon bar be taken into account when rendering the document space of the application.</span></span> <span data-ttu-id="4ffe6-216">Dans ce cas, l’ajout d’une fenêtre masquée pour superposer la barre du ruban et forcer l’espace du document à la hauteur souhaitée est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-216">In these cases, the addition of a hidden window to overlay the ribbon bar and force the document space to the desired height is necessary.</span></span> <span data-ttu-id="4ffe6-217">Pour obtenir un exemple de cette approche, où une fonction de disposition est appelée en fonction de la hauteur du ruban retournée par la méthode [**IUIRibbon :: GetHeight**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) , consultez l' [exemple HTMLEditRibbon](windowsribbon-htmleditribbonsample.md).</span><span class="sxs-lookup"><span data-stu-id="4ffe6-217">For an example of this approach, where a layout function is called based on the ribbon height returned by the [**IUIRibbon::GetHeight**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) method, see the [HTMLEditRibbon Sample](windowsribbon-htmleditribbonsample.md).</span></span>

<span data-ttu-id="4ffe6-218">L’exemple de code suivant illustre une implémentation de [**IUIApplication :: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) :</span><span class="sxs-lookup"><span data-stu-id="4ffe6-218">The following code example demonstrates an [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) implementation:</span></span>


```C++
// This is the Ribbon implementation that is done by an application.
// Applications have to implement IUIApplication and IUICommandHandler to set up communication with the Windows Ribbon.
class CApplication
    : public CComObjectRootEx<CComSingleThreadModel>
    , public IUIApplication
    , public IUICommandHandler
{
public:

    BEGIN_COM_MAP(CApplication)
        COM_INTERFACE_ENTRY(IUIApplication)
        COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    CApplication() : _pMainFrame(NULL)
    {
    }

    void Initialize(CMainFrame* pFrame)
    {
        // Hold a reference to the main frame.
        _pMainFrame = pFrame;
    }

    void FinalRelease()
    {
        // Release the reference.
        _pMainFrame = NULL;
        __super::FinalRelease();
    }

    STDMETHOD(OnViewChanged)(UINT32 nViewID, __in UI_VIEWTYPE typeID, __in IUnknown* pView, UI_VIEWVERB verb, INT32 uReasonCode)
    {
        HRESULT hr;

        // The Ribbon size has changed.
        if (verb == UI_VIEWVERB_SIZE)
        {
            CComQIPtr<IUIRibbon> pRibbon = pView;
            if (!pRibbon)
                return E_FAIL;

            UINT ulRibbonHeight;
            // Get the Ribbon height.
            hr = pRibbon->GetHeight(&ulRibbonHeight);
            if (FAILED(hr))
                return hr;

            // Update the Ribbon bar so that the main frame can recalculate the child layout.
            _pMainFrame->m_RibbonBar.SetRibbonHeight(ulRibbonHeight);
            _pMainFrame->RecalcLayout();
        }

        return S_OK;
    }

    STDMETHOD(OnCreateUICommand)(UINT32 nCmdID, 
                               __in UI_COMMANDTYPE typeID,
                               __deref_out IUICommandHandler** ppCommandHandler)
    {
        // This application uses one command handler for all ribbon commands.
        return QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }

    STDMETHOD(OnDestroyUICommand)(UINT32 commandId, __in UI_COMMANDTYPE typeID,  __in_opt  IUICommandHandler *commandHandler)
    {        
        return E_NOTIMPL;
    }

private:
    CMainFrame* _pMainFrame;
};
```



### <a name="implement-an-iuicommandhandler-adapter"></a><span data-ttu-id="4ffe6-219">Implémenter un adaptateur IUICommandHandler</span><span class="sxs-lookup"><span data-stu-id="4ffe6-219">Implement an IUICommandHandler Adapter</span></span>

<span data-ttu-id="4ffe6-220">Selon la conception de l’application d’origine, il peut être plus facile d’avoir plusieurs implémentations de gestionnaire de commandes, ou un gestionnaire de commandes de pontage unique qui appelle la logique de commande d’application existante.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-220">Depending on the design of the original application, it may be easier to have multiple Command handler implementations, or a single bridging Command handler that invokes the existing-application command logic.</span></span> <span data-ttu-id="4ffe6-221">De nombreuses applications utilisent \_ des messages de commande WM à cet effet, où il suffit de fournir un gestionnaire de commandes unique et polyvalent qui transfère simplement les \_ messages de commande WM à la fenêtre de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-221">Many applications use WM\_COMMAND messages for this purpose where it is sufficient to provide a single, all-purpose command handler that simply forwards WM\_COMMAND messages to the top-level window.</span></span>

<span data-ttu-id="4ffe6-222">Toutefois, cette approche nécessite un traitement spécial pour les commandes telles que **Exit** ou **Close**.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-222">However, this approach requires special handling for Commands such as **Exit** or **Close**.</span></span> <span data-ttu-id="4ffe6-223">Étant donné que le ruban ne peut pas être détruit pendant qu’il traite un message de fenêtre, le \_ message WM Close doit être publié dans le thread d’interface utilisateur de l’application et ne doit pas être traité de façon synchrone, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="4ffe6-223">Because the Ribbon cannot be destroyed while it's processing a window message, the WM\_CLOSE message should be posted to the UI thread of the application and should not be processed synchronously, as shown in the following example:</span></span>


```C++
// User action callback, with transient execution parameters.
    STDMETHODIMP Execute(UINT nCmdID,
        UI_EXECUTIONVERB verb, 
        __in_opt const PROPERTYKEY* key,
        __in_opt const PROPVARIANT* ppropvarValue,
        __in_opt IUISimplePropertySet* pCommandExecutionProperties)
    {       
        switch(nCmdID)
        {
        case cmdExit:
            ::PostMessage(*_pMainFrame, WM_CLOSE, nCmdID, 0);
            break;
        default:
            ::SendMessage(*_pMainFrame, WM_COMMAND, nCmdID, 0);
        }
        return S_OK;
    }

    STDMETHODIMP UpdateProperty(UINT32 nCmdID, 
                                __in REFPROPERTYKEY key,
                                __in_opt  const PROPVARIANT *currentValue,
                                __out PROPVARIANT *newValue) 
    {        
        return S_OK;
    }

```



## <a name="migrating-resources"></a><span data-ttu-id="4ffe6-224">Migration des ressources</span><span class="sxs-lookup"><span data-stu-id="4ffe6-224">Migrating Resources</span></span>

<span data-ttu-id="4ffe6-225">Quand le manifeste des commandes a été défini, que la structure du ruban a été déclarée et que le code de l’application est adapté pour héberger l’infrastructure du ruban, la dernière étape consiste à spécifier des ressources de type chaîne et image pour chaque commande.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-225">When the manifest of commands has been defined, the structure of the Ribbon has been declared, and the application code adapted to host the Ribbon framework, the final step is the specification of string and image resources for each Command.</span></span>

> [!Note]  
> <span data-ttu-id="4ffe6-226">Les ressources de type chaîne et image sont généralement fournies dans le fichier de balisage.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-226">String and image resources are typically provided in the markup file.</span></span> <span data-ttu-id="4ffe6-227">Toutefois, elles peuvent être générées ou remplacées par programme en implémentant la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="4ffe6-227">However, they can be generated or replaced programmatically by implementing the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

 

### <a name="string-resources"></a><span data-ttu-id="4ffe6-228">Ressources de type chaîne</span><span class="sxs-lookup"><span data-stu-id="4ffe6-228">String Resources</span></span>

<span data-ttu-id="4ffe6-229">[**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) est la propriété de chaîne la plus courante définie pour une commande.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-229">[**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) is the most common string property defined for a Command.</span></span> <span data-ttu-id="4ffe6-230">Ils sont rendus sous la forme d’étiquettes de texte pour les onglets, les groupes et les contrôles individuels.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-230">These are rendered as the text labels for tabs, groups, and individual controls.</span></span> <span data-ttu-id="4ffe6-231">Une chaîne d’étiquette d’un élément de menu hérité peut généralement être réutilisée pour une **commande. LabelTitle** sans modification importante.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-231">A label string from a legacy menu item can typically be re-used for a **Command.LabelTitle** without much editing.</span></span>

<span data-ttu-id="4ffe6-232">Toutefois, les conventions suivantes ont été modifiées avec l’avènement du ruban :</span><span class="sxs-lookup"><span data-stu-id="4ffe6-232">However, the following conventions have changed with the advent of the Ribbon:</span></span>

-   <span data-ttu-id="4ffe6-233">Le suffixe des points de suspension (...), utilisé pour indiquer une commande de lancement de dialogue, n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-233">The ellipsis (...) suffix, used to indicate a dialog-launching command, is no longer necessary.</span></span>
-   <span data-ttu-id="4ffe6-234">La esperluette (&) peut toujours être utilisée pour indiquer un raccourci clavier pour une commande qui s’affiche dans un menu, mais la propriété [**Command. KeyTip**](windowsribbon-element-command-keytip.md) prise en charge par l’infrastructure respecte un objectif similaire.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-234">The ampersand (&) can still be used to indicate a keyboard-shortcut for a Command that appears in a menu, but the [**Command.Keytip**](windowsribbon-element-command-keytip.md) property supported by the framework fulfills a similar purpose.</span></span>

<span data-ttu-id="4ffe6-235">En vous référant à l’exemple d’éditeur de texte, les chaînes suivantes pour LabelTitle et KeyTip peuvent être spécifiées :</span><span class="sxs-lookup"><span data-stu-id="4ffe6-235">Referring back to the text editor example, the following strings for LabelTitle and Keytip could be specified:</span></span>



| <span data-ttu-id="4ffe6-236">Symbole</span><span class="sxs-lookup"><span data-stu-id="4ffe6-236">Symbol</span></span>           | <span data-ttu-id="4ffe6-237">Chaîne d’origine</span><span class="sxs-lookup"><span data-stu-id="4ffe6-237">Original string</span></span> | <span data-ttu-id="4ffe6-238">Chaîne LabelTitle</span><span class="sxs-lookup"><span data-stu-id="4ffe6-238">LabelTitle string</span></span> | <span data-ttu-id="4ffe6-239">Chaîne de KeyTip</span><span class="sxs-lookup"><span data-stu-id="4ffe6-239">Keytip string</span></span> |
|------------------|-----------------|-------------------|---------------|
| <span data-ttu-id="4ffe6-240">fichier d’ID \_ \_ nouveau</span><span class="sxs-lookup"><span data-stu-id="4ffe6-240">ID\_FILE\_NEW</span></span>    | <span data-ttu-id="4ffe6-241">&nouveau</span><span class="sxs-lookup"><span data-stu-id="4ffe6-241">&New</span></span>            | <span data-ttu-id="4ffe6-242">&nouveau</span><span class="sxs-lookup"><span data-stu-id="4ffe6-242">&New</span></span>              | <span data-ttu-id="4ffe6-243">N</span><span class="sxs-lookup"><span data-stu-id="4ffe6-243">N</span></span>             |
| <span data-ttu-id="4ffe6-244">\_enregistrement du fichier d’ID \_</span><span class="sxs-lookup"><span data-stu-id="4ffe6-244">ID\_FILE\_SAVE</span></span>   | <span data-ttu-id="4ffe6-245">&enregistrer</span><span class="sxs-lookup"><span data-stu-id="4ffe6-245">&Save</span></span>           | <span data-ttu-id="4ffe6-246">&enregistrer</span><span class="sxs-lookup"><span data-stu-id="4ffe6-246">&Save</span></span>             | <span data-ttu-id="4ffe6-247">S</span><span class="sxs-lookup"><span data-stu-id="4ffe6-247">S</span></span>             |
| <span data-ttu-id="4ffe6-248">\_enregistrement du fichier d’ID \_</span><span class="sxs-lookup"><span data-stu-id="4ffe6-248">ID\_FILE\_SAVEAS</span></span> | <span data-ttu-id="4ffe6-249">Enregistrer &sous...</span><span class="sxs-lookup"><span data-stu-id="4ffe6-249">Save &As…</span></span>       | <span data-ttu-id="4ffe6-250">Enregistrer &sous</span><span class="sxs-lookup"><span data-stu-id="4ffe6-250">Save &as</span></span>          | <span data-ttu-id="4ffe6-251">Un</span><span class="sxs-lookup"><span data-stu-id="4ffe6-251">A</span></span>             |
| <span data-ttu-id="4ffe6-252">fichier d’ID \_ \_ ouvert</span><span class="sxs-lookup"><span data-stu-id="4ffe6-252">ID\_FILE\_OPEN</span></span>   | <span data-ttu-id="4ffe6-253">&ouvrir...</span><span class="sxs-lookup"><span data-stu-id="4ffe6-253">&Open…</span></span>          | <span data-ttu-id="4ffe6-254">&amp;Open</span><span class="sxs-lookup"><span data-stu-id="4ffe6-254">&Open</span></span>             | <span data-ttu-id="4ffe6-255">O</span><span class="sxs-lookup"><span data-stu-id="4ffe6-255">O</span></span>             |
| <span data-ttu-id="4ffe6-256">\_sortie du fichier d’ID \_</span><span class="sxs-lookup"><span data-stu-id="4ffe6-256">ID\_FILE\_EXIT</span></span>   | <span data-ttu-id="4ffe6-257">&Quitter</span><span class="sxs-lookup"><span data-stu-id="4ffe6-257">E&xit</span></span>           | <span data-ttu-id="4ffe6-258">&Quitter</span><span class="sxs-lookup"><span data-stu-id="4ffe6-258">E&xit</span></span>             | <span data-ttu-id="4ffe6-259">X</span><span class="sxs-lookup"><span data-stu-id="4ffe6-259">X</span></span>             |
| <span data-ttu-id="4ffe6-260">\_annuler la modification de l’ID \_</span><span class="sxs-lookup"><span data-stu-id="4ffe6-260">ID\_EDIT\_UNDO</span></span>   | <span data-ttu-id="4ffe6-261">&annuler</span><span class="sxs-lookup"><span data-stu-id="4ffe6-261">&Undo</span></span>           | <span data-ttu-id="4ffe6-262">Annuler</span><span class="sxs-lookup"><span data-stu-id="4ffe6-262">Undo</span></span>              | <span data-ttu-id="4ffe6-263">Z</span><span class="sxs-lookup"><span data-stu-id="4ffe6-263">Z</span></span>             |
| <span data-ttu-id="4ffe6-264">modifier l’ID \_ \_ couper</span><span class="sxs-lookup"><span data-stu-id="4ffe6-264">ID\_EDIT\_CUT</span></span>    | <span data-ttu-id="4ffe6-265">Cu&t</span><span class="sxs-lookup"><span data-stu-id="4ffe6-265">Cu&t</span></span>            | <span data-ttu-id="4ffe6-266">Cu&t</span><span class="sxs-lookup"><span data-stu-id="4ffe6-266">Cu&t</span></span>              | <span data-ttu-id="4ffe6-267">X</span><span class="sxs-lookup"><span data-stu-id="4ffe6-267">X</span></span>             |
| <span data-ttu-id="4ffe6-268">copier l’ID \_ \_</span><span class="sxs-lookup"><span data-stu-id="4ffe6-268">ID\_EDIT\_COPY</span></span>   | <span data-ttu-id="4ffe6-269">Copie &</span><span class="sxs-lookup"><span data-stu-id="4ffe6-269">&Copy</span></span>           | <span data-ttu-id="4ffe6-270">Copie &</span><span class="sxs-lookup"><span data-stu-id="4ffe6-270">&Copy</span></span>             | <span data-ttu-id="4ffe6-271">C</span><span class="sxs-lookup"><span data-stu-id="4ffe6-271">C</span></span>             |
| <span data-ttu-id="4ffe6-272">édition de l’ID- \_ \_ coller</span><span class="sxs-lookup"><span data-stu-id="4ffe6-272">ID\_EDIT\_PASTE</span></span>  | <span data-ttu-id="4ffe6-273">&coller</span><span class="sxs-lookup"><span data-stu-id="4ffe6-273">&Paste</span></span>          | <span data-ttu-id="4ffe6-274">&coller</span><span class="sxs-lookup"><span data-stu-id="4ffe6-274">&Paste</span></span>            | <span data-ttu-id="4ffe6-275">V</span><span class="sxs-lookup"><span data-stu-id="4ffe6-275">V</span></span>             |
| <span data-ttu-id="4ffe6-276">modification d’ID \_ \_ Effacer</span><span class="sxs-lookup"><span data-stu-id="4ffe6-276">ID\_EDIT\_CLEAR</span></span>  | <span data-ttu-id="4ffe6-277">&supprimer</span><span class="sxs-lookup"><span data-stu-id="4ffe6-277">&Delete</span></span>         | <span data-ttu-id="4ffe6-278">&supprimer</span><span class="sxs-lookup"><span data-stu-id="4ffe6-278">&Delete</span></span>           | <span data-ttu-id="4ffe6-279">D</span><span class="sxs-lookup"><span data-stu-id="4ffe6-279">D</span></span>             |
| <span data-ttu-id="4ffe6-280">ZOOM de la vue d’ID \_ \_</span><span class="sxs-lookup"><span data-stu-id="4ffe6-280">ID\_VIEW\_ZOOM</span></span>   | <span data-ttu-id="4ffe6-281">&zoom...</span><span class="sxs-lookup"><span data-stu-id="4ffe6-281">&Zoom…</span></span>          | <span data-ttu-id="4ffe6-282">Zoom</span><span class="sxs-lookup"><span data-stu-id="4ffe6-282">Zoom</span></span>              | <span data-ttu-id="4ffe6-283">Z</span><span class="sxs-lookup"><span data-stu-id="4ffe6-283">Z</span></span>             |



 

<span data-ttu-id="4ffe6-284">Voici une liste d’autres propriétés de chaîne qui doivent être définies sur la plupart des commandes :</span><span class="sxs-lookup"><span data-stu-id="4ffe6-284">The following is a list of other string properties which should be set on most Commands:</span></span>

-   [<span data-ttu-id="4ffe6-285">**Commande. LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="4ffe6-285">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)
-   [<span data-ttu-id="4ffe6-286">**Commande. TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="4ffe6-286">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)
-   [<span data-ttu-id="4ffe6-287">**Commande. TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="4ffe6-287">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)

<span data-ttu-id="4ffe6-288">Les onglets, les groupes et les autres fonctionnalités de l’interface utilisateur du ruban peuvent désormais être déclarés avec toutes les ressources de chaîne et d’image spécifiées.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-288">Tabs, Groups, and other Ribbon UI features can now be declared with all string and image resources specified.</span></span>

<span data-ttu-id="4ffe6-289">L’exemple de balisage de ruban suivant illustre différentes ressources de type chaîne :</span><span class="sxs-lookup"><span data-stu-id="4ffe6-289">The following Ribbon markup example demonstrates various string resources:</span></span>


```C++
<Application.Commands>
    <!-- Tabs -->
    <Command Name="tabHome" LabelTitle="Home" Keytip="H" />
    <Command Name="tabView" LabelTitle="View" Keytip="V" />

    <!-- Groups -->
    <Command Name="grpClipboard" LabelTitle="Clipboard" />
    <Command Name="grpZoom" LabelTitle="Zoom" />

    <!-- App menu commands -->
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" Keytip="S">
      <Command.TooltipTitle>Save (Ctrl+S)</Command.TooltipTitle>
      <Command.TooltipDescription>Save the current document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" Keytip="A">
      <Command.TooltipDescription>Save the current document with a new name.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" Keytip="O">
      <Command.TooltipTitle>Open (Ctrl+O)</Command.TooltipTitle>
      <Command.TooltipDescription>Open a document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" Keytip="X">
      <Command.TooltipDescription>Exit the application.</Command.TooltipDescription>
    </Command>

    <!-- ...other commands -->

  </Application.Commands>
```



### <a name="image-resources"></a><span data-ttu-id="4ffe6-290">Ressources d’image</span><span class="sxs-lookup"><span data-stu-id="4ffe6-290">Image Resources</span></span>

<span data-ttu-id="4ffe6-291">L’infrastructure du ruban prend en charge les formats d’image qui offrent une apparence beaucoup plus riche que les formats d’image pris en charge par les composants de menu et de barre d’outils précédents.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-291">The Ribbon framework supports image formats that provide a much richer look and feel than the image formats supported by previous menu and toolbar components.</span></span>

<span data-ttu-id="4ffe6-292">Pour Windows 8 et versions ultérieures, l’infrastructure du ruban prend en charge les formats graphiques suivants : fichiers BMP (bitmaps) 32 bits et fichiers PNG (Portable Network Graphics) avec transparence.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-292">For Windows 8 and later, the Ribbon framework supports the following graphics formats: 32-bit ARGB bitmap (BMP) files and Portable Network Graphics (PNG) files with transparency.</span></span>

<span data-ttu-id="4ffe6-293">Pour Windows 7 et les versions antérieures, les ressources d’image doivent être conformes au format graphique BMP standard utilisé dans Windows.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-293">For Windows 7 and earlier, image resources must conform to the standard BMP graphics format used in Windows.</span></span>

> [!Note]  
> <span data-ttu-id="4ffe6-294">Les fichiers image existants peuvent être convertis dans l’un ou l’autre format.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-294">Existing image files can be converted to either format.</span></span> <span data-ttu-id="4ffe6-295">Toutefois, les résultats peuvent être moins satisfaisants si les fichiers image ne prennent pas en charge l’anticrénelage et la transparence.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-295">However, the results may be less than satisfactory if the image files do not support antialiasing and transparency.</span></span>

 

<span data-ttu-id="4ffe6-296">Il n’est pas possible de spécifier une taille par défaut unique pour les ressources d’image dans l’infrastructure du ruban.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-296">It is not possible to specify a single default size for image resources in the Ribbon framework.</span></span> <span data-ttu-id="4ffe6-297">Toutefois, pour prendre en charge la [disposition adaptative](windowsribbon-templates.md) des contrôles, les images peuvent être spécifiées en deux tailles (grande et petite).</span><span class="sxs-lookup"><span data-stu-id="4ffe6-297">However, to support [adaptive layout](windowsribbon-templates.md) of controls, images can be specified in two sizes (large and small) .</span></span> <span data-ttu-id="4ffe6-298">Toutes les images de l’infrastructure du ruban sont mises à l’échelle en fonction de la résolution en points par pouce (dpi) de l’affichage avec la taille de rendu exacte dépendante de ce paramètre PPP.</span><span class="sxs-lookup"><span data-stu-id="4ffe6-298">All images in the Ribbon framework are scaled according to the dots per inch (dpi) resolution of the display with the exact rendered size dependent on this dpi setting.</span></span> <span data-ttu-id="4ffe6-299">Pour plus d’informations, consultez [spécification des ressources d’image du ruban](windowsribbon-imageformats.md) .</span><span class="sxs-lookup"><span data-stu-id="4ffe6-299">See [Specifying Ribbon Image Resources](windowsribbon-imageformats.md) for more information.</span></span>

<span data-ttu-id="4ffe6-300">L’exemple suivant montre comment un ensemble d’images spécifiques à PPP est référencé dans le balisage :</span><span class="sxs-lookup"><span data-stu-id="4ffe6-300">The following example demonstrates how a set of dpi-specific images are referenced in markup:</span></span>


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.png" MinDPI="96" />
        <Image Source="cmdNew-40px.png" MinDPI="120" />
        <Image Source="cmdNew-48px.png" MinDPI="144" />
        <Image Source="cmdNew-64px.png" MinDPI="192" />
      </Command.LargeImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.png" MinDPI="96" />
        <Image Source="cmdNew-20px.png" MinDPI="120" />
        <Image Source="cmdNew-24px.png" MinDPI="144" />
        <Image Source="cmdNew-32px.png" MinDPI="192" />
      </Command.SmallImages>
    </Command>
```



## <a name="related-topics"></a><span data-ttu-id="4ffe6-301">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4ffe6-301">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ffe6-302">Spécification des ressources d’image du ruban</span><span class="sxs-lookup"><span data-stu-id="4ffe6-302">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> </dl>

 

 