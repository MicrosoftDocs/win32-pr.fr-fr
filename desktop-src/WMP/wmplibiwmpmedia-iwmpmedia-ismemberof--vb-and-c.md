---
title: Méthode IWMPMedia isMemberOf
description: La méthode isMemberOf retourne une valeur indiquant si l’élément multimédia spécifié est membre de la sélection spécifiée.
ms.assetid: 491e0dd5-38e5-47a5-9c94-f1d27d297f8d
keywords:
- méthode isMemberOf lecteur Windows Media
- méthode isMemberOf lecteur Windows Media, interface IWMPMedia
- Interface IWMPMedia lecteur Windows Media, méthode isMemberOf
topic_type:
- apiref
api_name:
- IWMPMedia.isMemberOf
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f627e9b2f0e1c4b226dda13d280d521ad52df2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526850"
---
# <a name="iwmpmediaismemberof-method"></a><span data-ttu-id="1cfc0-106">IWMPMedia :: isMemberOf, méthode</span><span class="sxs-lookup"><span data-stu-id="1cfc0-106">IWMPMedia::isMemberOf method</span></span>

<span data-ttu-id="1cfc0-107">La méthode **isMemberOf** retourne une valeur indiquant si l’élément multimédia spécifié est membre de la sélection spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1cfc0-107">The **isMemberOf** method returns a value indicating whether the specified media item is a member of the specified playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cfc0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cfc0-108">Syntax</span></span>


```CSharp
public System.Boolean isMemberOf(
  IWMPPlaylist pPlaylist
);
```


```VB

Public Function isMemberOf( _
  ByVal pPlaylist As IWMPPlaylist _
) As System.Boolean
Implements IWMPMedia.isMemberOf
```





## <a name="parameters"></a><span data-ttu-id="1cfc0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cfc0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cfc0-110">*pPlaylist* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1cfc0-110">*pPlaylist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cfc0-111">Interface **wmplib. IWMPPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="1cfc0-111">A **WMPLib.IWMPPlaylist** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cfc0-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1cfc0-112">Return value</span></span>

<span data-ttu-id="1cfc0-113">Valeur **System. Boolean** qui indique si l’élément multimédia est membre de la sélection.</span><span class="sxs-lookup"><span data-stu-id="1cfc0-113">A **System.Boolean** value that indicates whether the media item is a member of the playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cfc0-114">Notes</span><span class="sxs-lookup"><span data-stu-id="1cfc0-114">Remarks</span></span>

<span data-ttu-id="1cfc0-115">Cette méthode ne peut pas vérifier les sélections récupérées par le biais de l’interface **IWMPMediaCollection** .</span><span class="sxs-lookup"><span data-stu-id="1cfc0-115">This method cannot check playlists retrieved through the **IWMPMediaCollection** interface.</span></span> <span data-ttu-id="1cfc0-116">Pour déterminer si un élément multimédia est membre d’une sélection nommée particulière, récupérez la collection de sélections avec la propriété **AxWindowsMediaPlayer. playlistCollection** .</span><span class="sxs-lookup"><span data-stu-id="1cfc0-116">To test whether a media item is a member of a particular named playlist, retrieve the playlist collection with the **AxWindowsMediaPlayer.playlistCollection** property.</span></span> <span data-ttu-id="1cfc0-117">Une fois que vous récupérez la collection, récupérez la playlist en appelant la méthode **IWMPPlaylistCollection. GetByName** .</span><span class="sxs-lookup"><span data-stu-id="1cfc0-117">Once you retrieve the collection, retrieve the individual playlist by calling the **IWMPPlaylistCollection.getByName** method.</span></span>

<span data-ttu-id="1cfc0-118">Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="1cfc0-118">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="1cfc0-119">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="1cfc0-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1cfc0-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="1cfc0-120">Examples</span></span>

<span data-ttu-id="1cfc0-121">L’exemple suivant utilise **isMemberOf** pour déterminer si l’élément multimédia actuel est membre de la sélection nommée All Music.</span><span class="sxs-lookup"><span data-stu-id="1cfc0-121">The following example uses **isMemberOf** to test whether the current media item is a member of the playlist named All Music.</span></span> <span data-ttu-id="1cfc0-122">Si ce n’est pas le cas, l’élément multimédia actuel est ajouté à la sélection.</span><span class="sxs-lookup"><span data-stu-id="1cfc0-122">If it is not, the current media item is appended to the playlist.</span></span> <span data-ttu-id="1cfc0-123">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="1cfc0-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the playlist named All Music.
WMPLib.IWMPPlaylist sPlaylist = player.playlistCollection.getByName("All Music").Item(0);

// Test whether the current media item is a member of the All Music playlist.
// If it is not a member, append the current media item to the playlist.
if (player.currentMedia.isMemberOf(sPlaylist) == false)
{
    sPlaylist.appendItem(player.currentMedia);
}
```


```VB

' Get an interface to the playlist named All Music.
Dim sPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Test whether the current media item is a member of the All Music playlist.
&#39; If it is not a member, then append the current media item to the playlist.
If (player.currentMedia.isMemberOf(sPlaylist) = False) Then

    sPlaylist.appendItem(player.currentMedia)

End If
```





## <a name="requirements"></a><span data-ttu-id="1cfc0-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cfc0-124">Requirements</span></span>



| <span data-ttu-id="1cfc0-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cfc0-125">Requirement</span></span> | <span data-ttu-id="1cfc0-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cfc0-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cfc0-127">Version</span><span class="sxs-lookup"><span data-stu-id="1cfc0-127">Version</span></span><br/>   | <span data-ttu-id="1cfc0-128">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="1cfc0-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1cfc0-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1cfc0-129">Namespace</span></span><br/> | <span data-ttu-id="1cfc0-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1cfc0-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1cfc0-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="1cfc0-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1cfc0-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1cfc0-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cfc0-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cfc0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cfc0-134">**AxWindowsMediaPlayer. playlistCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="1cfc0-134">**AxWindowsMediaPlayer.playlistCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1cfc0-135">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="1cfc0-135">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1cfc0-136">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="1cfc0-136">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1cfc0-137">**IWMPPlaylistCollection. getByName (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="1cfc0-137">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





