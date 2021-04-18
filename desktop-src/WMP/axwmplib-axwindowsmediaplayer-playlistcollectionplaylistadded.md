---
title: Événement PlaylistCollectionPlaylistAdded de l’objet AxWindowsMediaPlayer
description: L’événement PlaylistCollectionPlaylistAdded se produit lorsqu’une sélection est ajoutée à la collection de sélections. | Événement PlaylistCollectionPlaylistAdded de l’objet AxWindowsMediaPlayer
ms.assetid: 13d3bc86-6655-4536-a58f-327eabb2b8f9
keywords:
- Événement PlaylistCollectionPlaylistAdded de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b019e58ae8955f6df894101956e4776c2cd71626
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526436"
---
# <a name="playlistcollectionplaylistadded-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="40af5-105">Événement PlaylistCollectionPlaylistAdded de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="40af5-105">PlaylistCollectionPlaylistAdded Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="40af5-106">L’événement PlaylistCollectionPlaylistAdded se produit lorsqu’une sélection est ajoutée à la collection de sélections.</span><span class="sxs-lookup"><span data-stu-id="40af5-106">The PlaylistCollectionPlaylistAdded event occurs when a playlist is added to the playlist collection.</span></span>

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistAdded(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistAdded(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent
) Handles player.PlaylistCollectionPlaylistAdded
```

## <a name="event-data"></a><span data-ttu-id="40af5-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="40af5-107">Event Data</span></span>

<span data-ttu-id="40af5-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistAddedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="40af5-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistAddedEventHandler**.</span></span> <span data-ttu-id="40af5-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistAddedEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="40af5-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistAddedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="40af5-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="40af5-110">Property</span></span>             | <span data-ttu-id="40af5-111">Description</span><span class="sxs-lookup"><span data-stu-id="40af5-111">Description</span></span>                                                                |
|----------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="40af5-112">**bstrPlaylistName**</span><span class="sxs-lookup"><span data-stu-id="40af5-112">**bstrPlaylistName**</span></span> | <span data-ttu-id="40af5-113">System. StringSpecifies nom de la sélection qui a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="40af5-113">System.StringSpecifies the name of the playlist that was added.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="40af5-114">Notes</span><span class="sxs-lookup"><span data-stu-id="40af5-114">Remarks</span></span>

<span data-ttu-id="40af5-115">Le nom de la sélection ajoutée peut être utilisé pour récupérer la playlist correspondante à l’aide de IWMPPlaylistCollection. méthode **GetByName** .</span><span class="sxs-lookup"><span data-stu-id="40af5-115">The name of the playlist that was added can be used to retrieve the corresponding playlist by using the IWMPPlaylistCollection.**getByName** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="40af5-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40af5-116">Requirements</span></span>



| <span data-ttu-id="40af5-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40af5-117">Requirement</span></span> | <span data-ttu-id="40af5-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="40af5-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40af5-119">Version</span><span class="sxs-lookup"><span data-stu-id="40af5-119">Version</span></span><br/>   | <span data-ttu-id="40af5-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="40af5-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="40af5-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="40af5-121">Namespace</span></span><br/> | <span data-ttu-id="40af5-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="40af5-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="40af5-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="40af5-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="40af5-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="40af5-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40af5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40af5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40af5-126">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="40af5-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="40af5-127">**IWMPPlaylistCollection. getByName (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="40af5-127">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





