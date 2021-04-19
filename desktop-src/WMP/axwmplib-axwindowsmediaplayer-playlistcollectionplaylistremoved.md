---
title: Événement PlaylistCollectionPlaylistRemoved de l’objet AxWindowsMediaPlayer
description: L’événement PlaylistCollectionPlaylistRemoved se produit lorsqu’une sélection est supprimée de la collection de sélections. | Événement PlaylistCollectionPlaylistRemoved de l’objet AxWindowsMediaPlayer
ms.assetid: 96935a9e-4c08-42e9-a63f-7b6cda41b243
keywords:
- Événement PlaylistCollectionPlaylistRemoved de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b982ff566380a7aa5bf4d0b1a1219739b52dd35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541480"
---
# <a name="playlistcollectionplaylistremoved-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="551f3-105">Événement PlaylistCollectionPlaylistRemoved de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="551f3-105">PlaylistCollectionPlaylistRemoved Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="551f3-106">L’événement PlaylistCollectionPlaylistRemoved se produit lorsqu’une sélection est supprimée de la collection de sélections.</span><span class="sxs-lookup"><span data-stu-id="551f3-106">The PlaylistCollectionPlaylistRemoved event occurs when a playlist is removed from the playlist collection.</span></span>

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistRemoved(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistRemoved(  
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent
) Handles player.PlaylistCollectionPlaylistRemoved
```

## <a name="event-data"></a><span data-ttu-id="551f3-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="551f3-107">Event Data</span></span>

<span data-ttu-id="551f3-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistRemovedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="551f3-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistRemovedEventHandler**.</span></span> <span data-ttu-id="551f3-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistRemovedEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="551f3-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistRemovedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="551f3-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="551f3-110">Property</span></span>             | <span data-ttu-id="551f3-111">Description</span><span class="sxs-lookup"><span data-stu-id="551f3-111">Description</span></span>                                                                  |
|----------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="551f3-112">**bstrPlaylistName**</span><span class="sxs-lookup"><span data-stu-id="551f3-112">**bstrPlaylistName**</span></span> | <span data-ttu-id="551f3-113">System. StringSpecifies nom de la sélection qui a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="551f3-113">System.StringSpecifies the name of the playlist that was removed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="551f3-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="551f3-114">Requirements</span></span>



| <span data-ttu-id="551f3-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="551f3-115">Requirement</span></span> | <span data-ttu-id="551f3-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="551f3-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="551f3-117">Version</span><span class="sxs-lookup"><span data-stu-id="551f3-117">Version</span></span><br/>   | <span data-ttu-id="551f3-118">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="551f3-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="551f3-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="551f3-119">Namespace</span></span><br/> | <span data-ttu-id="551f3-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="551f3-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="551f3-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="551f3-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="551f3-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="551f3-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="551f3-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="551f3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="551f3-124">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="551f3-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="551f3-125">**IWMPPlaylistCollection. getByName (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="551f3-125">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





