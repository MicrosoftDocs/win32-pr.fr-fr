---
description: Cette application montre comment vous pouvez créer une application de reconnaissance de l’écriture manuscrite. Le kit de développement logiciel (SDK) Windows Vista fournit également des versions de cet exemple en C \# et Visual Basic .net.
ms.assetid: 4b3fc078-731e-4263-8e95-2c273d69a457
title: Exemple de reconnaissance manuscrite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d97d9d15ef64a3d7a1fe1fc5d45b3cb0454ba7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201394"
---
# <a name="ink-recognition-sample"></a><span data-ttu-id="bdf39-103">Exemple de reconnaissance manuscrite</span><span class="sxs-lookup"><span data-stu-id="bdf39-103">Ink Recognition Sample</span></span>

<span data-ttu-id="bdf39-104">Cette application montre comment vous pouvez créer une application de reconnaissance de l’écriture manuscrite. Le kit de développement logiciel (SDK) Windows Vista fournit également des versions de cet exemple en C \# et Visual Basic .net.</span><span class="sxs-lookup"><span data-stu-id="bdf39-104">This application demonstrates how you can build a handwriting recognition application.The Windows Vista SDK provides versions of this sample in C\# and Visual Basic .NET, as well.</span></span> <span data-ttu-id="bdf39-105">Cette rubrique fait référence à l’exemple .NET Visual Basic, mais les concepts sont les mêmes entre les versions.</span><span class="sxs-lookup"><span data-stu-id="bdf39-105">This topic refers to the Visual Basic .NET sample, but the concepts are the same between versions.</span></span>

## <a name="access-the-tablet-pc-interfaces"></a><span data-ttu-id="bdf39-106">Accéder aux interfaces Tablet PC</span><span class="sxs-lookup"><span data-stu-id="bdf39-106">Access the Tablet PC Interfaces</span></span>

<span data-ttu-id="bdf39-107">Tout d’abord, référencez l’API Tablet PC qui est installée avec le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="bdf39-107">First, reference the Tablet PC API, which are installed with the SDK.</span></span>


```VB
' The Ink namespace, which contains the Tablet PC Platform API
Imports Microsoft.Ink
```



## <a name="initialize-the-inkcollector"></a><span data-ttu-id="bdf39-108">Initialiser le InkCollector</span><span class="sxs-lookup"><span data-stu-id="bdf39-108">Initialize the InkCollector</span></span>

<span data-ttu-id="bdf39-109">L’exemple ajoute du code au gestionnaire d’événements [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) du formulaire qui sert à associer le [InkCollector](/previous-versions/ms583683(v=vs.100)), myInkCollector, à la fenêtre de la zone de groupe et à activer le InkCollector.</span><span class="sxs-lookup"><span data-stu-id="bdf39-109">The sample adds code to the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler that serves to associate the [InkCollector](/previous-versions/ms583683(v=vs.100)), myInkCollector, with the group box window and enable the InkCollector.</span></span>


```VB
Private Sub InkRecognition_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load

   ' Create the recognizers collection
    myRecognizers = New Recognizers()

    ' Create an ink collector that uses the group box handle
    myInkCollector = New InkCollector(gbInkArea.Handle)

    ' Turn the ink collector on
    myInkCollector.Enabled = True

End Sub
```



## <a name="recognize-the-strokes"></a><span data-ttu-id="bdf39-110">Reconnaître les traits</span><span class="sxs-lookup"><span data-stu-id="bdf39-110">Recognize the Strokes</span></span>

<span data-ttu-id="bdf39-111">Le gestionnaire d’événements [Click](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) de l’objet [Button](/dotnet/api/system.windows.forms.button?view=netcore-3.1) vérifie que l’utilisateur dispose d’au moins un module de reconnaissance, en examinant la propriété [Count](/previous-versions/ms828521(v=msdn.10)) de la collection [Recognizers](/previous-versions/ms828520(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="bdf39-111">The [Button](/dotnet/api/system.windows.forms.button?view=netcore-3.1) object's [Click](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) event handler checks to ensure that the user has at least one recognizer installed by examining the [Count](/previous-versions/ms828521(v=msdn.10)) property of the [Recognizers](/previous-versions/ms828520(v=msdn.10)) collection.</span></span>

<span data-ttu-id="bdf39-112">La propriété [SelectedText](/previous-versions/windows/) de la zone de texte est définie sur la meilleure correspondance pour les traits à l’aide de la méthode [ToString](/previous-versions/ms827836(v=msdn.10)) sur la collection de [traits](/previous-versions/ms552701(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="bdf39-112">The [SelectedText](/previous-versions/windows/) property of the text box is set to the best match for the strokes using the [ToString](/previous-versions/ms827836(v=msdn.10)) method on the [Strokes](/previous-versions/ms552701(v=vs.100)) collection.</span></span> <span data-ttu-id="bdf39-113">Une fois les traits reconnus, ils sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="bdf39-113">After the strokes have been recognized, they are deleted.</span></span> <span data-ttu-id="bdf39-114">Enfin, le code force la redessin de la zone de dessin, en l’effaçant pour une utilisation manuscrite plus poussée.</span><span class="sxs-lookup"><span data-stu-id="bdf39-114">Finally, the code forces drawing area repaint, clearing it for further ink use.</span></span>


```VB
Private Sub btnRecognize_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles btnRecognize.Click

    ' Check to ensure that the user has at least one recognizer installed
    ' Note that this is a preventive check - otherwise, an exception 
    ' occurs during recognition
    If 0 = myRecognizers.Count Then
        MessageBox.Show("There are no handwriting recognizers installed.  You need to have at least one in order to run this sample.")
    Else
        ' ...
        txtResults.SelectedText = myInkCollector.Ink.Strokes.ToString

        ' If the mouse is pressed, do not perform the recognition -
        ' this prevents deleting a stroke that is still being drawn
        If Not myInkCollector.CollectingInk Then

            ' Delete the ink from the ink collector
            myInkCollector.Ink.DeleteStrokes(myInkCollector.Ink.Strokes)

            ' Force the Frame to redraw (so the deleted ink goes away)
            gbInkArea.Refresh()

        End If
    End If
End Sub
```



## <a name="closing-the-form"></a><span data-ttu-id="bdf39-115">Fermeture du formulaire</span><span class="sxs-lookup"><span data-stu-id="bdf39-115">Closing the Form</span></span>

<span data-ttu-id="bdf39-116">La méthode dispose du formulaire [supprime](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) l’objet [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="bdf39-116">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>

 

 
