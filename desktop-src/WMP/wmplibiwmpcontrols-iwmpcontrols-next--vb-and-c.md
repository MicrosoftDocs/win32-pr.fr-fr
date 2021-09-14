---
title: IWMPControls méthode Next
description: La méthode suivante définit l’élément suivant dans la sélection comme élément actuel.
ms.assetid: 3f82ef25-a1e0-4845-b0ed-dd6463719577
keywords:
- méthode suivante Lecteur Windows Media
- next, méthode Lecteur Windows Media, IWMPControls, interface
- Lecteur Windows Media de l’interface IWMPControls, méthode next
topic_type:
- apiref
api_name:
- IWMPControls.next
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8444ba7d9209759cb64c4b582e1af9d074332ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010762"
---
# <a name="iwmpcontrolsnext-method"></a>IWMPControls :: Next, méthode

La méthode **suivante** définit l’élément suivant dans la sélection comme élément actuel.

## <a name="syntax"></a>Syntaxe


```CSharp
public void next();
```


```VB

Public Sub next()
Implements IWMPControls.next
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si la sélection se trouve sur la dernière entrée **lors de** l’appel de la méthode, la première entrée de la sélection devient la dernière.

Pour les sélections côté serveur, cette méthode passe à l’élément suivant dans la sélection côté serveur, et non à la sélection du client.

Lors de la lecture d’un DVD, cette méthode passe au chapitre logique suivant dans la séquence de lecture, qui peut ne pas être le chapitre suivant de la sélection. Lors de la diffusion d’images continues sur DVD, cette méthode passe à l’image suivante.

## <a name="examples"></a>Exemples

L’exemple suivant utilise **Next** pour passer à l’élément suivant dans la sélection en cours en réponse à l’événement Click d’un bouton. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
private void nextButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("next"))
    {
        controls.next();
    }
}
```


```VB

Public Sub nextButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles nextButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;next&quot;)) Then

        controls.next()

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

[**IWMPControls. previous (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> <dt>

[**IWMPControls. stop (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





