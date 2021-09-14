---
title: Événement d’erreur de l’objet AxWindowsMediaPlayer
description: l’événement d’erreur se produit lorsque le contrôle de Lecteur Windows Media a une condition d’erreur.
ms.assetid: d28c18a9-c650-4169-989b-8727b7a5a831
keywords:
- événement d’erreur de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- Error Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cfd3571538aa2cdd263a9f5d57e479e73818806
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192431"
---
# <a name="error-event-of-the-axwindowsmediaplayer-object"></a>Événement d’erreur de l’objet AxWindowsMediaPlayer

l’événement d’erreur se produit lorsque le contrôle de Lecteur Windows Media a une condition d’erreur.

``` syntax
[C#]
private void player_ErrorEvent(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_ErrorEvent(  
  sender As Object,  
  e As System.EventArgs
) Handles player.ErrorEvent
```

## <a name="event-data"></a>Données d'événements

Cet événement ne contient pas de données.

## <a name="examples"></a>Exemples

L’exemple suivant crée un gestionnaire d’événements pour l’événement d’erreur afin d’afficher le texte de description de la première erreur dans la file d’attente d’erreurs. L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.


```CSharp
// Add a delegate for the Error event.
player.ErrorEvent += new EventHandler(player_ErrorEvent);

private void player_ErrorEvent(object sender, System.EventArgs e)
{
    // Get the description of the first error. 
    string errDesc = player.Error.get_Item(0).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the description of the first error. 
    Dim errDesc As String = player.Error.Item(0).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

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
</dt> <dt>

[**IWMPError. Item (VB et C#)**](iwmperror-item--vb-and-c.md)
</dt> <dt>

[**IWMPErrorItem. errorDescription (VB et C#)**](wmplibiwmperroritem-iwmperroritem-errordescription--vb-and-c.md)
</dt> </dl>

 

 





