---
title: IWMPSettings muet, propriété
description: La propriété Mute obtient ou définit une valeur indiquant si l’audio est muet.
ms.assetid: d99e47db-70cc-41e0-aca9-b765b075e7b4
keywords:
- Lecteur Windows Media de propriété muet
- propriété muet Lecteur Windows Media, interface IWMPSettings
- Lecteur Windows Media de l’interface IWMPSettings, propriété muet
topic_type:
- apiref
api_name:
- IWMPSettings.mute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d4cb13fd8884df7779b2780fd7014d058f32086d67ace286d9d8a9fd57cb8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053407"
---
# <a name="iwmpsettingsmute-property"></a>IWMPSettings :: Mute, propriété

La propriété **Mute** obtient ou définit une valeur indiquant si l’audio est muet.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Boolean mute {get; set;}
```


```VB

Public Property mute As System.Boolean
```





## <a name="property-value"></a>Valeur de la propriété

Valeur **System. Boolean** indiquant si l’audio est muet. La valeur par défaut est **false**.

## <a name="examples"></a>Exemples

L’exemple suivant permet de créer une case à cocher et de basculer la propriété **muet** sur muet et de désactiver l’audio lorsque l’état activé de la case est modifié. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
private void Mute_CheckStateChanged(object sender, System.EventArgs e)
{
    System.Windows.Forms.CheckBox Mute = (System.Windows.Forms.CheckBox)sender;

    // Change the check box text depending on the checked state.
    Mute.Text = Mute.Checked ? "Un-mute Audio" : Mute.Text = "Mute Audio";

    // Use the checked state to set the mute property. 
    player.settings.mute = Mute.Checked;
}
```


```VB

Public Sub Mute_CheckStateChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles Mute.CheckStateChanged

    Dim cb As System.Windows.Forms.CheckBox = sender

    &#39;  Change the check box text depending on the checked state.
    If (cb.Checked) Then

        cb.Text = &quot;Un-mute Audio&quot;

    Else

        cb.Text = &quot;Mute Audio&quot;

    End If

    &#39;  Use the checked state to set the mute property. 
    player.settings.mute = cb.Checked

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

[**Interface IWMPSettings (VB et C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. rate (VB et C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





