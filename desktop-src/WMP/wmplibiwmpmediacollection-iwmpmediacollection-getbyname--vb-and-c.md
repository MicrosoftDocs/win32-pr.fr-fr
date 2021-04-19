---
title: Méthode IWMPMediaCollection getByName
description: La méthode getByName retourne une interface IWMPPlaylist qui fournit l’accès aux éléments multimédias avec le nom spécifié.
ms.assetid: 137e938c-eb9f-4a87-8962-880e71a11ca2
keywords:
- méthode getByName lecteur Windows Media
- méthode getByName lecteur Windows Media, interface IWMPMediaCollection
- Interface IWMPMediaCollection lecteur Windows Media, méthode getByName
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64c68e2a5359eadf9c6212571ed948c103c01bdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541533"
---
# <a name="iwmpmediacollectiongetbyname-method"></a><span data-ttu-id="404d9-106">IWMPMediaCollection :: getByName, méthode</span><span class="sxs-lookup"><span data-stu-id="404d9-106">IWMPMediaCollection::getByName method</span></span>

<span data-ttu-id="404d9-107">La `getByName` méthode retourne une interface **IWMPPlaylist** qui fournit l’accès aux éléments multimédias avec le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="404d9-107">The `getByName` method returns an **IWMPPlaylist** interface that provides access to media items with the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="404d9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="404d9-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByName(
  System.String bstrName
);
```


```VB

Public Function getByName( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByName
```





## <a name="parameters"></a><span data-ttu-id="404d9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="404d9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="404d9-110">*bstrName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="404d9-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="404d9-111">**System. String** qui est le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="404d9-111">The **System.String** that is the specified name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="404d9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="404d9-112">Return value</span></span>

<span data-ttu-id="404d9-113">Interface **wmplib. IWMPPlaylist** pour les éléments multimédias récupérés.</span><span class="sxs-lookup"><span data-stu-id="404d9-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="404d9-114">Notes</span><span class="sxs-lookup"><span data-stu-id="404d9-114">Remarks</span></span>

<span data-ttu-id="404d9-115">Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="404d9-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="404d9-116">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="404d9-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="404d9-117">Il existe deux façons de récupérer une interface **IWMPMediaCollection** , et le comportement de la `getByName` méthode dépend de ce que vous utilisez pour ces deux méthodes.</span><span class="sxs-lookup"><span data-stu-id="404d9-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the `getByName` method depends on which of those two ways you use.</span></span> <span data-ttu-id="404d9-118">Si vous récupérez l’interface en appelant [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), la `getByName` méthode retourne tous les éléments multimédias de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="404d9-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the `getByName` method returns all the media items in the library.</span></span> <span data-ttu-id="404d9-119">Toutefois, si vous récupérez l’interface en appelant [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), la `getByName` méthode retourne uniquement les éléments audio de la bibliothèque qui ont l’attribut et la valeur spécifiés.</span><span class="sxs-lookup"><span data-stu-id="404d9-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the `getByName` method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="404d9-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="404d9-120">Examples</span></span>

<span data-ttu-id="404d9-121">L’exemple suivant utilise `getByName` pour récupérer trois éléments de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="404d9-121">The following example uses `getByName` to retrieve three items from the library.</span></span> <span data-ttu-id="404d9-122">Chaque élément est ensuite ajouté à la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="404d9-122">Each item is then appended to the current playlist.</span></span> <span data-ttu-id="404d9-123">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="404d9-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// In each case, use the name exactly as it appears in the library.
// Windows Media Player does not include file name extensions or file paths
// in the name. Internet URLs include the entire path, but not the 
// file name extension.

// Get an interface to a playlist that contains an Internet URL.
WMPLib.IWMPPlaylist one = player.mediaCollection.getByName("https://www.proseware.com/Media/Laure");

// Get an interface to a playlist that contains a file on a network server.
WMPLib.IWMPPlaylist two = player.mediaCollection.getByName("Jeanne");

// Get an interface to a playlist that contains a file on a local drive.
WMPLib.IWMPPlaylist three = player.mediaCollection.getByName("house");

// Append each item to the current playlist. Since each playlist retrieved
// using getByName contains one digital media item, use the get_Item
// method with an index of zero to reference that item.
player.currentPlaylist.appendItem(one.get_Item(0));
player.currentPlaylist.appendItem(two.get_Item(0));
player.currentPlaylist.appendItem(three.get_Item(0));
```


```VB

' In each case, use the name exactly as it appears in the library.
&#39; Windows Media Player does not include file name extensions or file paths
&#39; in the name. Internet URLs include the entire path, but not the 
&#39; file name extension.

&#39; Get an interface to a playlist that contains an Internet URL.
Dim one As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;https://www.proseware.com/Media/Laure&quot;)

&#39; Get an interface to a playlist that contains a file on a network server.
Dim two As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;Jeanne&quot;)

&#39; Get an interface to a playlist that contains a file on a local drive.
Dim three As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;house&quot;)

&#39; Append each item to the current playlist. Since each playlist retrieved
&#39; using getByName contains one digital media item, use the Item
&#39; property with an index of zero to reference that item.
player.currentPlaylist.appendItem(one.Item(0))
player.currentPlaylist.appendItem(two.Item(0))
player.currentPlaylist.appendItem(three.Item(0))
```





## <a name="requirements"></a><span data-ttu-id="404d9-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="404d9-124">Requirements</span></span>



| <span data-ttu-id="404d9-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="404d9-125">Requirement</span></span> | <span data-ttu-id="404d9-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="404d9-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="404d9-127">Version</span><span class="sxs-lookup"><span data-stu-id="404d9-127">Version</span></span><br/>   | <span data-ttu-id="404d9-128">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="404d9-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="404d9-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="404d9-129">Namespace</span></span><br/> | <span data-ttu-id="404d9-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="404d9-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="404d9-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="404d9-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="404d9-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="404d9-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="404d9-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="404d9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="404d9-134">**Interface IWMPMediaCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="404d9-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="404d9-135">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="404d9-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





