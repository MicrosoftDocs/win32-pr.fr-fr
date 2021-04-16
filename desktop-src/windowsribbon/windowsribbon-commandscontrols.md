---
title: Fonctionnement des commandes et des contrôles
description: La séparation de la logique de la présentation est la philosophie de conception qui inspire le système de présentation de commande de l’infrastructure de ruban Windows \ 8212 ; un système basé sur un modèle de conception où les fonctionnalités et le comportement sont implémentés indépendamment des contrôles qui exposent cette fonctionnalité.
ms.assetid: fdea0d70-c6e0-4d13-99bc-ff0c1dbff10d
keywords:
- Ruban Windows, vue d’ensemble des commandes
- Ruban, vue d’ensemble des commandes
- Ruban Windows, vue d’ensemble des contrôles
- Ruban, vue d’ensemble des contrôles
- système de commandes pour le ruban Windows
- contrôles pour le ruban Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2659da608a3d3e73f3f35ac1911946a6685c74e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104551747"
---
# <a name="understanding-commands-and-controls"></a><span data-ttu-id="9ecb5-109">Fonctionnement des commandes et des contrôles</span><span class="sxs-lookup"><span data-stu-id="9ecb5-109">Understanding Commands and Controls</span></span>

<span data-ttu-id="9ecb5-110">La séparation de la logique de la présentation est la philosophie de conception qui inspire le système de présentation de commande de l’infrastructure de ruban Windows, un système basé sur un modèle de conception dans lequel les fonctionnalités et le comportement sont implémentés indépendamment des contrôles qui exposent cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-110">The separation of logic from presentation is the design philosophy that inspires the command presentation system of the Windows Ribbon framework—a system that is based on a design pattern where functionality and behavior are implemented independently from the controls that expose this functionality.</span></span>

