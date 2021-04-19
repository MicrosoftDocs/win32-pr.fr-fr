---
title: Méthode IWMPPlaylistCollection newPlaylist
description: La méthode newPlaylist retourne une interface IWMPPlaylist pour une nouvelle playlist vide dans la bibliothèque.
ms.assetid: cc0cb356-9a90-421c-8d1a-b79585f71124
keywords:
- méthode newPlaylist lecteur Windows Media
- méthode newPlaylist lecteur Windows Media, interface IWMPPlaylistCollection
- Interface IWMPPlaylistCollection lecteur Windows Media, méthode newPlaylist
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.newPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbc455c5815cee1aaac139886bca1d847ddc62b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523481"
---
# <a name="iwmpplaylistcollectionnewplaylist-method"></a><span data-ttu-id="4223a-106">IWMPPlaylistCollection :: newPlaylist, méthode</span><span class="sxs-lookup"><span data-stu-id="4223a-106">IWMPPlaylistCollection::newPlaylist method</span></span>

<span data-ttu-id="4223a-107">La méthode **newPlaylist** retourne une interface **IWMPPlaylist** pour une nouvelle playlist vide dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4223a-107">The **newPlaylist** method returns an **IWMPPlaylist** interface for a new, empty playlist in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="4223a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4223a-108">Syntax</span></span>


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.newPlaylist
```





## <a name="parameters"></a><span data-ttu-id="4223a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4223a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4223a-110">*bstrName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4223a-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4223a-111">**System. String** qui est le nom de la nouvelle sélection.</span><span class="sxs-lookup"><span data-stu-id="4223a-111">A **System.String** that is the name of the new playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4223a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4223a-112">Return value</span></span>

<span data-ttu-id="4223a-113">Interface **wmplib. IWMPPlaylist** pour la nouvelle sélection.</span><span class="sxs-lookup"><span data-stu-id="4223a-113">A **WMPLib.IWMPPlaylist** interface for the new playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="4223a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="4223a-114">Remarks</span></span>

<span data-ttu-id="4223a-115">Cette méthode crée une sélection vide dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4223a-115">This method creates an empty playlist in the library.</span></span> <span data-ttu-id="4223a-116">Pour remplir la sélection avec des éléments multimédias, utilisez **IWMPPlaylist. appendItem** ou **IWMPPlaylist. InsertItem**.</span><span class="sxs-lookup"><span data-stu-id="4223a-116">To fill the playlist with media items, use **IWMPPlaylist.appendItem** or **IWMPPlaylist.insertItem**.</span></span>

<span data-ttu-id="4223a-117">Plusieurs playlists portant le même nom sont autorisées dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4223a-117">Multiple playlists having the same name are permitted in the library.</span></span> <span data-ttu-id="4223a-118">Pour éviter de créer un nom de playlist dupliqué avec cette méthode, utilisez la méthode **GetByName** et **IWMPPlaylistArray. Count** pour déterminer si une sélection portant un nom particulier existe déjà.</span><span class="sxs-lookup"><span data-stu-id="4223a-118">To avoid creating a duplicate playlist name with this method, use the **getByName** method and **IWMPPlaylistArray.count** to discover whether a playlist with a particular name already exists.</span></span>

<span data-ttu-id="4223a-119">Les espaces de début et de fin ne sont pas autorisés dans les noms de playlist et sont automatiquement supprimés de la valeur spécifiée pour le paramètre *bstrName* .</span><span class="sxs-lookup"><span data-stu-id="4223a-119">Leading and trailing spaces are not permitted in playlist names, and are automatically removed from the value specified for the *bstrName* parameter.</span></span>

<span data-ttu-id="4223a-120">Avant d’appeler cette méthode, vous devez disposer d’un accès complet à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4223a-120">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="4223a-121">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="4223a-121">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4223a-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="4223a-122">Examples</span></span>

<span data-ttu-id="4223a-123">L’exemple suivant crée une nouvelle sélection vide appelée « ThreeList », l’ajoute à la collection de sélections et lui retourne une interface.</span><span class="sxs-lookup"><span data-stu-id="4223a-123">The following example creates a new empty playlist called "ThreeList", adds it to the playlist collection, and returns an interface to it.</span></span> <span data-ttu-id="4223a-124">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="4223a-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a new empty playlist, named ThreeList, to the playlist collection.
WMPLib.IWMPPlaylist newList = player.playlistCollection.newPlaylist("ThreeList");
```


```VB

'  Add a new empty playlist, named ThreeList, to the playlist collection.
Dim newList As WMPLib.IWMPPlaylist = player.playlistCollection.newPlaylist(&quot;ThreeList&quot;)
```





## <a name="requirements"></a><span data-ttu-id="4223a-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4223a-125">Requirements</span></span>



| <span data-ttu-id="4223a-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4223a-126">Requirement</span></span> | <span data-ttu-id="4223a-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="4223a-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4223a-128">Version</span><span class="sxs-lookup"><span data-stu-id="4223a-128">Version</span></span><br/>   | <span data-ttu-id="4223a-129">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4223a-129">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="4223a-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4223a-130">Namespace</span></span><br/> | <span data-ttu-id="4223a-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4223a-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4223a-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="4223a-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4223a-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4223a-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4223a-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4223a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4223a-135">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4223a-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4223a-136">**IWMPPlaylist. appendItem (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4223a-136">**IWMPPlaylist.appendItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4223a-137">**IWMPPlaylist. insertItem (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4223a-137">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4223a-138">**IWMPPlaylistArray. Count (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4223a-138">**IWMPPlaylistArray.count (VB and C#)**</span></span>](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4223a-139">**Interface IWMPPlaylistCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4223a-139">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4223a-140">**IWMPPlaylistCollection. getByName (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4223a-140">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





