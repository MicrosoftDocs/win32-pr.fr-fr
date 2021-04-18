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
# <a name="creating-the-windows-media-player-control-programmatically"></a>Création du contrôle du lecteur Windows Media par programmation

Quand vous ajoutez le contrôle du lecteur Windows Media à un formulaire à partir de la boîte à outils, un objet de la classe **AxWMPLib. AxWindowsMediaPlayer** est créé. Cette classe wrapper donne au joueur toutes les fonctionnalités d’un contrôle ActiveX, y compris l’accès aux propriétés de l’interface utilisateur telles que l' **emplacement** et la **taille**.

Si vous n’avez pas besoin des propriétés exposées par **AxWindowsMediaPlayer**, ou si votre application n’a pas d’interface utilisateur graphique, vous pouvez créer un contrôle de lecteur par programme. Dans ce cas, vous créez un objet de la classe **wmplib. WindowsMediaPlayer** .

> [!Note]  
> Étant donné que l’objet **WindowsMediaPlayer** n’est pas encapsulé en tant que contrôle ActiveX, il n’a pas de propriétés héritées de **System. Windows. Forms. Control**. Par conséquent, la propriété **Controls** n’est pas renommée en **CtlControls**, comme c’est le cas dans **AxWindowsMediaPlayer**.

 

Pour créer le contrôle du lecteur Windows Media par programme, vous devez d’abord ajouter une référence à wmp.dll, qui se trouve dans \\ le \\ dossier Windows system32. L’ajout de cette référence crée WMPLib.dll dans le dossier de votre projet, et une référence à WMPLib apparaît dans Explorateur de solutions.

L’exemple de code suivant, qui fait partie d’une classe Form1, montre comment créer un objet **joueur** et lire un fichier. À la fin de la lecture, ou si le fichier ne peut pas être lu, le formulaire est fermé.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Intégration du contrôle du lecteur Windows Media dans une solution .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




