---
title: Méthode PlaylistCollection. getByName
description: La méthode getByName récupère un objet PlaylistArray contenant des sélections portant le nom spécifié, le cas échéant.
ms.assetid: 0308a98d-1149-4367-b602-33fa54c1760f
keywords:
- méthode getByName lecteur Windows Media
- méthode getByName lecteur Windows Media, classe PlaylistCollection
- Classe PlaylistCollection lecteur Windows Media, méthode getByName
topic_type:
- apiref
api_name:
- PlaylistCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7954df8e0ccc487df77ea31b3a26dce9eea6d2e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539974"
---
# <a name="playlistcollectiongetbyname-method"></a><span data-ttu-id="ed2f1-106">Méthode PlaylistCollection. getByName</span><span class="sxs-lookup"><span data-stu-id="ed2f1-106">PlaylistCollection.getByName method</span></span>

<span data-ttu-id="ed2f1-107">La méthode **GetByName** récupère un objet **PlaylistArray** contenant des sélections portant le nom spécifié, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="ed2f1-107">The **getByName** method retrieves a **PlaylistArray** object containing playlists with the specified name, if any exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed2f1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed2f1-108">Syntax</span></span>


```JScript
retVal = PlaylistCollection.getByName(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="ed2f1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed2f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed2f1-110">*nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ed2f1-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed2f1-111">**Chaîne** contenant le nom des sélections à récupérer.</span><span class="sxs-lookup"><span data-stu-id="ed2f1-111">**String** containing the name of the playlists to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed2f1-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ed2f1-112">Return value</span></span>

<span data-ttu-id="ed2f1-113">Cette méthode retourne un objet **PlaylistArray** .</span><span class="sxs-lookup"><span data-stu-id="ed2f1-113">This method returns a **PlaylistArray** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed2f1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ed2f1-114">Remarks</span></span>

<span data-ttu-id="ed2f1-115">Utilisez *PlaylistArray*. **Count** pour déterminer si une sélection existe.</span><span class="sxs-lookup"><span data-stu-id="ed2f1-115">Use *PlaylistArray*.**count** to determine whether a playlist exists.</span></span> <span data-ttu-id="ed2f1-116">Si **Count** est égal à zéro, aucune playlist n’existe.</span><span class="sxs-lookup"><span data-stu-id="ed2f1-116">If **count** is zero, a playlist does not exist.</span></span>

<span data-ttu-id="ed2f1-117">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="ed2f1-117">To use this method, read access to the library is required.</span></span> <span data-ttu-id="ed2f1-118">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ed2f1-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ed2f1-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="ed2f1-119">Examples</span></span>

<span data-ttu-id="ed2f1-120">L’exemple JScript suivant utilise *playlistCollection*. **GetByName** pour vérifier l’objet **playlistCollection** pour une sélection nommée « ThreeList ».</span><span class="sxs-lookup"><span data-stu-id="ed2f1-120">The following JScript example uses *playlistCollection*.**getByName** to check the **playlistCollection** object for a playlist named "ThreeList".</span></span> <span data-ttu-id="ed2f1-121">Si la sélection « Threelist » existe, **GetByName** définit « Threelist » comme sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="ed2f1-121">If the "Threelist" playlist exists, **getByName** sets "ThreeList" as the current playlist.</span></span> <span data-ttu-id="ed2f1-122">L’objet **Player** a été créé avec l’ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="ed2f1-122">The **Player** object was created with the ID = "Player".</span></span>


```JScript
//Retrieve the count of the playlists named "ThreeList".
var Checkit = Player.playlistCollection.getByName("ThreeList").count;

//Since duplicate playlist names are allowed, the count returned
//will be either zero (no playlist) or greater than zero 
//(playlist exists).
if (Checkit > 0){ 
    
   //Retrieve a playlistArray object containing "ThreeList". Assume that
   //there is only one playlist with that name, and assign it to the 
   //current playlist.
   Player.currentPlaylist = Player.playlistCollection.getByName("ThreeList").item(0);
}

```



## <a name="requirements"></a><span data-ttu-id="ed2f1-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed2f1-123">Requirements</span></span>



| <span data-ttu-id="ed2f1-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed2f1-124">Requirement</span></span> | <span data-ttu-id="ed2f1-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed2f1-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ed2f1-126">Version</span><span class="sxs-lookup"><span data-stu-id="ed2f1-126">Version</span></span><br/> | <span data-ttu-id="ed2f1-127">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ed2f1-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ed2f1-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ed2f1-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="ed2f1-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed2f1-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed2f1-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed2f1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed2f1-131">**Objet PlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="ed2f1-131">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="ed2f1-132">**PlaylistArray. Count**</span><span class="sxs-lookup"><span data-stu-id="ed2f1-132">**PlaylistArray.count**</span></span>](playlistarray-count.md)
</dt> <dt>

[<span data-ttu-id="ed2f1-133">**Objet PlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="ed2f1-133">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="ed2f1-134">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="ed2f1-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="ed2f1-135">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="ed2f1-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





