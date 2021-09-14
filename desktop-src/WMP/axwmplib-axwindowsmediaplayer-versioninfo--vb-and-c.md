---
title: AxWindowsMediaPlayer. versionInfo, propriété
description: la propriété versionInfo obtient une valeur qui spécifie la version du Lecteur Windows Media.
ms.assetid: e128bec5-1ae9-4710-800e-4f97df362909
keywords:
- Lecteur Windows Media de propriétés versionInfo
- Lecteur Windows Media de propriétés versionInfo, classe AxWindowsMediaPlayer
- Lecteur Windows Media de la classe AxWindowsMediaPlayer, propriété versionInfo
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.versionInfo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2f759c2aedb19e21c4b7d90f3634141e4c37ec8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193299"
---
# <a name="axwindowsmediaplayerversioninfo-property"></a>AxWindowsMediaPlayer. versionInfo, propriété

la propriété versionInfo obtient une valeur qui spécifie la version du Lecteur Windows Media.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String versionInfo {get;}
```


```VB

Public ReadOnly Property versionInfo As System.String
```





## <a name="property-value"></a>Valeur de la propriété

System. String qui correspond aux informations de version au format suivant : «*X*. 0,0. *Yyyy*"où *X* représente le numéro de version principale et *yyyy* représente le numéro de Build.

## <a name="examples"></a>Exemples

l’exemple suivant crée un bouton qui, lorsque vous cliquez dessus, affiche une boîte de message contenant les informations de version de Lecteur Windows Media. L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.


```CSharp
private void showVersion_Click(object sender, System.EventArgs e)
{
    // Build the message containing the version info. 
    string message = ("Windows Media Player Version: " + player.versionInfo);

    // Display the message. 
    System.Windows.Forms.MessageBox.Show(message);
}
```


```VB

Public Sub showVersion_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showVersion.Click

    &#39; Build the message containing the version info. 
    Dim message As String = (&quot;Windows Media Player Version: &quot; + player.versionInfo)

    &#39; Display the message. 
    System.Windows.Forms.MessageBox.Show(message)

End Sub
```





## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





