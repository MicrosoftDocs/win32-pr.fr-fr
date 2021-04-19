---
title: Controls. currentItem
description: La propriété currentItem spécifie ou récupère l’élément multimédia actuel.
ms.assetid: 77e21585-3cc8-41f5-97b5-da6eb992c7bc
keywords:
- Controls. currentItem, lecteur Windows Media
topic_type:
- apiref
api_name:
- Controls.currentItem
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81658665cb6f31acd327f5050a733a2fc3c70371
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521621"
---
# <a name="controlscurrentitem"></a><span data-ttu-id="6247e-104">Controls. currentItem</span><span class="sxs-lookup"><span data-stu-id="6247e-104">Controls.currentItem</span></span>

<span data-ttu-id="6247e-105">La propriété **CurrentItem** spécifie ou récupère l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="6247e-105">The **currentItem** property specifies or retrieves the current media item.</span></span>

``` syntax
player.controls.currentItem
      
```

## <a name="possible-values"></a><span data-ttu-id="6247e-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="6247e-106">Possible Values</span></span>

<span data-ttu-id="6247e-107">Cette propriété est un objet **multimédia** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6247e-107">This property is a read/write **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6247e-108">Notes</span><span class="sxs-lookup"><span data-stu-id="6247e-108">Remarks</span></span>

<span data-ttu-id="6247e-109">Cette méthode fonctionne uniquement avec les éléments dans *Player*. **currentPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="6247e-109">This method works only with items in *Player*.**currentPlaylist**.</span></span> <span data-ttu-id="6247e-110">L’appel de **CurrentItem** avec une référence à un élément multimédia enregistré n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6247e-110">Calling **currentItem** with a reference to a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="6247e-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="6247e-111">Examples</span></span>

<span data-ttu-id="6247e-112">L’exemple JScript suivant utilise **CurrentItem** pour affecter à l’élément multimédia actuel du contrôle du lecteur la valeur sélectionnée dans un élément Select HTML.</span><span class="sxs-lookup"><span data-stu-id="6247e-112">The following JScript example uses **currentItem** to set the player control current media item to the selected value in an HTML SELECT element.</span></span> <span data-ttu-id="6247e-113">La sélection actuelle a été spécifiée pour la première fois à l’aide de *PlaylistCollection*. **GetByName**.</span><span class="sxs-lookup"><span data-stu-id="6247e-113">The current playlist was first specified by using *PlaylistCollection*.**getByName**.</span></span> <span data-ttu-id="6247e-114">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="6247e-114">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SELECT ID = playItem  NAME = "playItem"  LANGUAGE = "JScript"

    /* Specify the current item when the selected list value changes. */
    onChange = "Player.controls.currentItem = Player.currentPlaylist.item(playItem.value);">

    /* Fill the SELECT element list with three items that match
       the songs in the playlist. */
    <OPTION VALUE = 0 >Laure
    <OPTION VALUE = 1 >Jeanne
    <OPTION VALUE = 2 >House
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="6247e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6247e-115">Requirements</span></span>



| <span data-ttu-id="6247e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6247e-116">Requirement</span></span> | <span data-ttu-id="6247e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6247e-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6247e-118">Version</span><span class="sxs-lookup"><span data-stu-id="6247e-118">Version</span></span><br/> | <span data-ttu-id="6247e-119">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="6247e-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6247e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="6247e-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="6247e-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6247e-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6247e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6247e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6247e-123">**Controls (objet)**</span><span class="sxs-lookup"><span data-stu-id="6247e-123">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="6247e-124">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="6247e-124">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="6247e-125">**PlaylistCollection.getByName**</span><span class="sxs-lookup"><span data-stu-id="6247e-125">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





