---
title: Méthode IWMPMediaCollection getByAttribute
description: La méthode getByAttribute retourne une interface IWMPPlaylist qui correspond à l’attribut spécifié ayant la valeur spécifiée.
ms.assetid: ece70a2c-38bc-4652-8319-efcde5f9720a
keywords:
- méthode getByAttribute lecteur Windows Media
- méthode getByAttribute lecteur Windows Media, interface IWMPMediaCollection
- Interface IWMPMediaCollection lecteur Windows Media, méthode getByAttribute
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAttribute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd7adba98fbfa450cd938b56ec6d91598b918d0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540703"
---
# <a name="iwmpmediacollectiongetbyattribute-method"></a><span data-ttu-id="1df04-106">IWMPMediaCollection :: getByAttribute, méthode</span><span class="sxs-lookup"><span data-stu-id="1df04-106">IWMPMediaCollection::getByAttribute method</span></span>

<span data-ttu-id="1df04-107">La méthode **getByAttribute** retourne une interface **IWMPPlaylist** qui correspond à l’attribut spécifié ayant la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1df04-107">The **getByAttribute** method returns an **IWMPPlaylist** interface that corresponds to the specified attribute having the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1df04-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1df04-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAttribute(
  System.String bstrAttribute,
  System.String bstrValue
);
```


```VB

