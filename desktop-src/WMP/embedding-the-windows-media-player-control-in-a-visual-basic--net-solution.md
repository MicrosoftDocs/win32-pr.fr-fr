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
# <a name="embedding-the-windows-media-player-control-in-a-visual-basic-net-solution"></a>Intégration du contrôle du lecteur Windows Media dans une solution Visual Basic .NET

Pour utiliser les fonctionnalités du lecteur Windows Media série 9 ou version ultérieure dans une application Visual Basic .NET, ajoutez d’abord le composant à un formulaire comme décrit dans [utilisation du contrôle du lecteur Windows Media avec Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)

Cette section décrit comment créer une application qui lit des vidéos et contient des boutons de lecture et d’arrêt personnalisés.

## <a name="add-the-video-window"></a>Ajouter la fenêtre vidéo

Ajoutez le contrôle du lecteur Windows Media à un formulaire. Redimensionnez le contrôle, puis placez-le à l’emplacement où vous souhaitez que la fenêtre vidéo apparaisse.

Sélectionnez le contrôle du lecteur Windows Media, puis modifiez la propriété **UIMODE** en « None ». Ce paramètre masque les contrôles d’interface utilisateur. Quand l’utilisateur lit une vidéo, elle s’affiche dans la fenêtre. Pour le contenu audio uniquement, une visualisation s’affiche.

## <a name="add-two-buttons-and-adjust-the-form"></a>Ajouter deux boutons et ajuster le formulaire

À présent, ajoutez deux boutons au formulaire. Sélectionnez le premier bouton et affectez à la propriété **Text** la valeur « Play ». Sélectionnez le deuxième bouton et définissez sa propriété **Text** sur « STOP ».

## <a name="add-the-play-code"></a>Ajouter le code de lecture

Double-cliquez sur le bouton **lecture** pour afficher la fenêtre de code. Le code suivant s’affiche :


```VB
Private Sub Button1_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub
```



Ajoutez cette ligne à la sous-routine :


```VB
AxWindowsMediaPlayer1.URL = "c:\mediafile.wmv"
```



Dans l’exemple de code précédent, « axWindowsMediaPlayer1 » est le nom par défaut du contrôle du lecteur Windows Media et « c : \\ mediafile. wmv » est un espace réservé pour le nom du média que vous souhaitez lire.

Si vous avez ajouté le contenu multimédia numérique du kit de développement logiciel (SDK) du lecteur Windows Media à la bibliothèque dans le lecteur Windows Media, vous pouvez utiliser ce code à la place :


```VB
axWindowsMediaPlayer1.currentPlaylist = _
    axWindowsMediaPlayer1.mediaCollection.getByName("mediafile")

```



Étant donné que la propriété **AutoStart** est définie sur true par défaut, le lecteur Windows Media démarre la lecture lorsque vous définissez la propriété **currentPlaylist** ou **URL** .

## <a name="add-the-stop-code"></a>Ajouter le code d’arrêt

Double-cliquez sur le bouton **arrêter** pour afficher la fenêtre de code. Le code suivant s’affiche :


```VB
Private Sub Button2_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub

```



Ajoutez cette ligne à la sous-routine :


```VB
AxWindowsMediaPlayer1.Ctlcontrols.stop()

```



> [!Note]  
> Le wrapper de code managé pour le contrôle du lecteur Windows Media expose l’objet **contrôles** en tant que **Ctlcontrols** pour éviter toute collision avec la propriété **Controls** héritée de **System. Windows. Forms. Control**.

 

## <a name="add-error-handling"></a>Ajouter la gestion des erreurs

Le contrôle du lecteur Windows Media ne lève pas d’exception lorsqu’il rencontre une erreur telle qu’une URL non valide. Au lieu de cela, le contrôle signale un événement. Votre application doit gérer les événements d’erreur envoyés par le lecteur.

Pour créer un gestionnaire d’événements, ouvrez la fenêtre de code de votre classe de formulaire. Dans la liste déroulante en haut de la fenêtre, sélectionnez le contrôle du lecteur Windows Media. Une liste d’événements s’affiche dans la liste déroulante à droite. Dans cette liste, sélectionnez [**MediaError**](axwmplib-axwindowsmediaplayer-mediaerror.md). Le code suivant s’affiche :


```VB
Private Sub AxWindowsMediaPlayer1_MediaError(ByVal sender As Object, _
    ByVal e As _WMPOCXEvents_MediaErrorEvent) Handles AxWindowsMediaPlayer1.MediaError

End Sub

```



Le code suivant peut être inséré dans la sous-routine pour fournir une fonctionnalité de gestion des erreurs minimale. Notez que les informations sur l’erreur peuvent être récupérées à partir de l’argument **\_ WMPOCXEvents \_ MediaErrorEvent** .


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Intégration du contrôle du lecteur Windows Media dans une solution .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




