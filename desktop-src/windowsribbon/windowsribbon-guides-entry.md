---
title: Guides du développeur de l’infrastructure de ruban Windows
description: Les rubriques contenues dans cette section décrivent des aspects spécifiques de l’infrastructure du ruban Windows.
ms.assetid: 87434a15-ba13-4c6f-a814-49ae2349bfa2
keywords:
- Ruban Windows, infrastructure
- Ruban, infrastructure
- Ruban Windows, guides pour les développeurs
- Ruban, guides pour les développeurs
- Guide du développeur pour le ruban Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b6e88045efdd31384d99370fdd9bb9cb264598
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102156"
---
# <a name="windows-ribbon-framework-developer-guides"></a><span data-ttu-id="ba07a-108">Guides du développeur de l’infrastructure de ruban Windows</span><span class="sxs-lookup"><span data-stu-id="ba07a-108">Windows Ribbon Framework Developer Guides</span></span>

<span data-ttu-id="ba07a-109">Les rubriques contenues dans cette section décrivent des aspects spécifiques de l’infrastructure du ruban Windows.</span><span class="sxs-lookup"><span data-stu-id="ba07a-109">The topics contained in this section describe specific aspects of the Windows Ribbon framework.</span></span>

## <a name="basics"></a><span data-ttu-id="ba07a-110">Concepts de base</span><span class="sxs-lookup"><span data-stu-id="ba07a-110">Basics</span></span>

[<span data-ttu-id="ba07a-111">Création d’une application de ruban</span><span class="sxs-lookup"><span data-stu-id="ba07a-111">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)

<span data-ttu-id="ba07a-112">Pour que l’infrastructure du ruban Windows utilise le fichier de balisage du ruban, le fichier de balisage doit être compilé dans un fichier de ressources au format binaire.</span><span class="sxs-lookup"><span data-stu-id="ba07a-112">For the Windows Ribbon framework to consume the Ribbon markup file, the markup file must be compiled into a binary format resource file.</span></span> <span data-ttu-id="ba07a-113">Un compilateur de balisage du ruban dédié, le compilateur de commandes d’interface utilisateur (UICC), est inclus dans le kit de développement logiciel (SDK) Microsoft Windows (7,0 ou version ultérieure) à cet effet.</span><span class="sxs-lookup"><span data-stu-id="ba07a-113">A dedicated Ribbon markup compiler, the UI Command Compiler (UICC), is included with the Microsoft Windows Software Development Kit (SDK) (7.0 or later) for this purpose.</span></span> <span data-ttu-id="ba07a-114">En plus de compiler la version binaire du balisage du ruban, UICC génère un fichier d’en-tête de définition d’ID (. h) qui expose tous les éléments de balisage à l’application hôte du ruban et un fichier de ressources (. RC) qui est utilisé pour lier des ressources d’image et de chaîne à l’application hôte au moment de la génération.</span><span class="sxs-lookup"><span data-stu-id="ba07a-114">In addition to compiling the binary version of the Ribbon markup, the UICC generates an ID definition header (.h) file that exposes all markup elements to the Ribbon host application and a resource (.rc) file that is used to link image and string resources to the host application at build time.</span></span>

[<span data-ttu-id="ba07a-115">Migration vers l’infrastructure de ruban Windows</span><span class="sxs-lookup"><span data-stu-id="ba07a-115">Migrating to the Windows Ribbon Framework</span></span>](ribbon-migration.md)

<span data-ttu-id="ba07a-116">Une application qui s’appuie sur des menus, des barres d’outils et des boîtes de dialogue traditionnels peut être migrée vers l’interface utilisateur riche, dynamique et basée sur le contexte du système de commandes de l’infrastructure du ruban.</span><span class="sxs-lookup"><span data-stu-id="ba07a-116">An application that relies on traditional menus, toolbars, and dialogs can be migrated to the rich, dynamic, and context-driven user interface (UI) of the Ribbon framework Command system.</span></span> <span data-ttu-id="ba07a-117">Il s’agit d’un moyen simple et efficace de moderniser et de revitaliser l’application tout en améliorant également l’accessibilité, la convivialité et la détectabilité de ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="ba07a-117">This is an easy and effective way to modernize and revitalize the application while also improving the accessibility, usability, and discoverability of its functionality.</span></span>

