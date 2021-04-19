---
title: Player. newPlaylist, méthode
description: La méthode newPlaylist crée un nouvel objet playlist.
ms.assetid: a566006e-8647-4c51-ab77-762728f25a30
keywords:
- méthode newPlaylist lecteur Windows Media
- méthode newPlaylist lecteur Windows Media, classe Player
- Classe player lecteur Windows Media, méthode newPlaylist
topic_type:
- apiref
api_name:
- Player.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa65ae4b453fe919116a33c5ee86b14ba353f681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537338"
---
# <a name="playernewplaylist-method"></a><span data-ttu-id="2d910-106">Player. newPlaylist, méthode</span><span class="sxs-lookup"><span data-stu-id="2d910-106">Player.newPlaylist method</span></span>

<span data-ttu-id="2d910-107">La méthode **newPlaylist** crée un nouvel objet **playlist** .</span><span class="sxs-lookup"><span data-stu-id="2d910-107">The **newPlaylist** method creates a new **Playlist** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d910-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d910-108">Syntax</span></span>


```JScript
retVal = Player.newPlaylist(
  name,
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="2d910-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d910-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d910-110">*nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d910-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d910-111">**Chaîne** contenant le nom de la nouvelle sélection.</span><span class="sxs-lookup"><span data-stu-id="2d910-111">**String** containing the name of the new playlist.</span></span>

</dd> <dt>

<span data-ttu-id="2d910-112">*URL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d910-112">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d910-113">**Chaîne** contenant l’URL de la sélection des métafichiers Windows Media pour créer l’objet de **sélection** .</span><span class="sxs-lookup"><span data-stu-id="2d910-113">**String** containing the URL of the Windows Media metafile playlist to create the **Playlist** object with.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d910-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d910-114">Return value</span></span>

<span data-ttu-id="2d910-115">Cette méthode retourne un objet **playlist** .</span><span class="sxs-lookup"><span data-stu-id="2d910-115">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d910-116">Notes</span><span class="sxs-lookup"><span data-stu-id="2d910-116">Remarks</span></span>

<span data-ttu-id="2d910-117">Si le paramètre *URL* a la valeur null ou «» (chaîne vide), un objet **playlist** vide est créé.</span><span class="sxs-lookup"><span data-stu-id="2d910-117">If the *URL* parameter is set to null or "" (empty string), an empty **Playlist** object will be created.</span></span> <span data-ttu-id="2d910-118">Si le paramètre *Name* est défini sur «», le nom dans le métafichier est utilisé.</span><span class="sxs-lookup"><span data-stu-id="2d910-118">If the *name* parameter is set to "", the name in the metafile is used.</span></span>

<span data-ttu-id="2d910-119">La nouvelle playlist créée avec cette méthode n’est pas ajoutée à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="2d910-119">The new playlist created with this method is not added to the library.</span></span> <span data-ttu-id="2d910-120">Pour ajouter une nouvelle sélection à la bibliothèque, utilisez *PlaylistCollection*. **importPlaylist** ou *PlaylistCollection*. **newPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="2d910-120">To add a new playlist to the library, use *PlaylistCollection*.**importPlaylist** or *PlaylistCollection*.**newPlaylist**.</span></span> <span data-ttu-id="2d910-121">Tout espace de début ou de fin dans le nom de la playlist est automatiquement supprimé lorsqu’il est ajouté à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="2d910-121">Any leading or trailing spaces in the playlist name are automatically removed when it is added to the library.</span></span>

<span data-ttu-id="2d910-122">Étant donné que la bibliothèque autorise plusieurs sélections portant le même nom, vous souhaiterez peut-être vérifier la présence d’une sélection avec un nom donné avant d’en ajouter une nouvelle.</span><span class="sxs-lookup"><span data-stu-id="2d910-122">Because the library allows multiple playlists with the same name, you may want to check for the presence of a playlist with a given name before adding a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d910-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d910-123">Requirements</span></span>



| <span data-ttu-id="2d910-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d910-124">Requirement</span></span> | <span data-ttu-id="2d910-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d910-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2d910-126">Version</span><span class="sxs-lookup"><span data-stu-id="2d910-126">Version</span></span><br/> | <span data-ttu-id="2d910-127">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2d910-127">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="2d910-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2d910-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="2d910-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d910-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d910-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d910-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d910-131">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="2d910-131">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="2d910-132">**PlaylistCollection.importPlaylist**</span><span class="sxs-lookup"><span data-stu-id="2d910-132">**PlaylistCollection.importPlaylist**</span></span>](playlistcollection-importplaylist.md)
</dt> <dt>

[<span data-ttu-id="2d910-133">**PlaylistCollection. newPlaylist**</span><span class="sxs-lookup"><span data-stu-id="2d910-133">**PlaylistCollection.newPlaylist**</span></span>](playlistcollection-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="2d910-134">**Fichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="2d910-134">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 





