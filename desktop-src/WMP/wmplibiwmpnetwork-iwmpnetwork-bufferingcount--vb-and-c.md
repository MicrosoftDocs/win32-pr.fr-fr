---
title: IWMPNetwork propriété bufferingCount
description: La propriété bufferingCount obtient le nombre de fois où la mise en mémoire tampon s’est produite pendant la lecture.
ms.assetid: 2e3a2914-fc38-4477-8c4c-15b4a2e424dc
keywords:
- Lecteur Windows Media de la propriété bufferingCount
- Lecteur Windows Media de la propriété bufferingCount, interface IWMPNetwork
- Lecteur Windows Media de l’interface IWMPNetwork, propriété bufferingCount
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92b69169e950cf3794d613bfd1d79d4953ce8f8a8bb01efe9ff17d6fa5961071
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899969"
---
# <a name="iwmpnetworkbufferingcount-property"></a>IWMPNetwork :: bufferingCount, propriété

La propriété **bufferingCount** obtient le nombre de fois où la mise en mémoire tampon s’est produite pendant la lecture.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 bufferingCount {get; set;}
```


```VB

Public ReadOnly Property bufferingCount As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui est le nombre de mises en mémoire tampon.

## <a name="remarks"></a>Remarques

Chaque fois que la lecture est arrêtée et redémarrée, cette propriété est réinitialisée à zéro. Elle n’est pas réinitialisée si la lecture est suspendue.

La mise en mémoire tampon s’applique uniquement au contenu de diffusion en continu. Cette propriété obtient des informations valides uniquement au moment de l’exécution lorsque l’URL pour la lecture est définie à l’aide de la propriété **AxWindowsMediaPlayer. URL** .

## <a name="examples"></a>Exemples

L’exemple suivant utilise *bufferingCount* pour afficher le nombre de fois que la mise en mémoire tampon se produit pendant la lecture. Les informations s’affichent dans une étiquette en réponse à l’événement de mise en mémoire tampon. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Display the bufferingCount when buffering has started.
    if (e.start == true)
    {
        bufferingCountLabel.Text = ("Buffering count: " + player.network.bufferingCount);
    }  
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Display the bufferingCount when buffering has started.
    If (e.start = True) Then

        bufferingCountLabel.Text = (&quot;Buffering count: &quot; + player.network.bufferingCount)

    End If

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

[**AxWindowsMediaPlayer. URL (VB et C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Interface IWMPNetwork (VB et C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





