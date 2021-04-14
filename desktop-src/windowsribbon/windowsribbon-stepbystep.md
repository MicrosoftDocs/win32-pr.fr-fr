---
title: Création d’une application de ruban
description: L’infrastructure du ruban Windows est composée de deux plateformes de développement distinctes, mais dépendantes, d’un langage de balisage basé sur Extensible Application Markup Language (XAML) pour déclarer des contrôles et leur disposition visuelle, et d’un jeu d’interfaces COM (Component Object Model) C++ pour définir les fonctionnalités de commande et les hooks d’application. Cette division de main-d’œuvre au sein de l’architecture de l’infrastructure du ruban requiert qu’un développeur qui souhaite tirer parti des fonctionnalités d’interface utilisateur enrichies offertes par l’infrastructure doive concevoir et décrire l’interface utilisateur dans le balisage, puis utiliser les interfaces COM de l’infrastructure du ruban pour connecter l’infrastructure à l’application hôte.
ms.assetid: 1bd3dbb5-822b-4551-8330-8b202a4cecdf
keywords:
- Ruban Windows, création d’applications
- Ruban, création d’applications
- Ruban Windows, feuille de route
- Ruban, feuille de route
- Ruban Windows, balisage
- Ruban, balisage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a10f683c7fbb07b9992e418a4c09dc9aecba280
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382379"
---
# <a name="creating-a-ribbon-application"></a><span data-ttu-id="279e8-110">Création d’une application de ruban</span><span class="sxs-lookup"><span data-stu-id="279e8-110">Creating a Ribbon Application</span></span>

<span data-ttu-id="279e8-111">L’infrastructure du ruban Windows est composée de deux plates-formes de développement distinctes et dépendantes. il s’agit d’un langage de balisage basé sur Extensible Application Markup Language (XAML) pour déclarer des contrôles et leur disposition visuelle, ainsi qu’un ensemble d’interfaces COM (Component Object Model) C++ pour définir les fonctionnalités de commande et les hooks d’application.</span><span class="sxs-lookup"><span data-stu-id="279e8-111">The Windows Ribbon framework is composed of two distinct, yet dependent, development platforms: a markup language based on Extensible Application Markup Language (XAML) to declare controls and their visual layout, and a C++ Component Object Model (COM)-based set of interfaces to define command functionality and application hooks.</span></span> <span data-ttu-id="279e8-112">Cette division de main-d’œuvre au sein de l’architecture de l’infrastructure du ruban requiert qu’un développeur qui souhaite tirer parti des fonctionnalités d’interface utilisateur enrichies offertes par l’infrastructure doive concevoir et décrire l’interface utilisateur dans le balisage, puis utiliser les interfaces COM de l’infrastructure du ruban pour connecter l’infrastructure à l’application hôte.</span><span class="sxs-lookup"><span data-stu-id="279e8-112">This division of labor within the Ribbon framework architecture requires that a developer who wants to take advantage of the rich UI capabilities offered by the framework must design and describe the UI in markup, and then use the Ribbon framework COM interfaces to connect the framework to the host application.</span></span>

