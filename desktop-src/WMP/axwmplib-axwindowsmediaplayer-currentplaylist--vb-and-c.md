---
title: AxWindowsMediaPlayer. currentPlaylist, propriété
description: La propriété currentPlaylist obtient ou définit l’interface IWMPPlaylist actuelle qui fournit un moyen simple d’organiser et de manipuler des éléments multimédias dans une liste.
ms.assetid: d5a9f126-a628-499c-a012-8a47c6c987ef
keywords:
- propriété currentPlaylist lecteur Windows Media
- propriété currentPlaylist lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, propriété currentPlaylist
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0f5b91a2e65b81fd1f13da0bad5f77c5ea1415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542649"
---
# <a name="axwindowsmediaplayercurrentplaylist-property"></a><span data-ttu-id="82cba-106">AxWindowsMediaPlayer. currentPlaylist, propriété</span><span class="sxs-lookup"><span data-stu-id="82cba-106">AxWindowsMediaPlayer.currentPlaylist property</span></span>

<span data-ttu-id="82cba-107">La propriété currentPlaylist obtient ou définit l’interface **IWMPPlaylist** actuelle qui fournit un moyen simple d’organiser et de manipuler des éléments multimédias dans une liste.</span><span class="sxs-lookup"><span data-stu-id="82cba-107">The currentPlaylist property gets or sets the current **IWMPPlaylist** interface that provides an easy way to organize and manipulate media items in a list.</span></span>

## <a name="syntax"></a><span data-ttu-id="82cba-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82cba-108">Syntax</span></span>


```CSharp
public IWMPPlaylist currentPlaylist {get; set;}
```


```VB

Public Property currentPlaylist As IWMPPlaylist
```





## <a name="property-value"></a><span data-ttu-id="82cba-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="82cba-109">Property value</span></span>

<span data-ttu-id="82cba-110">Interface WMPLib. IWMPPlaylist qui fournit l’accès à la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="82cba-110">The WMPLib.IWMPPlaylist interface that provides access to the current playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="82cba-111">Notes</span><span class="sxs-lookup"><span data-stu-id="82cba-111">Remarks</span></span>

<span data-ttu-id="82cba-112">Si la propriété IWMPSettings. AutoStart (également accessible via AxWindowsMediaPlayer. Settings.**AutoStart**) a la valeur true, la lecture commence automatiquement chaque fois que vous définissez **currentPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="82cba-112">If the IWMPSettings.autoStart property (also accessed via AxWindowsMediaPlayer.settings.**autoStart**) is true, playback begins automatically whenever you set **currentPlaylist**.</span></span>

<span data-ttu-id="82cba-113">Cette propriété prend une interface IWMPPlaylist, qui peut être acquise de plusieurs façons, par exemple en obtenant la valeur de *IWMPPlaylistArray*. **Item** ou *IWMPPlaylistCollection*. Propriétés de **newPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="82cba-113">This property takes an IWMPPlaylist interface, which can be acquired in several ways, such as by getting the value from the *IWMPPlaylistArray*.**Item** or *IWMPPlaylistCollection*.**newPlaylist** properties.</span></span> <span data-ttu-id="82cba-114">Pour charger un élément de **sélection** à l’aide d’un nom de fichier, définissez la propriété URL ou utilisez AxWindowsMediaPlayer. **newPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="82cba-114">To load a **playlist** item using a file name, set the URL property or use AxWindowsMediaPlayer.**newPlaylist**.</span></span>

## <a name="examples"></a><span data-ttu-id="82cba-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="82cba-115">Examples</span></span>

<span data-ttu-id="82cba-116">L’exemple suivant récupère la première sélection de la bibliothèque et utilise la propriété currentPlaylist pour définir la sélection Récupérée comme playlist actuelle et afficher son nom.</span><span class="sxs-lookup"><span data-stu-id="82cba-116">The following example retrieves the first playlist in the library and uses the currentPlaylist property to set the retrieved playlist as the current playlist, and display its name.</span></span> <span data-ttu-id="82cba-117">L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="82cba-117">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the first playlist from the library. 
WMPLib.IWMPPlaylist firstPlaylist = player.playlistCollection.getAll().Item(0);

// Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist;

// Display the name of the current playlist.
currentPlaylistLabel.Text = ("Found first playlist. Name = " + player.currentPlaylist.name);
```


```VB

' Get an interface to the first playlist from the library. 
Dim firstPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getAll().Item(0)

&#39; Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist

&#39; Display the name of the current playlist.
currentPlaylistLabel.Text = (&quot;Found first playlist. Name = &quot; + player.currentPlaylist.name)
```





## <a name="requirements"></a><span data-ttu-id="82cba-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82cba-118">Requirements</span></span>



| <span data-ttu-id="82cba-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82cba-119">Requirement</span></span> | <span data-ttu-id="82cba-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="82cba-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82cba-121">Version</span><span class="sxs-lookup"><span data-stu-id="82cba-121">Version</span></span><br/>   | <span data-ttu-id="82cba-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="82cba-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="82cba-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="82cba-123">Namespace</span></span><br/> | <span data-ttu-id="82cba-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="82cba-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="82cba-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="82cba-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="82cba-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="82cba-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82cba-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82cba-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82cba-128">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="82cba-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="82cba-129">**AxWindowsMediaPlayer. newPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="82cba-129">**AxWindowsMediaPlayer.newPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="82cba-130">**AxWindowsMediaPlayer. Settings (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="82cba-130">**AxWindowsMediaPlayer.settings (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="82cba-131">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="82cba-131">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="82cba-132">**IWMPPlaylistArray. Item (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="82cba-132">**IWMPPlaylistArray.Item (VB and C#)**</span></span>](wmplibiwmpplaylistarray-iwmpplaylistarray-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="82cba-133">**IWMPPlaylistCollection. newPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="82cba-133">**IWMPPlaylistCollection.newPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="82cba-134">**IWMPSettings. AutoStart (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="82cba-134">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





