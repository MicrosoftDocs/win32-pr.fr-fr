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
# <a name="ink-analysis-scanned-paper-form"></a>Formulaire papier analysé par l’analyse d’encre

Cet exemple montre comment utiliser l’analyse de l’encre pour créer une application de remplissage de formulaires, où le formulaire est basé sur un formulaire papier numérisé.

## <a name="features-demonstrated"></a>Fonctionnalités illustrées

Cet exemple d’application illustre les fonctionnalités suivantes de l’API d’analyse d’encre et des contrôles Windows Forms Ink :

-   Chargement d’un formulaire papier numérisé. L’exemple importe le formulaire à partir d’une image au format. png.
-   Collecte et rendu de l’encre en haut du formulaire numérisé.
-   Utilisation d’un objet [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) pour analyser l’écriture manuscrite.
-   Génération d’objets [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) pour améliorer les résultats de l’écriture manuscrite.
-   Remplissage des zones de texte à partir des indicateurs d’analyse.
-   Création d’une expérience de correction de texte de base.

## <a name="project-references"></a>Références de projets

L’exemple est disponible en tant qu’application Windows Forms ou Windows Presentation Foundation. Les références de version du Windows Forms :

-   Microsoft.Ink.dll
-   Microsoft.Ink.Analysis.dll

La version de Windows Presentation Foundation référence des IAWinFX.dll en plus des dll de Windows Presentation Foundation principales.

> [!Note]  
> La version Windows Presentation Foundation de cet exemple (qui se trouve dans le répertoire XAML) requiert que les extensions Windows Presentation Foundation pour Microsoft Visual Studio 2005 soient installées sur le système.

 

## <a name="user-interface"></a>Interface utilisateur

L’interface utilisateur de cette application se compose d’un [TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) avec deux objets [TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) associés : forme manuscrite et texte converti. L’onglet de formulaire manuscrit contient

-   Panneau qui contient une image d’un formulaire papier numérisé utilisé pour la capture de messages téléphoniques.
-   Une case à cocher avec l’application affiche les limites de l’indicateur d’analyse lorsqu’elle est sélectionnée.
-   Paire de boutons, Clear et Analyze, qui effacent l’encre du formulaire et initialisent l’analyse de l’encre.

La forme texte convertie contient la même image et est la page sur laquelle l’application affiche le texte reconnu. Lorsque vous cliquez sur analyser, l’application effectue une analyse de l’encre de façon synchrone et les résultats de la reconnaissance s’affichent sous l’onglet texte converti.

## <a name="functionality"></a>Fonctionnalités

Cette application utilise un [InkOverlay](/previous-versions/ms552322(v=vs.100)) pour permettre l’écriture. L’objet InkOverlay est bien adapté aux prises de notes et au griffonnage de base. L’utilisation principale prévue de cet objet est d’afficher l’encre sous forme d’encre. La classe principale pour l’analyse de l’encre est la classe [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) . Lorsque vous appelez la méthode [analyze](/previous-versions/ms568971(v=vs.100)) de l’objet InkAnalyzer, l’analyse de l’encre se produit de façon synchrone.

L’application initialise deux tableaux, l’un des chaînes et l’autre les rectangles. Le tableau de chaînes, `factoidStrings` , est constitué d’objets [Factoid](/previous-versions/ms583657(v=vs.100)) qui sont passés dans le [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) en tant qu’objets [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) . Les objets AnalysisHintNode biaisent le InkAnalyzer vers une entrée particulière. Cet exemple utilise les indicateurs de date, d’heure et de téléphone, ainsi que d’autres.

Chaque [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) est associé à une zone spécifique du formulaire. Les zones sont représentées par le tableau de rectangles, `rects` . En créant une [zone](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) de texte pour chaque rectangle, l’exemple génère le texte reconnu à l’emplacement approprié.


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



Après cela, il suffit de créer un gestionnaire d’événements qui déclenche l’analyse de l’encre lorsque l’utilisateur clique sur analyser.


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



 

 
