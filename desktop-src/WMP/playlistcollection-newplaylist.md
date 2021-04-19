---
title: Méthode PlaylistCollection. newPlaylist
description: La méthode newPlaylist crée une nouvelle sélection dans la bibliothèque.
ms.assetid: 428b5779-4dc0-466b-9834-6b2c43324013
keywords:
- méthode newPlaylist lecteur Windows Media
- méthode newPlaylist lecteur Windows Media, classe PlaylistCollection
- Classe PlaylistCollection lecteur Windows Media, méthode newPlaylist
topic_type:
- apiref
api_name:
- PlaylistCollection.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d94c25a8dfe6f1eb7c4dac40dd644433a5f0d7e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537612"
---
# <a name="playlistcollectionnewplaylist-method"></a><span data-ttu-id="dd0c4-106">Méthode PlaylistCollection. newPlaylist</span><span class="sxs-lookup"><span data-stu-id="dd0c4-106">PlaylistCollection.newPlaylist method</span></span>

<span data-ttu-id="dd0c4-107">La méthode **newPlaylist** crée une nouvelle sélection dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-107">The **newPlaylist** method creates a new playlist in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd0c4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd0c4-108">Syntax</span></span>


```JScript
retVal = PlaylistCollection.newPlaylist(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="dd0c4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd0c4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd0c4-110">*nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dd0c4-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd0c4-111">**Chaîne** contenant le nom de la sélection à créer.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-111">**String** containing the name of the playlist to be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd0c4-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd0c4-112">Return value</span></span>

<span data-ttu-id="dd0c4-113">Cette méthode retourne un objet **playlist** .</span><span class="sxs-lookup"><span data-stu-id="dd0c4-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd0c4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="dd0c4-114">Remarks</span></span>

<span data-ttu-id="dd0c4-115">Cette méthode crée une sélection vide dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-115">This method creates an empty playlist in the library.</span></span> <span data-ttu-id="dd0c4-116">Pour remplir la sélection avec des éléments multimédias, utilisez la *sélection*. **appendItem** ou *playlist*. **InsertItem**.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-116">To fill the playlist with media items, use *Playlist*.**appendItem** or *Playlist*.**insertItem**.</span></span>

<span data-ttu-id="dd0c4-117">Plusieurs playlists portant le même nom sont autorisées dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-117">Multiple playlists having the same name are permitted in the library.</span></span> <span data-ttu-id="dd0c4-118">Pour éviter de créer un nom de playlist dupliqué avec cette méthode, utilisez **GetByName** et *PlaylistArray*. **Count** pour déterminer si une sélection portant un nom particulier existe déjà.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-118">To avoid creating a duplicate playlist name with this method, use **getByName** and *PlaylistArray*.**count** to determine whether a playlist with a particular name already exists.</span></span>

<span data-ttu-id="dd0c4-119">Les espaces de début et de fin ne sont pas autorisés dans les noms de playlist et sont automatiquement supprimés de la valeur spécifiée pour le paramètre *Name* .</span><span class="sxs-lookup"><span data-stu-id="dd0c4-119">Leading and trailing spaces are not permitted in playlist names, and are automatically removed from the value specified for the *name* parameter.</span></span>

<span data-ttu-id="dd0c4-120">Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-120">To use this method, full access to the library is required.</span></span> <span data-ttu-id="dd0c4-121">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="dd0c4-121">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="dd0c4-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="dd0c4-122">Examples</span></span>

<span data-ttu-id="dd0c4-123">L’exemple JScript suivant crée une nouvelle sélection vide appelée « ThreeList ».</span><span class="sxs-lookup"><span data-stu-id="dd0c4-123">The following JScript example creates a new empty playlist called "ThreeList".</span></span> <span data-ttu-id="dd0c4-124">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="dd0c4-124">The **Player** object was created with ID="Player".</span></span>


```JScript
//Add a new empty playlist, named ThreeList, to the playlist collection.
var NewList = Player.playlistCollection.newPlaylist("ThreeList");

```



## <a name="requirements"></a><span data-ttu-id="dd0c4-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd0c4-125">Requirements</span></span>



| <span data-ttu-id="dd0c4-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd0c4-126">Requirement</span></span> | <span data-ttu-id="dd0c4-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd0c4-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dd0c4-128">Version</span><span class="sxs-lookup"><span data-stu-id="dd0c4-128">Version</span></span><br/> | <span data-ttu-id="dd0c4-129">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="dd0c4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="dd0c4-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="dd0c4-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd0c4-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd0c4-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd0c4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd0c4-133">**MediaCollection. Add**</span><span class="sxs-lookup"><span data-stu-id="dd0c4-133">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="dd0c4-134">**Playlist. appendItem**</span><span class="sxs-lookup"><span data-stu-id="dd0c4-134">**Playlist.appendItem**</span></span>](playlist-appenditem.md)
</dt> <dt>

[<span data-ttu-id="dd0c4-135">**Playlist. insertItem**</span><span class="sxs-lookup"><span data-stu-id="dd0c4-135">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="dd0c4-136">**PlaylistArray. Count**</span><span class="sxs-lookup"><span data-stu-id="dd0c4-136">**PlaylistArray.count**</span></span>](playlistarray-count.md)
</dt> <dt>

[<span data-ttu-id="dd0c4-137">**Objet PlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="dd0c4-137">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="dd0c4-138">**PlaylistCollection.getByName**</span><span class="sxs-lookup"><span data-stu-id="dd0c4-138">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> <dt>

[<span data-ttu-id="dd0c4-139">**PlaylistCollection.importPlaylist**</span><span class="sxs-lookup"><span data-stu-id="dd0c4-139">**PlaylistCollection.importPlaylist**</span></span>](playlistcollection-importplaylist.md)
</dt> <dt>

[<span data-ttu-id="dd0c4-140">**PlaylistCollection. Remove**</span><span class="sxs-lookup"><span data-stu-id="dd0c4-140">**PlaylistCollection.remove**</span></span>](playlistcollection-remove.md)
</dt> <dt>

[<span data-ttu-id="dd0c4-141">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="dd0c4-141">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="dd0c4-142">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="dd0c4-142">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





