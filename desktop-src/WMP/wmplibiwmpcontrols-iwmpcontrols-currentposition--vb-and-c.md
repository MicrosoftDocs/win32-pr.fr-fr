---
title: IWMPControls propriété currentPosition
description: La propriété currentPosition obtient ou définit la position actuelle dans l’élément multimédia, en secondes, à partir du début.
ms.assetid: 48f5241e-7528-485e-bf47-d655ba842af2
keywords:
- propriété currentPosition lecteur Windows Media
- propriété currentPosition lecteur Windows Media, interface IWMPControls
- Interface IWMPControls lecteur Windows Media, propriété currentPosition
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
ms.openlocfilehash: fee8c2c8244d6034069f21033978ce2883ff852d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544121"
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

 

 





