---
title: Création du contrôle du lecteur Windows Media par programmation
description: Création du contrôle du lecteur Windows Media par programmation
ms.assetid: 9a4856ce-6a44-47fb-b863-59ce4deb0597
keywords:
- Lecteur Windows Media, création d’un contrôle ActiveX par programmation
- Windows Media Player Object Model, création d’un contrôle ActiveX par programmation
- modèle objet, créer un contrôle ActiveX par programmation
- Windows Media Player Mobile, création d’un contrôle ActiveX par programmation
- Contrôle ActiveX du lecteur Windows Media, création par programmation
- Contrôle ActiveX Windows Media Player Mobile, création par programmation
- Contrôle ActiveX, création par programmation
- création d’un contrôle ActiveX par programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222c207b33dcc13a5392f79dad267d6ee82a677c
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2019
ms.locfileid: "104311683"
---
# <a name="creating-the-windows-media-player-control-programmatically"></a><span data-ttu-id="43de8-111">Création du contrôle du lecteur Windows Media par programmation</span><span class="sxs-lookup"><span data-stu-id="43de8-111">Creating the Windows Media Player Control Programmatically</span></span>

<span data-ttu-id="43de8-112">Quand vous ajoutez le contrôle du lecteur Windows Media à un formulaire à partir de la boîte à outils, un objet de la classe **AxWMPLib. AxWindowsMediaPlayer** est créé.</span><span class="sxs-lookup"><span data-stu-id="43de8-112">When you add the Windows Media Player control to a form from the Toolbox, an object of the class **AxWMPLib.AxWindowsMediaPlayer** is created.</span></span> <span data-ttu-id="43de8-113">Cette classe wrapper donne au joueur toutes les fonctionnalités d’un contrôle ActiveX, y compris l’accès aux propriétés de l’interface utilisateur telles que l' **emplacement** et la **taille**.</span><span class="sxs-lookup"><span data-stu-id="43de8-113">This wrapper class gives the Player all the functionality of an ActiveX control, including access to UI properties such as **Location** and **Size**.</span></span>

<span data-ttu-id="43de8-114">Si vous n’avez pas besoin des propriétés exposées par **AxWindowsMediaPlayer**, ou si votre application n’a pas d’interface utilisateur graphique, vous pouvez créer un contrôle de lecteur par programme.</span><span class="sxs-lookup"><span data-stu-id="43de8-114">If you do not require the properties exposed by **AxWindowsMediaPlayer**, or if your application does not have a graphical user interface, you can create a Player control programmatically.</span></span> <span data-ttu-id="43de8-115">Dans ce cas, vous créez un objet de la classe **wmplib. WindowsMediaPlayer** .</span><span class="sxs-lookup"><span data-stu-id="43de8-115">In this case, you create an object of the **WMPLib.WindowsMediaPlayer** class.</span></span>

> [!Note]  
> <span data-ttu-id="43de8-116">Étant donné que l’objet **WindowsMediaPlayer** n’est pas encapsulé en tant que contrôle ActiveX, il n’a pas de propriétés héritées de **System. Windows. Forms. Control**.</span><span class="sxs-lookup"><span data-stu-id="43de8-116">Because the **WindowsMediaPlayer** object is not wrapped as an ActiveX control, it does not have any properties inherited from **System.Windows.Forms.Control**.</span></span> <span data-ttu-id="43de8-117">Par conséquent, la propriété **Controls** n’est pas renommée en **CtlControls**, comme c’est le cas dans **AxWindowsMediaPlayer**.</span><span class="sxs-lookup"><span data-stu-id="43de8-117">As a result, the **Controls** property is not renamed to **CtlControls**, as it is in **AxWindowsMediaPlayer**.</span></span>

 

<span data-ttu-id="43de8-118">Pour créer le contrôle du lecteur Windows Media par programme, vous devez d’abord ajouter une référence à wmp.dll, qui se trouve dans \\ le \\ dossier Windows system32.</span><span class="sxs-lookup"><span data-stu-id="43de8-118">To create the Windows Media Player control programmatically, you must first add a reference to wmp.dll, which is found in the \\Windows\\system32 folder.</span></span> <span data-ttu-id="43de8-119">L’ajout de cette référence crée WMPLib.dll dans le dossier de votre projet, et une référence à WMPLib apparaît dans Explorateur de solutions.</span><span class="sxs-lookup"><span data-stu-id="43de8-119">Adding this reference creates WMPLib.dll in your project folder, and a reference to WMPLib appears in Solution Explorer.</span></span>

<span data-ttu-id="43de8-120">L’exemple de code suivant, qui fait partie d’une classe Form1, montre comment créer un objet **joueur** et lire un fichier.</span><span class="sxs-lookup"><span data-stu-id="43de8-120">The following example code, part of a Form1 class, shows how to create a **Player** object and play a file.</span></span> <span data-ttu-id="43de8-121">À la fin de la lecture, ou si le fichier ne peut pas être lu, le formulaire est fermé.</span><span class="sxs-lookup"><span data-stu-id="43de8-121">When playback ends, or if the file cannot be played, the form is closed.</span></span>


```VB
Dim WithEvents Player As WMPLib.WindowsMediaPlayer

Private Sub PlayFile(ByVal url As String)
    Player = New WMPLib.WindowsMediaPlayer
    Player.URL = url
    Player.controls.play()
End Sub

Private Sub Form1_Load(ByVal sender As Object, ByVal e As System.EventArgs) _
                       Handles MyBase.Load
    ' TODO  Insert a valid path in the line below.
    PlayFile("c:\media\myaudio.wma")
End Sub

Private Sub Player_MediaError(ByVal pMediaObject As Object) _
                              Handles Player.MediaError
    MessageBox.Show("Cannot play media file.")
    Me.Close()
End Sub

Private Sub Player_PlayStateChange(ByVal NewState As Integer) _
                                   Handles Player.PlayStateChange
    If NewState = WMPLib.WMPPlayState.wmppsStopped Then
        Me.Close()
    End If
End Sub

```




```CSharp
WMPLib.WindowsMediaPlayer Player;

private void PlayFile(String url)
{
    Player = new WMPLib.WindowsMediaPlayer();
    Player.PlayStateChange += 
        new WMPLib._WMPOCXEvents_PlayStateChangeEventHandler(Player_PlayStateChange);
    Player.MediaError += 
        new WMPLib._WMPOCXEvents_MediaErrorEventHandler(Player_MediaError);
    Player.URL = url;
    Player.controls.play();
}

private void Form1_Load(object sender, System.EventArgs e)
{
    // TODO  Insert a valid path in the line below.
    PlayFile(@"c:\myaudio.wma");
}

private void Player_PlayStateChange(int NewState)
{
    if ((WMPLib.WMPPlayState)NewState == WMPLib.WMPPlayState.wmppsStopped)
    {
        this.Close();
    }
}

private void Player_MediaError(object pMediaObject)
{
    MessageBox.Show("Cannot play media file.");
    this.Close();
}


```



## <a name="related-topics"></a><span data-ttu-id="43de8-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="43de8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43de8-123">**Intégration du contrôle du lecteur Windows Media dans une solution .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="43de8-123">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




