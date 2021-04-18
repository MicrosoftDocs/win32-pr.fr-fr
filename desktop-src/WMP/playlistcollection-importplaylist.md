---
title: Méthode PlaylistCollection. importPlaylist
description: La méthode importPlaylist ajoute une sélection statique à la bibliothèque. | Méthode PlaylistCollection. importPlaylist
ms.assetid: 0611ba42-fd8f-4fb9-9fbb-809a82775c2a
keywords:
- méthode importPlaylist lecteur Windows Media
- méthode importPlaylist lecteur Windows Media, classe PlaylistCollection
- Classe PlaylistCollection lecteur Windows Media, méthode importPlaylist
topic_type:
- apiref
api_name:
- PlaylistCollection.importPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736e9afa17f571428fada48660726b606268796a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526326"
---
# <a name="playlistcollectionimportplaylist-method"></a><span data-ttu-id="3a113-107">Méthode PlaylistCollection. importPlaylist</span><span class="sxs-lookup"><span data-stu-id="3a113-107">PlaylistCollection.importPlaylist method</span></span>

<span data-ttu-id="3a113-108">La méthode **importPlaylist** ajoute une sélection statique à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="3a113-108">The **importPlaylist** method adds a static playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a113-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a113-109">Syntax</span></span>


```JScript
retVal = PlaylistCollection.importPlaylist(
  playlist
)
```



## <a name="parameters"></a><span data-ttu-id="3a113-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a113-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a113-111">*sélection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3a113-111">*playlist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a113-112">Objet **playlist** à ajouter.</span><span class="sxs-lookup"><span data-stu-id="3a113-112">**Playlist** object to be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a113-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a113-113">Return value</span></span>

<span data-ttu-id="3a113-114">Cette méthode retourne l’objet **playlist** qui a été ajouté.</span><span class="sxs-lookup"><span data-stu-id="3a113-114">This method returns the **Playlist** object that was added.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a113-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3a113-115">Remarks</span></span>

<span data-ttu-id="3a113-116">Les sélections qui ne contiennent pas d’éléments multimédias ne peuvent pas être ajoutées à la bibliothèque à l’aide de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3a113-116">Playlists that do not contain any media items cannot be added to the library by using this method.</span></span> <span data-ttu-id="3a113-117">Pour créer une playlist vide dans la bibliothèque, utilisez la méthode **newPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="3a113-117">To create an empty playlist in the library, use the **newPlaylist** method.</span></span> <span data-ttu-id="3a113-118">Vous pouvez ensuite remplir la playlist obtenue avec des éléments multimédias à l’aide d’une *sélection*. **appendItem** ou *playlist*. **InsertItem**.</span><span class="sxs-lookup"><span data-stu-id="3a113-118">You can then fill the resulting playlist with media items by using *Playlist*.**appendItem** or *Playlist*.**insertItem**.</span></span>

<span data-ttu-id="3a113-119">Si vous transmettez cette méthode à une sélection automatique, la requête est exécutée une fois et le résultat est ajouté à la bibliothèque en tant que sélection statique.</span><span class="sxs-lookup"><span data-stu-id="3a113-119">If you pass this method an auto playlist, the query is executed once and the result is added to the library as a static playlist.</span></span> <span data-ttu-id="3a113-120">Pour ajouter une sélection automatique à la bibliothèque et conserver son comportement automatique, utilisez *MediaCollection*. **Ajoutez**.</span><span class="sxs-lookup"><span data-stu-id="3a113-120">To add an auto playlist to the library and preserve its automatic behavior, use *MediaCollection*.**add**.</span></span> <span data-ttu-id="3a113-121">Pour plus d’informations, consultez [sélections statiques et automatiques](static-and-auto-playlists.md).</span><span class="sxs-lookup"><span data-stu-id="3a113-121">For more information, see [Static and Auto Playlists](static-and-auto-playlists.md).</span></span>

<span data-ttu-id="3a113-122">Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="3a113-122">To use this method, full access to the library is required.</span></span> <span data-ttu-id="3a113-123">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3a113-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a113-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a113-124">Requirements</span></span>



| <span data-ttu-id="3a113-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a113-125">Requirement</span></span> | <span data-ttu-id="3a113-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a113-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3a113-127">Version</span><span class="sxs-lookup"><span data-stu-id="3a113-127">Version</span></span><br/> | <span data-ttu-id="3a113-128">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3a113-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3a113-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3a113-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="3a113-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a113-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a113-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a113-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a113-132">**Gestion des sélections**</span><span class="sxs-lookup"><span data-stu-id="3a113-132">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="3a113-133">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="3a113-133">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="3a113-134">**MediaCollection. Add**</span><span class="sxs-lookup"><span data-stu-id="3a113-134">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="3a113-135">**Playlist. appendItem**</span><span class="sxs-lookup"><span data-stu-id="3a113-135">**Playlist.appendItem**</span></span>](playlist-appenditem.md)
</dt> <dt>

[<span data-ttu-id="3a113-136">**Playlist. insertItem**</span><span class="sxs-lookup"><span data-stu-id="3a113-136">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="3a113-137">**Objet PlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="3a113-137">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="3a113-138">**PlaylistCollection. newPlaylist**</span><span class="sxs-lookup"><span data-stu-id="3a113-138">**PlaylistCollection.newPlaylist**</span></span>](playlistcollection-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="3a113-139">**PlaylistCollection. Remove**</span><span class="sxs-lookup"><span data-stu-id="3a113-139">**PlaylistCollection.remove**</span></span>](playlistcollection-remove.md)
</dt> <dt>

[<span data-ttu-id="3a113-140">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3a113-140">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="3a113-141">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3a113-141">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





