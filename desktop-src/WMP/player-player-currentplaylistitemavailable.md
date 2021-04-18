---
title: Événement Player. CurrentPlaylistItemAvailable
description: L’événement CurrentPlaylistItemAvailable se produit lorsque la sélection actuelle est disponible. | Événement Player. CurrentPlaylistItemAvailable
ms.assetid: 4894e2fc-3464-413f-8abf-8b5e91899946
keywords:
- Événement CurrentPlaylistItemAvailable lecteur Windows Media
- Événement CurrentPlaylistItemAvailable lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement CurrentPlaylistItemAvailable
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe5809e50d572cfb8eb7a36220d083ec18a0a76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540500"
---
# <a name="playercurrentplaylistitemavailable-event"></a><span data-ttu-id="8c4c7-107">Événement Player. CurrentPlaylistItemAvailable</span><span class="sxs-lookup"><span data-stu-id="8c4c7-107">Player.CurrentPlaylistItemAvailable event</span></span>

<span data-ttu-id="8c4c7-108">L’événement **CurrentPlaylistItemAvailable** se produit lorsque la sélection actuelle est disponible.</span><span class="sxs-lookup"><span data-stu-id="8c4c7-108">The **CurrentPlaylistItemAvailable** event occurs when the current playlist becomes available.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c4c7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c4c7-109">Syntax</span></span>


```JScript
Player.CurrentPlaylistItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a><span data-ttu-id="8c4c7-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c4c7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c4c7-111">*bstrItemName*</span><span class="sxs-lookup"><span data-stu-id="8c4c7-111">*bstrItemName*</span></span> 
</dt> <dd>

<span data-ttu-id="8c4c7-112">**Chaîne** contenant le nom de l’élément de sélection actuel.</span><span class="sxs-lookup"><span data-stu-id="8c4c7-112">**String** containing the name of the current playlist item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c4c7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c4c7-113">Return value</span></span>

<span data-ttu-id="8c4c7-114">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8c4c7-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c4c7-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8c4c7-115">Remarks</span></span>

<span data-ttu-id="8c4c7-116">Le nom de la sélection actuelle peut être utilisé pour récupérer l’objet de **sélection** correspondant à l’aide de *PlaylistCollection*. méthode **GetByName** .</span><span class="sxs-lookup"><span data-stu-id="8c4c7-116">The name of the current playlist can be used to retrieve the corresponding **Playlist** object using the *PlaylistCollection*.**getByName** method.</span></span>

<span data-ttu-id="8c4c7-117">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="8c4c7-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="8c4c7-118">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="8c4c7-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="8c4c7-119">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8c4c7-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c4c7-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c4c7-120">Requirements</span></span>



| <span data-ttu-id="8c4c7-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c4c7-121">Requirement</span></span> | <span data-ttu-id="8c4c7-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c4c7-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8c4c7-123">Version</span><span class="sxs-lookup"><span data-stu-id="8c4c7-123">Version</span></span><br/> | <span data-ttu-id="8c4c7-124">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8c4c7-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="8c4c7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8c4c7-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="8c4c7-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c4c7-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c4c7-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c4c7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c4c7-128">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="8c4c7-128">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="8c4c7-129">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="8c4c7-129">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="8c4c7-130">**PlaylistCollection.getByName**</span><span class="sxs-lookup"><span data-stu-id="8c4c7-130">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





