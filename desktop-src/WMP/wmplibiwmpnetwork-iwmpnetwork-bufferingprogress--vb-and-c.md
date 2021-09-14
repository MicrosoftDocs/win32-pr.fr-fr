---
title: IWMPNetwork propriété bufferingProgress
description: La propriété bufferingProgress obtient le pourcentage de la mise en mémoire tampon terminée.
ms.assetid: 8dc9f31e-7c34-4714-a633-d92c3da3052b
keywords:
- Lecteur Windows Media de la propriété bufferingProgress
- Lecteur Windows Media de la propriété bufferingProgress, interface IWMPNetwork
- Lecteur Windows Media de l’interface IWMPNetwork, propriété bufferingProgress
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1da8a27ba41e5c4e201a5bdf0197992c30bce80b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192224"
---
# <a name="iwmpnetworkbufferingprogress-property"></a>IWMPNetwork :: bufferingProgress, propriété

La propriété **bufferingProgress** obtient le pourcentage de la mise en mémoire tampon terminée.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 bufferingProgress {get; set;}
```


```VB

Public ReadOnly Property bufferingProgress As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui correspond à la progression de la mise en mémoire tampon exprimée en pourcentage.

## <a name="remarks"></a>Notes

Chaque fois que la lecture est arrêtée et redémarrée, cette propriété est réinitialisée à zéro. Elle n’est pas réinitialisée si la lecture est suspendue.

La mise en mémoire tampon s’applique uniquement au contenu de diffusion en continu. Cette propriété obtient des informations valides uniquement au moment de l’exécution lorsque l’URL pour la lecture est définie à l’aide de la propriété **AxWindowsMediaPlayer. URL** .

Utilisez **AxWindowsMediaPlayer. \_ WMPOCXEvents \_ BufferingEvent** pour déterminer à quel moment la mise en mémoire tampon démarre ou s’arrête.

## <a name="examples"></a>Exemples

L’exemple suivant utilise **bufferingProgress** pour afficher le pourcentage de mise en mémoire tampon effectuée dans une étiquette, en réponse à l’événement de mise en mémoire tampon. L’exemple utilise un minuteur avec un intervalle de 1 seconde pour mettre à jour l’affichage. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


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

// Update the buffering progress in a timer event handler.
private void UpdateBufferingProgress(object sender, EventArgs e)
{
    bufferingProgressLabel.Text = ("Buffering progress: " + player.network.bufferingProgress + " percent complete");
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

&#39; Update the buffering progress in a timer event handler.
Public Sub UpdateBufferingProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    bufferingProgressLabel.Text = (&quot;Buffering progress: &quot; + player.network.bufferingProgress + &quot; percent complete&quot;)

End Sub
```





## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AxWindowsMediaPlayer. URL (VB et C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**événement AxWindowsMediaPlayer. buffering (VB et C#)**](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[**Interface IWMPNetwork (VB et C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





