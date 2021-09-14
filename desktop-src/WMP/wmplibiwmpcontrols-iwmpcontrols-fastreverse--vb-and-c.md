---
title: Méthode IWMPControls fastReverse
description: La méthode fastReverse démarre la lecture rapide de l’élément multimédia dans le sens inverse.
ms.assetid: 5c872e8d-2ffc-425f-a4dd-938ddd1426e0
keywords:
- Lecteur Windows Media de la méthode fastReverse
- méthode fastReverse Lecteur Windows Media, interface IWMPControls
- Lecteur Windows Media de l’interface IWMPControls, méthode fastReverse
topic_type:
- apiref
api_name:
- IWMPControls.fastReverse
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061481aea13b0ed83c3a3d0eb47ca24b940358b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237132"
---
# <a name="iwmpcontrolsfastreverse-method"></a>IWMPControls :: fastReverse, méthode

La méthode **fastReverse** démarre la lecture rapide de l’élément multimédia dans le sens inverse.

## <a name="syntax"></a>Syntaxe


```CSharp
public void fastReverse();
```


```VB

Public Sub fastReverse()
Implements IWMPControls.fastReverse
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La méthode **fastReverse** analyse le clip en sens inverse à cinq fois la vitesse normale, en affichant uniquement les images clés s’il s’agit d’un fichier vidéo. L’appel de **fastReverse** équivaut à spécifier-5,0 pour le taux en définissant la propriété **IWMPSettings. rate** . si la fréquence est modifiée par la suite, ou si **IWMPControls. play** ou **IWMPControls. stop** est appelé, Lecteur Windows Media cessera de tourner rapidement.

Si l’élément fait partie d’une sélection, **fastReverse** s’arrête au début de la piste actuelle. par exemple, si la piste 3 se trouve dans **fastReverse**, lorsque le début de la piste 3 est atteint, Lecteur Windows Media n’accède pas à track 2. Le nombre de lecture n’est pas incrémenté lors de l’appel de **fastReverse**.

Si vous appelez **IWMPControls. fastForward** alors que **fastReverse** est en cours d’exécution, **fastReverse** sera arrêté et **IWMPControls. fastForward** démarrera.

Cette méthode ne fonctionne pas pour les diffusions en direct et certains types de médias numériques. Pour déterminer si vous pouvez utiliser l’inverse rapide dans un clip, transmettez la valeur **System. String** « FastReverse » à la propriété **IWMPControls. IsAvailable** (méthode **IWMPControls. obtenir \_ isAvailable** en C#).

## <a name="examples"></a>Exemples

L’exemple suivant utilise **fastReverse** pour inverser l’élément multimédia en cours en réponse à l’événement Click d’un bouton. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
private void fastReverseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastReverse"))
    {
        controls.fastReverse();
    }
}
```


```VB

Public Sub fastReverseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastReverseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastReverse&quot;)) Then

        controls.fastReverse()

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

[**Interface IWMPControls (VB et C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls. fastForward (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[**IWMPControls. isAvailable (VB et C#)**](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPControls. play (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls. stop (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. rate (VB et C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





