---
description: Cet exemple montre comment utiliser l’analyse de l’encre pour créer une application de remplissage de formulaires, où le formulaire est basé sur un formulaire papier numérisé.
ms.assetid: 1eae5962-b4e0-4947-a6d2-63713a68198c
title: Formulaire papier analysé par l’analyse d’encre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94d366c77e19bd5c32d3d1e4efa286cb3b089ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201261"
---
# <a name="ink-analysis-scanned-paper-form"></a><span data-ttu-id="d3802-103">Formulaire papier analysé par l’analyse d’encre</span><span class="sxs-lookup"><span data-stu-id="d3802-103">Ink Analysis Scanned Paper Form</span></span>

<span data-ttu-id="d3802-104">Cet exemple montre comment utiliser l’analyse de l’encre pour créer une application de remplissage de formulaires, où le formulaire est basé sur un formulaire papier numérisé.</span><span class="sxs-lookup"><span data-stu-id="d3802-104">This sample shows how to use Ink Analysis to create a form-filling application, where the form is based on a scanned paper form.</span></span>

## <a name="features-demonstrated"></a><span data-ttu-id="d3802-105">Fonctionnalités illustrées</span><span class="sxs-lookup"><span data-stu-id="d3802-105">Features Demonstrated</span></span>

<span data-ttu-id="d3802-106">Cet exemple d’application illustre les fonctionnalités suivantes de l’API d’analyse d’encre et des contrôles Windows Forms Ink :</span><span class="sxs-lookup"><span data-stu-id="d3802-106">This sample application demonstrates the following features of the Ink Analysis API and the Windows Forms Ink Controls:</span></span>

-   <span data-ttu-id="d3802-107">Chargement d’un formulaire papier numérisé.</span><span class="sxs-lookup"><span data-stu-id="d3802-107">Loading a scanned paper form.</span></span> <span data-ttu-id="d3802-108">L’exemple importe le formulaire à partir d’une image au format. png.</span><span class="sxs-lookup"><span data-stu-id="d3802-108">The sample imports the form from an image in .png format.</span></span>
-   <span data-ttu-id="d3802-109">Collecte et rendu de l’encre en haut du formulaire numérisé.</span><span class="sxs-lookup"><span data-stu-id="d3802-109">Collecting and rendering ink on top of the scanned form.</span></span>
-   <span data-ttu-id="d3802-110">Utilisation d’un objet [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) pour analyser l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="d3802-110">Using an [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) object to parse handwriting.</span></span>
-   <span data-ttu-id="d3802-111">Génération d’objets [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) pour améliorer les résultats de l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="d3802-111">Generating [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) objects to improve handwriting results.</span></span>
-   <span data-ttu-id="d3802-112">Remplissage des zones de texte à partir des indicateurs d’analyse.</span><span class="sxs-lookup"><span data-stu-id="d3802-112">Populating text boxes from analysis hints.</span></span>
-   <span data-ttu-id="d3802-113">Création d’une expérience de correction de texte de base.</span><span class="sxs-lookup"><span data-stu-id="d3802-113">Creating a basic text correction experience.</span></span>

## <a name="project-references"></a><span data-ttu-id="d3802-114">Références de projets</span><span class="sxs-lookup"><span data-stu-id="d3802-114">Project References</span></span>

<span data-ttu-id="d3802-115">L’exemple est disponible en tant qu’application Windows Forms ou Windows Presentation Foundation.</span><span class="sxs-lookup"><span data-stu-id="d3802-115">The sample is available as a Windows Forms or Windows Presentation Foundation application.</span></span> <span data-ttu-id="d3802-116">Les références de version du Windows Forms :</span><span class="sxs-lookup"><span data-stu-id="d3802-116">The Windows Forms version references:</span></span>

-   <span data-ttu-id="d3802-117">Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="d3802-117">Microsoft.Ink.dll</span></span>
-   <span data-ttu-id="d3802-118">Microsoft.Ink.Analysis.dll</span><span class="sxs-lookup"><span data-stu-id="d3802-118">Microsoft.Ink.Analysis.dll</span></span>

