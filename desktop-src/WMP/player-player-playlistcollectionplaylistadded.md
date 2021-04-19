---
title: Événement Player. PlaylistCollectionPlaylistAdded
description: L’événement PlaylistCollectionPlaylistAdded se produit lorsqu’une sélection est ajoutée à la collection de sélections. | Événement Player. PlaylistCollectionPlaylistAdded
ms.assetid: 07acb5e6-d832-4f0b-a6bb-2b7ba27c368d
keywords:
- Événement PlaylistCollectionPlaylistAdded lecteur Windows Media
- Événement PlaylistCollectionPlaylistAdded lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement PlaylistCollectionPlaylistAdded
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e6a229aff95d29ae93433dab538521d88c50c1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541289"
---
# <a name="playerplaylistcollectionplaylistadded-event"></a><span data-ttu-id="bf0db-107">Événement Player. PlaylistCollectionPlaylistAdded</span><span class="sxs-lookup"><span data-stu-id="bf0db-107">Player.PlaylistCollectionPlaylistAdded event</span></span>

<span data-ttu-id="bf0db-108">L’événement **PlaylistCollectionPlaylistAdded** se produit lorsqu’une sélection est ajoutée à la collection de sélections.</span><span class="sxs-lookup"><span data-stu-id="bf0db-108">The **PlaylistCollectionPlaylistAdded** event occurs when a playlist is added to the playlist collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf0db-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf0db-109">Syntax</span></span>


```JScript
Player.PlaylistCollectionPlaylistAdded(
  bstrPlaylistName
)
```



## <a name="parameters"></a><span data-ttu-id="bf0db-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf0db-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf0db-111">*bstrPlaylistName*</span><span class="sxs-lookup"><span data-stu-id="bf0db-111">*bstrPlaylistName*</span></span> 
</dt> <dd>

<span data-ttu-id="bf0db-112">**Chaîne** spécifiant le nom de la sélection ajoutée.</span><span class="sxs-lookup"><span data-stu-id="bf0db-112">**String** specifying the name of the playlist that was added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf0db-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bf0db-113">Return value</span></span>

<span data-ttu-id="bf0db-114">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="bf0db-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf0db-115">Notes</span><span class="sxs-lookup"><span data-stu-id="bf0db-115">Remarks</span></span>

<span data-ttu-id="bf0db-116">Le nom de la sélection ajoutée peut être utilisé pour récupérer l’objet de **sélection** correspondant à l’aide de *PlaylistCollection*. méthode **GetByName** .</span><span class="sxs-lookup"><span data-stu-id="bf0db-116">The name of the playlist that was added can be used to retrieve the corresponding **Playlist** object using the *PlaylistCollection*.**getByName** method.</span></span>

<span data-ttu-id="bf0db-117">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="bf0db-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="bf0db-118">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="bf0db-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="bf0db-119">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="bf0db-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf0db-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf0db-120">Requirements</span></span>



| <span data-ttu-id="bf0db-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf0db-121">Requirement</span></span> | <span data-ttu-id="bf0db-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf0db-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bf0db-123">Version</span><span class="sxs-lookup"><span data-stu-id="bf0db-123">Version</span></span><br/> | <span data-ttu-id="bf0db-124">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bf0db-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="bf0db-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bf0db-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="bf0db-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf0db-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf0db-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf0db-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf0db-128">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="bf0db-128">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="bf0db-129">**PlaylistCollection.getByName**</span><span class="sxs-lookup"><span data-stu-id="bf0db-129">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





