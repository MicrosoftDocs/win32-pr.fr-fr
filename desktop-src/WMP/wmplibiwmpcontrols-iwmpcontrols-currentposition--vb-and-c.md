---
title: IWMPControls propriété currentPosition
description: La propriété currentPosition obtient ou définit la position actuelle dans l’élément multimédia, en secondes, à partir du début.
ms.assetid: 48f5241e-7528-485e-bf47-d655ba842af2
keywords:
- Lecteur Windows Media de la propriété currentPosition
- Lecteur Windows Media de la propriété currentPosition, interface IWMPControls
- Lecteur Windows Media de l’interface IWMPControls, propriété currentPosition
topic_type:
- apiref
api_name:
- IWMPControls.currentPosition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8eca861240256899fa19513fc1fb64cd540d47acb213f718674ebbda2d5f17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053667"
---
# <a name="iwmpcontrolscurrentposition-property"></a>IWMPControls :: currentPosition, propriété

La propriété **CurrentPosition** obtient ou définit la position actuelle dans l’élément multimédia, en secondes, à partir du début.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Double currentPosition {get; set;}
```


```VB

Public Property currentPosition As System.Double
```





## <a name="property-value"></a>Valeur de la propriété

**System. double** qui correspond à la position actuelle.

## <a name="examples"></a>Exemples

L’exemple suivant utilise **CurrentPosition** pour rechercher une position fournie par l’utilisateur. En réponse à un clic sur un bouton, **CurrentPosition** est défini sur la valeur entrée dans une zone de texte appelée NewPosition. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
private void setPosition_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text);
}
```


```VB

Public Sub setPosition_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setPosition.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text)

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

[**IWMPControls. currentPositionString (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)
</dt> </dl>

 

 





