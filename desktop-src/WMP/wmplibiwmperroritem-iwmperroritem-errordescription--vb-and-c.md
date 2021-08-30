---
title: Propriété errorDescription IWMPErrorItem
description: La propriété errorDescription obtient une description de l’erreur.
ms.assetid: a9914c24-1d10-422a-bcba-80be9fb85108
keywords:
- propriété errorDescription Lecteur Windows Media
- propriété errorDescription Lecteur Windows Media, interface IWMPErrorItem
- Lecteur Windows Media de l’interface IWMPErrorItem, propriété errorDescription
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2976db1b8c67a3b467dfed87eeab13ff9ab46d21f0778dc0542b97080f231943
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031189"
---
# <a name="iwmperroritemerrordescription-property"></a>IWMPErrorItem :: errorDescription, propriété

La propriété **errorDescription** obtient une description de l’erreur.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String errorDescription {get; set;}
```


```VB

Public ReadOnly Property errorDescription As System.String
```





## <a name="property-value"></a>Valeur de la propriété

**System. String** qui est la description de l’erreur.

## <a name="remarks"></a>Remarques

Vous devez définir **IWMPSettings. enableErrorDialogs** sur **false** si vous choisissez d’afficher des messages d’erreur personnalisés.

## <a name="examples"></a>Exemples

L’exemple suivant utilise **errorDescription** dans un gestionnaire d’événements d’erreur pour afficher la description de l’erreur à l’utilisateur. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
private void player_ErrorEvent_errorDescription(object sender, System.EventArgs e)
{
    // Get the error description for the first error item.
    string errDesc = player.Error.get_Item(0).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show("Error: " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorDescription(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error description for the first error item.
    Dim errDesc As String = player.Error.Item(0).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(&quot;Error: &quot; + errDesc)

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

[**Interface IWMPErrorItem (VB et C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. enableErrorDialogs (VB et C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





