---
title: Méthode playlist. appendItem
description: La méthode appendItem ajoute un élément multimédia à la fin de la sélection.
ms.assetid: cc956491-7936-49e7-90ca-1f71e03448cd
keywords:
- méthode appendItem lecteur Windows Media
- méthode appendItem lecteur Windows Media, classe de sélection
- Classe de sélection lecteur Windows Media, méthode appendItem
topic_type:
- apiref
api_name:
- Playlist.appendItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 828799d5b6e71e7ff0e7be4c1e55714f6343be51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540418"
---
# <a name="playlistappenditem-method"></a><span data-ttu-id="07e90-106">Méthode playlist. appendItem</span><span class="sxs-lookup"><span data-stu-id="07e90-106">Playlist.appendItem method</span></span>

<span data-ttu-id="07e90-107">La méthode **appendItem** ajoute un élément multimédia à la fin de la sélection.</span><span class="sxs-lookup"><span data-stu-id="07e90-107">The **appendItem** method adds a media item to the end of the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="07e90-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07e90-108">Syntax</span></span>


```JScript
Playlist.appendItem(
  item
)
```



## <a name="parameters"></a><span data-ttu-id="07e90-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07e90-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07e90-110">*élément* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="07e90-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07e90-111">Objet **multimédia** à ajouter.</span><span class="sxs-lookup"><span data-stu-id="07e90-111">**Media** object to be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07e90-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="07e90-112">Return value</span></span>

<span data-ttu-id="07e90-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="07e90-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="07e90-114">Notes</span><span class="sxs-lookup"><span data-stu-id="07e90-114">Remarks</span></span>

<span data-ttu-id="07e90-115">Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="07e90-115">To use this method, full access to the library is required.</span></span> <span data-ttu-id="07e90-116">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="07e90-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="07e90-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="07e90-117">Examples</span></span>

<span data-ttu-id="07e90-118">L’exemple JScript suivant utilise la *sélection*. **appendItem** pour ajouter l’élément multimédia actuel à la sélection nommée « ThreeList ».</span><span class="sxs-lookup"><span data-stu-id="07e90-118">The following JScript example uses *Playlist*.**appendItem** to add the current media item to the playlist named "ThreeList".</span></span> <span data-ttu-id="07e90-119">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="07e90-119">The **Player** object was created with ID="Player".</span></span>


```JScript
// Get the current media item.
var currMedia = Player.currentMedia;

// Get the playlist object by name.
var plThreeList = Player.playlistCollection.getByName("ThreeList").item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);

```



## <a name="requirements"></a><span data-ttu-id="07e90-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07e90-120">Requirements</span></span>



| <span data-ttu-id="07e90-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07e90-121">Requirement</span></span> | <span data-ttu-id="07e90-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="07e90-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="07e90-123">Version</span><span class="sxs-lookup"><span data-stu-id="07e90-123">Version</span></span><br/> | <span data-ttu-id="07e90-124">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="07e90-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="07e90-125">DLL</span><span class="sxs-lookup"><span data-stu-id="07e90-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="07e90-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07e90-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07e90-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07e90-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07e90-128">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="07e90-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="07e90-129">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="07e90-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="07e90-130">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="07e90-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





