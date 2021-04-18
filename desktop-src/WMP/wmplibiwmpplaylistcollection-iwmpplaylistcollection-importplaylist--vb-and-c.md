---
title: Méthode IWMPPlaylistCollection importPlaylist
description: La méthode importPlaylist ajoute une sélection statique à la bibliothèque. | Méthode IWMPPlaylistCollection importPlaylist
ms.assetid: 7a64e618-920d-419d-8769-612ab5dff49b
keywords:
- méthode importPlaylist lecteur Windows Media
- méthode importPlaylist lecteur Windows Media, interface IWMPPlaylistCollection
- Interface IWMPPlaylistCollection lecteur Windows Media, méthode importPlaylist
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.importPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3ca727155d6ae859123d427812d93ebaa0b05c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525953"
---
# <a name="iwmpplaylistcollectionimportplaylist-method"></a><span data-ttu-id="53a95-107">IWMPPlaylistCollection :: importPlaylist, méthode</span><span class="sxs-lookup"><span data-stu-id="53a95-107">IWMPPlaylistCollection::importPlaylist method</span></span>

<span data-ttu-id="53a95-108">La méthode **importPlaylist** ajoute une sélection statique à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="53a95-108">The **importPlaylist** method adds a static playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="53a95-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53a95-109">Syntax</span></span>


```CSharp
public IWMPPlaylist importPlaylist(
  IWMPPlaylist pItem
);
```


```VB

Public Function importPlaylist( _
  ByVal pItem As IWMPPlaylist _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.importPlaylist
```





## <a name="parameters"></a><span data-ttu-id="53a95-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53a95-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53a95-111">*pItem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="53a95-111">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53a95-112">Une interface **wmplib. IWMPPlaylist** pour la sélection que cette méthode ajoutera.</span><span class="sxs-lookup"><span data-stu-id="53a95-112">A **WMPLib.IWMPPlaylist** interface for the playlist that this method will add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53a95-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="53a95-113">Return value</span></span>

<span data-ttu-id="53a95-114">Interface **wmplib. IWMPPlaylist** pour la sélection ajoutée.</span><span class="sxs-lookup"><span data-stu-id="53a95-114">A **WMPLib.IWMPPlaylist** interface for the added playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="53a95-115">Notes</span><span class="sxs-lookup"><span data-stu-id="53a95-115">Remarks</span></span>

<span data-ttu-id="53a95-116">Les sélections qui ne contiennent pas d’éléments multimédias ne peuvent pas être ajoutées à la bibliothèque à l’aide de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="53a95-116">Playlists that do not contain any media items cannot be added to the library by using this method.</span></span> <span data-ttu-id="53a95-117">Pour créer une playlist vide dans la bibliothèque, utilisez la méthode **newPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="53a95-117">To create an empty playlist in the library, use the **newPlaylist** method.</span></span> <span data-ttu-id="53a95-118">Vous pouvez ensuite remplir la playlist obtenue avec des éléments multimédias à l’aide de **IWMPPlaylist. appendItem** ou **IWMPPlaylist. InsertItem**.</span><span class="sxs-lookup"><span data-stu-id="53a95-118">You can then fill the resulting playlist with media items by using **IWMPPlaylist.appendItem** or **IWMPPlaylist.insertItem**.</span></span>

<span data-ttu-id="53a95-119">Si vous transmettez cette méthode à une sélection automatique, la requête est exécutée une fois et le résultat est ajouté à la bibliothèque en tant que sélection statique.</span><span class="sxs-lookup"><span data-stu-id="53a95-119">If you pass this method an auto playlist, the query is executed once and the result is added to the library as a static playlist.</span></span> <span data-ttu-id="53a95-120">Pour ajouter une sélection automatique à la bibliothèque et conserver son comportement automatique, utilisez **IWMPMediaCollection. Add**.</span><span class="sxs-lookup"><span data-stu-id="53a95-120">To add an auto playlist to the library and preserve its automatic behavior, use **IWMPMediaCollection.add**.</span></span> <span data-ttu-id="53a95-121">Pour plus d’informations, consultez [sélections statiques et automatiques](static-and-auto-playlists.md).</span><span class="sxs-lookup"><span data-stu-id="53a95-121">For more information, see [Static and Auto Playlists](static-and-auto-playlists.md).</span></span>

<span data-ttu-id="53a95-122">Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="53a95-122">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="53a95-123">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="53a95-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="53a95-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53a95-124">Requirements</span></span>



| <span data-ttu-id="53a95-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53a95-125">Requirement</span></span> | <span data-ttu-id="53a95-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="53a95-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53a95-127">Version</span><span class="sxs-lookup"><span data-stu-id="53a95-127">Version</span></span><br/>   | <span data-ttu-id="53a95-128">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="53a95-128">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="53a95-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="53a95-129">Namespace</span></span><br/> | <span data-ttu-id="53a95-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="53a95-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="53a95-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="53a95-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="53a95-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="53a95-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53a95-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53a95-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53a95-134">**IWMPMediaCollection. Add (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="53a95-134">**IWMPMediaCollection.add (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="53a95-135">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="53a95-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="53a95-136">**IWMPPlaylist. appendItem (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="53a95-136">**IWMPPlaylist.appendItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="53a95-137">**IWMPPlaylist. insertItem (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="53a95-137">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="53a95-138">**Interface IWMPPlaylistCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="53a95-138">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="53a95-139">**IWMPPlaylistCollection. newPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="53a95-139">**IWMPPlaylistCollection.newPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