[<span data-ttu-id="ba07a-118">Fonctionnement des commandes et des contrôles</span><span class="sxs-lookup"><span data-stu-id="ba07a-118">Understanding Commands and Controls</span></span>](windowsribbon-commandscontrols.md)

<span data-ttu-id="ba07a-119">La séparation de la logique de la présentation est la philosophie de conception qui inspire le système de présentation de commande de l’infrastructure du ruban, un système basé sur un modèle de conception où les fonctionnalités et le comportement sont implémentés indépendamment des contrôles qui exposent cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="ba07a-119">The separation of logic from presentation is the design philosophy that inspires the command presentation system of the Ribbon framework—a system that is based on a design pattern where functionality and behavior are implemented independently from the controls that expose this functionality.</span></span>

## <a name="user-interface"></a><span data-ttu-id="ba07a-120">Interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="ba07a-120">User Interface</span></span>

[<span data-ttu-id="ba07a-121">Spécification des ressources d’image du ruban</span><span class="sxs-lookup"><span data-stu-id="ba07a-121">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)

<span data-ttu-id="ba07a-122">En tant que système de présentation de commande riche, l’infrastructure du ruban est conçue pour prendre en charge les ressources d’image de manière intensive dans l’interface utilisateur du ruban.</span><span class="sxs-lookup"><span data-stu-id="ba07a-122">As a rich command presentation system, the Ribbon framework is designed to support image resources extensively throughout the Ribbon user interface (UI).</span></span> <span data-ttu-id="ba07a-123">Toutes les ressources d’image sont déclarées dans le [balisage du ruban](windowsribbon-schema.md) ou interrogées à partir d’une application hôte du ruban.</span><span class="sxs-lookup"><span data-stu-id="ba07a-123">All image resources are declared in [Ribbon markup](windowsribbon-schema.md) or queried from a Ribbon host application.</span></span>

<span data-ttu-id="ba07a-124">Pour Windows 8 et versions ultérieures, l’infrastructure du ruban prend en charge les formats graphiques suivants : fichiers BMP (bitmaps) 32 bits et fichiers PNG (Portable Network Graphics) avec transparence.</span><span class="sxs-lookup"><span data-stu-id="ba07a-124">For Windows 8 and later, the Ribbon framework supports the following graphics formats: 32-bit ARGB bitmap (BMP) files and Portable Network Graphics (PNG) files with transparency.</span></span>

<span data-ttu-id="ba07a-125">Pour Windows 7 et les versions antérieures, les ressources d’image doivent être conformes au format graphique BMP standard utilisé dans Windows.</span><span class="sxs-lookup"><span data-stu-id="ba07a-125">For Windows 7 and earlier, image resources must conform to the standard BMP graphics format used in Windows.</span></span>

[<span data-ttu-id="ba07a-126">Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="ba07a-126">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)

<span data-ttu-id="ba07a-127">Les contrôles hébergés dans la barre de commandes du ruban sont soumis à des règles de disposition appliquées par l’infrastructure du ruban et basées sur une combinaison de comportements par défaut et de modèles de disposition (à la fois définis par l’infrastructure et personnalisées) comme déclaré dans le balisage du ruban.</span><span class="sxs-lookup"><span data-stu-id="ba07a-127">Controls hosted in the ribbon Command bar are subject to layout rules that are enforced by the Ribbon framework and based on a combination of default behaviors and layout templates (both framework-defined and custom) as declared in the Ribbon markup.</span></span> <span data-ttu-id="ba07a-128">Ces règles définissent les comportements de disposition adaptative de l’infrastructure du ruban qui influencent la manière dont les contrôles de la barre de commandes s’adaptent aux différentes tailles de ruban au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="ba07a-128">These rules define the adaptive layout behaviors of the Ribbon framework that influence how controls in the Command bar adapt to various ribbon sizes at run time.</span></span>

[<span data-ttu-id="ba07a-129">Utilisation des galeries</span><span class="sxs-lookup"><span data-stu-id="ba07a-129">Working with Galleries</span></span>](ribbon-controls-galleries.md)

