---
title: IWMPNetwork propriété downloadProgress
description: La propriété downloadProgress obtient le pourcentage de téléchargement terminé.
ms.assetid: 40568c81-5bb5-45d9-b654-31072608663d
keywords:
- propriété downloadProgress lecteur Windows Media
- propriété downloadProgress lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, propriété downloadProgress
topic_type:
- apiref
api_name:
- IWMPNetwork.downloadProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b10b767845ac951e1364e15c7f6f1d729882e0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539511"
---
# <a name="iwmpnetworkdownloadprogress-property"></a>IWMPNetwork ::d propriété ownloadProgress

La propriété **downloadProgress** obtient le pourcentage de téléchargement terminé.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 downloadProgress {get; set;}
```


```VB

Public ReadOnly Property downloadProgress As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui est la progression du téléchargement exprimée sous forme de pourcentage.

## <a name="remarks"></a>Notes

Lorsque le contrôle du lecteur Windows Media est connecté à un fichier multimédia numérique qui peut être lu et téléchargé en même temps, la propriété **downloadProgress** obtient le pourcentage du fichier total téléchargé. Cette fonctionnalité est actuellement prise en charge uniquement pour les fichiers multimédias numériques téléchargés à partir de serveurs Web. Un fichier de l’un des formats suivants peut être téléchargé et lu simultanément :

-   ASF (Advanced Systems Format)
-   Audio Windows Media (WMA)
-   Vidéo Windows Media (WMV)
-   MP3
-   MPEG4
-   WAV

En outre, certains fichiers AVI peuvent être téléchargés et lus simultanément.

Utilisez **AxWindowsMediaPlayer. \_ WMPOCXEvents \_ BufferingEvent** pour déterminer à quel moment la mise en mémoire tampon démarre ou s’arrête.

## <a name="examples"></a>Exemples

L’exemple de code suivant utilise **downloadProgress** pour afficher le pourcentage de téléchargement effectué. Les informations s’affichent dans une étiquette, en réponse à l’événement de **mise en mémoire tampon** . L’exemple utilise un minuteur avec un intervalle de 1 seconde pour mettre à jour l’affichage. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Determine whether buffering has started or stopped.
    if (e.start == true)
    {
        // Set the timer interval at one second (1000 miliseconds).
        timer.Interval = 1000;
        
        // Start the timer.
        timer.Start();
    }
    else
    {
        // Buffering is complete. Stop the timer.
        timer.Stop();
    }
}

// Update the download progress in a timer event handler.
private void UpdateDownloadProgress(object sender, EventArgs e)
{
    downloadProgressLabel.Text = ("Download progress: " + player.network.downloadProgress + " percent complete");
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Test whether packets may be arriving.
    Select Case e.newState

    &#39; If WMPPlayState is Stopped, Paused, ScanForward, ScanReverse, Waiting, MediaEnded
    &#39; or Transitioning then stop the timer. 
        Case 1
        Case 2
        Case 4
        Case 5
        Case 7
        Case 8
        Case 9
            timer.Stop()

        &#39; If WMPPlayState is Playing or Buffering then set the timer interval and start the timer.
        Case Else
            timer.Interval = 1000
            timer.Start()

    End Select

End Sub

&#39; Update the download progress in a timer event handler.
Public Sub UpdateDownloadProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    downloadProgressLabel.Text = (&quot;Download progress: &quot; + player.network.downloadProgress + &quot; percent complete&quot;)

End Sub
```





## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AxWindowsMediaPlayer. Buffering, événement (VB et C#)**](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[**Interface IWMPNetwork (VB et C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





