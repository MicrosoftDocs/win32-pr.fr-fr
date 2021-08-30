---
title: Méthode IWMPControls fastForward
description: La méthode fastForward démarre la lecture rapide de l’élément multimédia dans le sens avant. | Méthode IWMPControls fastForward
ms.assetid: 44609d63-1d1a-489c-ac17-60b6d3ddc588
keywords:
- Lecteur Windows Media de la méthode fastForward
- méthode fastForward Lecteur Windows Media, interface IWMPControls
- Lecteur Windows Media de l’interface IWMPControls, méthode fastForward
topic_type:
- apiref
api_name:
- IWMPControls.fastForward
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f283ef56f3831f58b8d57f3d172ad3b80163ee62fdaa24b05bdca02c68cafcf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031329"
---
# <a name="iwmpcontrolsfastforward-method"></a>IWMPControls :: fastForward, méthode

La méthode **fastForward** démarre la lecture rapide de l’élément multimédia dans le sens avant.

## <a name="syntax"></a>Syntaxe


```CSharp
public void fastForward();
```


```VB

Public Sub fastForward()
Implements IWMPControls.fastForward
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La méthode **fastForward** lit le clip à cinq fois la vitesse normale. L’appel de **fastForward** équivaut à spécifier 5,0 pour le taux en définissant la propriété **IWMPSettings. rate** . si la fréquence est modifiée par la suite ou si **IWMPControls. play** ou **IWMPControls. stop** est appelé, Lecteur Windows Media interrompt le transfert rapide.

La méthode **fastForward** ne fonctionne pas pour les diffusions en direct et certains types de média. Pour déterminer si vous pouvez avancer rapidement dans un clip, transmettez la valeur **System. String** « Fastforward » à la propriété **IWMPControls. IsAvailable** (méthode **IWMPControls. obtenir \_ isAvailable** en C#).

## <a name="examples"></a>Exemples

L’exemple suivant utilise **fastForward** pour avancer rapidement l’élément multimédia actuel en réponse à l’événement Click d’un bouton. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
private void fastForwardButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastForward"))
    {
        controls.fastForward();
    }
}
```


```VB

Public Sub fastForwardButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastForwardButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface. 
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastForward&quot;)) Then

        controls.fastForward()

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

[**Interface IWMPControls (VB et C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls. isAvailable (VB et C#)**](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPControls. play (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls. stop (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. rate (VB et C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





