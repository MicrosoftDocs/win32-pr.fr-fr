---
title: Méthode IWMPPlaylistCollection getByName
description: La méthode getByName retourne une interface IWMPPlaylistArray qui fournit l’accès aux sélections portant le nom spécifié, le cas échéant.
ms.assetid: d41afab1-4103-4f59-a432-21a502499444
keywords:
- méthode getByName lecteur Windows Media
- méthode getByName lecteur Windows Media, interface IWMPPlaylistCollection
- Interface IWMPPlaylistCollection lecteur Windows Media, méthode getByName
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getByName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e51f83b4db019286c04762a081e649fec282135e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541594"
---
# <a name="iwmpplaylistcollectiongetbyname-method"></a><span data-ttu-id="e7819-106">IWMPPlaylistCollection :: getByName, méthode</span><span class="sxs-lookup"><span data-stu-id="e7819-106">IWMPPlaylistCollection::getByName method</span></span>

<span data-ttu-id="e7819-107">La méthode **GetByName** retourne une interface **IWMPPlaylistArray** qui fournit l’accès aux sélections portant le nom spécifié, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="e7819-107">The **getByName** method returns a **IWMPPlaylistArray** interface that provides access to playlists with the specified name, if any exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7819-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7819-108">Syntax</span></span>


```CSharp
public IWMPPlaylistArray getByName(
  System.String bstrName
);
```


```VB

Public Function getByName( _
  ByVal bstrName As System.String _
) As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getByName
```





## <a name="parameters"></a><span data-ttu-id="e7819-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7819-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7819-110">*bstrName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7819-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7819-111">**System. String** qui est le nom de la sélection.</span><span class="sxs-lookup"><span data-stu-id="e7819-111">A **System.String** that is the name of the playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7819-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7819-112">Return value</span></span>

<span data-ttu-id="e7819-113">Interface **wmplib. IWMPPlaylistArray** pour le tableau de sélections récupéré.</span><span class="sxs-lookup"><span data-stu-id="e7819-113">A **WMPLib.IWMPPlaylistArray** interface for the retrieved array of playlists.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7819-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e7819-114">Remarks</span></span>

<span data-ttu-id="e7819-115">Utilisez **IWMPPlaylistArray. Count** pour déterminer si une sélection existe.</span><span class="sxs-lookup"><span data-stu-id="e7819-115">Use **IWMPPlaylistArray.count** to determine whether a playlist exists.</span></span> <span data-ttu-id="e7819-116">Si **Count** est égal à zéro, le tableau est vide.</span><span class="sxs-lookup"><span data-stu-id="e7819-116">If **count** is zero, the array is empty.</span></span>

<span data-ttu-id="e7819-117">Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="e7819-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="e7819-118">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e7819-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e7819-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="e7819-119">Examples</span></span>

<span data-ttu-id="e7819-120">L’exemple suivant utilise **GetByName** pour vérifier la collection de sélections pour une sélection nommée « favoris--4 et 5 étoiles évaluées ».</span><span class="sxs-lookup"><span data-stu-id="e7819-120">The following example uses **getByName** to check the playlist collection for a playlist named "Favorites -- 4 and 5 star rated".</span></span> <span data-ttu-id="e7819-121">Si une sélection de ce nom existe, **GetByName** la définit en tant que sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="e7819-121">If a playlist by that name exists, **getByName** sets it as the current playlist.</span></span> <span data-ttu-id="e7819-122">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="e7819-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the count of the playlists named "Favorites -- 4 and 5 star rated".
int checkit = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").count;

// Since duplicate playlist names are allowed, the count returned
// will be either zero (no playlist) or greater than zero (playlist exists).
if (checkit > 0)
{
    // Retrieve a playlist array containing "Favorites -- 4 and 5 star rated".
    // Assume that there is only one playlist with that name, and assign it to the 
    // current playlist.
    player.currentPlaylist = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").Item(0);
}
```


```VB

'  Get the count of the playlists named &quot;Favorites -- 4 and 5 star rated&quot;.
Dim checkit As Integer = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).count

&#39;  Since duplicate playlist names are allowed, the count returned
&#39;  will be either zero (no playlist) or greater than zero (playlist exists).
If (checkit > 0) Then

    &#39;  Retrieve a playlist array object containing &quot;Favorites -- 4 and 5 star rated&quot;.
    &#39;  Assume that there is only one playlist with that name, and assign it to the 
    &#39;  current playlist.
    player.currentPlaylist = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).Item(0)

End If
```





## <a name="requirements"></a><span data-ttu-id="e7819-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7819-123">Requirements</span></span>



| <span data-ttu-id="e7819-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7819-124">Requirement</span></span> | <span data-ttu-id="e7819-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7819-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7819-126">Version</span><span class="sxs-lookup"><span data-stu-id="e7819-126">Version</span></span><br/>   | <span data-ttu-id="e7819-127">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e7819-127">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="e7819-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e7819-128">Namespace</span></span><br/> | <span data-ttu-id="e7819-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e7819-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e7819-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="e7819-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e7819-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e7819-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7819-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7819-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7819-133">**Interface IWMPPlaylistArray (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="e7819-133">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e7819-134">**IWMPPlaylistArray. Count (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="e7819-134">**IWMPPlaylistArray.count (VB and C#)**</span></span>](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e7819-135">**Interface IWMPPlaylistCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="e7819-135">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





