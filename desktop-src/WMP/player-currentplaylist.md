---
title: Player. currentPlaylist
description: La propriété currentPlaylist spécifie ou récupère l’objet de sélection actuel.
ms.assetid: fabfb927-5f64-4fc4-8ee5-e2449082dfbc
keywords:
- Lecteur Windows Media Player. currentPlaylist
topic_type:
- apiref
api_name:
- Player.currentPlaylist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceae33a201086d268942e47496874678ec13f459
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526811"
---
# <a name="playercurrentplaylist"></a><span data-ttu-id="857e3-104">Player. currentPlaylist</span><span class="sxs-lookup"><span data-stu-id="857e3-104">Player.currentPlaylist</span></span>

<span data-ttu-id="857e3-105">La propriété currentPlaylist spécifie ou récupère l’objet de **sélection** actuel.</span><span class="sxs-lookup"><span data-stu-id="857e3-105">The currentPlaylist property specifies or retrieves the current **Playlist** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="857e3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="857e3-106">Syntax</span></span>

<span data-ttu-id="857e3-107">*lecteur* . **currentPlaylist**</span><span class="sxs-lookup"><span data-stu-id="857e3-107">*player* .**currentPlaylist**</span></span>

## <a name="possible-values"></a><span data-ttu-id="857e3-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="857e3-108">Possible Values</span></span>

<span data-ttu-id="857e3-109">Cette propriété est un objet de **sélection** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="857e3-109">This property is a read/write **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="857e3-110">Notes</span><span class="sxs-lookup"><span data-stu-id="857e3-110">Remarks</span></span>

<span data-ttu-id="857e3-111">Si les *paramètres*. la propriété **AutoStart** a la valeur true, la lecture commence automatiquement chaque fois que vous définissez **currentPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="857e3-111">If the *Settings*.**autoStart** property is true, playback begins automatically whenever you set **currentPlaylist**.</span></span>

<span data-ttu-id="857e3-112">Cette propriété prend un objet playlist, qui peut être acquis de plusieurs façons, par exemple en appelant *PlaylistArray*. **Item** ou *PlaylistCollection*. **newPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="857e3-112">This property takes a Playlist object, which can be acquired in several ways, such as by calling *PlaylistArray*.**item** or *PlaylistCollection*.**newPlaylist**.</span></span> <span data-ttu-id="857e3-113">Pour charger un élément de **sélection** à l’aide d’un nom de fichier, définissez la propriété URL ou utilisez *Player*. **newPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="857e3-113">To load a **Playlist** item using a file name, set the URL property or use *Player*.**newPlaylist**.</span></span>

## <a name="examples"></a><span data-ttu-id="857e3-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="857e3-114">Examples</span></span>

<span data-ttu-id="857e3-115">L’exemple JScript suivant récupère la première sélection de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="857e3-115">The following JScript example retrieves the first playlist in the library.</span></span> <span data-ttu-id="857e3-116">Il utilise ensuite **currentPlaylist** pour faire de la sélection Récupérée la sélection actuelle, puis pour afficher le nom de la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="857e3-116">It then uses **currentPlaylist** to make the retrieved playlist the current playlist, and then to display the name of the current playlist.</span></span> <span data-ttu-id="857e3-117">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="857e3-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve the first playlist from the library.
var firstPL = Player.playlistCollection.getAll().item(0);

// Make the retrieved playlist the current playlist.
Player.currentPlaylist = firstPL;

// Display the name of the current playlist.
document.write("Found first playlist. Name: " + Player.currentPlaylist.name);
```



## <a name="requirements"></a><span data-ttu-id="857e3-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="857e3-118">Requirements</span></span>



| <span data-ttu-id="857e3-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="857e3-119">Requirement</span></span> | <span data-ttu-id="857e3-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="857e3-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="857e3-121">Version</span><span class="sxs-lookup"><span data-stu-id="857e3-121">Version</span></span><br/> | <span data-ttu-id="857e3-122">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="857e3-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="857e3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="857e3-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="857e3-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="857e3-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="857e3-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="857e3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="857e3-126">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="857e3-126">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="857e3-127">**Player. newPlaylist**</span><span class="sxs-lookup"><span data-stu-id="857e3-127">**Player.newPlaylist**</span></span>](player-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="857e3-128">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="857e3-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="857e3-129">**PlaylistArray. Item**</span><span class="sxs-lookup"><span data-stu-id="857e3-129">**PlaylistArray.item**</span></span>](playlistarray-item.md)
</dt> <dt>

[<span data-ttu-id="857e3-130">**PlaylistCollection. newPlaylist**</span><span class="sxs-lookup"><span data-stu-id="857e3-130">**PlaylistCollection.newPlaylist**</span></span>](playlistcollection-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="857e3-131">**Paramètres. démarrage automatique**</span><span class="sxs-lookup"><span data-stu-id="857e3-131">**Settings.autoStart**</span></span>](settings-autostart.md)
</dt> </dl>

 

 





