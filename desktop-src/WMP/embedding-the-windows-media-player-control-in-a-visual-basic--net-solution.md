---
title: Intégration du contrôle du lecteur Windows Media dans une solution Visual Basic .NET
description: Intégration du contrôle du lecteur Windows Media dans une solution Visual Basic .NET
ms.assetid: e6428b42-5d8b-48ef-9f7a-c90a4625b745
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX, incorporation
- Windows Media Player, Visual Basic .NET
- Windows Media Player Object Model, Visual Basic .NET
- modèle objet, Visual Basic .NET
- Windows Media Player Mobile, Visual Basic .NET
- Contrôle ActiveX du lecteur Windows Media, Visual Basic .NET
- Contrôle ActiveX Windows Media Player Mobile, Visual Basic .NET
- Contrôle ActiveX, Visual Basic .NET
- incorporation, Visual Basic des programmes .NET
- Visual Basic l’incorporation de programmes .NET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d578b456a5064f1846ead7f074f178753dbc7c97
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2019
ms.locfileid: "104311689"
---
# <a name="embedding-the-windows-media-player-control-in-a-visual-basic-net-solution"></a><span data-ttu-id="8bf21-119">Intégration du contrôle du lecteur Windows Media dans une solution Visual Basic .NET</span><span class="sxs-lookup"><span data-stu-id="8bf21-119">Embedding the Windows Media Player Control in a Visual Basic .NET Solution</span></span>

