---
title: Routines de vérification personnalisées
description: Cette section décrit comment créer une routine de vérification personnalisée pour l’outil de vérification de l’accessibilité de l’interface utilisateur (AccChecker).
ms.assetid: 56F3EA1F-39C3-4DD9-8F2B-0C3608DD8737
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d66ad2fe0e27d16b55dd2d50d367250aadd15c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939746"
---
# <a name="custom-verification-routines"></a><span data-ttu-id="ee000-103">Routines de vérification personnalisées</span><span class="sxs-lookup"><span data-stu-id="ee000-103">Custom Verification Routines</span></span>

<span data-ttu-id="ee000-104">Cette section décrit comment créer une routine de vérification personnalisée pour l’outil de vérification de l’accessibilité de l’interface utilisateur (AccChecker).</span><span class="sxs-lookup"><span data-stu-id="ee000-104">This section describes how to create a custom verification routine for the UI Accessibility Checker (AccChecker) tool.</span></span>

-   [<span data-ttu-id="ee000-105">Création d’une vérification personnalisée</span><span class="sxs-lookup"><span data-stu-id="ee000-105">Creating a Custom Verification</span></span>](#creating-a-custom-verification)
    -   [<span data-ttu-id="ee000-106">Exemple de vérification personnalisée</span><span class="sxs-lookup"><span data-stu-id="ee000-106">Sample Custom Verification</span></span>](#sample-custom-verification)
-   [<span data-ttu-id="ee000-107">Utilisation d’une vérification personnalisée</span><span class="sxs-lookup"><span data-stu-id="ee000-107">Using a Custom Verification</span></span>](#using-a-custom-verification)
    -   [<span data-ttu-id="ee000-108">Interface utilisateur graphique (GUI) AccChecker</span><span class="sxs-lookup"><span data-stu-id="ee000-108">The AccChecker Graphical User Interface (GUI)</span></span>](#the-accchecker-graphical-user-interface-gui)
    -   [<span data-ttu-id="ee000-109">AccChecker Automation</span><span class="sxs-lookup"><span data-stu-id="ee000-109">AccChecker Automation</span></span>](#accchecker-automation)
-   [<span data-ttu-id="ee000-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ee000-110">Related topics</span></span>](#related-topics)

<span data-ttu-id="ee000-111">L’outil de vérification de l’accessibilité de l’interface utilisateur (AccChecker) est un outil de test d’accessibilité conçu pour vérifier l’implémentation de Microsoft Active Accessibility (MSAA) dans une interface utilisateur de contrôle ou d’application.</span><span class="sxs-lookup"><span data-stu-id="ee000-111">UI Accessibility Checker (AccChecker) is an accessibility test tool designed to verify the implementation of Microsoft Active Accessibility (MSAA) in a control or application UI.</span></span> <span data-ttu-id="ee000-112">Les problèmes d’accessibilité ayant un impact élevé qui peuvent être exposés par l’implémentation MSAA sont testés avec un ensemble de routines de vérification automatisées intégrées.</span><span class="sxs-lookup"><span data-stu-id="ee000-112">High impact accessibility issues that might be exposed by the MSAA implementation are tested with a set of built-in automated verification routines.</span></span> <span data-ttu-id="ee000-113">Ces routines de vérification natives peuvent être complétées par des routines personnalisées à l’aide de la plateforme AccChecker extensible.</span><span class="sxs-lookup"><span data-stu-id="ee000-113">These native verification routines can be augmented with customized routines using the extensible AccChecker platform.</span></span>

## <a name="creating-a-custom-verification"></a><span data-ttu-id="ee000-114">Création d’une vérification personnalisée</span><span class="sxs-lookup"><span data-stu-id="ee000-114">Creating a Custom Verification</span></span>

<span data-ttu-id="ee000-115">Une vérification personnalisée est créée sous la forme d’une bibliothèque de classes (DLL) qui implémente une interface unique ( `IVerificationRoutine` ) contenant un membre ( `Execute` ) :</span><span class="sxs-lookup"><span data-stu-id="ee000-115">A custom verification is built as a class library (DLL) that implements a single interface (`IVerificationRoutine`) containing one member (`Execute`):</span></span>


```CSharp
void Execute(
    System.IntPtr hwnd, 
    AccCheck.Logging.ILogger logger, 
    bool AllowUI, 
    AccCheck.GraphicsHelper graphics
);
```



<span data-ttu-id="ee000-116">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="ee000-116">**Parameters**</span></span>

<span data-ttu-id="ee000-117">*HWND*</span><span class="sxs-lookup"><span data-stu-id="ee000-117">*hwnd*</span></span>

<span data-ttu-id="ee000-118">Type : **System. IntPtr**</span><span class="sxs-lookup"><span data-stu-id="ee000-118">Type: **System.IntPtr**</span></span>

<span data-ttu-id="ee000-119">HWND de l’élément en cours de vérification.</span><span class="sxs-lookup"><span data-stu-id="ee000-119">The HWND of the element being verified.</span></span>

<span data-ttu-id="ee000-120">*suivi*</span><span class="sxs-lookup"><span data-stu-id="ee000-120">*logger*</span></span>

<span data-ttu-id="ee000-121">Tapez : **AccCheck. Logging. ILogger**</span><span class="sxs-lookup"><span data-stu-id="ee000-121">Type: **AccCheck.Logging.ILogger**</span></span>

<span data-ttu-id="ee000-122">Méthode de journalisation sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="ee000-122">The selected logging method.</span></span> <span data-ttu-id="ee000-123">Parmi les types possibles, citons **AccumulatingLogger** (utilisé par AccChecker pour mettre en cache toutes les entrées de journal jusqu’à ce que les vérifications soient terminées), **ConsoleLogger**, **TextFileLogger** et **XMLSerializingLogger**.</span><span class="sxs-lookup"><span data-stu-id="ee000-123">Possible types include **AccumulatingLogger** (used by AccChecker to cache all log entries until verifications are complete), **ConsoleLogger**, **TextFileLogger**, and **XMLSerializingLogger**.</span></span>

<span data-ttu-id="ee000-124">*AllowUI*</span><span class="sxs-lookup"><span data-stu-id="ee000-124">*AllowUI*</span></span>

<span data-ttu-id="ee000-125">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="ee000-125">Type: **bool**</span></span>

<span data-ttu-id="ee000-126">Indique si la routine de vérification affiche l’interface utilisateur testée.</span><span class="sxs-lookup"><span data-stu-id="ee000-126">Indicates whether the verification routine displays the UI it is testing.</span></span> <span data-ttu-id="ee000-127">Généralement défini sur false dans les scénarios de test automatisé.</span><span class="sxs-lookup"><span data-stu-id="ee000-127">Generally set to false in automated testing scenarios.</span></span>

<span data-ttu-id="ee000-128">*graphismes*</span><span class="sxs-lookup"><span data-stu-id="ee000-128">*graphics*</span></span>

<span data-ttu-id="ee000-129">Tapez : **AccCheck. GraphicsHelper**</span><span class="sxs-lookup"><span data-stu-id="ee000-129">Type: **AccCheck.GraphicsHelper**</span></span>

<span data-ttu-id="ee000-130">Utilisé pour les captures d’écran et autres visualisations dans AccChecker.</span><span class="sxs-lookup"><span data-stu-id="ee000-130">Used for screenshots and other visualizations within AccChecker.</span></span>

### <a name="sample-custom-verification"></a><span data-ttu-id="ee000-131">Exemple de vérification personnalisée</span><span class="sxs-lookup"><span data-stu-id="ee000-131">Sample Custom Verification</span></span>

<span data-ttu-id="ee000-132">L’exemple suivant est une vérification personnalisée C# qui effectue une vérification de la profondeur d’une arborescence d’éléments simple.</span><span class="sxs-lookup"><span data-stu-id="ee000-132">The following example is a C# custom verification that performs a simple element tree depth check.</span></span> <span data-ttu-id="ee000-133">Une erreur est consignée si l’arborescence d’éléments est supérieure à 50 niveaux, un avertissement est consigné si l’arborescence des éléments est comprise entre 20 et 50 niveaux et un message d’information est enregistré dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ee000-133">An error is logged if the element tree is greater than 50 levels deep, a warning is logged if the element tree is 20 to 50 levels deep, and an informational message is logged otherwise.</span></span>


```CSharp
using System;
using System.Collections.Generic;
using System.Text;
using AccCheck;
using AccCheck.Logging;
using AccCheck.Verification;

namespace VerificationRoutines
{
    \\ Verification routine attributes.
    \\ If these values are not specified, the verification will not be displayed in the 
    \\ AccChecker UI. However, it is still loaded and will be included in all subsequent 
    \\ verification runs since it cannot be unchecked and excluded.
    [Verification(
        // Title - the title of the verification routine.
        "Sample Check Tree Depth",
        // Description - this attribute is not currently displayed.
        "Checks that the accessibility tree isn't excessively deep.",
        // Group Title - the verification group to add the routine. This can be a new or 
        //  existing group.
        Group = "TreeDepthCheck"
        )]

    public class CheckTreeDepth : IVerificationRoutine
    {
        private const int S_OK = 0;
        private const int ERROR_TREE_DEPTH = 50;
        private const int WARNING_TREE_DEPTH = 20;
        private int _depth = 0;

        private void TraverseTree(Accessible parent, int level)
        {
            if (level > _depth)
            {
                _depth = level;
            }

            // never go deeper than ERROR_TREE_DEPTH, that's a sign of a loop
            if (_depth > ERROR_TREE_DEPTH)
            {
                return;
            }

            Accessible[] children;
            if (parent.Children(out children) == S_OK)
            {
                foreach (Accessible child in children)
                {
                    TraverseTree(child, level + 1);
                }
            }
        }

        public void Execute(IntPtr hwnd, ILogger logger, bool AllowUI, 
                GraphicsHelper graphics)
        {
            Accessible root;
            if (Accessible.FromWindow(hwnd, out root) == S_OK)
            {
                TraverseTree(root, 0);
            }
            else
            {
                return;
            }

            if (_depth >= ERROR_TREE_DEPTH)
            {
                logger.Log(new LogEvent(EventLevel.Error, "DepthCheck", String.Format(
                    "The tree is too deep; the tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
            else if (_depth >= WARNING_TREE_DEPTH)
            {
                logger.Log(new LogEvent(EventLevel.Warning, "DepthCheck", String.Format(
                    "The tree might be too deep; the tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
            else
            {
                logger.Log(new LogEvent(EventLevel.Information, "DepthCheck", String.Format(
                    "The tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
        }
    }
}
```



> [!Note]  
> <span data-ttu-id="ee000-134">Une solution Microsoft Visual Studio qui contient un exemple de code de vérification est incluse dans la documentation d’aide.</span><span class="sxs-lookup"><span data-stu-id="ee000-134">A Microsoft Visual Studio solution that contains verification sample code is included with the help documentation.</span></span> <span data-ttu-id="ee000-135">Les fichiers se trouvent dans le chemin d’installation de AccChecker.</span><span class="sxs-lookup"><span data-stu-id="ee000-135">The files are located in the AccChecker installation path.</span></span>

 

## <a name="using-a-custom-verification"></a><span data-ttu-id="ee000-136">Utilisation d’une vérification personnalisée</span><span class="sxs-lookup"><span data-stu-id="ee000-136">Using a Custom Verification</span></span>

<span data-ttu-id="ee000-137">Cette section décrit comment incorporer une vérification personnalisée dans les scénarios de test AccChecker.</span><span class="sxs-lookup"><span data-stu-id="ee000-137">This section describes how to incorporate a custom verification into AccChecker test scenarios.</span></span>

### <a name="the-accchecker-graphical-user-interface-gui"></a><span data-ttu-id="ee000-138">Interface utilisateur graphique (GUI) AccChecker</span><span class="sxs-lookup"><span data-stu-id="ee000-138">The AccChecker Graphical User Interface (GUI)</span></span>

<span data-ttu-id="ee000-139">Pour inclure une routine de vérification personnalisée dans l’application AccChecker, cliquez simplement sur Ouvrir la DLL dans le menu fichier et recherchez la DLL de la routine.</span><span class="sxs-lookup"><span data-stu-id="ee000-139">To include a custom verification routine in the AccChecker application, simply click Open DLL from the File menu and locate the DLL for the routine.</span></span> <span data-ttu-id="ee000-140">La routine personnalisée sera ajoutée au bas de la liste des vérifications dans le volet Sélectionner les routines de vérification.</span><span class="sxs-lookup"><span data-stu-id="ee000-140">The custom routine will be added to the bottom of the list of verifications in the Select verification routines pane.</span></span>

<span data-ttu-id="ee000-141">La capture d’écran suivante montre l’exemple de vérification personnalisée de profondeur d’arborescence de vérification ajoutée à AccChecker.</span><span class="sxs-lookup"><span data-stu-id="ee000-141">The following screen shot shows the Sample Check Tree Depth custom verification added to AccChecker.</span></span>

![exemple de la routine de vérification personnalisée de la profondeur de l’arborescence de vérification ajoutée à l’interface utilisateur accchecker](images/accchecker-sample-custom-verification.png)

> [!Note]  
> <span data-ttu-id="ee000-143">Si les valeurs d’attribut de vérification ne sont pas spécifiées dans la routine de vérification personnalisée, la vérification est toujours chargée dans AccChecker même si elle n’apparaît pas dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ee000-143">If the verification attribute values are not specified in the custom verification routine, the verification is still loaded into AccChecker even though it does not appear in the UI.</span></span> <span data-ttu-id="ee000-144">Étant donné qu’elle n’est pas affichée dans l’interface utilisateur, elle ne peut pas être désactivée et exclue des exécutions de vérification suivantes.</span><span class="sxs-lookup"><span data-stu-id="ee000-144">Since it is not displayed in the UI, it cannot be unchecked and excluded from subsequent verification runs.</span></span>

 

### <a name="accchecker-automation"></a><span data-ttu-id="ee000-145">AccChecker Automation</span><span class="sxs-lookup"><span data-stu-id="ee000-145">AccChecker Automation</span></span>

<span data-ttu-id="ee000-146">L’incorporation d’une routine de vérification personnalisée dans une infrastructure AccChecker automatisée est aussi simple que l’ajout de la DLL de vérification et l’activation des routines de vérification souhaitées.</span><span class="sxs-lookup"><span data-stu-id="ee000-146">Incorporating a custom verification routine into an automated AccChecker framework is as simple as adding the verification DLL and enabling the desired verification routines.</span></span>

<span data-ttu-id="ee000-147">L’extrait de code suivant montre comment utiliser l’API AccChecker pour tester la fonctionnalité de tabulation dans l’application du panneau de configuration du pare-feu Windows.</span><span class="sxs-lookup"><span data-stu-id="ee000-147">The following code snippet demonstrates how to use the AccChecker API to test tabbing functionality in the Windows Firewall control panel application.</span></span>


```CSharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using AccCheck.Logging;

public class TestCases : TestBase
{
    public void AccessibilityTestCase()
    {
        //  Get our user interface ready for AccChecker.
        Setup();

        //  AccChecker's class representing verifications that you can run.
        AccCheck.Verification.VerificationManager vm = new AccCheck.Verification.VerificationManager();

        //  Create a console logger to get output in the console.
        ConsoleLogger consoleLogger = new ConsoleLogger();

        //  Add the AccChecker Console Logger.
        vm.AddLogger(consoleLogger);

        //  Disable all verifications; all verifications are enabled by default.
        vm.DisableVerifications(AccCheck.Verification.VerificationFilter.All);

        // Add a custom verification DLL.
        vm.AddVerificationDll("CheckTreeDepthVerification.dll");
        
        // Enable the routine we want to run.
        vm.EnableRoutine("Sample Check Tree Depth");

        //  Run the verification routine against the firewall.
        vm.ExecuteEnabled(_fireWallHwnd);

        //  Check the logger to see if the verification failed.
        if (consoleLogger.ErrorCount > 0)
        {
            Console.WriteLine("Test failed!");
            Console.WriteLine("Error count = " + consoleLogger.ErrorCount);
        }

        // Clean up the user interface.
        Cleanup();
    }
}
```



> [!Note]  
> Une solution Microsoft Visual Studio 2008 qui contient un exemple de code de vérification est incluse dans la documentation d’aide. <span data-ttu-id="ee000-149">Les fichiers se trouvent dans le chemin d’installation de AccChecker.</span><span class="sxs-lookup"><span data-stu-id="ee000-149">The files are located in the AccChecker installation path.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ee000-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ee000-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee000-151">Vérificateur d’accessibilité de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="ee000-151">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




