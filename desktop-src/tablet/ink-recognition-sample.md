---
description: Cette application montre comment vous pouvez créer une application de reconnaissance de l’écriture manuscrite. le kit de développement logiciel (SDK) Windows Vista fournit également des versions de cet exemple en C \# et Visual Basic .net.
ms.assetid: 4b3fc078-731e-4263-8e95-2c273d69a457
title: Exemple de reconnaissance manuscrite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c151c92c9f407461c34ecffb015af179e57b5c9ed4735b36f70c9a4d26c78088
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935119"
---
# <a name="ink-recognition-sample"></a>Exemple de reconnaissance manuscrite

Cette application montre comment vous pouvez créer une application de reconnaissance de l’écriture manuscrite. le kit de développement logiciel (SDK) Windows Vista fournit également des versions de cet exemple en C \# et Visual Basic .net. cette rubrique fait référence à l’exemple .net Visual Basic, mais les concepts sont les mêmes entre les versions.

## <a name="access-the-tablet-pc-interfaces"></a>Accéder aux interfaces Tablet PC

Tout d’abord, référencez l’API Tablet PC qui est installée avec le kit de développement logiciel (SDK).


```VB
' The Ink namespace, which contains the Tablet PC Platform API
Imports Microsoft.Ink
```



## <a name="initialize-the-inkcollector"></a>Initialiser le InkCollector

L’exemple ajoute du code au gestionnaire d’événements [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) du formulaire qui sert à associer le [InkCollector](/previous-versions/ms583683(v=vs.100)), myInkCollector, à la fenêtre de la zone de groupe et à activer le InkCollector.


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



## <a name="recognize-the-strokes"></a>Reconnaître les traits

Le gestionnaire d’événements [Click](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) de l’objet [Button](/dotnet/api/system.windows.forms.button?view=netcore-3.1) vérifie que l’utilisateur dispose d’au moins un module de reconnaissance, en examinant la propriété [Count](/previous-versions/ms828521(v=msdn.10)) de la collection [Recognizers](/previous-versions/ms828520(v=msdn.10)) .

La propriété [SelectedText](/previous-versions/windows/) de la zone de texte est définie sur la meilleure correspondance pour les traits à l’aide de la méthode [ToString](/previous-versions/ms827836(v=msdn.10)) sur la collection de [traits](/previous-versions/ms552701(v=vs.100)) . Une fois les traits reconnus, ils sont supprimés. Enfin, le code force la redessin de la zone de dessin, en l’effaçant pour une utilisation manuscrite plus poussée.


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



## <a name="closing-the-form"></a>Fermeture du formulaire

La méthode dispose du formulaire [supprime](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) l’objet [InkCollector](/previous-versions/ms583683(v=vs.100)) .

 

 
