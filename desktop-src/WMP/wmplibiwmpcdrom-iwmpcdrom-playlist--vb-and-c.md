---
title: Propriété de la sélection IWMPCdrom
description: La propriété playlist obtient une interface IWMPPlaylist représentant les pistes sur le CD-ROM actuellement dans le lecteur de CD ou les entrées de titre au niveau de la racine pour un DVD.
ms.assetid: 09c3db45-6586-4a5b-b72c-77c64473bdd0
keywords:
- Propriété playlist lecteur Windows Media
- Propriété playlist lecteur Windows Media, interface IWMPCdrom
- Interface IWMPCdrom lecteur Windows Media, propriété playlist
topic_type:
- apiref
api_name:
- IWMPCdrom.Playlist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a386881c8416f4ea1881f3ccd68ee4291aa3fa84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535285"
---
# <a name="iwmpcdromplaylist-property"></a><span data-ttu-id="8ea11-106">IWMPCdrom ::P propriété laylist</span><span class="sxs-lookup"><span data-stu-id="8ea11-106">IWMPCdrom::Playlist property</span></span>

<span data-ttu-id="8ea11-107">La propriété **playlist** obtient une interface **IWMPPlaylist** représentant les pistes sur le CD-ROM actuellement dans le lecteur de CD ou les entrées de titre au niveau de la racine pour un DVD.</span><span class="sxs-lookup"><span data-stu-id="8ea11-107">The **Playlist** property gets an **IWMPPlaylist** interface representing the tracks on the CD currently in the CD drive or the root-level title entries for a DVD.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ea11-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ea11-108">Syntax</span></span>


```CSharp
public IWMPPlaylist Playlist {get; set;}
```


```VB

Public ReadOnly Property Playlist As IWMPPlaylist
```





## <a name="property-value"></a><span data-ttu-id="8ea11-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="8ea11-109">Property value</span></span>

<span data-ttu-id="8ea11-110">Interface **wmplib. IWMPPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="8ea11-110">A **WMPLib.IWMPPlaylist** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ea11-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8ea11-111">Remarks</span></span>

<span data-ttu-id="8ea11-112">En général, le contenu basé sur DVD est organisé en titres.</span><span class="sxs-lookup"><span data-stu-id="8ea11-112">Typically, DVD-based content organized into titles.</span></span> <span data-ttu-id="8ea11-113">Chaque titre contient un ou plusieurs chapitres.</span><span class="sxs-lookup"><span data-stu-id="8ea11-113">Each title contains one or more chapters.</span></span> <span data-ttu-id="8ea11-114">Chaque DVD étant créé différemment, la façon dont les titres et les chapitres sont utilisés est celle de l’auteur du contenu.</span><span class="sxs-lookup"><span data-stu-id="8ea11-114">Each DVD is authored differently, so how titles and chapters are used is up to the content author.</span></span>

<span data-ttu-id="8ea11-115">Pour un DVD, cette propriété obtient une sélection qui contient comme premier élément une interface **IWMPMedia** nommée « DVD ».</span><span class="sxs-lookup"><span data-stu-id="8ea11-115">For a DVD, this property gets a playlist that contains as the first item an **IWMPMedia** interface named "DVD".</span></span> <span data-ttu-id="8ea11-116">Cette interface représente le support DVD.</span><span class="sxs-lookup"><span data-stu-id="8ea11-116">This interface represents the DVD media.</span></span> <span data-ttu-id="8ea11-117">La lecture de l’élément entraîne la lecture du DVD à partir du début s’il s’agit de la première lecture après l’insertion d’un nouveau DVD, ou la reprise de la lecture si le DVD est le même que le dernier DVD affiché.</span><span class="sxs-lookup"><span data-stu-id="8ea11-117">Playing the item results in the DVD playing from the beginning if it is the first play after inserting a new DVD, or resuming playback if the DVD is the same as the last DVD viewed.</span></span> <span data-ttu-id="8ea11-118">La définition de cet élément en tant qu’élément actuel pendant la lecture entraîne la lecture du DVD à partir du début.</span><span class="sxs-lookup"><span data-stu-id="8ea11-118">Setting this item as the current item during playback results in the DVD playing from the beginning.</span></span>

