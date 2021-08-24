---
title: IWMPMediaCollection méthode Remove
description: La méthode Remove supprime un élément spécifié de la collection de supports.
ms.assetid: 2ed45159-0a92-4353-8bf1-1d20de404bf7
keywords:
- supprimer la méthode Lecteur Windows Media
- remove, méthode Lecteur Windows Media, IWMPMediaCollection, interface
- Lecteur Windows Media de l’interface IWMPMediaCollection, remove (méthode)
topic_type:
- apiref
api_name:
- IWMPMediaCollection.remove
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771ae8be7a8a4586c132cb29b3af4d5d9180398d7db7d05e66c6e84b5a013b48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734999"
---
# <a name="iwmpmediacollectionremove-method"></a>IWMPMediaCollection :: Remove, méthode

La `remove` méthode supprime un élément spécifié de la collection de supports.

## <a name="syntax"></a>Syntaxe


```CSharp
public void remove(
  IWMPMedia pItem,
  System.Boolean varfDeleteFile
);
```


```VB

Public Sub remove( _
  ByVal pItem As IWMPMedia, _
  ByVal varfDeleteFile As System.Boolean _
)
Implements IWMPMediaCollection.remove
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*pItem* \[ dans\]
</dt> <dd>

Interface **wmplib. IWMPMedia** qui identifie l’élément à supprimer.

</dd> <dt>

*varfDeleteFile* \[ dans\]
</dt> <dd>

Valeur **System. Boolean** qui spécifie si la méthode doit supprimer l’élément spécifié de la bibliothèque.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode supprime un élément de la bibliothèque. Cette méthode ne supprime pas les fichiers de l’ordinateur de l’utilisateur.

Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

L’exemple suivant, après l’invite de l’utilisateur, supprime définitivement le premier élément multimédia de la collection de supports à l’aide de `remove` . L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.


```CSharp
// Get an interface to the first item from the media collection. 
WMPLib.IWMPMedia3 media = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Store the name of the retrieved media item.
string mediaName = media.name;

// Prepare a message, a caption and buttons for the user prompt.
string message = ("OK to permanently delete " + mediaName + "?");
string caption = "Confirm deletion";
System.Windows.Forms.MessageBoxButtons buttons = System.Windows.Forms.MessageBoxButtons.OKCancel;

// Prompt the user for permission to delete the object.
System.Windows.Forms.DialogResult result = System.Windows.Forms.MessageBox.Show(message, caption, buttons);

// Check the user response.
if (result == System.Windows.Forms.DialogResult.OK)
{
    // Permanently delete the item.
    player.mediaCollection.remove(media, true);

    // Report that the item was deleted.
    System.Windows.Forms.MessageBox.Show("Deleted item " + mediaName);
}
```


```VB

' Get an interface to the first item from the media collection. 
Dim media As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Store the name of the retrieved media item.
Dim mediaName As String = media.name

&#39; Prepare a message, a caption and buttons for the user prompt.
Dim message As String = (&quot;OK to permanently delete &quot; + mediaName + &quot;?&quot;)
Dim caption As String = &quot;Confirm deletion&quot;
Dim buttons As System.Windows.Forms.MessageBoxButtons = System.Windows.Forms.MessageBoxButtons.OKCancel

&#39; Prompt the user for permission to delete the object.
Dim result As System.Windows.Forms.DialogResult = System.Windows.Forms.MessageBox.Show(message, caption, buttons)

&#39; Check the user response.
If (result = System.Windows.Forms.DialogResult.OK) Then

    &#39; Permanently delete the item.
    player.mediaCollection.remove(media, True)

    &#39; Report that the item was deleted.
    System.Windows.Forms.MessageBox.Show(&quot;Deleted item &quot; + mediaName)

End If
```





## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPMedia (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMediaCollection (VB et C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection. add (VB et C#)**](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> </dl>

 

 





