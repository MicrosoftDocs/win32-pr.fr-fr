---
title: Propriété de débit binaire IWMPNetwork
description: La propriété de débit binaire obtient la vitesse de transmission actuelle en cours de réception.
ms.assetid: f7dda557-3954-45ed-9eac-6d27109e2dfa
keywords:
- Lecteur Windows Media de propriétés de débit binaire
- Lecteur Windows Media de propriétés de la vitesse de transmission, interface IWMPNetwork
- Lecteur Windows Media de l’interface IWMPNetwork, propriété de vitesse de transmission
topic_type:
- apiref
api_name:
- IWMPNetwork.bitRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4346a20c5c5b5a5ca68b2a90293afd9d657e472d335b9ee8bf2ad647ff0914
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098739"
---
# <a name="iwmpnetworkbitrate-property"></a>IWMPNetwork :: transmission binaire, propriété

La propriété de **débit** binaire obtient la vitesse de transmission actuelle en cours de réception.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 bitRate {get; set;}
```


```VB

Public ReadOnly Property bitRate As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui correspond à la vitesse de transmission.

## <a name="remarks"></a>Remarques

La valeur de cette propriété est une combinaison des vitesses de transmission des flux vidéo et audio.

## <a name="examples"></a>Exemples

L’exemple suivant utilise la vitesse de **transmission** pour afficher le taux binaire actuel. Les informations s’affichent dans une étiquette en réponse à l’événement **PlayStateChange** . L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the bitRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.bitRate != 0)
            {
                bitRateLabel.Text = "Current Bit Rate: " + player.network.bitRate + " K bits/second";
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

    &#39; Display the bitRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.bitRate <> 0) Then

                bitRateLabel.Text = &quot;Current Bit Rate: &quot; + player.network.bitRate + &quot; K bits/second&quot;

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
</dt> </dl>

 

 





