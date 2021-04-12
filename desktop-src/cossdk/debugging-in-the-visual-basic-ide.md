---
description: L’utilisation de l’environnement de développement intégré (IDE) de Microsoft Visual Basic pour le débogage offre aux développeurs Visual Basic accès à des outils familiers et à une facilité d’utilisation.
ms.assetid: d31efc97-c286-434d-93f5-77b34ec16205
title: Débogage dans l’IDE Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74574fdb289e1ad334337f17943c6961b95bf288
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393003"
---
# <a name="debugging-in-the-visual-basic-ide"></a><span data-ttu-id="10e15-103">Débogage dans l’IDE Visual Basic</span><span class="sxs-lookup"><span data-stu-id="10e15-103">Debugging in the Visual Basic IDE</span></span>

<span data-ttu-id="10e15-104">L’utilisation de l’environnement de développement intégré (IDE) de Microsoft Visual Basic pour le débogage offre aux développeurs Visual Basic accès à des outils familiers et à une facilité d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="10e15-104">Using the Microsoft Visual Basic integrated development environment (IDE) for debugging gives Visual Basic developers access to familiar tools and ease-of-use.</span></span> <span data-ttu-id="10e15-105">Si de nombreux composants finiront par être plus complètement débogués à l’aide de l’environnement Microsoft Visual C++, une stratégie peut consister à déboguer autant de fonctionnalités que possible avec Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="10e15-105">While many components will eventually need to be more fully debugged using the Microsoft Visual C++ environment, one strategy might be to first debug as much functionality as possible with Visual Basic.</span></span> <span data-ttu-id="10e15-106">Par exemple, vous pouvez utiliser l’IDE Visual Basic pour le débogage dans COM+ lorsque vous n’êtes pas encore en train de déboguer le multithreading, le suivi des composants, les appels distants ou l’isolation des processus.</span><span class="sxs-lookup"><span data-stu-id="10e15-106">For example, you might want to use the Visual Basic IDE for debugging within COM+ when you aren't yet debugging multithreading, component tracking, remote calls, or process isolation.</span></span>

<span data-ttu-id="10e15-107">En général, lors de l’utilisation de l’environnement de Visual Basic pour le débogage, vous devez d’abord compiler le projet et ajouter la DLL à une application COM+.</span><span class="sxs-lookup"><span data-stu-id="10e15-107">In general, when using the Visual Basic environment for debugging, you first compile the project and add the DLL to a COM+ application.</span></span> <span data-ttu-id="10e15-108">Vous définissez ensuite la compatibilité binaire pour le projet, en référençant la DLL que vous avez créée et démarrez le projet pour commencer le débogage.</span><span class="sxs-lookup"><span data-stu-id="10e15-108">Then you set binary compatibility for the project, referencing the DLL you made, and start the project to begin debugging.</span></span>

## <a name="general-guidelines-for-debugging-in-the-visual-basic-environment"></a><span data-ttu-id="10e15-109">Instructions générales pour le débogage dans l’environnement de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="10e15-109">General Guidelines for Debugging in the Visual Basic Environment</span></span>

-   <span data-ttu-id="10e15-110">Lors du débogage à l’aide de Visual Basic, COM+ traite les composants Visual Basic comme s’ils appartenaient à une application de bibliothèque, même si les composants sont inscrits comme appartenant à une application serveur.</span><span class="sxs-lookup"><span data-stu-id="10e15-110">While you are debugging using Visual Basic, COM+ treats the Visual Basic components as if they belong to a library application, even if the components are registered as belonging to a server application.</span></span> <span data-ttu-id="10e15-111">Étant donné qu’il s’exécute en tant qu’application de bibliothèque, les icônes de composant dans l’outil d’administration Services de composants ne s’exécutent pas lorsque les composants sont débogués.</span><span class="sxs-lookup"><span data-stu-id="10e15-111">Because it runs as a library application, the component icons in the Component Services administrative tool do not spin as the components are debugged.</span></span>
-   <span data-ttu-id="10e15-112">Si vous modifiez les attributs de transaction sur un composant pendant le débogage ou que vous modifiez le code source qui requiert Visual Basic pour générer un nouveau CLSID ou ProgID, veillez à supprimer et réinstaller l’application COM+ contenant le composant.</span><span class="sxs-lookup"><span data-stu-id="10e15-112">If you change transaction attributes on a component during debugging or make a source code change that requires Visual Basic to generate a new CLSID or ProgID, be sure to delete and reinstall the COM+ application containing the component.</span></span> <span data-ttu-id="10e15-113">Si vous avez défini la compatibilité binaire pour le composant, vous êtes averti que des modifications ont été apportées.</span><span class="sxs-lookup"><span data-stu-id="10e15-113">If you have set binary compatibility for the component, you will be warned that changes have occurred.</span></span>

## <a name="notes-on-debugging-within-a-com-application"></a><span data-ttu-id="10e15-114">Remarques sur le débogage dans une application COM+</span><span class="sxs-lookup"><span data-stu-id="10e15-114">Notes on Debugging Within a COM+ Application</span></span>

