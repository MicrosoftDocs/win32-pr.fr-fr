---
title: IWMPMediaCollection Add (méthode)
description: La méthode Add ajoute un nouvel élément multimédia ou une nouvelle sélection à la bibliothèque. | IWMPMediaCollection Add (méthode)
ms.assetid: a3539646-797b-4481-a31e-86771f3633a9
keywords:
- Ajouter une méthode lecteur Windows Media
- Add, méthode lecteur Windows Media, interface IWMPMediaCollection
- Interface IWMPMediaCollection lecteur Windows Media, méthode Add
topic_type:
- apiref
api_name:
- IWMPMediaCollection.add
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7953067281e394df71a1a53c874cb80837a5f35d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532713"
---
# <a name="iwmpmediacollectionadd-method"></a><span data-ttu-id="d123d-107">IWMPMediaCollection :: Add, méthode</span><span class="sxs-lookup"><span data-stu-id="d123d-107">IWMPMediaCollection::add method</span></span>

<span data-ttu-id="d123d-108">La méthode **Add** ajoute un nouvel élément multimédia ou une nouvelle sélection à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d123d-108">The **add** method adds a new media item or playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="d123d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d123d-109">Syntax</span></span>


```CSharp
public IWMPMedia add(
  System.String bstrURL
);
```


```VB

Public Function add( _
  ByVal bstrURL As System.String _
) As IWMPMedia
Implements IWMPMediaCollection.add
```





## <a name="parameters"></a><span data-ttu-id="d123d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d123d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d123d-111">*du bstrURL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d123d-111">*bstrURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d123d-112">**System. String** qui est l’URL qui spécifie l’emplacement de l’élément multimédia ou de la sélection.</span><span class="sxs-lookup"><span data-stu-id="d123d-112">A **System.String** that is the URL that specifies the location of the media item or playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d123d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d123d-113">Return value</span></span>

<span data-ttu-id="d123d-114">Interface **wmplib. IWMPMedia** pour l’élément ajouté ou la sélection.</span><span class="sxs-lookup"><span data-stu-id="d123d-114">The **WMPLib.IWMPMedia** interface for the added item or playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="d123d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d123d-115">Remarks</span></span>

<span data-ttu-id="d123d-116">Cette méthode charge un élément multimédia existant ou une sélection dans la bibliothèque, en fonction d’un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="d123d-116">This method loads an existing media item or playlist into the library, given a path.</span></span> <span data-ttu-id="d123d-117">Cette méthode ne déplace pas ou ne modifie pas le fichier.</span><span class="sxs-lookup"><span data-stu-id="d123d-117">This method does not move or change the file.</span></span> <span data-ttu-id="d123d-118">Cette méthode échoue si le chemin d’accès local n’est pas valide, mais que la validité des éléments de média n’est pas vérifiée avant leur ajout à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d123d-118">This method fails if given an invalid local path, but media items themselves are not checked for validity before they are added to the library.</span></span>

<span data-ttu-id="d123d-119">Cette méthode accepte à la fois les fichiers de sélection statique et automatique.</span><span class="sxs-lookup"><span data-stu-id="d123d-119">This method accepts both static and auto playlist files.</span></span> <span data-ttu-id="d123d-120">La méthode **IWMPPlaylistCollection. importPlaylist** peut également être utilisée pour ajouter une sélection statique à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d123d-120">The **IWMPPlaylistCollection.importPlaylist** method can also be used to add a static playlist to the library.</span></span>

<span data-ttu-id="d123d-121">Avant d’appeler cette méthode, vous devez disposer d’un accès complet à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d123d-121">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="d123d-122">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="d123d-122">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d123d-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="d123d-123">Examples</span></span>

<span data-ttu-id="d123d-124">L’exemple suivant ajoute trois objets multimédias à la collection de supports du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d123d-124">The following example adds three media objects to the Windows Media Player media collection.</span></span> <span data-ttu-id="d123d-125">L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="d123d-125">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Adding a media object using a website.
player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"\\yourservername\Public\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"C:\WMSDK\WMPSDK\samples\media\house.wma");
```


```VB

' Adding a media object using a website.
player.mediaCollection.add(&quot;http:&#39;www.proseware.com/Media/Laure.wma&quot;)

&#39; Adding a media object from a local network.
player.mediaCollection.add(&quot;\\yourservername\Public\Jeanne.wma&quot;)

&#39; Adding a media object from a file on a local drive.
player.mediaCollection.add(&quot;C:\WMSDK\WMPSDK\samples\media\house.wma&quot;)
```





## <a name="requirements"></a><span data-ttu-id="d123d-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d123d-126">Requirements</span></span>



| <span data-ttu-id="d123d-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d123d-127">Requirement</span></span> | <span data-ttu-id="d123d-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="d123d-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d123d-129">Version</span><span class="sxs-lookup"><span data-stu-id="d123d-129">Version</span></span><br/>   | <span data-ttu-id="d123d-130">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="d123d-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d123d-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d123d-131">Namespace</span></span><br/> | <span data-ttu-id="d123d-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d123d-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d123d-133">Assembly</span><span class="sxs-lookup"><span data-stu-id="d123d-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d123d-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d123d-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d123d-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d123d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d123d-136">**Interface IWMPMediaCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d123d-136">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d123d-137">**IWMPMediaCollection. Remove (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d123d-137">**IWMPMediaCollection.remove (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d123d-138">**IWMPPlaylistCollection. importPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d123d-138">**IWMPPlaylistCollection.importPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> </dl>

 

 