<span data-ttu-id="ba07a-130">L’infrastructure du ruban offre aux développeurs un modèle robuste et cohérent pour la gestion du contenu dynamique sur divers contrôles basés sur des collections.</span><span class="sxs-lookup"><span data-stu-id="ba07a-130">The Ribbon framework provides developers with a robust and consistent model for managing dynamic content across a variety of collection-based controls.</span></span> <span data-ttu-id="ba07a-131">En adaptant et en reconfigurant l’interface utilisateur du ruban, ces contrôles dynamiques permettent à l’infrastructure de répondre à l’interaction de l’utilisateur dans l’application hôte et le ruban lui-même, et offrent la flexibilité nécessaire pour gérer différents environnements d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ba07a-131">By adapting and reconfiguring the Ribbon user interface (UI), these dynamic controls allow the framework to respond to user interaction in both the host application and Ribbon itself, and provide the flexibility to handle various run time environments.</span></span>

[<span data-ttu-id="ba07a-132">Affichage des onglets contextuels</span><span class="sxs-lookup"><span data-stu-id="ba07a-132">Displaying Contextual Tabs</span></span>](ribbon-contextualtabs.md)

<span data-ttu-id="ba07a-133">Dans une application de Framework de ruban, un onglet contextuel est un contrôle [onglet](windowsribbon-controls-tab.md) masqué qui est affiché dans la ligne d’onglet lorsqu’un objet dans l’espace de travail d’application, tel qu’une image, est sélectionné ou mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="ba07a-133">In a Ribbon framework application, a contextual tab is a hidden [Tab](windowsribbon-controls-tab.md) control that is displayed in the tab row when an object in the application workspace, such as an image, is selected or highlighted.</span></span>

[<span data-ttu-id="ba07a-134">Reconfiguration du ruban avec les modes d’application</span><span class="sxs-lookup"><span data-stu-id="ba07a-134">Reconfiguring the Ribbon with Application Modes</span></span>](ribbon-applicationmodes.md)

<span data-ttu-id="ba07a-135">L’infrastructure du ruban prend en charge la reconfiguration et l’exposition dynamiques des éléments principaux de l’interface utilisateur du ruban au moment de l’exécution, en fonction de l’état de l’application (également appelé contexte).</span><span class="sxs-lookup"><span data-stu-id="ba07a-135">The Ribbon framework supports the dynamic reconfiguring and exposing of core elements of the Ribbon user interface (UI) at run time, based on the application's state (also referred to as context).</span></span> <span data-ttu-id="ba07a-136">Déclarés et associés à des éléments spécifiques dans le balisage, les différents États pris en charge par une application sont appelés modes d’application.</span><span class="sxs-lookup"><span data-stu-id="ba07a-136">Declared and associated with specific elements in markup, the various states supported by an application are referred to as application modes.</span></span>

[<span data-ttu-id="ba07a-137">Personnalisation des couleurs du ruban</span><span class="sxs-lookup"><span data-stu-id="ba07a-137">Customizing Ribbon Colors</span></span>](ribbon-color.md)

<span data-ttu-id="ba07a-138">L’infrastructure du ruban expose un jeu de propriétés de couleur qui permettent à une application de personnaliser l’apparence des différents éléments de l’interface utilisateur du ruban au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="ba07a-138">The Ribbon framework exposes a set of color properties that allow an application to customize the appearance of various Ribbon user interface (UI) elements at run time.</span></span>

[<span data-ttu-id="ba07a-139">Affichage du ruban</span><span class="sxs-lookup"><span data-stu-id="ba07a-139">Displaying the Ribbon</span></span>](ribbon-visibility.md)

<span data-ttu-id="ba07a-140">L’infrastructure du ruban expose un ensemble de propriétés qui permettent à une application de spécifier la manière dont l’interface utilisateur du ruban est affichée au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="ba07a-140">The Ribbon framework exposes a set of properties that allow an application to specify how the Ribbon user interface (UI) is displayed at run time.</span></span>

## <a name="management"></a><span data-ttu-id="ba07a-141">Gestion</span><span class="sxs-lookup"><span data-stu-id="ba07a-141">Management</span></span>