<span data-ttu-id="8ea11-119">Les éléments supplémentaires (représentés par les interfaces **IWMPMedia** ) de la sélection sont des titres de DVD représentés par des sélections imbriquées.</span><span class="sxs-lookup"><span data-stu-id="8ea11-119">Additional items (represented by **IWMPMedia** interfaces) in the playlist are DVD titles that are represented by nested playlists.</span></span> <span data-ttu-id="8ea11-120">Lorsque vous affectez à **IWMPControls. CurrentItem** la valeur égal à l’un de ces éléments de sélection imbriqués, le lecteur Windows Media définit automatiquement la sélection imbriquée comme playlist actuelle après le début de la lecture du chapitre.</span><span class="sxs-lookup"><span data-stu-id="8ea11-120">When you set **IWMPControls.currentItem** to equal one of these nested playlist items, Windows Media Player automatically sets the nested playlist as the current playlist after chapter playback begins.</span></span> <span data-ttu-id="8ea11-121">Vous pouvez ensuite utiliser les propriétés de l’interface **IWMPPlaylist** , les méthodes et les événements associés pour travailler avec des chapitres DVD, qui sont également des éléments de sélection.</span><span class="sxs-lookup"><span data-stu-id="8ea11-121">You can then use the **IWMPPlaylist** interface properties, methods and associated events to work with DVD chapters, which are also playlist items.</span></span>

<span data-ttu-id="8ea11-122">Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="8ea11-122">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="8ea11-123">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="8ea11-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8ea11-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="8ea11-124">Examples</span></span>

<span data-ttu-id="8ea11-125">L’exemple suivant utilise la **sélection** pour remplir une zone de texte multiligne, nommée myText, avec la liste de pistes du CD audio actuellement insérée dans le premier lecteur de CD.</span><span class="sxs-lookup"><span data-stu-id="8ea11-125">The following example uses **Playlist** to fill a multi-line text box, named myText, with the track list of the audio CD currently in the first CD drive.</span></span> <span data-ttu-id="8ea11-126">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="8ea11-126">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface that provides access to the CD playlist.
WMPLib.IWMPPlaylist playlist = player.cdromCollection.Item(0).Playlist;

// Create a string array to hold the track list.
String[] trackList = new String[playlist.count];

// Iterate through the CD playlist.
for (int i = 0; i < playlist.count; i++)
{
    trackList[i]= playlist.get_Item(i).name;
}

// Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList;
```


```VB

'  Get an interface that provides access to the CD playlist.
Dim playlist As WMPLib.IWMPPlaylist = player.cdromCollection.Item(0).Playlist

&#39;  Create a string array to hold the track list.
Dim trackList(playlist.count) As String

&#39;  Iterate through the CD playlist.
For i As Integer = 0 To (playlist.count - 1)

    trackList(i) = playlist.Item(i).name

Next i

&#39;  Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList
```





## <a name="requirements"></a><span data-ttu-id="8ea11-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ea11-127">Requirements</span></span>



| <span data-ttu-id="8ea11-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ea11-128">Requirement</span></span> | <span data-ttu-id="8ea11-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ea11-129">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ea11-130">Version</span><span class="sxs-lookup"><span data-stu-id="8ea11-130">Version</span></span><br/>   | <span data-ttu-id="8ea11-131">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8ea11-131">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="8ea11-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8ea11-132">Namespace</span></span><br/> | <span data-ttu-id="8ea11-133">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8ea11-133">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8ea11-134">Assembly</span><span class="sxs-lookup"><span data-stu-id="8ea11-134">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8ea11-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8ea11-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ea11-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ea11-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ea11-137">**Interface IWMPCdrom (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="8ea11-137">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8ea11-138">**IWMPControls. currentItem (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="8ea11-138">**IWMPControls.currentItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8ea11-139">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="8ea11-139">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8ea11-140">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="8ea11-140">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8ea11-141">**IWMPSettings2. mediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="8ea11-141">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8ea11-142">**IWMPSettings2. requestMediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="8ea11-142">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





