---
title: Playlist. insertItem, méthode
description: La méthode insertItem insère un élément multimédia dans la sélection à l’emplacement spécifié.
ms.assetid: c186abc4-0a15-49d2-bbc4-5660e8cc0a4b
keywords:
- méthode insertItem Windows Media Player
- méthode insertItem lecteur Windows Media, classe playlist
- Classe de sélection lecteur Windows Media, méthode insertItem
topic_type:
- apiref
api_name:
- Playlist.insertItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a456b7a359d59958ce7693cc48c16eabba435621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539191"
---
# <a name="playlistinsertitem-method"></a><span data-ttu-id="39f1e-106">Playlist. insertItem, méthode</span><span class="sxs-lookup"><span data-stu-id="39f1e-106">Playlist.insertItem method</span></span>

<span data-ttu-id="39f1e-107">La méthode **InsertItem** insère un élément multimédia dans la sélection à l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="39f1e-107">The **insertItem** method inserts a media item into the playlist at the specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="39f1e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39f1e-108">Syntax</span></span>


```JScript
Playlist.insertItem(
  index,
  item
)
```



## <a name="parameters"></a><span data-ttu-id="39f1e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39f1e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39f1e-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="39f1e-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39f1e-111">**Nombre** (**long**) contenant l’index auquel ajouter l’élément.</span><span class="sxs-lookup"><span data-stu-id="39f1e-111">**Number** (**long**) containing the index at which to add the item.</span></span>

</dd> <dt>

<span data-ttu-id="39f1e-112">*élément* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="39f1e-112">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39f1e-113">Objet **multimédia** à insérer.</span><span class="sxs-lookup"><span data-stu-id="39f1e-113">**Media** object to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39f1e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="39f1e-114">Return value</span></span>

<span data-ttu-id="39f1e-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="39f1e-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="39f1e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="39f1e-116">Remarks</span></span>

<span data-ttu-id="39f1e-117">Tous les éléments après l’élément inséré auront leurs numéros d’index augmentés d’une unité.</span><span class="sxs-lookup"><span data-stu-id="39f1e-117">All items after the inserted item will have their index numbers increased by one.</span></span>

<span data-ttu-id="39f1e-118">Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="39f1e-118">To use this method, full access to the library is required.</span></span> <span data-ttu-id="39f1e-119">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="39f1e-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="39f1e-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39f1e-120">Requirements</span></span>



| <span data-ttu-id="39f1e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39f1e-121">Requirement</span></span> | <span data-ttu-id="39f1e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="39f1e-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39f1e-123">Version</span><span class="sxs-lookup"><span data-stu-id="39f1e-123">Version</span></span><br/> | <span data-ttu-id="39f1e-124">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="39f1e-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="39f1e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="39f1e-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="39f1e-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39f1e-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39f1e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39f1e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39f1e-128">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="39f1e-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="39f1e-129">**Playlist. Item**</span><span class="sxs-lookup"><span data-stu-id="39f1e-129">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="39f1e-130">**Playlist. removeItem**</span><span class="sxs-lookup"><span data-stu-id="39f1e-130">**Playlist.removeItem**</span></span>](playlist-removeitem.md)
</dt> <dt>

[<span data-ttu-id="39f1e-131">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="39f1e-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="39f1e-132">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="39f1e-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





