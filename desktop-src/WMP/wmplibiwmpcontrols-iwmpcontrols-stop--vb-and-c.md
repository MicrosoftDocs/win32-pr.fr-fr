---
title: IWMPControls Stop, méthode
description: La méthode Stop arrête la lecture de l’élément multimédia. | IWMPControls Stop, méthode
ms.assetid: 4be601af-6321-4115-a94d-cfc9228991cb
keywords:
- stop, méthode Lecteur Windows Media
- stop, méthode Lecteur Windows Media, IWMPControls, interface
- Lecteur Windows Media de l’interface IWMPControls, méthode stop
topic_type:
- apiref
api_name:
- IWMPControls.stop
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f941ac90fa86cdd16dedf5349c0a6d614c57f49bc91009f5d62c56bb83144bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332074"
---
# <a name="iwmpcontrolsstop-method"></a>IWMPControls :: Stop, méthode

La méthode **Stop** arrête la lecture de l’élément multimédia.

## <a name="syntax"></a>Syntaxe


```CSharp
public void stop();
```


```VB

Public Sub stop()
Implements IWMPControls.stop
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

cette méthode oblige Lecteur Windows Media à libérer toutes les ressources système qu’il utilise, telles que le périphérique audio. Toutefois, l’élément multimédia actuel n’est pas libéré.

lorsque Lecteur Windows Media est arrêté, la position de lecture actuelle dans l’élément multimédia est réinitialisée au début de l’élément. Par la suite, l’appel de **IWMPControls. Play** démarre la lecture à partir du début de l’élément multimédia. Pour arrêter une opération de lecture sans modifier la position actuelle, utilisez la méthode **IWMPControls. pause** .

## <a name="examples"></a>Exemples

L’exemple suivant utilise **Stop** pour arrêter l’élément multimédia en cours en réponse à l’événement Click d’un bouton. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
private void stopButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("stop"))
    {
        controls.stop();
    }
}
```


```VB

Public Sub stopButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles stopButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;stop&quot;)) Then

        controls.stop()

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

[**IWMPControls. next (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[**IWMPControls. pause (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[**IWMPControls. play (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls. previous (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> </dl>

 

 