-   [<span data-ttu-id="9ecb5-111">Introduction</span><span class="sxs-lookup"><span data-stu-id="9ecb5-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="9ecb5-112">Système de commandes du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="9ecb5-112">The Windows Ribbon Command System</span></span>](#the-windows-ribbon-command-system)
    -   [<span data-ttu-id="9ecb5-113">Contrôles</span><span class="sxs-lookup"><span data-stu-id="9ecb5-113">Controls</span></span>](#understanding-commands-and-controls)
    -   [<span data-ttu-id="9ecb5-114">Commandes</span><span class="sxs-lookup"><span data-stu-id="9ecb5-114">Commands</span></span>](#understanding-commands-and-controls)
    -   [<span data-ttu-id="9ecb5-115">L’expérience de commande en action</span><span class="sxs-lookup"><span data-stu-id="9ecb5-115">The Command Experience In Action</span></span>](#the-command-experience-in-action)
-   [<span data-ttu-id="9ecb5-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9ecb5-116">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="9ecb5-117">Introduction</span><span class="sxs-lookup"><span data-stu-id="9ecb5-117">Introduction</span></span>

<span data-ttu-id="9ecb5-118">Cet article décrit la conception du système de commandes du Framework du ruban.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-118">This article discusses the design of the Ribbon framework command system.</span></span> <span data-ttu-id="9ecb5-119">Il décrit les concepts des commandes et des contrôles et explore comment ils fonctionnent ensemble pour fournir une expérience de commande riche avec un grand nombre de nouvelles fonctionnalités de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-119">It describes the concepts of Commands and controls and explores how they work together to provide a rich command experience with a host of new UI capabilities.</span></span>

## <a name="the-windows-ribbon-command-system"></a><span data-ttu-id="9ecb5-120">Système de commandes du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="9ecb5-120">The Windows Ribbon Command System</span></span>

<span data-ttu-id="9ecb5-121">Dans l’infrastructure du ruban, les commandes et les contrôles sont des entités indépendantes.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-121">In the Ribbon framework, Commands and controls are independent entities.</span></span> <span data-ttu-id="9ecb5-122">Une commande est une structure abstraite, sans contraintes de présentation, qui représente une tâche ou une classe de fonctionnalité spécifique.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-122">A Command is an abstract structure, without presentation constraints, that represents a specific task or class of functionality.</span></span> <span data-ttu-id="9ecb5-123">Un contrôle, en revanche, est un objet concret qui expose les fonctionnalités de commande par le biais de l’interface ruban.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-123">A control, on the other hand, is a concrete object that exposes Command functionality through the Ribbon UI.</span></span>

<span data-ttu-id="9ecb5-124">Cette distinction permet de définir des commandes qui sont exemptes de détails de l’interface utilisateur et de s’exécuter sur l’intention d’une action sans avoir à gérer la façon dont l’action a été appelée.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-124">This distinction provides the ability to define Commands that are free of UI details and able to execute on the intent of an action without the need to manage how the action was invoked.</span></span>

### <a name="controls"></a><span data-ttu-id="9ecb5-125">Commandes</span><span class="sxs-lookup"><span data-stu-id="9ecb5-125">Controls</span></span>

<span data-ttu-id="9ecb5-126">Les contrôles sont les objets d’interface utilisateur requis pour la présentation de commande.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-126">Controls are the UI objects required for Command presentation.</span></span> <span data-ttu-id="9ecb5-127">Elles sont rendues et gérées au moment de l’exécution par le Framework en fonction de l’interaction de l’utilisateur et d’un ensemble de propriétés et de comportements inhérents.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-127">They are rendered and managed at run time by the framework based on user interaction and a set of inherent properties and behaviors.</span></span>

<span data-ttu-id="9ecb5-128">Appelée disposition adaptative, la flexibilité gérée par l’infrastructure de l’interface utilisateur est l’un des atouts du ruban.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-128">Known as adaptive layout, the framework-managed flexibility of the UI is one of the great strengths of the Ribbon.</span></span> <span data-ttu-id="9ecb5-129">Les contrôles de ruban peuvent être reconfigurés automatiquement à l’aide de modèles de disposition dépendants du Framework ou définis par le développeur qui sont en mesure de répondre à différentes exigences de temps d’exécution, tout cela sans écrire une seule ligne de code de présentation.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-129">Ribbon controls can automatically reconfigure themselves through framework-dependent or developer-defined layout templates that are able to respond to various run time requirements, all without writing a single line of presentation code.</span></span> <span data-ttu-id="9ecb5-130">Pour plus d’informations, consultez [Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="9ecb5-130">For more information, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

<span data-ttu-id="9ecb5-131">Outre les avantages de la mise en page adaptative, un certain nombre de contrôles de ruban complexes fournissent des solutions autonomes pour des espaces de problème d’interface utilisateur spécifiques.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-131">Besides the benefits of adaptive layout, a number of complex Ribbon controls provide self-contained solutions for specific UI problem spaces.</span></span> <span data-ttu-id="9ecb5-132">En proposant un modèle d’interaction sophistiqué, les contrôles de ruban, tels que FontControl ou ColorPicker, permettent de manipuler des données en termes plus abstraits par le biais de conteneurs de propriétés d’attributs de police ou de couleur réels plutôt que par l’intermédiaire de différents sous-contrôles, énumérations et valeurs d’index de contrôles Windows standard.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-132">By offering a sophisticated interaction model, Ribbon controls, such as the FontControl or ColorPicker, provide the ability to manipulate data in more abstract terms through property bags of actual font or color attributes rather than through various sub-controls, enumerations, and index values of standard Windows controls.</span></span>

### <a name="commands"></a><span data-ttu-id="9ecb5-133">Commandes</span><span class="sxs-lookup"><span data-stu-id="9ecb5-133">Commands</span></span>

<span data-ttu-id="9ecb5-134">Faiblement couplé aux contrôles du ruban qui exposent leurs fonctionnalités, les implémentations de commande sont le domaine de l’application hôte et prennent la forme d’écouteurs d’événements, de gestionnaires de commandes et de diverses propriétés de commande.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-134">Loosely coupled to the Ribbon controls that expose their functionality, Command implementations are the domain of the host application and take the form of event listeners, Command handlers, and various Command properties.</span></span>

<span data-ttu-id="9ecb5-135">Les commandes sont déclarées dans le balisage du ruban avec un ID unique, ou un ID généré par le compilateur de balisage est assigné lors de la compilation.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-135">Commands are declared in Ribbon markup with a unique ID, or assigned a markup compiler-generated ID at compilation.</span></span> <span data-ttu-id="9ecb5-136">Les commandes sont associées à des contrôles via un nom de commande mais, contrairement aux contrôles, leurs fonctionnalités réelles sont définies dans le code où elles sont liées à des gestionnaires de commandes spécifiques par le biais de l’ID de commande.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-136">Commands are associated with controls through a Command name but, unlike controls, their actual functionality is defined in code where they are bound to specific Command handlers through the Command ID.</span></span>

> [!Note]  
> <span data-ttu-id="9ecb5-137">Lors de la compilation, cet ID est stocké dans un fichier d’en-tête de définition d’ID qui expose des commandes à leurs gestionnaires de commandes correspondants dans l’application hôte du ruban.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-137">At compilation, this ID is stored in an ID definition header file that exposes Commands to their corresponding Command handlers in the Ribbon host application.</span></span>

 

<span data-ttu-id="9ecb5-138">Chaque commande possède un type de commande sous-jacent dans l’énumération [**\_ COMMANDTYPE de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype) .</span><span class="sxs-lookup"><span data-stu-id="9ecb5-138">Each Command has an underlying Command type itemized in the [**UI\_COMMANDTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype) enumeration.</span></span>

### <a name="the-command-experience-in-action"></a><span data-ttu-id="9ecb5-139">L’expérience de commande en action</span><span class="sxs-lookup"><span data-stu-id="9ecb5-139">The Command Experience In Action</span></span>

<span data-ttu-id="9ecb5-140">Les fonctionnalités de ce modèle de commande sont illustrées par la barre d’outils accès rapide du ruban.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-140">The capabilities of this command model are demonstrated by the Ribbon Quick Access Toolbar (QAT).</span></span> <span data-ttu-id="9ecb5-141">Le QAT fournit aux utilisateurs finaux un moyen de définir facilement leurs propres raccourcis pour quasiment n’importe quel contrôle dans l’interface utilisateur du ruban.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-141">The QAT provides end users with a way to easily define their own shortcuts for virtually any control in the Ribbon UI.</span></span> <span data-ttu-id="9ecb5-142">Un raccourci est ajouté dynamiquement au QAT au moment de l’exécution lorsque l’utilisateur clique avec le bouton droit sur un contrôle de ruban et sélectionne **Ajouter à la barre d’outils accès rapide** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-142">A shortcut is added dynamically to the QAT at run time when the user right-clicks a Ribbon control and selects **Add to Quick Access Toolbar** from the context menu.</span></span>

<span data-ttu-id="9ecb5-143">L’illustration suivante montre les commandes **coller** et **coller à partir de** , représentées par un contrôle [**SplitButton**](windowsribbon-element-splitbutton.md) , dans le ruban de Windows 7 Paint.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-143">The following picture shows the **Paste** and **Paste from** Commands, represented by a [**SplitButton**](windowsribbon-element-splitbutton.md) control, in the Ribbon of Windows 7 Paint.</span></span>

![image du SplitButton coller dans le ruban Microsoft Paint.](images/overviews/paint-paste-splitbutton-ribbon.png)

<span data-ttu-id="9ecb5-145">L’illustration suivante montre les mêmes commandes **coller** et **coller à partir des** commandes, toujours représentées par un contrôle [**SplitButton**](windowsribbon-element-splitbutton.md) , dans le ruban de l’qat de Windows 7 Paint.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-145">The following picture shows the same **Paste** and **Paste from** Commands, still represented by a [**SplitButton**](windowsribbon-element-splitbutton.md) control, in the Ribbon QAT of Windows 7 Paint.</span></span>

![image du SplitButton coller dans Microsoft Paint qat.](images/overviews/paint-paste-splitbutton-qat.png)

<span data-ttu-id="9ecb5-147">Lorsqu’un contrôle est hébergé par le QAT, la nouvelle instance du contrôle conserve toutes les fonctionnalités du contrôle d’origine sans qu’il soit nécessaire d’utiliser des écouteurs d’événements et des gestionnaires de commandes supplémentaires pour le prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-147">When a control is hosted by the QAT, the new instance of the control maintains all the functionality of the original control without the need for additional event listeners and command handlers to support it.</span></span> <span data-ttu-id="9ecb5-148">Les deux contrôles sont liés au même gestionnaire de commandes du ruban via un identificateur de commande partagé.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-148">Both controls are bound to the same Ribbon Command handler through a shared Command identifier.</span></span> <span data-ttu-id="9ecb5-149">De cette façon, l’infrastructure traite les deux contrôles comme un, quelle que soit la méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-149">In this way, the framework treats both controls as one, no matter which is invoked.</span></span>

> [!Note]  
> <span data-ttu-id="9ecb5-150">Les mêmes avantages sont obtenus lorsque les commandes sont incorporées dans un [**ContextPopup**](windowsribbon-element-contextpopup.md) au moment de la conception.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-150">The same benefits are realized when Commands are incorporated into a [**ContextPopup**](windowsribbon-element-contextpopup.md) at design time.</span></span> <span data-ttu-id="9ecb5-151">Dans ce cas, les gestionnaires de commandes Coller peuvent être utilisés, que le contrôle [**SplitButton**](windowsribbon-element-splitbutton.md) apparaisse dans le ruban, le qat ou le **ContextPopup**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-151">In this case, the Paste Command handlers can be used whether the [**SplitButton**](windowsribbon-element-splitbutton.md) control appears in the Ribbon, the QAT, or the **ContextPopup**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9ecb5-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9ecb5-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ecb5-153">Présentation de l’infrastructure du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="9ecb5-153">Introducing the Windows Ribbon Framework</span></span>](windowsribbon-introduction.md)
</dt> <dt>

[<span data-ttu-id="9ecb5-154">Création d’une application de ruban</span><span class="sxs-lookup"><span data-stu-id="9ecb5-154">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)
</dt> <dt>

[<span data-ttu-id="9ecb5-155">Déclaration des commandes et des contrôles avec le balisage du ruban</span><span class="sxs-lookup"><span data-stu-id="9ecb5-155">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> </dl>

 

 