---
title: Événement Player. OpenPlaylistSwitch
description: L’événement OpenPlaylistSwitch se produit lorsqu’un titre sur un DVD commence à être lu. | Événement Player. OpenPlaylistSwitch
ms.assetid: 97d69716-602f-4522-b743-83f2dbc852a2
keywords:
- Événement OpenPlaylistSwitch lecteur Windows Media
- Événement OpenPlaylistSwitch lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement OpenPlaylistSwitch
topic_type:
- apiref
api_name:
- Player.OpenPlaylistSwitch
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d35d4568356365cc9276c13ea33f866e937da1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520851"
---
# <a name="playeropenplaylistswitch-event"></a><span data-ttu-id="1a4ae-107">Événement Player. OpenPlaylistSwitch</span><span class="sxs-lookup"><span data-stu-id="1a4ae-107">Player.OpenPlaylistSwitch event</span></span>

<span data-ttu-id="1a4ae-108">L’événement **OpenPlaylistSwitch** se produit lorsqu’un titre sur un DVD commence à être lu.</span><span class="sxs-lookup"><span data-stu-id="1a4ae-108">The **OpenPlaylistSwitch** event occurs when a title on a DVD begins playing.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a4ae-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a4ae-109">Syntax</span></span>


```JScript
Player.OpenPlaylistSwitch(
  pItem
)
```



## <a name="parameters"></a><span data-ttu-id="1a4ae-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a4ae-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a4ae-111">*pItem*</span><span class="sxs-lookup"><span data-stu-id="1a4ae-111">*pItem*</span></span> 
</dt> <dd>

<span data-ttu-id="1a4ae-112">Objet **playlist** représentant le titre.</span><span class="sxs-lookup"><span data-stu-id="1a4ae-112">**Playlist** object representing the title.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a4ae-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a4ae-113">Return value</span></span>

<span data-ttu-id="1a4ae-114">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1a4ae-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a4ae-115">Notes</span><span class="sxs-lookup"><span data-stu-id="1a4ae-115">Remarks</span></span>

<span data-ttu-id="1a4ae-116">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="1a4ae-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="1a4ae-117">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="1a4ae-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a4ae-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a4ae-118">Requirements</span></span>



| <span data-ttu-id="1a4ae-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a4ae-119">Requirement</span></span> | <span data-ttu-id="1a4ae-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a4ae-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1a4ae-121">Version</span><span class="sxs-lookup"><span data-stu-id="1a4ae-121">Version</span></span><br/> | <span data-ttu-id="1a4ae-122">Lecteur Windows Media pour Windows XP ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1a4ae-122">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="1a4ae-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1a4ae-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="1a4ae-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a4ae-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a4ae-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a4ae-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a4ae-126">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="1a4ae-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





