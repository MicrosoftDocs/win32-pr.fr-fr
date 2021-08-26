---
title: IWMPNetwork propriété encodedFrameRate
description: La propriété encodedFrameRate obtient la fréquence d’images vidéo spécifiée par l’auteur du contenu.
ms.assetid: 4faf5675-5bf3-485d-802f-a1f900ddae63
keywords:
- Lecteur Windows Media de la propriété encodedFrameRate
- Lecteur Windows Media de la propriété encodedFrameRate, interface IWMPNetwork
- Lecteur Windows Media de l’interface IWMPNetwork, propriété encodedFrameRate
topic_type:
- apiref
api_name:
- IWMPNetwork.encodedFrameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f8a08572f65e1e44027ed25d84acfe7d917f92bf4bb63d5d9b8cca1e1201d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000009"
---
# <a name="iwmpnetworkencodedframerate-property"></a>IWMPNetwork :: encodedFrameRate, propriété

La propriété **encodedFrameRate** obtient la fréquence d’images vidéo spécifiée par l’auteur du contenu.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 encodedFrameRate {get; set;}
```


```VB

Public ReadOnly Property encodedFrameRate As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui correspond à la fréquence d’images encodée en images par seconde (FPS).

> [!Note]  
> Bien que la propriété **encodedFrameRate** mesure la fréquence d’images encodée en images par seconde **, la propriété** Parate mesure la fréquence d’images actuelle en images par centaines de secondes.

 

## <a name="examples"></a>Exemples

L’exemple de code suivant utilise **encodedFrameRate** pour afficher la fréquence d’images spécifiée lors de l’encodage du fichier. Les informations s’affichent dans une étiquette, en réponse à l’événement **PlayStateChange** . L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the encodedFrameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.encodedFrameRate != 0)
            {
                encodedFrameRateLabel.Text = "Current Encoded Frame Rate: " + player.network.encodedFrameRate + " K bits/second";
            }
            break;

        default:
            break;
    }
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the encodedFrameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.encodedFrameRate <> 0) Then

                encodedFrameRateLabel.Text = &quot;Current Encoded Frame Rate: &quot; + player.network.encodedFrameRate + &quot; K bits/second&quot;

            End If

    End Select

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

[**Interface IWMPNetwork (VB et C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. cadence (VB et C#)**](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)
</dt> </dl>

 

 





