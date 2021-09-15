---
title: IWMPNetwork propriété sourceProtocol
description: La propriété sourceProtocol obtient le protocole source utilisé pour recevoir des données.
ms.assetid: db1d7651-3f25-4ac9-a3e1-dc3a8ddf8c40
keywords:
- Lecteur Windows Media de la propriété sourceProtocol
- Lecteur Windows Media de la propriété sourceProtocol, interface IWMPNetwork
- Lecteur Windows Media de l’interface IWMPNetwork, propriété sourceProtocol
topic_type:
- apiref
api_name:
- IWMPNetwork.sourceProtocol
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5017e1a053c124a1f7f50668c6f392eb541d57f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411303"
---
# <a name="iwmpnetworksourceprotocol-property"></a>IWMPNetwork :: sourceProtocol, propriété

La propriété **sourceProtocol** obtient le protocole source utilisé pour recevoir des données.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String sourceProtocol {get; set;}
```


```VB

Public ReadOnly Property sourceProtocol As System.String
```





## <a name="property-value"></a>Valeur de la propriété

**System. String** qui est le nom du protocole source.

## <a name="remarks"></a>Notes

Cette propriété obtient une chaîne de longueur nulle ("") lors de la diffusion d’un CD ou d’un DVD.

## <a name="examples"></a>Exemples

L’exemple de code suivant utilise **sourceProtocol** pour afficher le protocole source utilisé pour recevoir des données. Les informations s’affichent dans une étiquette, en réponse à l’événement **PlayStateChange** . L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the network source protocol when the player is playing by testing for a 
    // play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3. 
    if (e.newState == 3) 
    {
        sourceProtocolLabel.Text = ("Source protocol: " + player.network.sourceProtocol);
    } 
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the network source protocol when the player is playing by testing for a 
    &#39; play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3.
    If (e.newState = 3) Then

        sourceProtocolLabel.Text = (&quot;Source protocol: &quot; + player.network.sourceProtocol)

    End If

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

[**Interface IWMPNetwork (VB et C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





