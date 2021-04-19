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
# <a name="currentplaylistchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="ef5b1-105">Événement CurrentPlaylistChange de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="ef5b1-105">CurrentPlaylistChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="ef5b1-106">L’événement CurrentPlaylistChange se produit en cas de modification de la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="ef5b1-106">The CurrentPlaylistChange event occurs when something changes within the current playlist.</span></span>

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

## <a name="event-data"></a><span data-ttu-id="ef5b1-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="ef5b1-107">Event Data</span></span>

<span data-ttu-id="ef5b1-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="ef5b1-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistChangeEventHandler**.</span></span> <span data-ttu-id="ef5b1-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistChangeEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="ef5b1-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="ef5b1-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="ef5b1-110">Property</span></span> | <span data-ttu-id="ef5b1-111">Description</span><span class="sxs-lookup"><span data-stu-id="ef5b1-111">Description</span></span>                                                                                                                   |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef5b1-112">Modifier</span><span class="sxs-lookup"><span data-stu-id="ef5b1-112">change</span></span>   | <span data-ttu-id="ef5b1-113">Valeur d’énumération WMPLib. WMPPlaylistChangeEventTypeAn indiquant le type de modification qui s’est produite dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="ef5b1-113">WMPLib.WMPPlaylistChangeEventTypeAn enumeration value indicating the type of change that occurred to the playlist.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ef5b1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ef5b1-114">Remarks</span></span>

<span data-ttu-id="ef5b1-115">Cet événement ne se produit pas lorsqu’une sélection différente devient la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="ef5b1-115">This event does not occur when a different playlist becomes the current playlist.</span></span> <span data-ttu-id="ef5b1-116">Cela se produit uniquement lorsqu’une modification se produit dans la sélection actuelle, par exemple un élément multimédia ajouté à la sélection.</span><span class="sxs-lookup"><span data-stu-id="ef5b1-116">It occurs only when a change happens within the current playlist, such as a media item being appended to the playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="ef5b1-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="ef5b1-117">Examples</span></span>

<span data-ttu-id="ef5b1-118">L’exemple suivant affiche les noms de tous les éléments multimédias dans la sélection en cours en réponse à l’événement CurrentPlaylistChange.</span><span class="sxs-lookup"><span data-stu-id="ef5b1-118">The following example displays the names of all the media items in the current playlist in response to the CurrentPlaylistChange Event.</span></span> <span data-ttu-id="ef5b1-119">L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="ef5b1-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


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





## <a name="requirements"></a><span data-ttu-id="ef5b1-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef5b1-120">Requirements</span></span>



| <span data-ttu-id="ef5b1-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef5b1-121">Requirement</span></span> | <span data-ttu-id="ef5b1-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef5b1-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef5b1-123">Version</span><span class="sxs-lookup"><span data-stu-id="ef5b1-123">Version</span></span><br/>   | <span data-ttu-id="ef5b1-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ef5b1-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="ef5b1-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ef5b1-125">Namespace</span></span><br/> | <span data-ttu-id="ef5b1-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="ef5b1-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="ef5b1-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="ef5b1-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ef5b1-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ef5b1-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef5b1-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef5b1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef5b1-130">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="ef5b1-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ef5b1-131">**AxWindowsMediaPlayer. currentPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="ef5b1-131">**AxWindowsMediaPlayer.currentPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ef5b1-132">**Événement AxWindowsMediaPlayer. PlaylistChange (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="ef5b1-132">**AxWindowsMediaPlayer.PlaylistChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playlistchange.md)
</dt> <dt>

[<span data-ttu-id="ef5b1-133">**WMPPlaylistChangeEventType**</span><span class="sxs-lookup"><span data-stu-id="ef5b1-133">**WMPPlaylistChangeEventType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaylistchangeeventtype)
</dt> </dl>

 

 





