---
title: IWMPErrorItem errorCode, propriété
description: La propriété errorCode obtient le code d’erreur actuel.
ms.assetid: 00719067-685d-4ef2-9eec-72c7892fcdb9
keywords:
- errorCode, propriété Lecteur Windows Media
- errorCode, propriété Lecteur Windows Media, IWMPErrorItem, interface
- Lecteur Windows Media de l’interface IWMPErrorItem, propriété errorCode
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorCode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d7179684fb0332e25716282adfd47a5f769493f646f73c82d0391bbce4e6a91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031209"
---
# <a name="iwmperroritemerrorcode-property"></a>IWMPErrorItem :: errorCode, propriété

La propriété **ErrorCode** obtient le code d’erreur actuel.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 errorCode {get; set;}
```


```VB

Public ReadOnly Property errorCode As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui correspond au code d’erreur.

## <a name="remarks"></a>Remarques

Vous devez définir **IWMPSettings. enableErrorDialogs** sur **false** si vous choisissez d’afficher des messages d’erreur personnalisés.

## <a name="examples"></a>Exemples

L’exemple suivant utilise **ErrorCode** dans un gestionnaire d’événements d’erreur pour afficher le code d’erreur à l’utilisateur. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
private void player_ErrorEvent_errorCode(object sender, System.EventArgs e)
{
    // Get the error code for the first error item.
    int errCode = player.Error.get_Item(0).errorCode;

    // Display the error code.
    System.Windows.Forms.MessageBox.Show("Error number: " + errCode.ToString());
}
```


```VB

Public Sub player_ErrorEvent_errorCode(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error code for the first error item.
    Dim errCode As Integer = player.Error.Item(0).errorCode

    &#39; Display the error code.
    System.Windows.Forms.MessageBox.Show(&quot;Error number: &quot; + errCode.ToString())

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

 

 





