---
title: Playlist. removeItem, méthode
description: La méthode removeItem supprime l’élément spécifié de la sélection.
ms.assetid: 294ba4fb-967b-4a03-b0c5-6e9c15db3bff
keywords:
- méthode removeItem lecteur Windows Media
- méthode removeItem lecteur Windows Media, classe playlist
- Classe de sélection lecteur Windows Media, removeItem, méthode
topic_type:
- apiref
api_name:
- Playlist.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de03333e2373744f9e9197be8ed8582997c557d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525454"
---
# <a name="playlistremoveitem-method"></a><span data-ttu-id="c54ea-106">Playlist. removeItem, méthode</span><span class="sxs-lookup"><span data-stu-id="c54ea-106">Playlist.removeItem method</span></span>

<span data-ttu-id="c54ea-107">La méthode **RemoveItem** supprime l’élément spécifié de la sélection.</span><span class="sxs-lookup"><span data-stu-id="c54ea-107">The **removeItem** method removes the specified item from the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="c54ea-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c54ea-108">Syntax</span></span>


```JScript
Playlist.removeItem(
  item
)
```



## <a name="parameters"></a><span data-ttu-id="c54ea-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c54ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c54ea-110">*élément* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c54ea-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c54ea-111">Objet **multimédia** à supprimer.</span><span class="sxs-lookup"><span data-stu-id="c54ea-111">**Media** object to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c54ea-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c54ea-112">Return value</span></span>

<span data-ttu-id="c54ea-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c54ea-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c54ea-114">Notes</span><span class="sxs-lookup"><span data-stu-id="c54ea-114">Remarks</span></span>

<span data-ttu-id="c54ea-115">Si l’élément supprimé est la piste en cours de lecture (*Player*.**currentMedia**), la lecture s’arrête et l’élément suivant dans la sélection devient l’élément actuel.</span><span class="sxs-lookup"><span data-stu-id="c54ea-115">If the item removed is the currently playing track (*Player*.**currentMedia**), playback stops and the next item in the playlist becomes the current one.</span></span> <span data-ttu-id="c54ea-116">S’il n’y a pas d’élément suivant, l’élément précédent est utilisé, ou s’il n’y a pas d’autres éléments, alors *Player*. **currentMedia** a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="c54ea-116">If there is no next item, the previous item is used, or if there are no other items, then *Player*.**currentMedia** is set to **NULL**.</span></span>

<span data-ttu-id="c54ea-117">Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="c54ea-117">To use this method, full access to the library is required.</span></span> <span data-ttu-id="c54ea-118">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c54ea-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c54ea-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c54ea-119">Requirements</span></span>



| <span data-ttu-id="c54ea-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c54ea-120">Requirement</span></span> | <span data-ttu-id="c54ea-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c54ea-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c54ea-122">Version</span><span class="sxs-lookup"><span data-stu-id="c54ea-122">Version</span></span><br/> | <span data-ttu-id="c54ea-123">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c54ea-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c54ea-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c54ea-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="c54ea-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c54ea-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c54ea-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c54ea-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c54ea-127">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="c54ea-127">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="c54ea-128">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="c54ea-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="c54ea-129">**Playlist. insertItem**</span><span class="sxs-lookup"><span data-stu-id="c54ea-129">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="c54ea-130">**Playlist. Item**</span><span class="sxs-lookup"><span data-stu-id="c54ea-130">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="c54ea-131">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="c54ea-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="c54ea-132">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="c54ea-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





