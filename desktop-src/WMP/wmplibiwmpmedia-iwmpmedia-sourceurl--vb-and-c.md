---
title: IWMPMedia propriété sourceURL
description: La propriété sourceURL obtient l’URL de l’élément multimédia.
ms.assetid: adaef82c-eeed-4cce-859b-c54b9c8fa085
keywords:
- propriété sourceURL lecteur Windows Media
- propriété sourceURL lecteur Windows Media, interface IWMPMedia
- Interface IWMPMedia lecteur Windows Media, propriété sourceURL
topic_type:
- apiref
api_name:
- IWMPMedia.sourceURL
- IWMPMedia.get_sourceURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ad2cdb2c0a67f65f7b0cf722d1b613307806d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536012"
---
# <a name="iwmpmediasourceurl-property"></a><span data-ttu-id="61cab-106">IWMPMedia :: sourceURL, propriété</span><span class="sxs-lookup"><span data-stu-id="61cab-106">IWMPMedia::sourceURL property</span></span>

<span data-ttu-id="61cab-107">La propriété **sourceURL** obtient l’URL de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="61cab-107">The **sourceURL** property gets the URL of the media item.</span></span>

<span data-ttu-id="61cab-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="61cab-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="61cab-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61cab-109">Syntax</span></span>


```CSharp
public System.String sourceURL {get;}
```


```VB

Public ReadOnly Property sourceURL As System.String
```





## <a name="property-value"></a><span data-ttu-id="61cab-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="61cab-110">Property value</span></span>

<span data-ttu-id="61cab-111">**System. String** qui est l’URL source.</span><span class="sxs-lookup"><span data-stu-id="61cab-111">A **System.String** that is the source URL.</span></span>

## <a name="examples"></a><span data-ttu-id="61cab-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="61cab-112">Examples</span></span>

<span data-ttu-id="61cab-113">L’exemple suivant utilise **sourceURL** pour récupérer l’URL du premier élément multimédia dans la sélection « All Music ». l’URL de l’élément multimédia est ensuite affectée à la propriété URL de l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="61cab-113">The following example uses **sourceURL** to retrieve the URL of the first media item in the "All Music" playlist; the URL of the media item is then assigned to the player object URL property.</span></span> <span data-ttu-id="61cab-114">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="61cab-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the All Music Playlist. 
WMPLib.IWMPPlaylist pl = player.playlistCollection.getByName("All Music").Item(0);

// Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
WMPLib.IWMPMedia3 media = (WMPLib.IWMPMedia3)pl.get_Item(0);

// Change the URL property of the player to the URL of the media item.
player.URL = media.sourceURL;

// Play the media item.
player.Ctlcontrols.play();
```


```VB

' Get an interface to the All Music Playlist. 
Dim pl As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
Dim media As WMPLib.IWMPMedia3 = pl.Item(0)

&#39; Change the URL property of the player to the URL of the media item.
player.URL = Media.sourceURL

&#39; Play the media item.
player.Ctlcontrols.play()
```





## <a name="requirements"></a><span data-ttu-id="61cab-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61cab-115">Requirements</span></span>



| <span data-ttu-id="61cab-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61cab-116">Requirement</span></span> | <span data-ttu-id="61cab-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="61cab-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61cab-118">Version</span><span class="sxs-lookup"><span data-stu-id="61cab-118">Version</span></span><br/>   | <span data-ttu-id="61cab-119">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="61cab-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="61cab-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="61cab-120">Namespace</span></span><br/> | <span data-ttu-id="61cab-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="61cab-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="61cab-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="61cab-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="61cab-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="61cab-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61cab-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61cab-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61cab-125">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="61cab-125">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





