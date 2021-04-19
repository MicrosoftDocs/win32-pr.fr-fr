---
title: Player. openPlayer, méthode
description: La méthode openPlayer ouvre le lecteur Windows Media à l’aide de l’URL spécifiée. | Player. openPlayer, méthode
ms.assetid: 9ddd63c9-f4a0-490a-8543-51ad0fa74a26
keywords:
- méthode openPlayer lecteur Windows Media
- méthode openPlayer lecteur Windows Media, classe Player
- Classe player lecteur Windows Media, méthode openPlayer
topic_type:
- apiref
api_name:
- Player.openPlayer
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3378df48f961f1aa5e3fccec72e79b7f1c26ff08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532220"
---
# <a name="playeropenplayer-method"></a><span data-ttu-id="f1ac9-107">Player. openPlayer, méthode</span><span class="sxs-lookup"><span data-stu-id="f1ac9-107">Player.openPlayer method</span></span>

<span data-ttu-id="f1ac9-108">La méthode **openPlayer** ouvre le lecteur Windows Media à l’aide de l’URL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f1ac9-108">The **openPlayer** method opens Windows Media Player using the specified URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1ac9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1ac9-109">Syntax</span></span>


```JScript
Player.openPlayer(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="f1ac9-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1ac9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1ac9-111">*URL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f1ac9-111">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1ac9-112">**Chaîne** représentant l’URL de l’élément multimédia à lire.</span><span class="sxs-lookup"><span data-stu-id="f1ac9-112">**String** representing the URL of the media item to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1ac9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f1ac9-113">Return value</span></span>

<span data-ttu-id="f1ac9-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f1ac9-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1ac9-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f1ac9-115">Remarks</span></span>

<span data-ttu-id="f1ac9-116">Cette méthode lance le lecteur Windows Media avec l’URL spécifiée définie en tant qu’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="f1ac9-116">This method launches Windows Media Player with the specified URL set as the current media item.</span></span> <span data-ttu-id="f1ac9-117">Si le joueur a été précédemment fermé en mode apparence, il s’ouvre en utilisant la dernière apparence choisie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f1ac9-117">If the Player was previously closed in skin mode it will open using the skin last chosen by the user.</span></span> <span data-ttu-id="f1ac9-118">Dans le cas contraire, le joueur s’ouvre en mode complet.</span><span class="sxs-lookup"><span data-stu-id="f1ac9-118">Otherwise, the Player opens in full mode.</span></span>

<span data-ttu-id="f1ac9-119">Si cette méthode est appelée à partir d’un contrôle Windows Media PlayerActiveX incorporé en mode distant, son comportement est identique à celui de *PlayerApplication*. méthode **switchToPlayerApplication** .</span><span class="sxs-lookup"><span data-stu-id="f1ac9-119">If this method is called from a Windows Media PlayerActiveX control embedded in remote mode, its behavior is identical to the *PlayerApplication*.**switchToPlayerApplication** method.</span></span>

<span data-ttu-id="f1ac9-120">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f1ac9-120">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1ac9-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1ac9-121">Requirements</span></span>



| <span data-ttu-id="f1ac9-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1ac9-122">Requirement</span></span> | <span data-ttu-id="f1ac9-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1ac9-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f1ac9-124">Version</span><span class="sxs-lookup"><span data-stu-id="f1ac9-124">Version</span></span><br/> | <span data-ttu-id="f1ac9-125">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f1ac9-125">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="f1ac9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f1ac9-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="f1ac9-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1ac9-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1ac9-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1ac9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1ac9-129">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="f1ac9-129">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="f1ac9-130">**PlayerApplication.switchToPlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="f1ac9-130">**PlayerApplication.switchToPlayerApplication**</span></span>](playerapplication-switchtoplayerapplication.md)
</dt> </dl>

 

 





