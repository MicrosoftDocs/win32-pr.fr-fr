---
title: IWMPMediaCollection getAll, méthode
description: La méthode getAll retourne une interface IWMPPlaylist qui correspond à la sélection qui contient tous les éléments multimédias de la bibliothèque.
ms.assetid: f2bbb4a4-7397-4c97-afd9-e8ee380af9da
keywords:
- méthode getAll lecteur Windows Media
- méthode getAll lecteur Windows Media, interface IWMPMediaCollection
- IWMPMediaCollection interface Windows Media Player, getAll, méthode
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be08548ae29db12ded788f34563ef5e319c27d61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525128"
---
# <a name="iwmpmediacollectiongetall-method"></a><span data-ttu-id="2da75-106">IWMPMediaCollection :: getAll, méthode</span><span class="sxs-lookup"><span data-stu-id="2da75-106">IWMPMediaCollection::getAll method</span></span>

<span data-ttu-id="2da75-107">La méthode **GetAll** retourne une interface **IWMPPlaylist** qui correspond à la sélection qui contient tous les éléments multimédias de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="2da75-107">The **getAll** method returns an **IWMPPlaylist** interface that corresponds to the playlist that contains all media items in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="2da75-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2da75-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getAll();
```


```VB

Public Function getAll() As IWMPPlaylist
Implements IWMPMediaCollection.getAll
```





## <a name="parameters"></a><span data-ttu-id="2da75-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2da75-109">Parameters</span></span>

<span data-ttu-id="2da75-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2da75-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2da75-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2da75-111">Return value</span></span>

<span data-ttu-id="2da75-112">Interface **wmplib. IWMPPlaylist** pour la sélection qui contient tous les éléments multimédias demandés.</span><span class="sxs-lookup"><span data-stu-id="2da75-112">The **WMPLib.IWMPPlaylist** interface for the playlist that contains all of the requested media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="2da75-113">Notes</span><span class="sxs-lookup"><span data-stu-id="2da75-113">Remarks</span></span>

<span data-ttu-id="2da75-114">Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="2da75-114">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="2da75-115">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2da75-115">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="2da75-116">Il existe deux façons de récupérer une interface **IWMPMediaCollection** , et le comportement de la méthode **GetAll** dépend de ce que vous utilisez pour ces deux méthodes.</span><span class="sxs-lookup"><span data-stu-id="2da75-116">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the **getAll** method depends on which of those two ways you use.</span></span> <span data-ttu-id="2da75-117">Si vous récupérez l’interface en appelant [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), la méthode **GetAll** retourne tous les éléments multimédias de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="2da75-117">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the **getAll** method returns all the media items in the library.</span></span> <span data-ttu-id="2da75-118">Toutefois, si vous récupérez l’interface en appelant [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), la méthode **GetAll** retourne uniquement les éléments audio de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="2da75-118">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the **getAll** method returns only the audio items in the library.</span></span>

## <a name="examples"></a><span data-ttu-id="2da75-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="2da75-119">Examples</span></span>

<span data-ttu-id="2da75-120">L’exemple suivant utilise **GetAll** pour lire des éléments multimédias de manière aléatoire à partir de la collection de supports.</span><span class="sxs-lookup"><span data-stu-id="2da75-120">The following example uses **getAll** to play media items randomly from the media collection.</span></span> <span data-ttu-id="2da75-121">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="2da75-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create a random number generator. 
System.Random randGenerator = new System.Random();

// Store the count of all media items in the media collection.
int count = player.mediaCollection.getAll().count;

// Get a random integer using the count as the max value.
int rand = randGenerator.Next(count);

// Make the random media item the current media item.
player.currentMedia = player.mediaCollection.getAll().get_Item(rand);

// Play the media item.
player.Ctlcontrols.play();
```


```VB

' Create a random number generator. 
Dim randGenerator As System.Random = New System.Random()

&#39; Store the count of all media items in the media collection.
Dim count As Integer = player.mediaCollection.getAll().count

&#39; Get a random integer using the count as the max value.
Dim rand As Integer = randGenerator.Next(count)

&#39; Make the random media item the current media item.
player.currentMedia = player.mediaCollection.getAll().Item(rand)

&#39; Play the media item.
player.Ctlcontrols.play()
```





## <a name="requirements"></a><span data-ttu-id="2da75-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2da75-122">Requirements</span></span>



| <span data-ttu-id="2da75-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2da75-123">Requirement</span></span> | <span data-ttu-id="2da75-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="2da75-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2da75-125">Version</span><span class="sxs-lookup"><span data-stu-id="2da75-125">Version</span></span><br/>   | <span data-ttu-id="2da75-126">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2da75-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2da75-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2da75-127">Namespace</span></span><br/> | <span data-ttu-id="2da75-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2da75-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2da75-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="2da75-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2da75-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2da75-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2da75-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2da75-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2da75-132">**Interface IWMPMediaCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="2da75-132">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2da75-133">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="2da75-133">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