-   <span data-ttu-id="10e15-115">Si vous apportez des modifications dans l’IDE Visual Basic dans les interfaces de votre composant, les noms de classe, les noms de projet, la prise en charge transactionnelle ou d’autres paramètres, il peut y avoir des incompatibilités entre les données de configuration dans l’Explorateur de services de composants et la configuration réelle en cours d’exécution dans le débogueur Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="10e15-115">If you make changes in the Visual Basic IDE in your component's interfaces, class names, project names, transactional support or other settings, there may be mismatches between the configuration data in the Component Services explorer and the actual configuration running in the Visual Basic debugger.</span></span>
-   <span data-ttu-id="10e15-116">N’exportez pas une application COM+ pendant que vous déboguez un composant dans l’application.</span><span class="sxs-lookup"><span data-stu-id="10e15-116">Do not export a COM+ application while you are debugging a component in the application.</span></span> <span data-ttu-id="10e15-117">COM+ traitera l’environnement de développement Visual Basic en tant que composant.</span><span class="sxs-lookup"><span data-stu-id="10e15-117">COM+ will treat the Visual Basic development environment as the component.</span></span>
-   <span data-ttu-id="10e15-118">Si vous exécutez un composant en dehors du débogueur et décidez ensuite de commencer le débogage, une instance du composant peut toujours s’exécuter dans COM+ lorsque vous le démarrez dans le débogueur.</span><span class="sxs-lookup"><span data-stu-id="10e15-118">If you are running a component outside the debugger and then decide to begin debugging, an instance of the component may still be running in COM+ when you start it in the debugger.</span></span> <span data-ttu-id="10e15-119">COM+ détecte cette condition et tente d’arrêter silencieusement l’instance qu’il contrôle.</span><span class="sxs-lookup"><span data-stu-id="10e15-119">COM+ will detect this condition and attempt to silently shut down the instance it controls.</span></span> <span data-ttu-id="10e15-120">Pour éviter ce problème, supprimez le composant de l’outil d’administration Services de composants avant de commencer le débogage.</span><span class="sxs-lookup"><span data-stu-id="10e15-120">To avoid this problem, remove the component from the Component Services administrative tool before you begin debugging.</span></span>

<span data-ttu-id="10e15-121">**Pour déboguer à l’aide de l’environnement Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="10e15-121">**To debug using the Visual Basic environment**</span></span>

1.  <span data-ttu-id="10e15-122">Ouvrez le projet de composant dans Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="10e15-122">Open the component project in Visual Basic.</span></span>

2.  <span data-ttu-id="10e15-123">Compilez votre composant, puis définissez la compatibilité binaire de votre projet sur le composant compilé.</span><span class="sxs-lookup"><span data-stu-id="10e15-123">Compile your component, and then set binary compatibility in your project to the compiled component.</span></span>

3.  <span data-ttu-id="10e15-124">Affectez à la propriété MTSTransactionMode une valeur différente de 0-NotAnMTSObject.</span><span class="sxs-lookup"><span data-stu-id="10e15-124">Set the MTSTransactionMode property to a value other than 0 - NotAnMTSObject.</span></span> <span data-ttu-id="10e15-125">Quand vous démarrez le projet, ce paramètre invite Visual Basic à activer votre composant dans COM+.</span><span class="sxs-lookup"><span data-stu-id="10e15-125">When you start the project, this setting prompts Visual Basic to activate your component within COM+.</span></span>

4.  <span data-ttu-id="10e15-126">Dans le menu **projet** , cliquez sur **Propriétés**, puis entrez le programme Démarrer sous l’onglet **débogage** . Le programme de démarrage est l’exécutable client qui appelle ce composant.</span><span class="sxs-lookup"><span data-stu-id="10e15-126">From the **Project** menu, click **Properties**, and then enter the start program on the **Debugging** tab. The start program is the client executable that calls this component.</span></span>

    > [!Note]  
    > <span data-ttu-id="10e15-127">Le programme de démarrage doit être local pour le composant que vous déboguez.</span><span class="sxs-lookup"><span data-stu-id="10e15-127">The start program must be local to the component you are debugging.</span></span>

     

5.  <span data-ttu-id="10e15-128">Appuyez sur la touche F5 pour commencer le débogage du composant.</span><span class="sxs-lookup"><span data-stu-id="10e15-128">Press the F5 key to begin debugging the component.</span></span>

<span data-ttu-id="10e15-129">Une fois que vous avez appuyé sur F5, Visual Basic lance l’application cliente et exécute le composant en mode débogage.</span><span class="sxs-lookup"><span data-stu-id="10e15-129">After you press F5, Visual Basic launches the client application and runs the component in debug mode.</span></span> <span data-ttu-id="10e15-130">Vous pouvez placer des points d’arrêt dans le code du composant et définir des espions sur des variables.</span><span class="sxs-lookup"><span data-stu-id="10e15-130">You can place breakpoints in the component's code and set watches on variables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10e15-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="10e15-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10e15-132">Prise en charge du débogage des Visual Basic COM+ avec MTS</span><span class="sxs-lookup"><span data-stu-id="10e15-132">COM+ Visual Basic Debugging Support Contrasted with MTS</span></span>](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[<span data-ttu-id="10e15-133">Débogage de composants Visual Basic compilés</span><span class="sxs-lookup"><span data-stu-id="10e15-133">Debugging Compiled Visual Basic Components</span></span>](debugging-compiled-visual-basic-components.md)
</dt> </dl>

 

 