<span data-ttu-id="d3802-119">La version de Windows Presentation Foundation référence des IAWinFX.dll en plus des dll de Windows Presentation Foundation principales.</span><span class="sxs-lookup"><span data-stu-id="d3802-119">The Windows Presentation Foundation version references IAWinFX.dll in addition to the core Windows Presentation Foundation dlls.</span></span>

> [!Note]  
> <span data-ttu-id="d3802-120">La version Windows Presentation Foundation de cet exemple (qui se trouve dans le répertoire XAML) requiert que les extensions Windows Presentation Foundation pour Microsoft Visual Studio 2005 soient installées sur le système.</span><span class="sxs-lookup"><span data-stu-id="d3802-120">The Windows Presentation Foundation version of this sample (found in the XAML directory) requires that the Windows Presentation Foundation extensions for Microsoft Visual Studio 2005 is installed on the system.</span></span>

 

## <a name="user-interface"></a><span data-ttu-id="d3802-121">Interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="d3802-121">User Interface</span></span>

<span data-ttu-id="d3802-122">L’interface utilisateur de cette application se compose d’un [TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) avec deux objets [TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) associés : forme manuscrite et texte converti.</span><span class="sxs-lookup"><span data-stu-id="d3802-122">The UI for this application consists of a [TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) with two [TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) objects associated with it: Ink Form and Converted Text Form.</span></span> <span data-ttu-id="d3802-123">L’onglet de formulaire manuscrit contient</span><span class="sxs-lookup"><span data-stu-id="d3802-123">The Ink Form tab contains</span></span>

-   <span data-ttu-id="d3802-124">Panneau qui contient une image d’un formulaire papier numérisé utilisé pour la capture de messages téléphoniques.</span><span class="sxs-lookup"><span data-stu-id="d3802-124">A panel that contains an image of a scanned paper form used for taking telephone messages.</span></span>
-   <span data-ttu-id="d3802-125">Une case à cocher avec l’application affiche les limites de l’indicateur d’analyse lorsqu’elle est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="d3802-125">A check box that has the application show the analysis hint bounds when selected.</span></span>
-   <span data-ttu-id="d3802-126">Paire de boutons, Clear et Analyze, qui effacent l’encre du formulaire et initialisent l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="d3802-126">A pair of buttons, Clear and Analyze, that clear the ink from the form and initialize ink analysis.</span></span>

<span data-ttu-id="d3802-127">La forme texte convertie contient la même image et est la page sur laquelle l’application affiche le texte reconnu.</span><span class="sxs-lookup"><span data-stu-id="d3802-127">The Converted Text Form contains the same image and is the page on which the application displays the recognized text.</span></span> <span data-ttu-id="d3802-128">Lorsque vous cliquez sur analyser, l’application effectue une analyse de l’encre de façon synchrone et les résultats de la reconnaissance s’affichent sous l’onglet texte converti.</span><span class="sxs-lookup"><span data-stu-id="d3802-128">When you click Analyze, the application performs ink analysis synchronously, and the recognition results appear on the Converted Text Form tab.</span></span>

## <a name="functionality"></a><span data-ttu-id="d3802-129">Fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="d3802-129">Functionality</span></span>

<span data-ttu-id="d3802-130">Cette application utilise un [InkOverlay](/previous-versions/ms552322(v=vs.100)) pour permettre l’écriture.</span><span class="sxs-lookup"><span data-stu-id="d3802-130">This application uses an [InkOverlay](/previous-versions/ms552322(v=vs.100)) to enable writing.</span></span> <span data-ttu-id="d3802-131">L’objet InkOverlay est bien adapté aux prises de notes et au griffonnage de base.</span><span class="sxs-lookup"><span data-stu-id="d3802-131">The InkOverlay object is well suited for note taking and basic scribbling.</span></span> <span data-ttu-id="d3802-132">L’utilisation principale prévue de cet objet est d’afficher l’encre sous forme d’encre.</span><span class="sxs-lookup"><span data-stu-id="d3802-132">The primary intended use of this object is to display ink as ink.</span></span> <span data-ttu-id="d3802-133">La classe principale pour l’analyse de l’encre est la classe [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="d3802-133">The main class for ink analysis is the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) class.</span></span> <span data-ttu-id="d3802-134">Lorsque vous appelez la méthode [analyze](/previous-versions/ms568971(v=vs.100)) de l’objet InkAnalyzer, l’analyse de l’encre se produit de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="d3802-134">When you call the InkAnalyzer object's [Analyze](/previous-versions/ms568971(v=vs.100)) method, the ink analysis occurs synchronously.</span></span>