-   [<span data-ttu-id="279e8-113">Feuille de route du ruban</span><span class="sxs-lookup"><span data-stu-id="279e8-113">Ribbon Roadmap</span></span>](#ribbon-roadmap)
-   [<span data-ttu-id="279e8-114">Écrire le balisage</span><span class="sxs-lookup"><span data-stu-id="279e8-114">Write the Markup</span></span>](#write-the-markup)
    -   [<span data-ttu-id="279e8-115">Compiler le balisage</span><span class="sxs-lookup"><span data-stu-id="279e8-115">Compile the Markup</span></span>](#compile-the-markup)
-   [<span data-ttu-id="279e8-116">Générer l’application</span><span class="sxs-lookup"><span data-stu-id="279e8-116">Build the Application</span></span>](#build-the-application)
    -   [<span data-ttu-id="279e8-117">Initialiser le ruban</span><span class="sxs-lookup"><span data-stu-id="279e8-117">Initialize the Ribbon</span></span>](#initialize-the-ribbon)
    -   [<span data-ttu-id="279e8-118">Lier le balisage à l’application</span><span class="sxs-lookup"><span data-stu-id="279e8-118">Link the Markup to the Application</span></span>](#link-the-markup-to-the-application)
    -   [<span data-ttu-id="279e8-119">Compiler l’application</span><span class="sxs-lookup"><span data-stu-id="279e8-119">Compile the Application</span></span>](#link-the-markup-to-the-application)
-   [<span data-ttu-id="279e8-120">Exécutions et mises à jour de l’heure d’exécution</span><span class="sxs-lookup"><span data-stu-id="279e8-120">Run Time Updates and Executions</span></span>](#run-time-updates-and-executions)
-   [<span data-ttu-id="279e8-121">Prise en charge OLE</span><span class="sxs-lookup"><span data-stu-id="279e8-121">OLE Support</span></span>](#ole-support)
-   [<span data-ttu-id="279e8-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="279e8-122">Related topics</span></span>](#related-topics)

## <a name="ribbon-roadmap"></a><span data-ttu-id="279e8-123">Feuille de route du ruban</span><span class="sxs-lookup"><span data-stu-id="279e8-123">Ribbon Roadmap</span></span>

<span data-ttu-id="279e8-124">Les aspects visuels d’une application de ruban, tels que les contrôles affichés et leur emplacement, sont déclarés dans le balisage (consultez [déclaration des commandes et des contrôles avec le balisage du ruban](windowsribbon-schema.md)).</span><span class="sxs-lookup"><span data-stu-id="279e8-124">The visual aspects of a Ribbon application, such as what controls are displayed and where they are placed, are declared in markup (see [Declaring Commands and Controls with Ribbon Markup](windowsribbon-schema.md)).</span></span> <span data-ttu-id="279e8-125">La logique de commande d’application, par exemple ce qui se produit quand un bouton est enfoncé, est implémentée dans le code.</span><span class="sxs-lookup"><span data-stu-id="279e8-125">The application command logic, such as what happens when a button is pressed, is implemented in code.</span></span>

<span data-ttu-id="279e8-126">Le processus d’implémentation d’un ruban et de son incorporation dans une application Windows requiert quatre tâches de base : écrire le balisage, compiler le balisage, écrire le code, compiler et lier l’application entière.</span><span class="sxs-lookup"><span data-stu-id="279e8-126">The process of implementing a Ribbon and incorporating it into a Windows application requires four basic tasks: write the markup, compile the markup, write the code, and compile and link the entire application.</span></span>

<span data-ttu-id="279e8-127">Le diagramme suivant illustre le flux de travail pour une implémentation de ruban typique.</span><span class="sxs-lookup"><span data-stu-id="279e8-127">The following diagram illustrates the workflow for a typical Ribbon implementation.</span></span>

![Diagramme montrant le flux de travail pour une implémentation de ruban typique.](images/overviews/ribbonroadmap.png)

<span data-ttu-id="279e8-129">Les sections suivantes décrivent ce processus plus en détail.</span><span class="sxs-lookup"><span data-stu-id="279e8-129">The following sections describe this process in more detail.</span></span>

## <a name="write-the-markup"></a><span data-ttu-id="279e8-130">Écrire le balisage</span><span class="sxs-lookup"><span data-stu-id="279e8-130">Write the Markup</span></span>

<span data-ttu-id="279e8-131">Une fois l’interface utilisateur du ruban conçue, la première tâche d’un développeur d’applications est de décrire l’interface utilisateur avec le balisage du ruban.</span><span class="sxs-lookup"><span data-stu-id="279e8-131">After the Ribbon UI has been designed, the first task for an application developer is to describe the UI with Ribbon markup.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="279e8-132">Le fichier de schéma de balisage de Framework du ruban, UICC. xsd, est installé avec le kit de développement logiciel (SDK) Microsoft Windows pour Windows 7 et .NET Framework 4,0.</span><span class="sxs-lookup"><span data-stu-id="279e8-132">The Ribbon framework markup schema file, UICC.xsd, is installed with the Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0.</span></span> <span data-ttu-id="279e8-133">À l’aide du chemin d’installation standard, le fichier se trouve dans le dossier% ProgramFiles% \\ Microsoft SDK numéro de la \\ \\ \[ version Windows \] \\ où il peut être référencé par de nombreux éditeurs XML pour fournir des indications et une saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="279e8-133">Using the standard installation path, the file is located in the %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Bin folder where it can be referenced by many XML editors to provide hinting and auto-completion.</span></span>

 

<span data-ttu-id="279e8-134">Les contrôles de ruban, les commandes de ruban (les éléments indépendants du contrôle qui fournissent les fonctionnalités de base pour les contrôles de ruban) et l’ensemble de la disposition de contrôle et des relations visuelles sont déclarés dans le balisage.</span><span class="sxs-lookup"><span data-stu-id="279e8-134">Ribbon controls, Ribbon Commands (the control-independent elements that provide the base functionality for Ribbon controls), and all control layout and visual relationships are declared in markup.</span></span> <span data-ttu-id="279e8-135">La structure du balisage du ruban met l’accent sur la distinction entre les contrôles du ruban et les commandes via deux hiérarchies de nœuds principales : une arborescence [commandes et ressources](windowsribbon-reference-elements-command.md) et une arborescence des [vues](windowsribbon-reference-elements-view.md) .</span><span class="sxs-lookup"><span data-stu-id="279e8-135">The structure of the Ribbon markup emphasizes the distinction between Ribbon controls and Commands through two primary node hierarchies: a [Commands and Resources](windowsribbon-reference-elements-command.md) tree and a [Views](windowsribbon-reference-elements-view.md) tree.</span></span>

<span data-ttu-id="279e8-136">Tous les conteneurs et actions qui sont exposés par le ruban sont déclarés dans l’arborescence [commandes et ressources](windowsribbon-reference-elements-command.md) .</span><span class="sxs-lookup"><span data-stu-id="279e8-136">All containers and actions that are exposed by the Ribbon are declared in the [Commands and Resources](windowsribbon-reference-elements-command.md) tree.</span></span> <span data-ttu-id="279e8-137">Chaque élément Command est associé à un ensemble de ressources, comme requis par la conception de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="279e8-137">Each Command element is associated with a set of resources, as required by the UI design.</span></span>

<span data-ttu-id="279e8-138">Une fois que vous avez créé les commandes pour une application, vous déclarez des contrôles dans l’arborescence des [vues](windowsribbon-reference-elements-view.md) et liez chaque contrôle à une commande pour exposer les fonctionnalités de commande.</span><span class="sxs-lookup"><span data-stu-id="279e8-138">After you create the Commands for an application, you declare controls in the [Views](windowsribbon-reference-elements-view.md) tree and bind each control to a Command to expose the Command functionality.</span></span> <span data-ttu-id="279e8-139">L’infrastructure du ruban détermine le positionnement réel des contrôles en fonction de la hiérarchie des contrôles déclarée ici.</span><span class="sxs-lookup"><span data-stu-id="279e8-139">The Ribbon framework determines the actual positioning of the controls based on the Control hierarchy declared here.</span></span>

<span data-ttu-id="279e8-140">L’exemple de code suivant montre comment déclarer un contrôle Button, étiqueté Exit application, et l’associer à une commande exit.</span><span class="sxs-lookup"><span data-stu-id="279e8-140">The following code example illustrates how to declare a Button control, labeled Exit application, and associate it with an Exit Command.</span></span>


```
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
  <Application.Commands>
    <Command Name="cmdExit" LabelTitle="Exit application" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.Tabs>
        <Tab>
          <Group>
            <Button CommandName="cmdExit" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>
</Application>
        
```



> [!TIP]
> <span data-ttu-id="279e8-141">Bien qu’il soit possible d’utiliser n’importe quelle extension de nom de fichier pour le fichier de balisage du ruban,. xml est l’extension recommandée qui est utilisée dans la documentation.</span><span class="sxs-lookup"><span data-stu-id="279e8-141">While it is possible to use any file name extension for the Ribbon markup file, .xml is the recommended extension that is used throughout the documentation.</span></span>

 

### <a name="compile-the-markup"></a><span data-ttu-id="279e8-142">Compiler le balisage</span><span class="sxs-lookup"><span data-stu-id="279e8-142">Compile the Markup</span></span>

<span data-ttu-id="279e8-143">Une fois le fichier de balisage du ruban créé, il doit être compilé dans un format binaire par le compilateur de balisage du ruban, le compilateur de commandes d’interface utilisateur (UICC), qui est inclus dans le kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="279e8-143">After the Ribbon markup file is created, it must be compiled into a binary format by the Ribbon markup compiler, UI Command Compiler (UICC), that is included with the Windows software development kit (SDK).</span></span> <span data-ttu-id="279e8-144">Une référence à ce fichier binaire est transmise à la méthode [**IUIFramework :: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) pendant l’initialisation de l’infrastructure du ruban par l’application hôte.</span><span class="sxs-lookup"><span data-stu-id="279e8-144">A reference to this binary file is passed to the [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) method during initialization of the Ribbon framework by the host application.</span></span>

<span data-ttu-id="279e8-145">UICC peut être exécuté directement à partir d’une fenêtre de ligne de commande ou ajouté en tant qu’étape de génération personnalisée dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="279e8-145">UICC can be executed directly from a command-line window or added as a "Custom Build Step" in Visual Studio.</span></span>

<span data-ttu-id="279e8-146">L’illustration suivante montre le compilateur de balisage UICC dans la fenêtre de l’interface de commande du kit de développement logiciel (SDK) Windows 7.</span><span class="sxs-lookup"><span data-stu-id="279e8-146">The following image shows the UICC markup compiler in the Windows 7 SDK CMD Shell window.</span></span>

![capture d’écran montrant uicc.exe dans une fenêtre de ligne de commande.](images/overviews/screenshot-intentcl-commandline.png)

<span data-ttu-id="279e8-148">L’illustration suivante montre la UICC ajoutée en tant qu’étape de génération personnalisée dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="279e8-148">The following image shows UICC added as a Custom Build Step in Visual Studio.</span></span>

![capture d’écran montrant uicc.exe ajouté comme étape de génération personnalisée dans Visual Studio.](images/overviews/screenshot-vs-intentcl-custombuildstep.png)

<span data-ttu-id="279e8-150">Le UICC génère trois fichiers : une version binaire du balisage (. BML), un en-tête de définition d’ID (fichier. h) pour exposer des éléments de balisage à l’application hôte du ruban, et un [script de définition de ressource](../menurc/about-resource-files.md) (fichier. RC) pour lier l’image de ruban et les ressources de type chaîne à l’application hôte au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="279e8-150">The UICC generates three files: a binary version of the markup (.bml), an ID definition header (.h file) to expose markup elements to the Ribbon host application, and a [resource-definition script](../menurc/about-resource-files.md) (.rc file) to link Ribbon image and string resources to the host application at compile time.</span></span>

<span data-ttu-id="279e8-151">Pour plus d’informations sur la compilation du balisage de l’infrastructure du ruban, consultez [compilation du balisage du ruban](windowsribbon-intentcl.md).</span><span class="sxs-lookup"><span data-stu-id="279e8-151">For more detail on compiling Ribbon framework markup, see [Compiling Ribbon Markup](windowsribbon-intentcl.md).</span></span>

## <a name="build-the-application"></a><span data-ttu-id="279e8-152">Générer l'application</span><span class="sxs-lookup"><span data-stu-id="279e8-152">Build the Application</span></span>

<span data-ttu-id="279e8-153">Une fois que l’interface utilisateur préliminaire d’une application de ruban a été conçue et implémentée dans le balisage, le code d’application doit être écrit pour initialiser le Framework, consomme le balisage et lie les commandes déclarées dans le balisage aux gestionnaires de commandes appropriés dans l’application.</span><span class="sxs-lookup"><span data-stu-id="279e8-153">Once the preliminary UI for a Ribbon application has been designed and implemented in markup, application code must be written that initializes the framework, consumes the markup, and binds the Commands declared in the markup to the appropriate Command handlers in the application.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="279e8-154">Étant donné que l’infrastructure de ruban est basée sur COM, il est recommandé que les projets de ruban utilisent l' \_ \_ opérateur uuidof () pour référencer les GUID pour les interfaces d’infrastructure de ruban (IID).</span><span class="sxs-lookup"><span data-stu-id="279e8-154">Since the Ribbon framework is COM-based, it is recommended that Ribbon projects use the \_\_uuidof() operator to reference the GUIDs for Ribbon framework interfaces (IIDs).</span></span> <span data-ttu-id="279e8-155">Dans les cas où il n’est pas possible d’utiliser l' \_ \_ opérateur uuidof (), par exemple lorsqu’un compilateur non-Microsoft est utilisé ou que l’application hôte est basée sur le langage C, les IID doivent être définis par l’application, car ils ne sont pas contenus dans UUID. lib.</span><span class="sxs-lookup"><span data-stu-id="279e8-155">In those cases where it is not possible to use the \_\_uuidof() operator, such as when a non-Microsoft compiler is used or the host application is C-based, the IIDs must be defined by the application since they are not contained in uuid.lib.</span></span>
>
> <span data-ttu-id="279e8-156">Si les IID sont définis par l’application, les GUID spécifiés dans UIRibbon. idl doivent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="279e8-156">If the IIDs are defined by the application then the GUIDs specified in UIRibbon.idl must be used.</span></span>
>
> <span data-ttu-id="279e8-157">UIRibbon. idl est fourni dans le cadre du [Kit de développement logiciel (SDK) Windows](https://msdn.microsoft.com/windows/bb980924.aspx) et se trouve dans le chemin d’installation standard de% ProgramFiles% \\ Microsoft SDK \\ Windows \\ v 7.0 \\ include.</span><span class="sxs-lookup"><span data-stu-id="279e8-157">UIRibbon.idl ships as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) and can be found at the standard installation path of %ProgramFiles%\\Microsoft SDKs\\Windows\\v7.0\\Include.</span></span>

 

### <a name="initialize-the-ribbon"></a><span data-ttu-id="279e8-158">Initialiser le ruban</span><span class="sxs-lookup"><span data-stu-id="279e8-158">Initialize the Ribbon</span></span>

<span data-ttu-id="279e8-159">Le diagramme suivant illustre les étapes requises pour implémenter une application de ruban simple.</span><span class="sxs-lookup"><span data-stu-id="279e8-159">The following diagram illustrates the steps required to implement a simple Ribbon application.</span></span>

![Diagramme montrant les étapes requises pour implémenter une implémentation de ruban simple.](images/overviews/initializationsteps.png)

<span data-ttu-id="279e8-161">Les étapes suivantes décrivent en détail comment implémenter une application de ruban simple.</span><span class="sxs-lookup"><span data-stu-id="279e8-161">The following steps describe in detail how to implement a simple Ribbon application.</span></span>

1.  <span data-ttu-id="279e8-162">CoCreateInstance</span><span class="sxs-lookup"><span data-stu-id="279e8-162">CoCreateInstance</span></span>

    <span data-ttu-id="279e8-163">L’application appelle la fonction COM CoCreateInstance standard avec l’ID de classe du Framework du ruban pour obtenir un pointeur vers le Framework.</span><span class="sxs-lookup"><span data-stu-id="279e8-163">The application calls the standard COM CoCreateInstance function with the Ribbon framework class ID to obtain a pointer to the framework.</span></span>

    ```
    IUIFramework* pFramework = NULL;
    HRESULT hr = ::CoCreateInstance(
                CLSID_UIRibbonFramework, 
                NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&pFramework));
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

2.  <span data-ttu-id="279e8-164">Initialize (HWND, IUIApplication \* )</span><span class="sxs-lookup"><span data-stu-id="279e8-164">Initialize(hwnd, IUIApplication\*)</span></span>

    <span data-ttu-id="279e8-165">L’application appelle [**IUIFramework :: Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize), en passant deux paramètres : le handle vers la fenêtre de niveau supérieur qui contiendra le ruban et un pointeur vers l’implémentation de [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) qui permet à l’infrastructure d’effectuer des rappels à l’application.</span><span class="sxs-lookup"><span data-stu-id="279e8-165">The application calls [**IUIFramework::Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize), passing in two parameters: the handle to the top-level window that will contain the Ribbon and a pointer to the [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) implementation that allows the framework to make callbacks to the application.</span></span>

    > <span data-ttu-id="279e8-166">\[! Précieuse\]</span><span class="sxs-lookup"><span data-stu-id="279e8-166">\[!Important\]</span></span>  
    > <span data-ttu-id="279e8-167">L’infrastructure du ruban est initialisée en tant que thread unique cloisonné (STA).</span><span class="sxs-lookup"><span data-stu-id="279e8-167">The Ribbon framework is initialized as a single-threaded apartment (STA).</span></span>

     

    ```
    hr = pFramework->Initialize(hWndHost, pApplication);
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

3.  <span data-ttu-id="279e8-168">LoadUI (instance, resourceName)</span><span class="sxs-lookup"><span data-stu-id="279e8-168">LoadUI(instance, resourceName)</span></span>

    <span data-ttu-id="279e8-169">L’application appelle [**IUIFramework :: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) pour lier la ressource de balisage.</span><span class="sxs-lookup"><span data-stu-id="279e8-169">The application calls [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) to bind the markup resource.</span></span> <span data-ttu-id="279e8-170">Le premier paramètre de cette fonction est un handle vers l’instance d’application du ruban.</span><span class="sxs-lookup"><span data-stu-id="279e8-170">The first parameter of this function is a handle to the Ribbon application instance.</span></span> <span data-ttu-id="279e8-171">Le deuxième paramètre est le nom de la ressource de balisage binaire qui a été compilée précédemment.</span><span class="sxs-lookup"><span data-stu-id="279e8-171">The second parameter is the name of the binary markup resource that was compiled previously.</span></span> <span data-ttu-id="279e8-172">En passant le balisage binaire à l’infrastructure du ruban, l’application signale la structure du ruban et la façon dont les contrôles doivent être disposés.</span><span class="sxs-lookup"><span data-stu-id="279e8-172">By passing the binary markup to the Ribbon framework, the application signals what the Ribbon structure should be and how controls should be arranged.</span></span> <span data-ttu-id="279e8-173">Il fournit également à l’infrastructure un manifeste de commandes à exposer (par exemple, coller, couper, Rechercher), qui sont utilisées par le Framework lorsqu’il effectue des rappels liés aux commandes au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="279e8-173">It also provides the framework with a manifest of commands to expose (such as Paste, Cut, Find), which are used by the framework when it makes Command-related callbacks at run time.</span></span>

    ```
    hr = pFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

4.  <span data-ttu-id="279e8-174">Rappels [**IUIApplication :: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand)</span><span class="sxs-lookup"><span data-stu-id="279e8-174">[**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) callbacks</span></span>

    <span data-ttu-id="279e8-175">Une fois les étapes 1 à 3 terminées, l’infrastructure du ruban connaît les commandes à exposer dans le ruban.</span><span class="sxs-lookup"><span data-stu-id="279e8-175">After steps 1 through 3 are completed, the Ribbon framework knows which Commands to expose in the Ribbon.</span></span> <span data-ttu-id="279e8-176">Toutefois, l’infrastructure a encore besoin de deux choses avant que le ruban soit entièrement fonctionnel : un moyen d’indiquer à l’application quand les commandes sont exécutées et un moyen d’obtenir des ressources de commande, ou des propriétés, au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="279e8-176">However, the framework still needs two things before the Ribbon is fully functional: a way to tell the application when Commands are executed and a way to get Command resources, or properties, at run time.</span></span> <span data-ttu-id="279e8-177">Par exemple, si une zone de liste déroulante doit apparaître dans l’interface utilisateur, le Framework doit demander les éléments avec lesquels remplir la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="279e8-177">For example, if a combo box is to appear in the UI, then the framework needs to ask for the items with which to populate the combo box.</span></span>

    <span data-ttu-id="279e8-178">Ces deux fonctionnalités sont gérées par le biais de l’interface [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) .</span><span class="sxs-lookup"><span data-stu-id="279e8-178">These two pieces of functionality are handled through the [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) interface.</span></span> <span data-ttu-id="279e8-179">Plus précisément, pour chaque commande déclarée dans le balisage binaire (Voir l’étape 3 ci-dessus), l’infrastructure appelle [**IUIApplication :: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) pour demander à l’application un objet **IUICommandHandler** pour cette commande.</span><span class="sxs-lookup"><span data-stu-id="279e8-179">Specifically, for each command declared in the binary markup (see Step 3 above), the framework calls [**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) to ask the application for an **IUICommandHandler** object for that command</span></span>

    > [!Note]  
    > <span data-ttu-id="279e8-180">L’interface [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) permet de lier un gestionnaire de commandes à une ou plusieurs commandes.</span><span class="sxs-lookup"><span data-stu-id="279e8-180">The [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) interface allows a Command handler to be bound to one or more Commands.</span></span>

     

<span data-ttu-id="279e8-181">Au minimum, l’application doit implémenter les stubs des méthodes [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) qui retournent E \_ NOTIMPL, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="279e8-181">At a minimum, the application is required to implement [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) methods stubs that return E\_NOTIMPL as shown in the following example.</span></span>


```
STDMETHOD(OnViewChanged)(UINT32 viewId,
                         UI_VIEWTYPE typeID,
                         IUnknown *view,
                         UI_VIEWVERB verb,
                         INT32 uReasonCode)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnCreateUICommand)(UINT32 commandId,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler **commandHandler)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnDestroyUICommand)(UINT32 commandId,
                              UI_COMMANDTYPE typeID,
                              IUICommandHandler *commandHandler) 
{ 
  return E_NOTIMPL; 
}
```



### <a name="link-the-markup-to-the-application"></a><span data-ttu-id="279e8-182">Lier le balisage à l’application</span><span class="sxs-lookup"><span data-stu-id="279e8-182">Link the Markup to the Application</span></span>

<span data-ttu-id="279e8-183">À ce stade, les fichiers de ressources de balisage doivent être liés à l’application hôte en incluant une référence au fichier de définition de ressource de balisage (qui contient une référence au fichier d’en-tête de balisage) dans le fichier de ressources de l’application.</span><span class="sxs-lookup"><span data-stu-id="279e8-183">At this point, the markup resource files must be linked to the host application by including a reference to the markup resource-definition file (which contains a reference to the markup header file) in the application resource file.</span></span> <span data-ttu-id="279e8-184">Par exemple, une application appelée RibbonApp avec un fichier de ressources appelé ribbonUI. RC requiert la ligne suivante dans le fichier RibbonApp. rc.</span><span class="sxs-lookup"><span data-stu-id="279e8-184">For example, an application called RibbonApp with a resource file called ribbonUI.rc requires the following line in the RibbonApp.rc file.</span></span>


```C++
#include "ribbonUI.rc"
```



<span data-ttu-id="279e8-185">En fonction du compilateur et de l’éditeur de liens utilisés, le script de définition de ressource peut également nécessiter une compilation avant que l’application du ruban puisse être compilée.</span><span class="sxs-lookup"><span data-stu-id="279e8-185">Depending on the compiler and linker being used, the resource-definition script may also require compiling before the Ribbon application can be compiled.</span></span> <span data-ttu-id="279e8-186">L’outil en ligne de commande [du compilateur de ressources (RC)](../menurc/using-rc-the-rc-command-line-.md) fourni avec Microsoft Visual Studio et le SDK Windows peuvent être utilisés pour cette tâche.</span><span class="sxs-lookup"><span data-stu-id="279e8-186">The [resource compiler (RC)](../menurc/using-rc-the-rc-command-line-.md) command line tool that ships with Microsoft Visual Studio and the Windows SDK can be used for this task.</span></span>

### <a name="compile-the-application"></a><span data-ttu-id="279e8-187">Compiler l’application</span><span class="sxs-lookup"><span data-stu-id="279e8-187">Compile the Application</span></span>

<span data-ttu-id="279e8-188">Une fois l’application de ruban compilée, elle peut être exécutée et l’interface utilisateur testée.</span><span class="sxs-lookup"><span data-stu-id="279e8-188">Once the Ribbon application is compiled, it can be run and the UI tested.</span></span> <span data-ttu-id="279e8-189">Si l’interface utilisateur requiert une modification et qu’aucune modification n’est apportée aux gestionnaires de commandes associés dans le code d’application principal, modifiez le fichier source du balisage, recompilez le balisage avec UICC.exe et liez les nouveaux fichiers de ressources de balisage.</span><span class="sxs-lookup"><span data-stu-id="279e8-189">If the UI requires tweaking and there are no changes to any associated Command handlers in the core application code, revise the markup source file, recompile the markup with UICC.exe, and link the new markup resource files.</span></span> <span data-ttu-id="279e8-190">Lorsque l’application est redémarrée, l’interface utilisateur modifiée est affichée.</span><span class="sxs-lookup"><span data-stu-id="279e8-190">When the application is restarted, the modified UI is displayed.</span></span>

<span data-ttu-id="279e8-191">Tout ceci est possible sans toucher au code d’application de base, ce qui est une amélioration significative par rapport au développement et à la distribution d’applications standard.</span><span class="sxs-lookup"><span data-stu-id="279e8-191">All this is possible without touching the core application code—a significant improvement over standard application development and distribution.</span></span>

## <a name="run-time-updates-and-executions"></a><span data-ttu-id="279e8-192">Exécutions et mises à jour de l’heure d’exécution</span><span class="sxs-lookup"><span data-stu-id="279e8-192">Run Time Updates and Executions</span></span>

<span data-ttu-id="279e8-193">La structure de communication au moment de l’exécution de l’infrastructure du ruban est basée sur un push et un pull, ou un appelant bidirectionnel.</span><span class="sxs-lookup"><span data-stu-id="279e8-193">The run-time communication structure of the Ribbon framework is based on a push and pull, or two-way caller, model.</span></span>

<span data-ttu-id="279e8-194">Ce modèle permet à l’infrastructure d’informer l’application lorsqu’une commande est exécutée et permet à l’infrastructure et à l’application d’interroger, de mettre à jour et d’invalider les valeurs de propriété et les ressources du ruban.</span><span class="sxs-lookup"><span data-stu-id="279e8-194">This model allows the framework to inform the application when a Command is executed and allows both the framework and the application to query, update, and invalidate property values and Ribbon resources.</span></span> <span data-ttu-id="279e8-195">Cette fonctionnalité est fournie par le biais d’un certain nombre d’interfaces et de méthodes.</span><span class="sxs-lookup"><span data-stu-id="279e8-195">This functionality is provided through a number of interfaces and methods.</span></span>

<span data-ttu-id="279e8-196">L’infrastructure extrait les informations de propriété mises à jour à partir de l’application ruban par le biais de la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="279e8-196">The framework pulls updated property information from the Ribbon application through the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span> <span data-ttu-id="279e8-197">Un ID de commande et une clé de propriété, qui identifie la propriété de commande à mettre à jour, sont passés à la méthode qui retourne, ou envoie, une valeur pour cette clé de propriété au Framework.</span><span class="sxs-lookup"><span data-stu-id="279e8-197">A Command ID and a property key, which identifies the Command property to update, are passed to the method which then returns, or pushes, a value for that property key to the framework.</span></span>

<span data-ttu-id="279e8-198">L’infrastructure appelle [**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) quand une commande est exécutée, en identifiant à la fois l’ID de commande et le type d’exécution qui se sont produits ([**UI \_ EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)).</span><span class="sxs-lookup"><span data-stu-id="279e8-198">The framework calls [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) when a Command is executed, identifying both the Command ID and the type of execution that occurred ([**UI\_EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)).</span></span> <span data-ttu-id="279e8-199">C’est là que l’application spécifie la logique d’exécution d’une commande.</span><span class="sxs-lookup"><span data-stu-id="279e8-199">This is where the application specifies the execution logic for a command.</span></span>

<span data-ttu-id="279e8-200">Le diagramme suivant illustre la communication au moment de l’exécution pour l’exécution des commandes entre l’infrastructure et l’application.</span><span class="sxs-lookup"><span data-stu-id="279e8-200">The following diagram illustrates the run-time communication for Command execution between the framework and the application.</span></span>

![Diagramme montrant un exemple de la communication au moment de l’exécution entre l’infrastructure du ruban et une application hôte.](images/overviews/updatesandexecutions.png)

> [!Note]  
> <span data-ttu-id="279e8-202">L’implémentation des fonctions [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) et [**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) n’est pas nécessaire pour afficher initialement un ruban dans une application.</span><span class="sxs-lookup"><span data-stu-id="279e8-202">Implementing the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) and [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) functions is not necessary to initially display a Ribbon in an application.</span></span> <span data-ttu-id="279e8-203">Toutefois, ces méthodes sont nécessaires pour s’assurer que l’application fonctionne correctement lorsque les commandes sont exécutées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="279e8-203">However, these methods are necessary to ensure that the application functions correctly when commands are executed by the user.</span></span>

 

## <a name="ole-support"></a><span data-ttu-id="279e8-204">Prise en charge OLE</span><span class="sxs-lookup"><span data-stu-id="279e8-204">OLE Support</span></span>

<span data-ttu-id="279e8-205">Une application de ruban peut être configurée en tant que serveur OLE pour prendre en charge l’activation OLE hors place.</span><span class="sxs-lookup"><span data-stu-id="279e8-205">A Ribbon application can be configured as an OLE server to support out-of-place OLE activation.</span></span>

<span data-ttu-id="279e8-206">Les objets créés dans une application serveur OLE conservent leur association avec l’application serveur lorsqu’ils sont insérés (collés ou placés) dans une application cliente OLE (ou un conteneur).</span><span class="sxs-lookup"><span data-stu-id="279e8-206">Objects created in an OLE server application maintain their association with the server application when inserted (either pasted or placed) into an OLE client application (or container).</span></span> <span data-ttu-id="279e8-207">Dans le cas d’une activation OLE hors place, le double-clic sur l’objet dans l’application cliente ouvre une instance dédiée de l’application serveur et charge l’objet pour modification.</span><span class="sxs-lookup"><span data-stu-id="279e8-207">In out-of-place OLE activation, double clicking the object in the client application opens a dedicated instance of the server application and loads the object for editing.</span></span> <span data-ttu-id="279e8-208">Lorsque l’application serveur est fermée, toutes les modifications apportées à l’objet sont reflétées dans l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="279e8-208">When the server application is closed, all changes made to the object are reflected in the client application.</span></span>

> [!Note]  
> <span data-ttu-id="279e8-209">L’infrastructure du ruban ne prend pas en charge l’activation OLE sur place.</span><span class="sxs-lookup"><span data-stu-id="279e8-209">The Ribbon framework does not support in-place OLE activation.</span></span> <span data-ttu-id="279e8-210">Les objets créés dans un serveur OLE basé sur le ruban ne peuvent pas être modifiés à partir de l’application cliente OLE.</span><span class="sxs-lookup"><span data-stu-id="279e8-210">Objects created in a Ribbon-based OLE server cannot be edited from within the OLE client application.</span></span> <span data-ttu-id="279e8-211">Une instance dédiée externe de l’application serveur est requise.</span><span class="sxs-lookup"><span data-stu-id="279e8-211">An external dedicated instance of the server application is required.</span></span>


## <a name="related-topics"></a><span data-ttu-id="279e8-212">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="279e8-212">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="279e8-213">Déclaration des commandes et des contrôles avec le balisage du ruban</span><span class="sxs-lookup"><span data-stu-id="279e8-213">Declaring Commands and Controls with Ribbon Markup</span></span>](./windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="279e8-214">Instructions relatives à l’expérience utilisateur du ruban</span><span class="sxs-lookup"><span data-stu-id="279e8-214">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="279e8-215">Processus de conception du ruban</span><span class="sxs-lookup"><span data-stu-id="279e8-215">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 