Public Function getByAttribute( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAttribute
```





## <a name="parameters"></a><span data-ttu-id="1df04-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1df04-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1df04-110">*bstrAttribute* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1df04-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1df04-111">**System. String** qui est l’attribut spécifié.</span><span class="sxs-lookup"><span data-stu-id="1df04-111">The **System.String** that is the specified attribute.</span></span>

</dd> <dt>

<span data-ttu-id="1df04-112">*bstrValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1df04-112">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1df04-113">**System. String** qui correspond à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1df04-113">The **System.String** that is the specified value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1df04-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1df04-114">Return value</span></span>

<span data-ttu-id="1df04-115">Interface **wmplib. IWMPPlaylist** pour les éléments multimédias récupérés.</span><span class="sxs-lookup"><span data-stu-id="1df04-115">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="1df04-116">Notes</span><span class="sxs-lookup"><span data-stu-id="1df04-116">Remarks</span></span>

<span data-ttu-id="1df04-117">Cette méthode peut être utilisée pour créer une requête générique pour les éléments multimédias qui correspondent à une valeur pour un attribut de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="1df04-117">This method can be used to create a generic query for media items that match a value for an attribute in the library.</span></span> <span data-ttu-id="1df04-118">Cela est utile dans le cas des attributs définis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1df04-118">This is useful in the case of user-defined attributes.</span></span> <span data-ttu-id="1df04-119">Si l’attribut n’existe pas, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="1df04-119">If the attribute does not exist, an error will result.</span></span>

<span data-ttu-id="1df04-120">Vous pouvez utiliser cette méthode pour récupérer tous les éléments multimédias d’un type spécifique.</span><span class="sxs-lookup"><span data-stu-id="1df04-120">You can use this method to retrieve all of the media items of a specific type.</span></span> <span data-ttu-id="1df04-121">Utilisez le nom d’attribut **MediaType** et l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1df04-121">Use the attribute name **MediaType** and one of the following values.</span></span>



| <span data-ttu-id="1df04-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="1df04-122">Value</span></span>    | <span data-ttu-id="1df04-123">Description</span><span class="sxs-lookup"><span data-stu-id="1df04-123">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="1df04-124">audio</span><span class="sxs-lookup"><span data-stu-id="1df04-124">audio</span></span>    | <span data-ttu-id="1df04-125">Musique et autres éléments audio uniquement</span><span class="sxs-lookup"><span data-stu-id="1df04-125">Music and other audio-only items</span></span>                          |
| <span data-ttu-id="1df04-126">autre</span><span class="sxs-lookup"><span data-stu-id="1df04-126">other</span></span>    | <span data-ttu-id="1df04-127">D’autres éléments, tels qu’un fichier. ASF ou l’URL d’un flux.</span><span class="sxs-lookup"><span data-stu-id="1df04-127">Other items, such as an .asf file or the URL of a stream.</span></span> |
| <span data-ttu-id="1df04-128">photos</span><span class="sxs-lookup"><span data-stu-id="1df04-128">photo</span></span>    | <span data-ttu-id="1df04-129">Éléments de photo.</span><span class="sxs-lookup"><span data-stu-id="1df04-129">Photo items.</span></span> <span data-ttu-id="1df04-130">Requiert le lecteur Windows Media 10.</span><span class="sxs-lookup"><span data-stu-id="1df04-130">Requires Windows Media Player 10.</span></span>            |
| <span data-ttu-id="1df04-131">playlist</span><span class="sxs-lookup"><span data-stu-id="1df04-131">playlist</span></span> | <span data-ttu-id="1df04-132">Sélections représentées en tant qu’éléments multimédias.</span><span class="sxs-lookup"><span data-stu-id="1df04-132">Playlists represented as media items.</span></span>                     |
| <span data-ttu-id="1df04-133">radio</span><span class="sxs-lookup"><span data-stu-id="1df04-133">radio</span></span>    | <span data-ttu-id="1df04-134">Éléments de station de radio.</span><span class="sxs-lookup"><span data-stu-id="1df04-134">Radio station items.</span></span> <span data-ttu-id="1df04-135">Non utilisé par le lecteur Windows Media 10.</span><span class="sxs-lookup"><span data-stu-id="1df04-135">Not used by Windows Media Player 10.</span></span> |
| <span data-ttu-id="1df04-136">video</span><span class="sxs-lookup"><span data-stu-id="1df04-136">video</span></span>    | <span data-ttu-id="1df04-137">Éléments vidéo.</span><span class="sxs-lookup"><span data-stu-id="1df04-137">Video items.</span></span>                                              |



 

<span data-ttu-id="1df04-138">Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="1df04-138">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="1df04-139">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="1df04-139">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="1df04-140">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="1df04-140">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="1df04-141">Il existe deux façons de récupérer une interface **IWMPMediaCollection** , et le comportement de la méthode **getByAttribute** dépend de ceux de ces deux méthodes.</span><span class="sxs-lookup"><span data-stu-id="1df04-141">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the **getByAttribute** method depends on which of those two ways you use.</span></span> <span data-ttu-id="1df04-142">Si vous récupérez l’interface en appelant [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), la méthode **getByAttribute** retourne tous les éléments multimédias de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="1df04-142">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the **getByAttribute** method returns all the media items in the library.</span></span> <span data-ttu-id="1df04-143">Toutefois, si vous récupérez l’interface en appelant [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), la méthode **getByAttribute** retourne uniquement les éléments audio de la bibliothèque qui ont l’attribut et la valeur spécifiés.</span><span class="sxs-lookup"><span data-stu-id="1df04-143">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the **getByAttribute** method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="1df04-144">Exemples</span><span class="sxs-lookup"><span data-stu-id="1df04-144">Examples</span></span>

<span data-ttu-id="1df04-145">L’exemple de code suivant utilise **getByAttribute** pour lire tout le contenu de la bibliothèque par l’artiste nommé triode 48.</span><span class="sxs-lookup"><span data-stu-id="1df04-145">The following code example uses **getByAttribute** to play all content from the library by the artist named Triode 48.</span></span> <span data-ttu-id="1df04-146">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="1df04-146">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to a playlist that contains media items by a particular artist.
WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
player.currentPlaylist = pl;

// Play the media items in the current playlist. 
player.Ctlcontrols.play();
```


```VB

' Get an interface to a playlist that contains media items by a particular artist.
Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAttribute(&quot;Artist&quot;, &quot;Triode 48&quot;)

&#39; Make the new playlist the current one.
player.currentPlaylist = pl

&#39; Play the media items in the current playlist. 
player.Ctlcontrols.play()
```





## <a name="requirements"></a><span data-ttu-id="1df04-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1df04-147">Requirements</span></span>



| <span data-ttu-id="1df04-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1df04-148">Requirement</span></span> | <span data-ttu-id="1df04-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="1df04-149">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1df04-150">Version</span><span class="sxs-lookup"><span data-stu-id="1df04-150">Version</span></span><br/>   | <span data-ttu-id="1df04-151">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="1df04-151">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1df04-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1df04-152">Namespace</span></span><br/> | <span data-ttu-id="1df04-153">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1df04-153">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1df04-154">Assembly</span><span class="sxs-lookup"><span data-stu-id="1df04-154">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1df04-155"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1df04-155"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1df04-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1df04-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1df04-157">**Interface IWMPMediaCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="1df04-157">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1df04-158">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="1df04-158">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1df04-159">**IWMPPlaylistCollection. getAll (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="1df04-159">**IWMPPlaylistCollection.getAll (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)
</dt> </dl>

 

 





