---
title: Méthode IWMPControls playItem
description: La méthode playItem lit l’élément multimédia spécifié. | Méthode IWMPControls playItem
ms.assetid: ddd4e4f7-475c-4964-a623-9123ed66be8e
keywords:
- méthode playItem lecteur Windows Media
- méthode playItem lecteur Windows Media, interface IWMPControls
- Interface IWMPControls lecteur Windows Media, méthode playItem
topic_type:
- apiref
api_name:
- IWMPControls.playItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2ac11f93409128eccc88c1d916144615d77476
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531100"
---
# <a name="iwmpcontrolsplayitem-method"></a><span data-ttu-id="660c6-107">IWMPControls ::p méthode layItem</span><span class="sxs-lookup"><span data-stu-id="660c6-107">IWMPControls::playItem method</span></span>

<span data-ttu-id="660c6-108">La méthode **playItem** lit l’élément multimédia spécifié.</span><span class="sxs-lookup"><span data-stu-id="660c6-108">The **playItem** method plays the specified media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="660c6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="660c6-109">Syntax</span></span>


```CSharp
public void playItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub playItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPControls.playItem
```





## <a name="parameters"></a><span data-ttu-id="660c6-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="660c6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="660c6-111">*pIWMPMedia* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="660c6-111">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="660c6-112">Interface **wmplib. IWMPMedia** pour l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="660c6-112">A **WMPLib.IWMPMedia** interface to the media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="660c6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="660c6-113">Return value</span></span>

<span data-ttu-id="660c6-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="660c6-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="660c6-115">Notes</span><span class="sxs-lookup"><span data-stu-id="660c6-115">Remarks</span></span>

<span data-ttu-id="660c6-116">L’élément multimédia est chargé et lu automatiquement, quelle que soit la valeur de la propriété **IWMPSettings. AutoStart** .</span><span class="sxs-lookup"><span data-stu-id="660c6-116">The media item will load and play automatically, regardless of the value of the **IWMPSettings.autoStart** property.</span></span> <span data-ttu-id="660c6-117">Pour charger un élément sans le lire automatiquement, définissez **IWMPSettings. AutoStart** sur **false** et affectez une valeur à **AxWindowsMediaPlayer. URL**, après quoi **IWMPControls. Play** peut être appelé pour démarrer la lecture de l’élément.</span><span class="sxs-lookup"><span data-stu-id="660c6-117">To load an item without playing it automatically, set **IWMPSettings.autoStart** to **false** and assign a value to **AxWindowsMediaPlayer.URL**, after which **IWMPControls.play** can be called to start playing the item.</span></span>

<span data-ttu-id="660c6-118">Remarque</span><span class="sxs-lookup"><span data-stu-id="660c6-118">Note</span></span>

<span data-ttu-id="660c6-119">**playItem** fonctionne uniquement avec les éléments dans **AxWindowsMediaPlayer. currentPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="660c6-119">**playItem** works only with items in **AxWindowsMediaPlayer.currentPlaylist**.</span></span> <span data-ttu-id="660c6-120">L’appel de **playItem** avec une référence à un élément multimédia enregistré n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="660c6-120">Calling **playItem** with a reference to a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="660c6-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="660c6-121">Examples</span></span>

<span data-ttu-id="660c6-122">L’exemple suivant utilise **playItem** pour lire un élément multimédia à partir de la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="660c6-122">The following example uses **playItem** to play a media item from the current playlist.</span></span> <span data-ttu-id="660c6-123">L’élément à lire est choisi en fonction de sa position dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="660c6-123">The item to play is chosen based upon its position in the playlist.</span></span> <span data-ttu-id="660c6-124">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="660c6-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
int index = 3;

// Get the media item at the fourth position in the current playlist.
WMPLib.IWMPMedia media = player.currentPlaylist.get_Item(index);

// Play the media item.
player.Ctlcontrols.playItem(media);
```


```VB

' Declare a variable to hold the position of the media item 
&#39; in the current playlist. An arbitrary value is supplied here.
Dim index As Integer = 3

&#39; Get the media item at the fourth position in the current playlist.
Dim Media As WMPLib.IWMPMedia = player.currentPlaylist.Item(index)

&#39; Play the media item.
player.Ctlcontrols.playItem(Media)
```





## <a name="requirements"></a><span data-ttu-id="660c6-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="660c6-125">Requirements</span></span>



| <span data-ttu-id="660c6-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="660c6-126">Requirement</span></span> | <span data-ttu-id="660c6-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="660c6-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="660c6-128">Version</span><span class="sxs-lookup"><span data-stu-id="660c6-128">Version</span></span><br/>   | <span data-ttu-id="660c6-129">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="660c6-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="660c6-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="660c6-130">Namespace</span></span><br/> | <span data-ttu-id="660c6-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="660c6-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="660c6-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="660c6-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="660c6-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="660c6-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="660c6-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="660c6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="660c6-135">**AxWindowsMediaPlayer. currentPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="660c6-135">**AxWindowsMediaPlayer.currentPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="660c6-136">**AxWindowsMediaPlayer. URL (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="660c6-136">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="660c6-137">**Interface IWMPControls (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="660c6-137">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="660c6-138">**IWMPControls. Play (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="660c6-138">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="660c6-139">**IWMPPlaylist. Item (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="660c6-139">**IWMPPlaylist.Item (VB and C#)**</span></span>](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="660c6-140">**IWMPSettings. AutoStart (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="660c6-140">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