<span data-ttu-id="d3802-135">L’application initialise deux tableaux, l’un des chaînes et l’autre les rectangles.</span><span class="sxs-lookup"><span data-stu-id="d3802-135">The application initializes two arrays, one of strings and one of rectangles.</span></span> <span data-ttu-id="d3802-136">Le tableau de chaînes, `factoidStrings` , est constitué d’objets [Factoid](/previous-versions/ms583657(v=vs.100)) qui sont passés dans le [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) en tant qu’objets [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="d3802-136">The string array, `factoidStrings`, is made of [Factoid](/previous-versions/ms583657(v=vs.100)) objects that are passed into the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) as [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) objects.</span></span> <span data-ttu-id="d3802-137">Les objets AnalysisHintNode biaisent le InkAnalyzer vers une entrée particulière.</span><span class="sxs-lookup"><span data-stu-id="d3802-137">The AnalysisHintNode objects bias the InkAnalyzer toward particular input.</span></span> <span data-ttu-id="d3802-138">Cet exemple utilise les indicateurs de date, d’heure et de téléphone, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="d3802-138">This sample uses the date, time, and telephone hints, as well as some others.</span></span>

<span data-ttu-id="d3802-139">Chaque [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) est associé à une zone spécifique du formulaire.</span><span class="sxs-lookup"><span data-stu-id="d3802-139">Each [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) is associated with a specific area of the form.</span></span> <span data-ttu-id="d3802-140">Les zones sont représentées par le tableau de rectangles, `rects` .</span><span class="sxs-lookup"><span data-stu-id="d3802-140">The areas are represented by the array of rectangles, `rects`.</span></span> <span data-ttu-id="d3802-141">En créant une [zone](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) de texte pour chaque rectangle, l’exemple génère le texte reconnu à l’emplacement approprié.</span><span class="sxs-lookup"><span data-stu-id="d3802-141">By creating a [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) for each rectangle, the sample outputs the recognized text in the correct location.</span></span>


```C++
        private void InitHints()
        {
            // Instantiate the collection of TextBoxes.
            this.textBoxes = new ArrayList();

            // For each Rectangle in Rectangles
            for (int i = 0; i < rects.Length; i++)
            {

                Rectangle rectangle = rects[i];

                // Create an AnalysisHintNode with the bounds of the Rectangle.  The bounds
                // of an AnalysisHintNode gives clues to the handwriting recognizer about
                // the way Strokes are grouped together.
                AnalysisHintNode hint = this.analyzer.CreateAnalysisHint(rectangle);

                // Set the corresponding Factoid on the AnalysisHintNode.  This gives the 
                // recognizer clues about the meaning of the strokes within the 
                // AnalysisHintNode's region.
                hint.Factoid = factoidStrings[i];

                // Create a corresponding TextBox where the results of the analysis
                // associated with this AnalysisHintNode will be displayed.  Store the reference
                // to the TextBox in the textBoxes Collection.
                this.textBoxes.Add(InitTextBox(hint));
            }
        }
```



<span data-ttu-id="d3802-142">Après cela, il suffit de créer un gestionnaire d’événements qui déclenche l’analyse de l’encre lorsque l’utilisateur clique sur analyser.</span><span class="sxs-lookup"><span data-stu-id="d3802-142">After that, it is merely a matter of creating an event handler that triggers the ink analysis when the user clicks Analyze.</span></span>


```C++
        private void UpdateTextBoxes()
        {
            // Get the AnalysisHintNodes that we previously added to the InkAnalyzer.
            ContextNodeCollection hints = this.analyzer.GetAnalysisHints();

            for (int i = 0; i < hints.Count; i++)
            {
                // Get the recognized string from the AnalysisHintNode
                string analyzedString = ((AnalysisHintNode)hints[i]).GetRecognizedString();

                // If we found a string, set the contents of the TextBox
                // to that string.
                if (analyzedString != null)
                {
                    ((TextBox)this.textBoxes[i]).Text = analyzedString;
                }
            }
        }
```



 

 
