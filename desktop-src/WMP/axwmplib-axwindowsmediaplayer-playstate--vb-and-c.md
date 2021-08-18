---
title: AxWindowsMediaPlayer. lecture, propriété
description: la propriété lecture obtient une valeur d’énumération indiquant l’état de l’opération de Lecteur Windows Media.
ms.assetid: ab9f1547-5c28-4289-beaf-9262f7f59b07
keywords:
- Lecteur Windows Media de la propriété lecture
- Lecteur Windows Media de la propriété lecture, classe AxWindowsMediaPlayer
- Lecteur Windows Media de la classe AxWindowsMediaPlayer, propriété lecture
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.playState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbd6d5ecbd4914864d812125143b1c5b6c0ae0d470b2c3951c060aacd3627ff2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119378179"
---
# <a name="axwindowsmediaplayerplaystate-property"></a>AxWindowsMediaPlayer. lecture, propriété

la propriété lecture obtient une valeur d’énumération indiquant l’état de l’opération de Lecteur Windows Media.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```CSharp
public WMPPlayState playState {get;}
```


```VB

Public ReadOnly Property playState As WMPPlayState
```





## <a name="property-value"></a>Valeur de la propriété

Valeur d’énumération WMPLib. WMPPlayState.

## <a name="remarks"></a>Remarques

il n’est pas garanti que les états de Lecteur Windows Media se produisent dans un ordre particulier. En outre, tous les États ne se produisent pas nécessairement au cours d’une séquence d’événements. Vous ne devez pas écrire du code qui s’appuie sur l’ordre de l’État.

## <a name="examples"></a>Exemples

L’exemple suivant utilise la propriété lecture pour afficher l’état de lecture actuel du joueur dans une étiquette. L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.


```CSharp
// Test whether Windows Media Player is in the playing state. 
if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
{
    playStateLabel.Text = "Windows Media Player is playing!";
}
else
{
    playStateLabel.Text = "Windows Media Player is NOT playing!";
}
```


```VB

' Test whether Windows Media Player is in the playing state. 
If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

    playStateLabel.Text = &quot;Windows Media Player is playing!&quot;

Else

    playStateLabel.Text = &quot;Windows Media Player is NOT playing!&quot;

End If
```





## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**événement AxWindowsMediaPlayer. PlayStateChange (VB et C#)**](axwmplib-axwindowsmediaplayer-playstatechange.md)
</dt> <dt>

[**WMPPlayState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaystate)
</dt> </dl>

 

 





