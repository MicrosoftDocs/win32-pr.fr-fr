---
title: Méthode IWMPMediaCollection getByAlbum
description: La méthode getByAlbum retourne une interface IWMPPlaylist qui fournit l’accès aux éléments multimédias à partir de l’album spécifié.
ms.assetid: 26f004c0-de46-4792-8212-9d4ac749bb21
keywords:
- méthode getByAlbum lecteur Windows Media
- méthode getByAlbum lecteur Windows Media, interface IWMPMediaCollection
- Interface IWMPMediaCollection lecteur Windows Media, méthode getByAlbum
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAlbum
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c455e9bd61038a4d72bb6537d7c62b30a5d0b733
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533259"
---
# <a name="iwmpmediacollectiongetbyalbum-method"></a><span data-ttu-id="32ca5-106">IWMPMediaCollection :: getByAlbum, méthode</span><span class="sxs-lookup"><span data-stu-id="32ca5-106">IWMPMediaCollection::getByAlbum method</span></span>

<span data-ttu-id="32ca5-107">La méthode **getByAlbum** retourne une interface **IWMPPlaylist** qui fournit l’accès aux éléments multimédias à partir de l’album spécifié.</span><span class="sxs-lookup"><span data-stu-id="32ca5-107">The **getByAlbum** method returns an **IWMPPlaylist** interface that provides access to media items from the specified album.</span></span>

## <a name="syntax"></a><span data-ttu-id="32ca5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32ca5-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAlbum(
  System.String bstrAlbum
);
```


```VB

Public Function getByAlbum( _
  ByVal bstrAlbum As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAlbum
```





## <a name="parameters"></a><span data-ttu-id="32ca5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32ca5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32ca5-110">*bstrAlbum* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="32ca5-110">*bstrAlbum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32ca5-111">**System. String** qui est le titre de l’album.</span><span class="sxs-lookup"><span data-stu-id="32ca5-111">The **System.String** that is the title of the album.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32ca5-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="32ca5-112">Return value</span></span>

<span data-ttu-id="32ca5-113">Interface **wmplib. IWMPPlaylist** pour les éléments multimédias récupérés.</span><span class="sxs-lookup"><span data-stu-id="32ca5-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="32ca5-114">Notes</span><span class="sxs-lookup"><span data-stu-id="32ca5-114">Remarks</span></span>

<span data-ttu-id="32ca5-115">Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="32ca5-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="32ca5-116">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="32ca5-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="32ca5-117">Il existe deux façons de récupérer une interface **IWMPMediaCollection** , et le comportement de la méthode **getByAlbum** dépend de ceux de ces deux méthodes.</span><span class="sxs-lookup"><span data-stu-id="32ca5-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the **getByAlbum** method depends on which of those two ways you use.</span></span> <span data-ttu-id="32ca5-118">Si vous récupérez l’interface en appelant [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), la méthode **getByAlbum** retourne tous les éléments multimédias de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="32ca5-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the **getByAlbum** method returns all the media items in the library.</span></span> <span data-ttu-id="32ca5-119">Toutefois, si vous récupérez l’interface en appelant [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), la méthode **getByAlbum** retourne uniquement les éléments audio de la bibliothèque qui appartiennent à l’album spécifié.</span><span class="sxs-lookup"><span data-stu-id="32ca5-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the **getByAlbum** method returns only the audio items in the library that belong to the specified album.</span></span>

## <a name="examples"></a><span data-ttu-id="32ca5-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="32ca5-120">Examples</span></span>

<span data-ttu-id="32ca5-121">L’exemple suivant utilise **getByAlbum** pour créer une sélection d’éléments multimédias lorsque l’utilisateur clique sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="32ca5-121">The following example uses **getByAlbum** to create a playlist of media items when the user clicks a button.</span></span> <span data-ttu-id="32ca5-122">La sélection contient des éléments avec l’album spécifié par l’utilisateur dans une zone de texte.</span><span class="sxs-lookup"><span data-stu-id="32ca5-122">The playlist contains items with the album specified by the user in a text box.</span></span> <span data-ttu-id="32ca5-123">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="32ca5-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playAlbum_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the album title text that the user entered in the text box. 
    string album = getAlbum.Text;

    // Create the playlist using getByAlbum. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAlbum(album);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAlbum_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAlbum.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the album title text that the user entered in the text box. 
    Dim album As String = getAlbum.Text

    &#39; Create the playlist using getByAlbum. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAlbum(album)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="32ca5-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32ca5-124">Requirements</span></span>



| <span data-ttu-id="32ca5-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32ca5-125">Requirement</span></span> | <span data-ttu-id="32ca5-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="32ca5-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32ca5-127">Version</span><span class="sxs-lookup"><span data-stu-id="32ca5-127">Version</span></span><br/>   | <span data-ttu-id="32ca5-128">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="32ca5-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="32ca5-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="32ca5-129">Namespace</span></span><br/> | <span data-ttu-id="32ca5-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="32ca5-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="32ca5-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="32ca5-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="32ca5-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="32ca5-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32ca5-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32ca5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32ca5-134">**Interface IWMPMediaCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="32ca5-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="32ca5-135">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="32ca5-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





