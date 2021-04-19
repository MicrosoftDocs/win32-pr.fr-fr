---
title: Événement Player. CurrentPlaylistChange
description: L’événement CurrentPlaylistChange se produit en cas de modification de la sélection actuelle. | Événement Player. CurrentPlaylistChange
ms.assetid: 5270373e-e401-40c6-bf8c-ef0557610372
keywords:
- Événement CurrentPlaylistChange lecteur Windows Media
- Événement CurrentPlaylistChange lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement CurrentPlaylistChange
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4722db224285587198e3ddb021022ec5d8f2cea6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542511"
---
# <a name="playercurrentplaylistchange-event"></a><span data-ttu-id="ad8b9-107">Événement Player. CurrentPlaylistChange</span><span class="sxs-lookup"><span data-stu-id="ad8b9-107">Player.CurrentPlaylistChange event</span></span>

<span data-ttu-id="ad8b9-108">L’événement **CurrentPlaylistChange** se produit en cas de modification de la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="ad8b9-108">The **CurrentPlaylistChange** event occurs when something changes within the current playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad8b9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad8b9-109">Syntax</span></span>


```JScript
Player.CurrentPlaylistChange(
  change
)
```



## <a name="parameters"></a><span data-ttu-id="ad8b9-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad8b9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad8b9-111">*change*</span><span class="sxs-lookup"><span data-stu-id="ad8b9-111">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="ad8b9-112">**Nombre** (**long**) indiquant le type de modification qui s’est produite dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="ad8b9-112">**Number** (**long**) indicating what type of change occurred to the playlist.</span></span> <span data-ttu-id="ad8b9-113">Consultez le *lecteur*. Événement **PlaylistChange** pour une table de valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="ad8b9-113">See the *Player*.**PlaylistChange** event for a table of possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad8b9-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ad8b9-114">Return value</span></span>

<span data-ttu-id="ad8b9-115">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ad8b9-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad8b9-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ad8b9-116">Remarks</span></span>

<span data-ttu-id="ad8b9-117">Cet événement ne se produit pas lorsqu’une sélection différente devient la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="ad8b9-117">This event does not occur when a different playlist becomes the current playlist.</span></span> <span data-ttu-id="ad8b9-118">Il se produit uniquement lorsqu’une modification se produit dans la sélection actuelle, par exemple un élément multimédia ajouté à la sélection.</span><span class="sxs-lookup"><span data-stu-id="ad8b9-118">It only occurs when a change happens within the current playlist, such as a media item being appended to the playlist.</span></span>

<span data-ttu-id="ad8b9-119">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="ad8b9-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="ad8b9-120">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="ad8b9-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="examples"></a><span data-ttu-id="ad8b9-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="ad8b9-121">Examples</span></span>

<span data-ttu-id="ad8b9-122">L’exemple JScript suivant met à jour le texte d’un élément DIV HTML, nommé PlItems, pour afficher les noms des éléments multimédias dans la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="ad8b9-122">The following JScript example updates the text in an HTML DIV element, named PlItems, to display the names of the media items in the current playlist.</span></span> <span data-ttu-id="ad8b9-123">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="ad8b9-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for current playlist change. -->
<SCRIPT FOR = "Player" EVENT = "currentPlaylistChange(change)">
   switch (change){
      // Only update for move, delete, insert, and append events.
      case 3, 4, 5, 6:

         // Clear the contents of the DIV.
         PlItems.innerHTML = "";

         // Loop through the playlist and display each item name.
         for (var i = 0; i < Player.currentPlaylist.count; i++){
            PlItems.innerHTML += Player.currentPlaylist.item(i).name;
            PlItems.innerHTML += "<br>";
         }
         break;
      
      default:
   } 
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="ad8b9-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad8b9-124">Requirements</span></span>



| <span data-ttu-id="ad8b9-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad8b9-125">Requirement</span></span> | <span data-ttu-id="ad8b9-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad8b9-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad8b9-127">Version</span><span class="sxs-lookup"><span data-stu-id="ad8b9-127">Version</span></span><br/> | <span data-ttu-id="ad8b9-128">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ad8b9-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ad8b9-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ad8b9-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="ad8b9-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad8b9-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad8b9-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad8b9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad8b9-132">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="ad8b9-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="ad8b9-133">**Player. currentPlaylist**</span><span class="sxs-lookup"><span data-stu-id="ad8b9-133">**Player.currentPlaylist**</span></span>](player-currentplaylist.md)
</dt> <dt>

[<span data-ttu-id="ad8b9-134">**Player. PlaylistChange**</span><span class="sxs-lookup"><span data-stu-id="ad8b9-134">**Player.PlaylistChange**</span></span>](player-player-playlistchange.md)
</dt> </dl>

 

 





