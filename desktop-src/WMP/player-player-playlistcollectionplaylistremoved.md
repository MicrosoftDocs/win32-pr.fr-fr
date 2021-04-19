---
title: Événement Player. PlaylistCollectionPlaylistRemoved
description: L’événement PlaylistCollectionPlaylistRemoved se produit lorsqu’une sélection est supprimée de la collection de sélections. | Événement Player. PlaylistCollectionPlaylistRemoved
ms.assetid: 2405be98-b4c2-4b4e-bea6-0c48a3e26f18
keywords:
- Événement PlaylistCollectionPlaylistRemoved lecteur Windows Media
- Événement PlaylistCollectionPlaylistRemoved lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement PlaylistCollectionPlaylistRemoved
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a449a7b00516f4fee613722d1cc126eb74227948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538010"
---
# <a name="playerplaylistcollectionplaylistremoved-event"></a><span data-ttu-id="a4f1d-107">Événement Player. PlaylistCollectionPlaylistRemoved</span><span class="sxs-lookup"><span data-stu-id="a4f1d-107">Player.PlaylistCollectionPlaylistRemoved event</span></span>

<span data-ttu-id="a4f1d-108">L’événement **PlaylistCollectionPlaylistRemoved** se produit lorsqu’une sélection est supprimée de la collection de sélections.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-108">The **PlaylistCollectionPlaylistRemoved** event occurs when a playlist is removed from the playlist collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4f1d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4f1d-109">Syntax</span></span>


```JScript
Player.PlaylistCollectionPlaylistRemoved(
  bstrPlaylistName
)
```



## <a name="parameters"></a><span data-ttu-id="a4f1d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4f1d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4f1d-111">*bstrPlaylistName*</span><span class="sxs-lookup"><span data-stu-id="a4f1d-111">*bstrPlaylistName*</span></span> 
</dt> <dd>

<span data-ttu-id="a4f1d-112">**Chaîne** spécifiant le nom de la sélection qui a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-112">**String** specifying the name of the playlist that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4f1d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a4f1d-113">Return value</span></span>

<span data-ttu-id="a4f1d-114">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4f1d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a4f1d-115">Remarks</span></span>

<span data-ttu-id="a4f1d-116">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="a4f1d-117">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="a4f1d-118">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-118">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4f1d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4f1d-119">Requirements</span></span>



| <span data-ttu-id="a4f1d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4f1d-120">Requirement</span></span> | <span data-ttu-id="a4f1d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4f1d-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f1d-122">Version</span><span class="sxs-lookup"><span data-stu-id="a4f1d-122">Version</span></span><br/> | <span data-ttu-id="a4f1d-123">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a4f1d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a4f1d-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="a4f1d-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4f1d-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4f1d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4f1d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4f1d-127">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="a4f1d-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="a4f1d-128">**PlaylistCollection.getByName**</span><span class="sxs-lookup"><span data-stu-id="a4f1d-128">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





