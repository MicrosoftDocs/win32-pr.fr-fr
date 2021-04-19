---
title: Méthode IWMPMediaCollection getByAuthor
description: La méthode getByAuthor retourne une interface IWMPPlaylist qui fournit l’accès aux éléments multimédias par l’auteur spécifié.
ms.assetid: eb3793f6-bad1-4c80-991e-c6d0093ae57f
keywords:
- méthode getByAuthor lecteur Windows Media
- méthode getByAuthor lecteur Windows Media, interface IWMPMediaCollection
- Interface IWMPMediaCollection lecteur Windows Media, méthode getByAuthor
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAuthor
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e594de010a65c15088e2a31a3ccbac2ac5a1fc6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541542"
---
# <a name="iwmpmediacollectiongetbyauthor-method"></a><span data-ttu-id="b53a9-106">IWMPMediaCollection :: getByAuthor, méthode</span><span class="sxs-lookup"><span data-stu-id="b53a9-106">IWMPMediaCollection::getByAuthor method</span></span>

<span data-ttu-id="b53a9-107">La `getByAuthor` méthode retourne une interface **IWMPPlaylist** qui fournit l’accès aux éléments multimédias par l’auteur spécifié.</span><span class="sxs-lookup"><span data-stu-id="b53a9-107">The `getByAuthor` method returns an **IWMPPlaylist** interface that provides access to the media items by the specified author.</span></span>

## <a name="syntax"></a><span data-ttu-id="b53a9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b53a9-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAuthor(
  System.String bstrAuthor
);
```


```VB

Public Function getByAuthor( _
  ByVal bstrAuthor As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAuthor
```





## <a name="parameters"></a><span data-ttu-id="b53a9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b53a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b53a9-110">*bstrAuthor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b53a9-110">*bstrAuthor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b53a9-111">**System. String** qui est le nom de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="b53a9-111">The **System.String** that is the name of the author.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b53a9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b53a9-112">Return value</span></span>

<span data-ttu-id="b53a9-113">Interface **wmplib. IWMPPlaylist** pour les éléments multimédias récupérés.</span><span class="sxs-lookup"><span data-stu-id="b53a9-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="b53a9-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b53a9-114">Remarks</span></span>

<span data-ttu-id="b53a9-115">Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b53a9-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="b53a9-116">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b53a9-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="b53a9-117">Il existe deux façons de récupérer une interface **IWMPMediaCollection** , et le comportement de la `getByAuthor` méthode dépend de ce que vous utilisez pour ces deux méthodes.</span><span class="sxs-lookup"><span data-stu-id="b53a9-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the `getByAuthor` method depends on which of those two ways you use.</span></span> <span data-ttu-id="b53a9-118">Si vous récupérez l’interface en appelant [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), la `getByAuthor` méthode retourne tous les éléments multimédias de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b53a9-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the `getByAuthor` method returns all the media items in the library.</span></span> <span data-ttu-id="b53a9-119">Toutefois, si vous récupérez l’interface en appelant [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), la `getByAuthor` méthode retourne uniquement les éléments audio de la bibliothèque qui ont l’attribut et la valeur spécifiés.</span><span class="sxs-lookup"><span data-stu-id="b53a9-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the `getByAuthor` method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="b53a9-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="b53a9-120">Examples</span></span>

<span data-ttu-id="b53a9-121">L’exemple suivant utilise `getByAuthor` pour créer une sélection d’éléments multimédias lorsque l’utilisateur clique sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="b53a9-121">The following example uses `getByAuthor` to create a playlist of media items when the user clicks a button.</span></span> <span data-ttu-id="b53a9-122">La sélection contient des éléments qui correspondent au nom de l’auteur spécifié par l’utilisateur dans une zone de texte.</span><span class="sxs-lookup"><span data-stu-id="b53a9-122">The playlist contains items matching the author's name specified by the user in a text box.</span></span> <span data-ttu-id="b53a9-123">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="b53a9-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playAuthor_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the author's name from the text box. 
    string author = getAuthor.Text;

    // Create the playlist using getByAuthor. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAuthor(author);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAuthor_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAuthor.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the author&#39;s name from the text box. 
    Dim author As String = getAuthor.Text

    &#39; Create the playlist using getByAuthor. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAuthor(author)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="b53a9-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b53a9-124">Requirements</span></span>



| <span data-ttu-id="b53a9-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b53a9-125">Requirement</span></span> | <span data-ttu-id="b53a9-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b53a9-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b53a9-127">Version</span><span class="sxs-lookup"><span data-stu-id="b53a9-127">Version</span></span><br/>   | <span data-ttu-id="b53a9-128">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b53a9-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b53a9-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b53a9-129">Namespace</span></span><br/> | <span data-ttu-id="b53a9-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b53a9-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b53a9-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="b53a9-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b53a9-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b53a9-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b53a9-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b53a9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b53a9-134">**Interface IWMPMediaCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b53a9-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b53a9-135">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b53a9-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





