---
title: Méthode playlist. Item
description: La méthode Item récupère l’élément multimédia au niveau de l’index spécifié.
ms.assetid: a564f6db-ede4-4c85-87ca-0e2539d914c2
keywords:
- méthode Item lecteur Windows Media
- méthode Item lecteur Windows Media, classe playlist
- Classe de sélection lecteur Windows Media, méthode d’élément
topic_type:
- apiref
api_name:
- Playlist.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c69386871aeec33dbc36a066ce3f75e80d7514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534872"
---
# <a name="playlistitem-method"></a><span data-ttu-id="5d411-106">Méthode playlist. Item</span><span class="sxs-lookup"><span data-stu-id="5d411-106">Playlist.item method</span></span>

<span data-ttu-id="5d411-107">La méthode **Item** récupère l’élément multimédia au niveau de l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="5d411-107">The **item** method retrieves the media item at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d411-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d411-108">Syntax</span></span>


```JScript
retVal = Playlist.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="5d411-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d411-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d411-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5d411-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d411-111">**Nombre** (**long**) contenant l’index de l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="5d411-111">**Number** (**long**) containing the index of the item to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d411-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d411-112">Return value</span></span>

<span data-ttu-id="5d411-113">Cette méthode retourne un objet **multimédia** .</span><span class="sxs-lookup"><span data-stu-id="5d411-113">This method returns a **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d411-114">Notes</span><span class="sxs-lookup"><span data-stu-id="5d411-114">Remarks</span></span>

<span data-ttu-id="5d411-115">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="5d411-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="5d411-116">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5d411-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5d411-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="5d411-117">Examples</span></span>

<span data-ttu-id="5d411-118">L’exemple JScript suivant utilise la *sélection*. **élément** permettant de récupérer un élément multimédia à partir de la sélection actuelle en fonction d’une sélection de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5d411-118">The following JScript example uses *Playlist*.**item** to retrieve a media item from the current playlist based on a user selection.</span></span> <span data-ttu-id="5d411-119">Un élément SELECT HTML a été créé avec le nom « weblist » et rempli avec les titres de la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="5d411-119">An HTML SELECT element was created with name "weblist", and filled with the titles from the current playlist.</span></span> <span data-ttu-id="5d411-120">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="5d411-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the value of the selected item in the list box
// using the selectedIndex property.
var index = weblist.selectedIndex;

// Store the corresponding digital media object from the current playlist.
var listItem = Player.currentPlaylist.item(index);

// Set the URL using the listItem variable.
Player.URL = listItem.sourceURL;

```



## <a name="requirements"></a><span data-ttu-id="5d411-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d411-121">Requirements</span></span>



| <span data-ttu-id="5d411-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d411-122">Requirement</span></span> | <span data-ttu-id="5d411-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d411-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5d411-124">Version</span><span class="sxs-lookup"><span data-stu-id="5d411-124">Version</span></span><br/> | <span data-ttu-id="5d411-125">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5d411-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5d411-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5d411-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="5d411-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d411-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d411-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d411-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d411-129">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="5d411-129">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="5d411-130">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="5d411-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="5d411-131">**Playlist. insertItem**</span><span class="sxs-lookup"><span data-stu-id="5d411-131">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="5d411-132">**Playlist. removeItem**</span><span class="sxs-lookup"><span data-stu-id="5d411-132">**Playlist.removeItem**</span></span>](playlist-removeitem.md)
</dt> <dt>

[<span data-ttu-id="5d411-133">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5d411-133">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="5d411-134">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5d411-134">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