[<span data-ttu-id="ba07a-142">Persistance de l’état du ruban</span><span class="sxs-lookup"><span data-stu-id="ba07a-142">Persisting Ribbon State</span></span>](ribbon-statepersistence.md)

<span data-ttu-id="ba07a-143">Windows Ribon Framework (ruban) offre la possibilité de conserver l’état d’une variété de paramètres utilisateur et de préférences dans les sessions d’application.</span><span class="sxs-lookup"><span data-stu-id="ba07a-143">The Windows Ribon framework (Ribbon) provides the ability to preserve the state of a variety of user settings and preferences across application sessions.</span></span>

[<span data-ttu-id="ba07a-144">Écoute des événements de ruban</span><span class="sxs-lookup"><span data-stu-id="ba07a-144">Listening for Ribbon Events</span></span>](listening-for-ribbon-events.md)

<span data-ttu-id="ba07a-145">L’infrastructure du ruban utilise l’infrastructure de [suivi d’v nements pour Windows (ETW)](../etw/event-tracing-portal.md) pour permettre aux développeurs d’apprendre comment les utilisateurs interagissent avec le ruban de leur application.</span><span class="sxs-lookup"><span data-stu-id="ba07a-145">The Ribbon framework uses the [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) infrastructure to enable developers to learn how users are interacting with their application's ribbon.</span></span>

## <a name="markup-compiler"></a><span data-ttu-id="ba07a-146">Compilateur de balisage</span><span class="sxs-lookup"><span data-stu-id="ba07a-146">Markup Compiler</span></span>

[<span data-ttu-id="ba07a-147">Compilation du balisage du ruban</span><span class="sxs-lookup"><span data-stu-id="ba07a-147">Compiling Ribbon Markup</span></span>](windowsribbon-intentcl.md)

<span data-ttu-id="ba07a-148">Pour que l’infrastructure du ruban utilise le fichier de [balisage du ruban](windowsribbon-schema.md) , le fichier de balisage doit être compilé dans un fichier de ressources au format binaire.</span><span class="sxs-lookup"><span data-stu-id="ba07a-148">For the Ribbon framework to consume the [Ribbon markup](windowsribbon-schema.md) file, the markup file must be compiled into a binary format resource file.</span></span> <span data-ttu-id="ba07a-149">Un compilateur de balisage dédié, le compilateur de commandes d’interface utilisateur (UICC), est inclus dans le kit de développement logiciel (SDK) Microsoft Windows (7,0 ou version ultérieure) à cet effet.</span><span class="sxs-lookup"><span data-stu-id="ba07a-149">A dedicated markup compiler, the UI Command Compiler (UICC), is included with the Microsoft Windows Software Development Kit (SDK) (7.0 or later) for this purpose.</span></span> <span data-ttu-id="ba07a-150">En plus de compiler la version binaire du balisage, UICC génère un fichier d’en-tête de définition d’ID (. h) qui expose tous les éléments de balisage à l’application hôte du ruban et un fichier de ressources (. RC) qui est utilisé pour lier des ressources d’image et de chaîne à l’application hôte au moment de la génération.</span><span class="sxs-lookup"><span data-stu-id="ba07a-150">In addition to compiling the binary version of the markup, the UICC generates an ID definition header (.h) file that exposes all markup elements to the Ribbon host application and a resource (.rc) file that is used to link image and string resources to the host application at build time.</span></span>

[<span data-ttu-id="ba07a-151">Fonctionnement des messages du compilateur de balisage</span><span class="sxs-lookup"><span data-stu-id="ba07a-151">Understanding Markup Compiler Messages</span></span>](windowsribbon-compilationerrors.md)

<span data-ttu-id="ba07a-152">Le compilateur de balisage de l’infrastructure du ruban Windows (ruban), compilateur de commande d’interface utilisateur (UICC.exe), valide la balise du ruban par rapport au schéma du ruban et à un ensemble supplémentaire de règles définies par l’infrastructure du ruban.</span><span class="sxs-lookup"><span data-stu-id="ba07a-152">The Windows Ribbon framework (Ribbon) markup compiler, UI Command Compiler (UICC.exe), validates the Ribbon markup against both the Ribbon schema and an additional set of rules defined by the Ribbon framework.</span></span>

 

 