---
title: Événement CurrentPlaylistChange de l’objet AxWindowsMediaPlayer
description: L’événement CurrentPlaylistChange se produit en cas de modification de la sélection actuelle. | Événement CurrentPlaylistChange de l’objet AxWindowsMediaPlayer
ms.assetid: 1f9c99a4-7d10-48bf-b5ff-b1c1d6753b20
keywords:
- Événement CurrentPlaylistChange de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- CurrentPlaylistChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f99f34f0e02d03352a61bbfca6767295d63d59a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529653"
---
# <a name="currentplaylistchange-event-of-the-axwindowsmediaplayer-object"></a>Événement CurrentPlaylistChange de l’objet AxWindowsMediaPlayer

L’événement CurrentPlaylistChange se produit en cas de modification de la sélection actuelle.

``` syntax
[C#]
private void player_CurrentPlaylistChange(
  object sender,
  _WMPOCXEvents_CurrentPlaylistChangeEvent e
)

[Visual Basic]
Private Sub player_CurrentPlaylistChange(
  sender As Object,
  e As _WMPOCXEvents_CurrentPlaylistChangeEvent
) Handles player.CurrentPlaylistChange
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistChangeEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistChangeEvent**, qui contient la propriété suivante associée à cet événement.



| Propriété | Description                                                                                                                   |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| Modifier   | Valeur d’énumération WMPLib. WMPPlaylistChangeEventTypeAn indiquant le type de modification qui s’est produite dans la sélection.<br/> |



 

## <a name="remarks"></a>Notes

Cet événement ne se produit pas lorsqu’une sélection différente devient la sélection actuelle. Cela se produit uniquement lorsqu’une modification se produit dans la sélection actuelle, par exemple un élément multimédia ajouté à la sélection.

## <a name="examples"></a>Exemples

L’exemple suivant affiche les noms de tous les éléments multimédias dans la sélection en cours en réponse à l’événement CurrentPlaylistChange. L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.


```CSharp
// Add a delegate for the CurrentPlaylistChange event.
player.CurrentPlaylistChange += new AxWMPLib._WMPOCXEvents_CurrentPlaylistChangeEventHandler(player_CurrentPlaylistChange);  


private void player_CurrentPlaylistChange(object sender, AxWMPLib._WMPOCXEvents_CurrentPlaylistChangeEvent e)
{
    switch(e.change)
    {
        // Only update the list for the move, delete, insert, and append event types.
        case WMPLib.WMPPlaylistChangeEventType.wmplcMove:    // Value = 3
        case WMPLib.WMPPlaylistChangeEventType.wmplcDelete:  // Value = 4
        case WMPLib.WMPPlaylistChangeEventType.wmplcInsert:  // Value = 5
        case WMPLib.WMPPlaylistChangeEventType.wmplcAppend:  // Value = 6

        // Create a string array large enough to hold all of the media item names.
        int count = player.currentPlaylist.count;
        string[] mediaItems = new string[count];

        // Clear any previous contents of the text box.
        playlistItems.Clear();

        // Loop through the playlist and store each media item name.
        for (int i = 0; i < count; i++)
        {
            mediaItems[i] = player.currentPlaylist.get_Item(i).name;
        }

        // Display the media item names.
        playlistItems.Lines = mediaItems;
        break;
      
        default:
            break;
    }
}
```


```VB

Public Sub player_CurrentPlaylistChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_CurrentPlaylistChangeEvent) Handles player.CurrentPlaylistChange

    Select Case e.change

        &#39; Only update the list for the move, delete, insert, and append event types.
        Case WMPLib.WMPPlaylistChangeEventType.wmplcMove   &#39; Value = 3
        Case WMPLib.WMPPlaylistChangeEventType.wmplcDelete &#39; Value = 4
        Case WMPLib.WMPPlaylistChangeEventType.wmplcInsert &#39; Value = 5
        Case WMPLib.WMPPlaylistChangeEventType.wmplcAppend &#39; Value = 6

            &#39; Create a string array large enough to hold all of the media item names.
            Dim count As Integer = player.currentPlaylist.count
            Dim mediaItems(count) As String

            &#39; Clear any previous contents of the text box.
            playlistItems.Clear()

            &#39; Loop through the playlist and store each media item name.
            For i As Integer = 0 To (count - 1)

                mediaItems(i) = player.currentPlaylist.Item(i).name

            Next i

            &#39; Display the media item names.
            playlistItems.Lines = mediaItems
    End Select

End Sub
```





## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. currentPlaylist (VB et C#)**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**Événement AxWindowsMediaPlayer. PlaylistChange (VB et C#)**](axwmplib-axwindowsmediaplayer-playlistchange.md)
</dt> <dt>

[**WMPPlaylistChangeEventType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaylistchangeeventtype)
</dt> </dl>

 

 