<span data-ttu-id="8bf21-120">Pour utiliser les fonctionnalités du lecteur Windows Media série 9 ou version ultérieure dans une application Visual Basic .NET, ajoutez d’abord le composant à un formulaire comme décrit dans [utilisation du contrôle du lecteur Windows Media avec Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span><span class="sxs-lookup"><span data-stu-id="8bf21-120">To use the functionality of Windows Media Player 9 Series or later in a Visual Basic .NET application, first add the component to a form as described in [Using the Windows Media Player Control with Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span></span>

<span data-ttu-id="8bf21-121">Cette section décrit comment créer une application qui lit des vidéos et contient des boutons de lecture et d’arrêt personnalisés.</span><span class="sxs-lookup"><span data-stu-id="8bf21-121">This section describes how to create an application that plays video and has custom play and stop buttons.</span></span>

## <a name="add-the-video-window"></a><span data-ttu-id="8bf21-122">Ajouter la fenêtre vidéo</span><span class="sxs-lookup"><span data-stu-id="8bf21-122">Add the Video Window</span></span>

<span data-ttu-id="8bf21-123">Ajoutez le contrôle du lecteur Windows Media à un formulaire.</span><span class="sxs-lookup"><span data-stu-id="8bf21-123">Add the Windows Media Player control to a form.</span></span> <span data-ttu-id="8bf21-124">Redimensionnez le contrôle, puis placez-le à l’emplacement où vous souhaitez que la fenêtre vidéo apparaisse.</span><span class="sxs-lookup"><span data-stu-id="8bf21-124">Resize the control, and then place it where you want the video window to appear.</span></span>

<span data-ttu-id="8bf21-125">Sélectionnez le contrôle du lecteur Windows Media, puis modifiez la propriété **UIMODE** en « None ».</span><span class="sxs-lookup"><span data-stu-id="8bf21-125">Select the Windows Media Player control, then change the **uiMode** property to "none".</span></span> <span data-ttu-id="8bf21-126">Ce paramètre masque les contrôles d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8bf21-126">This setting hides the UI controls.</span></span> <span data-ttu-id="8bf21-127">Quand l’utilisateur lit une vidéo, elle s’affiche dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8bf21-127">When the user plays a video, it will appear in the window.</span></span> <span data-ttu-id="8bf21-128">Pour le contenu audio uniquement, une visualisation s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8bf21-128">For audio-only content, a visualization will appear.</span></span>

## <a name="add-two-buttons-and-adjust-the-form"></a><span data-ttu-id="8bf21-129">Ajouter deux boutons et ajuster le formulaire</span><span class="sxs-lookup"><span data-stu-id="8bf21-129">Add Two Buttons and Adjust the Form</span></span>

<span data-ttu-id="8bf21-130">À présent, ajoutez deux boutons au formulaire.</span><span class="sxs-lookup"><span data-stu-id="8bf21-130">Now add two buttons to the form.</span></span> <span data-ttu-id="8bf21-131">Sélectionnez le premier bouton et affectez à la propriété **Text** la valeur « Play ».</span><span class="sxs-lookup"><span data-stu-id="8bf21-131">Select the first button and change the **Text** property to "Play".</span></span> <span data-ttu-id="8bf21-132">Sélectionnez le deuxième bouton et définissez sa propriété **Text** sur « STOP ».</span><span class="sxs-lookup"><span data-stu-id="8bf21-132">Select the second button and change its **Text** property to "Stop".</span></span>

## <a name="add-the-play-code"></a><span data-ttu-id="8bf21-133">Ajouter le code de lecture</span><span class="sxs-lookup"><span data-stu-id="8bf21-133">Add the Play Code</span></span>

<span data-ttu-id="8bf21-134">Double-cliquez sur le bouton **lecture** pour afficher la fenêtre de code.</span><span class="sxs-lookup"><span data-stu-id="8bf21-134">Double-click the **Play** button to reveal the Code window.</span></span> <span data-ttu-id="8bf21-135">Le code suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="8bf21-135">The following code is displayed:</span></span>


```VB
Private Sub Button1_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub
```



<span data-ttu-id="8bf21-136">Ajoutez cette ligne à la sous-routine :</span><span class="sxs-lookup"><span data-stu-id="8bf21-136">Add this line to the subroutine:</span></span>


```VB
AxWindowsMediaPlayer1.URL = "c:\mediafile.wmv"
```



<span data-ttu-id="8bf21-137">Dans l’exemple de code précédent, « axWindowsMediaPlayer1 » est le nom par défaut du contrôle du lecteur Windows Media et « c : \\ mediafile. wmv » est un espace réservé pour le nom du média que vous souhaitez lire.</span><span class="sxs-lookup"><span data-stu-id="8bf21-137">In the preceding code example, "axWindowsMediaPlayer1" is the default name of the Windows Media Player control and "c:\\mediafile.wmv" is a placeholder for the name of the media you want to play.</span></span>

<span data-ttu-id="8bf21-138">Si vous avez ajouté le contenu multimédia numérique du kit de développement logiciel (SDK) du lecteur Windows Media à la bibliothèque dans le lecteur Windows Media, vous pouvez utiliser ce code à la place :</span><span class="sxs-lookup"><span data-stu-id="8bf21-138">If you have added the digital media content from the Windows Media Player SDK to the library in Windows Media Player, you can use this code instead:</span></span>


```VB
axWindowsMediaPlayer1.currentPlaylist = _
    axWindowsMediaPlayer1.mediaCollection.getByName("mediafile")

```



<span data-ttu-id="8bf21-139">Étant donné que la propriété **AutoStart** est définie sur true par défaut, le lecteur Windows Media démarre la lecture lorsque vous définissez la propriété **currentPlaylist** ou **URL** .</span><span class="sxs-lookup"><span data-stu-id="8bf21-139">Because the **autoStart** property is true by default, Windows Media Player will start playing when you set the **currentPlaylist** or **URL** property.</span></span>

## <a name="add-the-stop-code"></a><span data-ttu-id="8bf21-140">Ajouter le code d’arrêt</span><span class="sxs-lookup"><span data-stu-id="8bf21-140">Add the Stop Code</span></span>

<span data-ttu-id="8bf21-141">Double-cliquez sur le bouton **arrêter** pour afficher la fenêtre de code.</span><span class="sxs-lookup"><span data-stu-id="8bf21-141">Double-click the **Stop** button to reveal the Code window.</span></span> <span data-ttu-id="8bf21-142">Le code suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="8bf21-142">The following code is displayed:</span></span>


```VB
Private Sub Button2_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub

```



<span data-ttu-id="8bf21-143">Ajoutez cette ligne à la sous-routine :</span><span class="sxs-lookup"><span data-stu-id="8bf21-143">Add this line to the subroutine:</span></span>


```VB
AxWindowsMediaPlayer1.Ctlcontrols.stop()

```



> [!Note]  
> <span data-ttu-id="8bf21-144">Le wrapper de code managé pour le contrôle du lecteur Windows Media expose l’objet **contrôles** en tant que **Ctlcontrols** pour éviter toute collision avec la propriété **Controls** héritée de **System. Windows. Forms. Control**.</span><span class="sxs-lookup"><span data-stu-id="8bf21-144">The managed-code wrapper for the Windows Media Player control exposes the **Controls** object as **Ctlcontrols** to avoid collision with the **Controls** property inherited from **System.Windows.Forms.Control**.</span></span>

 

## <a name="add-error-handling"></a><span data-ttu-id="8bf21-145">Ajouter la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="8bf21-145">Add Error-handling</span></span>

<span data-ttu-id="8bf21-146">Le contrôle du lecteur Windows Media ne lève pas d’exception lorsqu’il rencontre une erreur telle qu’une URL non valide.</span><span class="sxs-lookup"><span data-stu-id="8bf21-146">The Windows Media Player control does not raise an exception when it encounters an error such as an invalid URL.</span></span> <span data-ttu-id="8bf21-147">Au lieu de cela, le contrôle signale un événement.</span><span class="sxs-lookup"><span data-stu-id="8bf21-147">Instead, the control signals an event.</span></span> <span data-ttu-id="8bf21-148">Votre application doit gérer les événements d’erreur envoyés par le lecteur.</span><span class="sxs-lookup"><span data-stu-id="8bf21-148">Your application should handle error events sent by the Player.</span></span>

<span data-ttu-id="8bf21-149">Pour créer un gestionnaire d’événements, ouvrez la fenêtre de code de votre classe de formulaire.</span><span class="sxs-lookup"><span data-stu-id="8bf21-149">To create an event handler, open the code window for your form class.</span></span> <span data-ttu-id="8bf21-150">Dans la liste déroulante en haut de la fenêtre, sélectionnez le contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8bf21-150">From the drop-down list at the top of the window, select the Windows Media Player control.</span></span> <span data-ttu-id="8bf21-151">Une liste d’événements s’affiche dans la liste déroulante à droite.</span><span class="sxs-lookup"><span data-stu-id="8bf21-151">A list of events appears in the drop-down list to the right.</span></span> <span data-ttu-id="8bf21-152">Dans cette liste, sélectionnez [**MediaError**](axwmplib-axwindowsmediaplayer-mediaerror.md).</span><span class="sxs-lookup"><span data-stu-id="8bf21-152">From that list, select [**MediaError**](axwmplib-axwindowsmediaplayer-mediaerror.md).</span></span> <span data-ttu-id="8bf21-153">Le code suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="8bf21-153">The following code is displayed:</span></span>


```VB
Private Sub AxWindowsMediaPlayer1_MediaError(ByVal sender As Object, _
    ByVal e As _WMPOCXEvents_MediaErrorEvent) Handles AxWindowsMediaPlayer1.MediaError

End Sub

```



<span data-ttu-id="8bf21-154">Le code suivant peut être inséré dans la sous-routine pour fournir une fonctionnalité de gestion des erreurs minimale.</span><span class="sxs-lookup"><span data-stu-id="8bf21-154">The following code could be inserted in the subroutine to provide minimal error-handling capability.</span></span> <span data-ttu-id="8bf21-155">Notez que les informations sur l’erreur peuvent être récupérées à partir de l’argument **\_ WMPOCXEvents \_ MediaErrorEvent** .</span><span class="sxs-lookup"><span data-stu-id="8bf21-155">Note that information about the error can be retrieved from the **\_WMPOCXEvents\_MediaErrorEvent** argument.</span></span>


```VB
Try
    ' If the file is corrupt or missing, show the 
    ' hexadecimal error code and URL.
    Dim errSource As WMPLib.IWMPMedia2 = e.pMediaObject
    Dim errorItem As WMPLib.IWMPErrorItem = errSource.Error
    MessageBox.Show("Media error " + errorItem.errorCode.ToString("X") _
                    + " in " + errSource.sourceURL)
Catch ex As InvalidCastException
    ' In case pMediaObject is not an IWMPMedia item.
    MessageBox.Show("Player error.")
End Try

```



## <a name="related-topics"></a><span data-ttu-id="8bf21-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8bf21-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bf21-157">**Intégration du contrôle du lecteur Windows Media dans une solution .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="8bf21-157">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




