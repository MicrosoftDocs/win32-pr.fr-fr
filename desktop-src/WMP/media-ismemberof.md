---
title: Méthode Media. isMemberOf
description: La méthode isMemberOf retourne une valeur indiquant si l’élément multimédia est membre de la sélection spécifiée.
ms.assetid: e620741f-6807-4a61-ba9b-f45426d6e33e
keywords:
- méthode isMemberOf lecteur Windows Media
- méthode isMemberOf lecteur Windows Media, classe multimédia
- Classe multimédia lecteur Windows Media, méthode isMemberOf
topic_type:
- apiref
api_name:
- Media.isMemberOf
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41555bd5910ddb3151468a458c5becbf247ea484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540209"
---
# <a name="mediaismemberof-method"></a><span data-ttu-id="3804e-106">Méthode Media. isMemberOf</span><span class="sxs-lookup"><span data-stu-id="3804e-106">Media.isMemberOf method</span></span>

<span data-ttu-id="3804e-107">La méthode **isMemberOf** retourne une valeur indiquant si l’élément multimédia est membre de la sélection spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3804e-107">The **isMemberOf** method returns a value indicating whether the media item is a member of the specified playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="3804e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3804e-108">Syntax</span></span>


```JScript
bRetVal = Media.isMemberOf(
  playlist
)
```



## <a name="parameters"></a><span data-ttu-id="3804e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3804e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3804e-110">*sélection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3804e-110">*playlist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3804e-111">Objet **playlist** qui peut contenir l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="3804e-111">**Playlist** object that might contain the media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3804e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3804e-112">Return value</span></span>

<span data-ttu-id="3804e-113">Cette méthode retourne une **valeur booléenne**.</span><span class="sxs-lookup"><span data-stu-id="3804e-113">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3804e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3804e-114">Remarks</span></span>

<span data-ttu-id="3804e-115">Cette méthode ne peut pas vérifier les sélections récupérées par le biais de l’objet **MediaCollection** .</span><span class="sxs-lookup"><span data-stu-id="3804e-115">This method is cannot check playlists retrieved through the **MediaCollection** object.</span></span> <span data-ttu-id="3804e-116">Pour déterminer si un élément multimédia est membre d’une sélection nommée particulière, récupérez la sélection avec le *lecteur*. *playlistCollection*. **GetByName**(*nom*). **Item**(0).</span><span class="sxs-lookup"><span data-stu-id="3804e-116">To test whether a media item is a member of a particular named playlist, retrieve the playlist with *player*.*playlistCollection*.**getByName**(*name*).**item**(0).</span></span> <span data-ttu-id="3804e-117">Cette méthode peut également être utilisée avec les sélections de CD et les sélections de métafichiers.</span><span class="sxs-lookup"><span data-stu-id="3804e-117">This method can also be used with CD playlists and metafile playlists.</span></span>

<span data-ttu-id="3804e-118">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="3804e-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="3804e-119">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3804e-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3804e-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="3804e-120">Examples</span></span>

<span data-ttu-id="3804e-121">L’exemple JScript suivant utilise un *média*. **isMemberOf** pour vérifier si l’élément multimédia actuel est membre de la sélection nommée Sample playlist.</span><span class="sxs-lookup"><span data-stu-id="3804e-121">The following JScript example uses *Media*.**isMemberOf** to test whether the current media item is a member of the playlist named Sample Playlist.</span></span> <span data-ttu-id="3804e-122">Si ce n’est pas le cas, l’élément multimédia actuel est ajouté à l’exemple de sélection.</span><span class="sxs-lookup"><span data-stu-id="3804e-122">If it is not, the current media item is appended to the sample playlist.</span></span> <span data-ttu-id="3804e-123">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="3804e-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the playlist object named Sample Playlist.
var sPlaylist = Player.playlistcollection.getbyname("Sample Playlist").item(0);

// Test whether the current media item is a member of Sample Playlist.
 var answer = ((Player.currentMedia.isMemberOf(sPlaylist))?"Yes":"No");

// If the current media item is not a member of Sample Playlist,
// append the current media item to the playlist.
if (answer == "No"){
   sPlaylist.appendItem(Player.currentMedia);
}

```



## <a name="requirements"></a><span data-ttu-id="3804e-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3804e-124">Requirements</span></span>



| <span data-ttu-id="3804e-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3804e-125">Requirement</span></span> | <span data-ttu-id="3804e-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3804e-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3804e-127">Version</span><span class="sxs-lookup"><span data-stu-id="3804e-127">Version</span></span><br/> | <span data-ttu-id="3804e-128">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3804e-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3804e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3804e-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="3804e-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3804e-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3804e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3804e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3804e-132">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="3804e-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="3804e-133">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="3804e-133">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="3804e-134">**Objet PlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="3804e-134">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="3804e-135">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3804e-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="3804e-136">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3804e-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





