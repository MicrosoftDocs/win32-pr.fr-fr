---
title: IWMPNetwork propriété framesSkipped
description: La propriété framesSkipped obtient le nombre total de trames ignorées lors de la lecture.
ms.assetid: eedecfa9-0c82-4800-979e-ca85fb78c480
keywords:
- Lecteur Windows Media de la propriété framesSkipped
- Lecteur Windows Media de la propriété framesSkipped, interface IWMPNetwork
- Lecteur Windows Media de l’interface IWMPNetwork, propriété framesSkipped
topic_type:
- apiref
api_name:
- IWMPNetwork.framesSkipped
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8409cec50089111184f96e4463f57cc9c4fbae07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120493"
---
# <a name="iwmpnetworkframesskipped-property"></a>IWMPNetwork :: framesSkipped, propriété

La propriété **framesSkipped** obtient le nombre total de trames ignorées lors de la lecture.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 framesSkipped {get; set;}
```


```VB

Public ReadOnly Property framesSkipped As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui correspond au nombre de trames ignorées.

## <a name="examples"></a>Exemples

L’exemple de code suivant utilise **framesSkipped** pour afficher le nombre total de trames ignorées lors de la lecture. Les informations s’affichent dans une étiquette lorsque l’utilisateur clique sur un bouton. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
private void showFramesSkipped_Click(object sender, System.EventArgs e)
{
    framesSkippedLabel.Text = ("Frames skipped: " + player.network.framesSkipped.ToString());
}
```


```VB

Public Sub showFramesSkipped_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showFramesSkipped.Click

    framesSkippedLabel.Text = (&quot;Frames skipped: &quot; + player.network.framesSkipped.ToString())

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

 

 





